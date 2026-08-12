cmd@echo off
cls
echo ===================================================
echo         LIMPADOR DE ARQUIVOS TEMPORARIOS          
echo ===================================================
echo.
echo Este script ira eliminar arquivos inuteis do sistema:
echo 1) Limpeza da pasta TEMP do usuario
echo 2) Limpeza da pasta TEMP do sistema (Windows)
echo 3) Limpeza da pasta Prefetch (cache de programas)
echo.
echo IMPORTANTE: Salve seus trabalhos antes de prosseguir.
echo ===================================================
echo.

:pergunta
set /p resposta=Deseja prosseguir com a limpeza de disco? (S/N): 

if /i "%resposta%"=="S" goto executar
if /i "%resposta%"=="N" goto cancelar

echo Opcao invalida. Digite S para Sim ou N para Nao.
echo.
goto pergunta

:executar
echo.
echo [1/3] Limpando arquivos temporarios do usuario...
del /s /f /q "%temp%\*.*" >nul 2>&1
for /d %%i in ("%temp%\*") do rmdir /s /q "%%i" >nul 2>&1

echo [2/3] Limpando arquivos temporarios do sistema...
del /s /f /q "%systemroot%\Temp\*.*" >nul 2>&1
for /d %%i in ("%systemroot%\Temp\*") do rmdir /s /q "%%i" >nul 2>&1

echo [3/3] Limpando cache do Prefetch...
del /s /f /q "%systemroot%\Prefetch\*.*" >nul 2>&1
for /d %%i in ("%systemroot%\Prefetch\*") do rmdir /s /q "%%i" >nul 2>&1

echo.
echo ===================================================
echo Limpeza concluida com sucesso! Espaco liberado.
echo ===================================================
pause
exit

:cancelar
echo.
echo Operacao cancelada pelo usuario. Nenhuma alteracao feita.
echo.
pause
exit

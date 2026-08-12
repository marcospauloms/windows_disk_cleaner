# 💾 Windows Disk Cleaner

Este é um script automatizado focado na otimização de espaço e desempenho do sistema operacional. Ele localiza e remove de forma segura gigabytes de "lixo invisível" gerados por caches de programas, logs do sistema e arquivos temporários de instalações antigas que ficam acumulados no Windows.

## 🚀 O que este script faz?
1. **Limpa a pasta TEMP do usuário:** Apaga arquivos temporários gerados pelo uso diário de navegadores e aplicativos.
2. **Limpa a pasta TEMP do sistema:** Remove arquivos de cache criados pelo próprio Windows que perderam a utilidade.
3. **Esvazia o cache Prefetch:** Limpa dados antigos de inicialização de programas que deixam a leitura do disco lenta com o tempo.

## 💻 Como baixar e usar no seu PC

Como este script possui regras estritas de formatação de linha para o terminal do Windows, siga o método abaixo para garantir o funcionamento correto:

1. Baixe o arquivo `limpador_windows.bat` disponível neste repositório.
2. Mova o arquivo baixado para a sua **Área de Trabalho**.
3. Clique com o botão direito sobre o arquivo `limpador_windows.bat` e selecione **Executar como Administrador**.
4. Uma tela de confirmação aparecerá. Digite `S` para iniciar a limpeza ou `N` para cancelar sem alterar nada.

⚠️ **Aviso de segurança:** Arquivos ou documentos que estejam abertos ou em uso no exato momento da execução não serão apagados pelo script, garantindo que nenhum dado importante seja corrompido.

⚠️ **Nota para ambiente corporativo:** Este script exige privilégios de administrador. Se você estiver usando um computador empresarial ou de escritório, as políticas de segurança da sua equipe de TI podem bloquear a execução.

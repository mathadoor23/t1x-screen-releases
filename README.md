# T1x Screen

Compartilhe tela, câmera, voz e conversa em salas privadas por convite.

**Windows x64 · versão em desenvolvimento · distribuição oficial**

## Baixar

[**Baixar a versão mais recente**](https://github.com/mathadoor23/t1x-screen-releases/releases/latest)

Na página da versão, abra **Assets** e baixe o arquivo **T1x-Screen-Setup-VERSAO.exe**. Esse é o instalador completo. Os arquivos JSON, YAML, blockmap e SHA256SUMS são usados para atualização e conferência; não é necessário abri-los para instalar.

Não é necessário Node, Java ou conta GitHub. O aplicativo instala no usuário do Windows. Se uma versão antiga estiver aberta, encerre sua sala e feche o aplicativo antes de instalar. A edição portátil antiga precisa dessa primeira instalação para receber atualizações pelo app.

Quem recebeu um convite também pode entrar pelo Chrome ou Edge, sem instalar. A sala depende do PC anfitrião ligado e conectado.

## Atualizações

**Novo na 0.1.9:** Amigos agora fica na lateral da janela principal, com busca, pessoas online, pedidos e convites. Escolha um amigo para entrar na sala dele ou criar a sua e chamá-lo. O convite depende de aceite e expira em cinco minutos; câmera e microfone continuam desligados ao entrar. Os códigos e contatos oficiais existentes são preservados. Alternar a aba mantém a transmissão. Ambos devem atualizar para usar o novo fluxo; a presença pode levar cerca de vinte segundos para renovar.

**Novidade em 0.1.8:** correção do retorno de voz na captura do desktop e painel **Amigos**. Atualizem os dois aplicativos, abram Amigos, troquem os códigos e aceitem a solicitação. Amigos aceitos podem ver sua sala hospedada e entrar pelo painel. Há controles de presença, remoção, bloqueio e exclusão do perfil. Serviço gratuito sujeito a limites; leia os dados utilizados em [Privacidade](PRIVACIDADE.md). O áudio foi validado com voz sintética neste PC; conversas prolongadas em outras máquinas e redes ainda precisam de teste.

O app procura versões novas ao abrir e a cada quatro horas enquanto estiver aberto. Você também pode usar **Atualizações → Verificar agora**. O download e a instalação são separados; **Instalar e reiniciar** exige confirmação e encerra as salas deste aplicativo.

Na versão 0.1.7, a tela cheia do aplicativo usa composição por software como medida de compatibilidade para artefatos gráficos relatados. Isso pode aumentar o uso de CPU. A prévia da própria tela começa oculta para evitar efeito espelho; o envio aos convidados continua. Use **Mostrar prévia** para conferir e **Esc** para sair da tela cheia. A causa exata do relato de tela verde não foi reproduzida; a correção foi validada com captura de uma janela controlada e testes de cores/vídeo.

O canal verifica assinatura criptográfica dos metadados e integridade do instalador. A partir da versão 0.1.6, os arquivos publicados têm proteção de imutabilidade e atestado de origem do release no GitHub. Isso protege contra troca dos arquivos depois de publicar; não representa auditoria independente do código.

## Segurança ao baixar

- Use os downloads deste repositório oficial. Não dependa de executáveis reenviados por terceiros.
- Ainda não há certificado Authenticode de editor: o Windows pode mostrar editor desconhecido ou alertas de reputação. Hospedar no GitHub não remove esses alertas nem certifica que um programa é seguro.
- Não desative antivírus, SmartScreen ou outras proteções para usar o aplicativo. Se o Windows impedir a execução, interrompa e reporte o problema.
- Cada versão inclui **SHA256SUMS.txt**. Para comparar manualmente o instalador baixado, execute no PowerShell, substituindo VERSAO pelo número do arquivo:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\T1x-Screen-Setup-VERSAO.exe'
```

Compare o hash completo com a linha correspondente do arquivo de checksums da mesma versão. Um hash igual confirma correspondência com o arquivo publicado; não comprova ausência de malware. Quem usa GitHub CLI pode verificar o atestado do release:

```powershell
gh release verify-asset vVERSAO '.\T1x-Screen-Setup-VERSAO.exe' --repo mathadoor23/t1x-screen-releases
```

## Privacidade e suporte

Leia [Privacidade](PRIVACIDADE.md) antes de compartilhar informações sensíveis e [Segurança](SEGURANCA.md) para reportar problemas.

Falhas de uso podem ser registradas nas [Issues](https://github.com/mathadoor23/t1x-screen-releases/issues). Informe versão, Windows, passos e mensagem de erro. Não inclua senhas, convites completos, dados pessoais ou conteúdo privado das transmissões.

Esta é uma versão em desenvolvimento. Houve testes automatizados e locais; ainda faltam ensaios prolongados em outras máquinas e redes. A consulta de atualizações, o download e as verificações criptográficas foram testados; o ciclo completo de instalação/reinício por atualização ainda não foi ensaiado.

O repositório contém somente documentação e arquivos de distribuição. O código-fonte não está publicado aqui.

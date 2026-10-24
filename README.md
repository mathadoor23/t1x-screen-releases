# T1x Screen

Compartilhe tela, câmera, voz e conversa em salas privadas por convite.

**Windows x64 · Beta 1.1 (1.0.3) · distribuição oficial**

## Baixar

[**Baixar a versão mais recente**](https://github.com/mathadoor23/t1x-screen-releases/releases/latest)

Na página da versão, abra **Assets** e baixe o arquivo **T1x-Screen-Setup-VERSAO.exe**. Esse é o instalador completo. Os arquivos JSON, YAML, blockmap e SHA256SUMS são usados para atualização e conferência; não é necessário abri-los para instalar.

Não é necessário Node, Java ou conta GitHub. O aplicativo instala no usuário do Windows. Se uma versão antiga estiver aberta, encerre sua sala e feche o aplicativo antes de instalar. A edição portátil antiga precisa dessa primeira instalação para receber atualizações pelo app.

Quem recebeu um convite também pode entrar pelo Chrome ou Edge, sem instalar. A sala depende do PC anfitrião ligado e conectado.

## Atualizações

**Beta 1.1 — atualização 1.0.3:** as salas ficam mais fáceis de achar, os avisos usam o visual do T1x, o app abre maximizado e os detalhes das versões recentes aparecem nesta aba. O histórico é carregado do GitHub; se estiver sem internet, consulte as versões pelo link acima. Em perfis novos, Salas na lateral já vem ligada; perfis antigos recebem uma oferta para ativar. O botão de voz abre seus ajustes sem ligar o microfone. A 1.0.3 corrige o histórico que não carregava na primeira compilação 1.0.2. Prefira o instalador **T1x-Screen-Setup-1.0.3.exe**.

**Beta 1.0 — atualização 1.0.1:** cancelar o seletor não gera erro; janela maior/redimensionável e opções de voz visíveis apenas quando ativadas. Novo recurso **Salas na lateral**, desligado inicialmente: ative em Configurações → Áudio → Recursos experimentais. Guarda até cinco salas e permite voltar em um clique. Ao trocar de tela, desconecta sua participação; ao voltar, microfone, câmera e telas permanecem desligados. O anfitrião pode voltar ao início sem encerrar; salas opt-in vazias aguardam 120 s antes de fechar. Fechar o app continua encerrando as salas hospedadas. Entradas somente em memória, sem lista de salas no diretório Amigos; no navegador, fechar/recarregar perde a lista. Atualizem os dois aplicativos para usar o recurso novo. Contatos/códigos existentes preservados. Validado neste PC, sem homologação prolongada em redes diferentes.

**Novo na 1.0.0:** textos mais legíveis, estado único de conexão, botão Som da sala e Configurações organizadas. No desktop, fonte/qualidade/áudio ficam em um só seletor; há prévia estática para evitar espelho, Ajustar/Preencher, volume com porcentagem e opção manual de destacar os amigos. Esses ajustes começam ligados e podem ser desligados em Configurações → Controles de voz · experimental → Interface. Os cinco controles opcionais de voz começam desligados: indicador de fala, medidor/sensibilidade, apertar para falar, teste local e atalho de mudo. PTT exige a página da sala/aba em foco; teste local pede fone e desliga em 30 s. Sem gravação de áudio ou nova sinalização de níveis/fala. Testes locais com Electron, Chrome e Edge; ainda não é validação prolongada entre PCs.

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

Esta é uma versão Beta. Houve testes automatizados e locais; ainda faltam ensaios prolongados em outras máquinas e redes. A consulta de atualizações, o download e as verificações criptográficas foram testados; a instalação/reinício em uso real por diferentes pessoas ainda precisa ser observada.

O repositório contém somente documentação e arquivos de distribuição. O código-fonte não está publicado aqui.

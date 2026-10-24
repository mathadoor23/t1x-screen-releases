# Privacidade do T1x Screen

Este documento descreve o funcionamento implementado na versão de desenvolvimento atual. Não atribui ao aplicativo certificação ou auditoria de privacidade.

## Compartilhamento e participantes

Tela, câmera e microfone começam por ação da pessoa e pelas permissões do navegador ou do sistema. Confira a fonte escolhida antes de transmitir. Os outros participantes podem ver ou ouvir o conteúdo transmitido e podem capturá-lo com recursos próprios.

O convite dá acesso à sala: não publique o link. O anfitrião pode trancar e encerrar a sala ou remover participantes. Uma pessoa removida ainda pode retornar com convite válido se a sala estiver destrancada.

## Dados locais e duração

O aplicativo não implementa gravação de mídia em disco. A sala mantém participantes e até 80 mensagens recentes em memória no PC anfitrião; esses dados são descartados quando o processo ou a sala é encerrado. Salas vazias expiram após vinte minutos.

Nome e preferências de dispositivos/qualidade ficam no perfil local. Configurações opcionais de TURN no desktop usam a proteção local do Electron/Windows e são fornecidas aos participantes autenticados para estabelecer a conexão. Não envie credenciais pessoais pelo chat.

## Serviços e conexões externas

O recurso opcional **Amigos**, ativado ao abrir seu painel, usa um serviço próprio na Cloudflare com SQLite. São armazenados identificador e chave pública, nome escolhido, amizades aceitas, solicitações e bloqueios. A presença temporária contém o convite completo da sala que você hospeda; esse convite só é entregue a amigos aceitos. A lista de contatos mostra título e presença, sem o token do convite. Mídia e conversa não passam por esse diretório. A infraestrutura também recebe metadados de conexão, como IP.

A identidade privada é gerada no aplicativo e protegida pelo Windows no perfil local; o serviço recebe pedidos assinados, sem receber a chave privada. Não há cadastro por e-mail nem recuperação/sincronização entre computadores. Você pode desativar a presença, remover/bloquear contatos e excluir o perfil no painel. A presença expira em aproximadamente um minuto se o aplicativo perder a conexão; nomes e vínculos persistem até remoção/exclusão. Excluir o perfil remove seus vínculos ativos e pedidos do diretório; códigos já bloqueados por outros usuários podem permanecer nas listas deles. Convites já entregues não são revogados ao remover a amizade: tranque ou encerre a sala para impedir novas entradas.

O serviço opera no plano gratuito e está sujeito aos limites e à disponibilidade da Cloudflare.

Desde 0.1.9, convites enviados pela área Amigos também ficam temporariamente no diretório, por até cinco minutos, incluindo o link necessário para validar o acesso. Somente amizades aceitas podem enviar/consultar esses convites. A lista de avisos entrega nome e título da sala; o link completo é obtido quando a pessoa escolhe entrar. Recusar, expirar, remover/bloquear o vínculo ou alterar a sala invalida o convite pelo serviço; excluir o perfil remove seus convites recebidos e os enviados aos contatos ainda vinculados. Isso não revoga cópias de links já entregues, que continuam sob os controles normais da sala. Não existe entrada ou ativação automática de câmera/microfone ao receber um convite.

- **Cloudflare Quick Tunnel:** fornece o convite HTTPS temporário. O link depende do processo no PC anfitrião. No modo compatível, a mídia passa pelo Cloudflare e pelo servidor do anfitrião; não há criptografia adicional de ponta a ponta implementada nesse modo.
- **WebRTC/STUN:** a conexão direta usa os mecanismos de segurança do WebRTC e servidores STUN para descoberta de conectividade. Isso envolve compartilhamento de informações de conexão com a infraestrutura e os participantes. TURN próprio é opcional.
- **GitHub:** o aplicativo instalado consulta os arquivos públicos da versão e baixa atualizações. Essas requisições são recebidas pela infraestrutura do GitHub. Não exigem login GitHub do usuário.

O transporte protegido não impede que participantes vejam ou registrem o conteúdo que você compartilha. Evite transmitir senhas, documentos ou janelas privadas por engano.

## Relatos de suporte

Issues e comentários públicos no GitHub são públicos. Remova dados sensíveis de capturas e logs. Para vulnerabilidades, use o canal privado descrito em [Segurança](SEGURANCA.md).

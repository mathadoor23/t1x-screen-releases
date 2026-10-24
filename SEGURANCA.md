# Segurança e distribuição

## Canal oficial

Baixe por https://github.com/mathadoor23/t1x-screen-releases/releases/latest . O GitHub hospeda a distribuição; isso não equivale a aprovação, auditoria ou certificado de editor emitido pelo GitHub.

As atualizações do aplicativo verificam manifesto Ed25519 e hash do instalador. A chave privada do publicador não é distribuída. Releases a partir de 0.1.6 têm arquivos e tags protegidos contra alteração após publicar, com atestado verificável do GitHub. Essa proteção não se aplica retroativamente aos releases antigos.

Os instaladores são verificados pelo Microsoft Defender antes da publicação. O resultado é relativo ao arquivo e às definições usadas naquele momento; não é garantia de ausência de vulnerabilidades ou de detecção futura por outro antivírus. Consulte as notas de cada release para as verificações realizadas.

Não há certificado Authenticode de editor atualmente. Não desative antivírus ou SmartScreen para contornar uma falha. Uma alteração indevida no arquivo é motivo para interromper a instalação e reportar.

## Reportar vulnerabilidade em privado

Use [Report a vulnerability](https://github.com/mathadoor23/t1x-screen-releases/security/advisories/new). Esse canal é privado para o responsável pelo repositório. Informe versão, passos mínimos para reproduzir e impacto observado, sem dados de terceiros, credenciais ou convites reais.

Problemas comuns de uso podem ir para as Issues. Não publique detalhes de exploração ou dados sensíveis nelas. Não há programa de recompensa ou prazo de resposta anunciado.

## Estado do produto

Beta 1.1 (1.0.3), com testes locais e automatizados, incluindo verificação do pacote publicado. Não há declaração de certificação de segurança ou de conformidade comercial. Novas versões podem corrigir problemas; mantenha o aplicativo atualizado e compartilhe fontes somente com pessoas de confiança.

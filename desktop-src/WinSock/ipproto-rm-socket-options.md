---
description: A tabela a seguir descreve \_ as opções de soquete IPPROTO RM que se aplicam aos soquetes criados para a família de endereços IPv4 (INET série AF \_ ) com o parâmetro Protocol para a função socket especificada como multicast confiável (IPPROTO \_ RM).
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: Opções de soquete de IPPROTO_RM (WSRM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2144efec9b0a92c1da3f612e707bcb44366a38c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763320"
---
# <a name="ipproto_rm-socket-options"></a>Opções de soquete do IPPROTO \_ RM

A tabela a seguir descreve as opções de soquete **IPPROTO \_ RM** que se aplicam aos soquetes criados para a família de endereços IPv4 (INET série AF \_ ) com o parâmetro *Protocol* para a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) especificada como multicast confiável (IPPROTO \_ RM). Consulte as páginas de referência de função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

**Windows XP:** Não há suporte para a programação de multicast confiável (PGM).

Algumas opções de soquete exigem mais explicações do que essas tabelas podem ser transmitidas; essas opções contêm links para páginas adicionais.

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**Opções de soquete do IPPROTO \_ RM**</dt> <dd> <dl> <dt> 

| Opção                              | Obter | Definir | Tipo de optval                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Adicionar recebimento de RM \_ \_ If                |     | sim | ULONG                                            | Somente destinatário. Adiciona uma interface na qual escutar (o padrão é a primeira interface local enumerada). O parâmetro optval especifica a interface de rede em ordem de bytes de rede a ser adicionada. O valor especificado substitui a interface padrão na primeira chamada para um determinado soquete e adiciona outras interfaces em chamadas subsequentes. Para obter qualquer comportamento de inaddr \_ , cada interface de rede deve ser adicionada separadamente. |
| recebimento do RM \_ del \_ \_ se                |     | sim | ULONG                                            | Somente destinatário. Remove uma interface adicionada usando o RM \_ Add \_ Receive \_ If. O parâmetro optval especifica a interface de rede em ordem de bytes de rede a ser excluída.                                                                                                                                                                                                                                                            |
| \_FLUSHCACHE RM                      |     | sim | N/D                                              | Não implementado.                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_consentimento de intranet de alta velocidade do RM \_ \_ \_      | sim | sim | ULONG                                            | Somente destinatário. Especifica se uma conexão LAN de alta largura de banda (100 Mbps) é usada.                                                                                                                                                                                                                                                                                                                                   |
| \_LATEJOIN RM                        | sim | sim | ULONG                                            | Somente remetente. Porcentagem do tamanho da janela que pode ser solicitada por destinatários de ingresso tardia na aceitação da sessão. O valor máximo é 75% (o padrão é zero). Desabilite essa configuração chamando novamente com o valor definido como zero.                                                                                                                                                                                                |
| \_tamanho da \_ janela de taxa do RM \_              | sim | sim | [**\_janela de envio do RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | Somente remetente. Define o limite da taxa de transmissão, o tempo de adiantamento da janela e o tamanho da janela.                                                                                                                                                                                                                                                                                                                                   |
| \_estatísticas do receptor do RM \_            | sim |     | [**\_estatísticas do receptor do RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | Somente destinatário. Recupera estatísticas para a sessão de recebimento.                                                                                                                                                                                                                                                                                                                                                         |
| \_taxa de \_ avçd da janela de envio do RM \_ \_         | sim | sim | ULONG                                            | Somente remetente. Especifica a taxa de adiantamento incremental para a janela de envio de borda à direita (o padrão é 15%). O valor máximo é 50%.                                                                                                                                                                                                                                                                                          |
| \_estatísticas do remetente do RM \_              | sim |     | [**\_estatísticas do remetente do RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | Somente remetente. Recupera estatísticas para a sessão de envio.                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ método Advance da janela do remetente do \_ RM \_ | sim | sim | ULONG                                            | Somente remetente. O parâmetro optval especifica o método usado ao avançar a janela de envio de borda à direita. O parâmetro optval só pode ser E \_ \_ de janela antecipada \_ por \_ hora (o padrão). Observe que \_ \_ \_ \_ \_ não há suporte para o uso da janela e como cache de dados.                                                                                                                                                                     |
| \_ \_ mcast TTL do conjunto do RM \_                 |     | sim | ULONG                                            | Somente remetente. Define a configuração de tempo de vida máximo (TTL) para pacotes multicast. O valor máximo e padrão é 255.                                                                                                                                                                                                                                                                                                      |
| \_limite de \_ mensagem do conjunto do RM \_          |     | sim | ULONG                                            | Somente remetente. Especifica o tamanho da próxima mensagem a ser enviada, em bytes. Significativo apenas para soquetes de modo de mensagem (SOCK \_ RDM). Pode ser definido enquanto a sessão está em andamento.                                                                                                                                                                                                                                                |
| RM \_ set \_ Send \_ If                   | sim | sim | ULONG                                            | Somente remetente. Define o endereço IP da interface de envio na ordem de bytes da rede.                                                                                                                                                                                                                                                                                                                                              |
| RM \_ usar \_ FEC                        | sim | sim | [**\_informações de FEC do RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | Somente remetente. Notifica o remetente para aplicar técnicas de correção de erros de encaminhamento para enviar dados de reparo. O FEC tem três modos: somente pacotes de paridade Pro-active, somente pacotes de paridade OnDemand ou ambos. Consulte estrutura de [**\_ \_ informações de FEC do RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info) para obter mais informações.                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**Suporte do Windows para \_ Opções do IPPROTO RM**</dt> <dd> <dl> <dt> 

| Opção                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/me |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| \_Adicionar recebimento de RM \_ \_ If                | x         | x                   | x             | x                   | x          |              |             |               |
| recebimento do RM \_ del \_ \_ se                | x         | x                   | x             | x                   | x          |              |             |               |
| \_FLUSHCACHE RM                      | x         | x                   | x             | x                   | x          |              |             |               |
| \_consentimento de intranet de alta velocidade do RM \_ \_ \_      | x         | x                   | x             | x                   | x          |              |             |               |
| \_LATEJOIN RM                        | x         | x                   | x             | x                   | x          |              |             |               |
| \_tamanho da \_ janela de taxa do RM \_              | x         | x                   | x             | x                   | x          |              |             |               |
| \_estatísticas do receptor do RM \_            | x         | x                   | x             | x                   | x          |              |             |               |
| \_taxa de \_ avçd da janela de envio do RM \_ \_         | x         | x                   | x             | x                   | x          |              |             |               |
| \_estatísticas do remetente do RM \_              | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ método Advance da janela do remetente do \_ RM \_ | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ mcast TTL do conjunto do RM \_                 | x         | x                   | x             | x                   | x          |              |             |               |
| \_limite de \_ mensagem do conjunto do RM \_          | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ set \_ Send \_ If                   | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ usar \_ FEC                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

As opções de soquete do **IPPROTO \_ RM** e as estruturas usadas por essas opções de soquete são definidas no arquivo de cabeçalho *wsrm. h* .

A **constante \_ IPPROTO RM** ou **IPPROTO \_ PGM** pode ser usada para especificar o parâmetro de *protocolo* para a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) a fim de usar as opções de soquete do RM. No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a constante de **\_ PGM IPPROTO** é definida no arquivo de cabeçalho *Ws2def. h* com o mesmo valor que a constante de **\_ RM IPPROTO** definida no arquivo de cabeçalho *wsrm. h* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WSRM. h</dt> </dl> |



 

 





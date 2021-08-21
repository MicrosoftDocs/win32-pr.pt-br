---
description: A tabela a seguir descreve as opções de soquete IPPROTO RM que se aplicam a soquetes criados para a família de endereços IPv4 (AF INET) com o parâmetro de protocolo para a função de soquete especificada como \_ \_ multicast confiável (IPPROTO \_ RM).
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: IPPROTO_RM opções de soquete (Wsrm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1710b1135d2c645f5ff55de12b2feb2d62cfbe2b257e3f28367a66a81d5171
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051484"
---
# <a name="ipproto_rm-socket-options"></a>Opções de \_ soquete IPPROTO RM

A tabela a seguir descreve as opções de soquete **IPPROTO \_ RM** que se aplicam a soquetes criados para a família de endereços IPv4 (AF INET) com o parâmetro de protocolo para a função de soquete especificada como \_ multicast confiável (IPPROTO  [](/windows/desktop/api/Winsock2/nf-winsock2-socket) \_ RM). Consulte as páginas de referência da função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

**Windows XP:** Não há suporte para PGM (Programação Multicast Confiável).

Algumas opções de soquete exigem mais explicação do que essas tabelas podem transmitir; essas opções contêm links para páginas adicionais.

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**Opções de \_ soquete IPPROTO RM**</dt> <dd> <dl> <dt> 

| Opção                              | Obter | Definir | Tipo de aceitação                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RM \_ ADD \_ RECEIVE \_ IF                |     | sim | Ulong                                            | Somente receptor. Adiciona uma interface na qual escutar (o padrão é a primeira interface local enumerada). O parâmetro optval especifica o interface de rede na ordem de byte de rede a ser adicionar. O valor especificado substitui a interface padrão na primeira chamada para um determinado soquete e adiciona outras interfaces em chamadas subsequentes. Para obter o comportamento INADDR \_ ANY, cada interface de rede deve ser adicionada separadamente. |
| RM \_ DEL \_ RECEIVE \_ IF                |     | sim | Ulong                                            | Somente receptor. Remove uma interface adicionada usando RM \_ ADD \_ RECEIVE \_ IF. O parâmetro optval especifica o interface de rede na ordem de exclusão de byte de rede.                                                                                                                                                                                                                                                            |
| RM \_ FLUSHCACHE                      |     | sim | N/D                                              | Não implementado.                                                                                                                                                                                                                                                                                                                                                                                                       |
| RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT      | sim | sim | Ulong                                            | Somente receptor. Especifica se uma conexão LAN de alta largura de banda (100 Mbps+) é usada.                                                                                                                                                                                                                                                                                                                                   |
| RM \_ LATEJOIN                        | sim | sim | Ulong                                            | Somente remetente. Percentual do tamanho da janela permitido para ser solicitado por receptores de junção tardia após a aceitação da sessão. O valor máximo é 75% (o padrão é zero). Desabilite essa configuração chamando novamente com o valor definido como zero.                                                                                                                                                                                                |
| TAMANHO DA \_ \_ JANELA TAXA \_ RM              | sim | sim | [**JANELA RM \_ SEND \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | Somente remetente. Define o limite de taxa de transmissão, o tempo de avanço da janela e o tamanho da janela.                                                                                                                                                                                                                                                                                                                                   |
| ESTATÍSTICAS \_ DO \_ RECEPTOR RM            | sim |     | [**ESTATÍSTICAS \_ DO \_ RECEPTOR RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | Somente receptor. Recupera estatísticas para a sessão de recebimento.                                                                                                                                                                                                                                                                                                                                                         |
| RM \_ SEND \_ WINDOW \_ ADV \_ RATE         | sim | sim | Ulong                                            | Somente remetente. Especifica a taxa de avanço incremental para a janela de envio de borda à direita (o padrão é 15%). O valor máximo é 50%.                                                                                                                                                                                                                                                                                          |
| ESTATÍSTICAS \_ DO REMETENTE DO RM \_              | sim |     | [**ESTATÍSTICAS \_ DO REMETENTE DO RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | Somente remetente. Recupera estatísticas para a sessão de envio.                                                                                                                                                                                                                                                                                                                                                             |
| MÉTODO RM \_ SENDER \_ WINDOW \_ \_ ADVANCE | sim | sim | Ulong                                            | Somente remetente. O parâmetro optval especifica o método usado ao avançar a janela de envio de borda à direita. O parâmetro optval só pode ser E \_ WINDOW ADVANCE BY TIME \_ \_ \_ (o padrão). Observe que não há \_ suporte para E WINDOW USE AS DATA \_ \_ \_ \_ CACHE.                                                                                                                                                                     |
| RM \_ SET \_ MCAST \_ TTL                 |     | sim | Ulong                                            | Somente remetente. Define a configuração de TTL (vida máxima) para pacotes multicast. O valor máximo e padrão é 255.                                                                                                                                                                                                                                                                                                      |
| RM \_ SET \_ MESSAGE \_ BOUNDARY          |     | sim | Ulong                                            | Somente remetente. Especifica o tamanho da próxima mensagem a ser enviada, em bytes. Significativo somente para soquetes de modo de mensagem (SOCK \_ RDM). Pode ser definido enquanto a sessão está em andamento.                                                                                                                                                                                                                                                |
| RM \_ SET \_ SEND \_ IF                   | sim | sim | Ulong                                            | Somente remetente. Define o endereço IP da interface de envio na ordem de byte de rede.                                                                                                                                                                                                                                                                                                                                              |
| RM \_ USE \_ FEC                        | sim | sim | [**INFORMAÇÕES DO RM \_ FEC \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | Somente remetente. Notifica o remetente para aplicar técnicas de correção de erro de encaminhamento para enviar dados de reparo. O FEC tem três modos: somente pacotes de paridade pro-active, somente pacotes de paridade OnDemand ou ambos. Confira [**Estrutura RM \_ FEC \_ INFO**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info) para obter mais informações.                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**Windows Suporte para opções de IPPROTO \_ RM**</dt> <dd> <dl> <dt> 

| Opção                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| RM \_ ADD \_ RECEIVE \_ IF                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ DEL \_ RECEIVE \_ IF                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ FLUSHCACHE                      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ LATEJOIN                        | x         | x                   | x             | x                   | x          |              |             |               |
| TAMANHO DA \_ \_ JANELA TAXA \_ RM              | x         | x                   | x             | x                   | x          |              |             |               |
| ESTATÍSTICAS \_ DO \_ RECEPTOR RM            | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SEND \_ WINDOW \_ ADV \_ RATE         | x         | x                   | x             | x                   | x          |              |             |               |
| ESTATÍSTICAS \_ DO REMETENTE DO RM \_              | x         | x                   | x             | x                   | x          |              |             |               |
| MÉTODO RM \_ SENDER \_ WINDOW \_ \_ ADVANCE | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ MCAST \_ TTL                 | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ MESSAGE \_ BOUNDARY          | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ SEND \_ IF                   | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ USE \_ FEC                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

As **opções de soquete IPPROTO \_ RM** e as estruturas usadas por essas opções de soquete são definidas no arquivo de título *Wsrm.h.*

A **constante \_ IPPROTO RM** ou **IPPROTO \_ PGM** pode ser usada para especificar o parâmetro de *protocolo* para a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) a fim de usar as opções de soquete do RM. no SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a constante **IPPROTO do \_ PGM** é definida no arquivo de cabeçalho *Ws2def. h* com o mesmo valor que a constante de **\_ RM IPPROTO** definida no arquivo de cabeçalho *Wsrm. h* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WSRM. h</dt> </dl> |



 

 





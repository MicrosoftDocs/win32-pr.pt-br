---
title: Windows Funções de servidor dos Serviços de Implantação
description: As funções a seguir são usadas com a API do servidor PXE Windows Deployment Services.
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cc99f01dc88fce91beafe51a65f8e8ddccfdf08c4361fb194a7e60451a5aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330591"
---
# <a name="windows-deployment-services-server-functions"></a>Windows Funções de servidor dos Serviços de Implantação

As funções a seguir são usadas com a API do servidor PXE Windows Deployment Services.



| Função                                                           | Descrição                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | Retorna resultados assíncronos da solicitação do cliente.                                                                                |
| [**PxeDhcpAppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | Anexa uma opção DHCP ao pacote de resposta.                                                                                     |
| [**PxeDhcpAppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | Anexa uma opção DHCP ao pacote de resposta.                                                                                     |
| [**PxeDhcpGetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | Recupera um valor de opção de um pacote DHCP.                                                                                  |
| [**PxeDhcpGetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | Recupera um valor de opção do campo Informações Específicas do Fornecedor (43) de um pacote DHCP.                                    |
| [**PxeDhcpInitialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | Inicializa um pacote de resposta como um pacote de resposta DHCP.                                                                          |
| [**PxeDhcpIsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | Valida se um pacote é um pacote DHCP.                                                                                      |
| [**PxeGetServerInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | Retorna informações sobre o servidor PXE.                                                                                      |
| [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | Aloca um pacote a ser enviado com a [**função PxeSendReply.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                                          |
| [**PxePacketFree**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | Libera um pacote alocado pela [**função PxePacketAllocate.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                                       |
| [**PxeProviderEnumClose**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | Fecha a enumeração de provedores aberta pela [**função PxeProviderEnumFirst.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               |
| [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | Inicia uma enumeração de provedores registrados.                                                                                 |
| [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | Enumera provedores registrados.                                                                                               |
| [**PxeProviderFreeInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | Libera a memória alocada pela [**função PxeProviderEnumNext.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                                     |
| [*PxeProviderInitialize*](pxeproviderinitialize.md)               | Uma exportação de uma DLL (biblioteca de vínculo dinâmico) do provedor que inicializa o provedor e o prepara para receber solicitações do cliente. |
| [**PxeProviderQueryIndex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | Retorna o índice do provedor especificado na lista de provedores registrados.                                               |
| [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)             | Chamado quando uma solicitação é recebida de um cliente.                                                                               |
| [**PxeProviderRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | Registra um provedor com o sistema.                                                                                          |
| [*PxeProviderServiceControl*](pxeproviderservicecontrol.md)       | Chamado quando um código de controle de serviço é recebido pelo serviço WDS.                                                             |
| [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | Especifica atributos para o provedor.                                                                                         |
| [*PxeProviderShutdown*](pxeprovidershutdown.md)                   | Chamado para desligar o provedor.                                                                                               |
| [**PxeProviderUnRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | Remove um provedor da lista de provedores registrados.                                                                      |
| [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | Registra funções de retorno de chamada para diferentes eventos de notificação.                                                                |
| [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | Envia um pacote para uma solicitação do cliente.                                                                                            |
| [**PxeTrace**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | Adiciona uma entrada de rastreamento ao log PXE.                                                                                             |



 

O seguinte está disponível a partir do Windows 8 e Windows Server 2012.

| Função                                                               | Descrição                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | Anexa uma opção DHCPv6 ao pacote de resposta.                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | Anexa uma opção DHCPv6 ao pacote de resposta.                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | Recupera um valor de opção de um pacote DHCPv6.                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | Recupera valores de opção do campo OPTION \_ VENDOR \_ OPTS (17) de um pacote DHCPv6.          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | Inicializa um pacote de resposta como um pacote de resposta DHCPv6.                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | Valida se um pacote é um pacote DHCPv6 válido.                                             |
| [**PxeGetServerInfoEx**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | Retorna informações sobre o servidor PXE.                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | Permite que um provedor analisar mensagens RELAY-FORW e suas mensagens MSG DE RETRANSMISSÃO DE OPÇÃO \_ \_ aninhadas. |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | Gera uma mensagem RELAY-REPL.                                                               |



 

 

 





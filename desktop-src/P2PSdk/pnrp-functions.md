---
description: A API do provedor de namespace do PNRP usa as funções a seguir.
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: Funções PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0e811c2d10927064e380970456c76f30730ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748416"
---
# <a name="pnrp-functions"></a>Funções PNRP

A API do provedor de namespace do PNRP usa as funções a seguir.



| Função                                                             | Descrição                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | Codifica o nome de par fornecido como um formato que pode ser usado com uma chamada subsequente para a função [**Getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) do Windows Sockets. |
| [**PeerHostNameToPeerName**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | Decodifica um nome de host retornado por [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) na cadeia de caracteres de nome de par que ele representa.                            |
| [**PeerPnrpStartup**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | Inicia o serviço PNRP (Peer Name Resolution Protocol) para o ponto de chamada.                                                                                |
| [**PeerPnrpShutdown**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | Desliga uma instância em execução do serviço PNRP (Peer Name Resolution Protocol) e libera todos os recursos associados a ele.                             |
| [**PeerPnrpRegister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | Registra um par com uma nuvem PNRP e retorna um identificador que pode ser usado para atualizações de registro.                                                           |
| [**PeerPnrpUpdateRegistration**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | Atualiza as informações de registro do PNRP para um nome.                                                                                                        |
| [**PeerPnrpUnregister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | Cancela o registro de um par de uma nuvem PNRP.                                                                                                                        |
| [**PeerPnrpResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | Obtém os endereços de ponto de extremidade registrados para um nome de par específico.                                                                                        |
| [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | Inicia uma operação de resolução de nome de par assíncrono.                                                                                                       |
| [**PeerPnrpGetCloudInfo**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | Recupera informações sobre as nuvens PNRP (Peer Name Resolution Protocol) nas quais o peer de chamada está participando.                                         |
| [**PeerPnrpEndResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | Fecha o identificador de uma operação de resolução de PNRP assíncrona iniciada com uma chamada anterior para [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve).      |
| [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md) | Inicia o processo que permite que um aplicativo resolva nomes e enumere nuvens de rede.                                                                 |
| [PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)     | Encerra uma consulta iniciada em uma chamada anterior para [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                             |
| [PNRP e WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)   | Faz a correspondência de consultas especificadas em uma chamada anterior para [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                                |
| [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md)                     | Recebe notificações sobre alterações na lista de nuvem de rede e disponibilidade de resultados de uma solicitação de resolução de nomes.                                     |
| [PNRP e WSASetService](pnrp-and-wsasetservice.md)                 | Registra ou remove [nomes de pares](peer-names.md).                                                                                                           |



 

 

 

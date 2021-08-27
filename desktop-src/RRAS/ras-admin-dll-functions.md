---
title: Funções de DLL de administração ras
description: Uma DLL de administração RAS deve implementar e exportar todas as funções a seguir
ms.assetid: bf2bd4d4-6da2-471e-843c-c0f0563d3795
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4ed327cf3114ec4bf7844518f3c1500845450021f80bbd59ddd642de9eeac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036386"
---
# <a name="ras-administration-dll-functions"></a>Funções de DLL de administração ras

Uma DLL de administração RAS deve implementar e exportar todas as seguintes funções:

-   [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)
-   [**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) [ **ou MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)
-   [**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) ou [ **MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)
-   [**MprAdminLinkLinkNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)
-   [**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

**Windows 2000/NT:** A DLL de administração ras também deve implementar e exportar o seguinte par de funções: [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) [**e MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)

Além disso, a DLL de administração ras deve implementar e exportar um dos seguintes pares de funções:

-   [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) [ **e MprAdminConnectionConnectupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)
-   [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) e [ **MprAdminConnectionConnectionNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)
-   [**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) [ **e MprAdminConnectionConnectionNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)
-   [**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) [ **e MprAdminConnectionConnectionNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)

Se uma das funções necessárias não for implementada, o serviço de acesso remoto falhará ao iniciar.

Uma DLL de administração não é necessária para implementar os seguintes pares de funções:

-   [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) [ **e MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)
-   [*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) [ *e MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)

No entanto, se a DLL implementar uma função em um par listado acima, ela também deverá implementar a outra função no par.

Para obter mais informações sobre DLLs de administração ras, consulte o tópico de visão geral, [DLL de administração ras](ras-administration-dll.md).

 

 
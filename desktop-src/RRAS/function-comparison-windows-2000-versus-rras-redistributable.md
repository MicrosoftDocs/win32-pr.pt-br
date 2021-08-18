---
title: comparação de funções Windows 2000 vs. redistribuível de RRAS
description: a API RAS é distribuída como um recurso do Windows 2000 e sistemas operacionais posteriores e está disponível como um pacote redistribuível para o Windows NT 4,0 com Service Pack 3 (SP3) e anterior.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027c120133573b1d0c452b74dd02ab8fa0aa6f3367eb1a5fc9668a2de089c758
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995336"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a>comparação de funções: Windows 2000 vs. redistribuível de RRAS

a API RAS é distribuída como um recurso do Windows 2000 e sistemas operacionais posteriores e está disponível como um pacote redistribuível para o Windows NT 4,0 com Service Pack 3 (SP3) e anterior. O RAS fornece a mesma funcionalidade em ambos os formulários, mas a Convenção de nomenclatura usada é diferente para os elementos de referência em cada versão da API RAS.

as funções RAS para Windows NT 4,0 com SP3 e versões anteriores normalmente começam com o prefixo "RasAdmin". As funções análogas para roteamento e serviço de acesso remoto (RRAS) começam com o prefixo "MprAdmin". Por exemplo, o RAS fornece uma função chamada [**RasAdminPortGetInfo**](rasadminportgetinfo.md). A função análoga no RRAS é chamada de [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo). Como exemplo semelhante, o RAS fornece a função de retorno de chamada [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md). O RRAS fornece uma função de retorno de chamada semelhante chamada [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser). As exceções a essa regra são [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), que sob o RRAS é [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), e [**RASADMINFREEBUFFER**](rasadminfreebuffer.md), que sob o RRAS é [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).

a tabela a seguir lista as funções RAS do Windows NT 4,0 SP3 e as funções de RRAS correspondentes.



| Windows NT RAS 4,0                                                                   | RRAS                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)                   | [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) | [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [**RasAdminFreeBuffer**](rasadminfreebuffer.md)                                     | [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [**RasAdminGetErrorString**](rasadmingeterrorstring.md)                             | [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)                   | [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)                   | [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [**RasAdminPortDisconnect**](rasadminportdisconnect.md)                             | [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [**RasAdminPortEnum**](rasadminportenum.md)                                         | [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [**RasAdminPortGetInfo**](rasadminportgetinfo.md)                                   | [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)                         | [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [**RasAdminUserGetInfo**](rasadminusergetinfo.md)                                   | [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [**RasAdminUserSetInfo**](rasadminusersetinfo.md)                                   | [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

embora as funções de RRAS sejam semelhantes às suas Windows NT 4,0 com o SP3 e as contrapartes RAS anteriores na funcionalidade, as funções de RRAS geralmente usam um conjunto diferente de parâmetros. Consulte a página de referência de uma função específica para obter informações completas sobre a lista de parâmetros da função.

o RRAS redistribuível para Windows NT 4,0 com SP3 e versões anteriores adiciona as seguintes funções, que não têm nenhuma contraparte de RAS:

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminConnectionClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[**MprAdminConnectionGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminPortReset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[**MprAdminServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

além das funções anteriores, Windows 2000 e sistemas operacionais posteriores adicionam as seguintes funções:

[**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 





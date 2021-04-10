---
title: Funções de interface do roteador
description: Use as funções a seguir para administrar interfaces no roteador.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291747"
---
# <a name="router-interface-functions"></a>Funções de interface do roteador

Use as funções a seguir para administrar interfaces no roteador.



| Função de administração                                          | Função de configuração                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [**MprConfigInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [**MprAdminInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [**MprConfigInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [**MprAdminInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [**MprConfigInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [**MprAdminInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [**MprConfigInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

Essas funções afetam as interfaces, e não os clientes em execução nas interfaces. Por esse motivo, nenhuma das funções exige que o chamador especifique um transporte específico (IP ou IPX); Embora os clientes (como protocolos de roteamento) estejam associados a transportes específicos, as próprias interfaces não são.

Essas funções são tratadas diretamente por DIM. Eles não utilizam os gerenciadores de roteador.

As funções [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) e [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) não podem criar ou excluir interfaces de LAN. Eles só podem criar ou excluir interfaces de discagem por demanda. Consulte [**\_ \_ tipo de interface do roteador**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) para obter uma lista de tipos de interface.

 

 





---
title: Compreendendo as funções MprInfo e os cabeçalhos de informações
description: As funções a seguir exigem que o chamador transmita uma estrutura de informações ou um cabeçalho como um dos parâmetros.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916335"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a>Compreendendo as funções MprInfo e os cabeçalhos de informações

As funções a seguir exigem que o chamador transmita uma estrutura de informações ou um *cabeçalho* como um dos parâmetros.



| Função de administração                                                        | Função de configuração                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Nenhuma função de administração                                                     | [**MprConfigTransportCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [**MprAdminInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [**MprConfigInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

Da mesma forma, as funções a seguir retornam cabeçalhos de informações.



| Função de administração                                                        | Função de configuração                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

Para as funções de transporte, o cabeçalho de informações contém informações globais para o transporte. Para as funções de cliente (InterfaceTransport), o cabeçalho contém informações específicas para o cliente (por exemplo, OSPF) sendo administrado.

Os cabeçalhos de informações e seu conteúdo devem ser manipulados somente usando as funções [MprInfo](router-information-functions.md) . Os desenvolvedores não devem tentar manipular o conteúdo dos cabeçalhos de informações diretamente.

As funções somente de interface, como [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , não exigem o uso de funções MprInfo. As informações passadas e retornadas com essas funções estão sempre na forma de uma estrutura [**de \_ interface de MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .

 

 





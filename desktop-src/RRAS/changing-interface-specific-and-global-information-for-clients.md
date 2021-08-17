---
title: Alterando Interface-Specific e informações globais para clientes
description: Para alterar as informações de interface de um cliente específico, por exemplo, NAT, primeiro use o \ 0034; GetInfo \ 0034; função para recuperar as informações atuais.
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcea02c6d70e7d7e2da53926854879f1ca5b76526a83185b786b0074b8098434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791749"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>Alterando Interface-Specific e informações globais para clientes

Para alterar as informações de interface de um cliente específico, por exemplo, NAT, primeiro use a função "GetInfo" apropriada para recuperar as informações atuais. Se o roteador estiver em execução, use [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Se o roteador não estiver em execução, use o [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo). Essa chamada recupera as informações de todos os clientes em execução na interface especificada. Por exemplo, se o OSPF e o RIP estiverem em execução em uma interface específica, essa chamada recuperará as informações de interface para ambos. Use a função [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) para localizar o bloco de informações que corresponde ao cliente que você deseja modificar. Em seguida, use a função [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) para executar as modificações. Por fim, use [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) ou [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) para fazer as alterações no roteador em execução ou na configuração do roteador no registro.

As informações globais do cliente são informações que não são específicas de nenhuma interface específica na qual o cliente está executando o. Use um procedimento semelhante para modificar informações globais de um cliente específico. Primeiro, recupere as informações globais para todos os clientes usando [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) ou [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo). Em seguida, use as funções MprInfo para modificar as informações. Por fim, use as funções [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) ou [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) para salvar as informações modificadas de volta para o roteador em execução ou o registro.

Chamadas para as funções de administração anteriores passam pelo Gerenciador de interface dinâmica (DIM) e eventualmente se traduzem em chamadas do Gerenciador de roteador para os próprios clientes. Todos os clientes, independentemente de serem ou não protocolos de roteamento, devem estar em conformidade com a interface descrita na seção [interface de protocolo do roteador](about-routing-protocol-interface.md). Como parte dessa interface, o protocolo de roteamento deve dar suporte às seguintes funções (entre outras):

-   [**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

O Gerenciador de roteador chama as funções [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) para cada um dos clientes para coletar as informações retornadas de uma chamada para [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Da mesma forma, quando o Gerenciador de roteador recebe informações atualizadas por meio de chamada [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) , ele usa as funções [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) para atualizar as informações de interface para cada um dos clientes.

 

 





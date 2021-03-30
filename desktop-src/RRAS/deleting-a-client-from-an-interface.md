---
title: Excluindo um cliente de uma interface
description: Para excluir um cliente, como um protocolo de roteamento, de uma interface específica, use MprAdminInterfaceTransportGetInfo ou MprConfigInterfaceTransportGetInfo para recuperar todas as informações do cliente para a interface.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585a37920b59f47a0c933427d7218d08a61bed9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916433"
---
# <a name="deleting-a-client-from-an-interface"></a>Excluindo um cliente de uma interface

Para excluir um cliente, como um protocolo de roteamento, de uma interface específica, use [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) ou [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) para recuperar todas as informações do cliente para a interface. Use [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) para remover o bloco de informações do cliente a ser excluído. Em seguida, use [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) para adicionar um bloco de comprimento zero para o cliente a ser excluído. Por fim, use [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) ou [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) para salvar as informações de volta para o roteador em execução ou o registro.

Se o Gerenciador de roteador receber um bloco de informações de interface de comprimento zero para um cliente, ele saberá excluir esse cliente da interface. O Gerenciador de roteador exclui o cliente chamando a implementação do cliente do [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface). Observe a distinção importante entre passar um cabeçalho de informações que não contenha um bloco de informações para um cliente e passar um cabeçalho de informações que contenha um bloco de informações de comprimento zero para o cliente. No primeiro caso, o Gerenciador de roteador não executa nenhuma ação em relação ao cliente. No segundo caso, o Gerenciador de roteador exclui o cliente da interface.

 

 





---
title: Excluindo um cliente de uma interface
description: Para excluir um cliente, como um protocolo de roteamento, de uma interface específica, use MprAdminInterfaceTransportGetInfo ou MprConfigInterfaceTransportGetInfo para recuperar todas as informações do cliente para a interface.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e5b93e062f5971f6e43ad1d7c08f7a0c2ef3bff72e66849815a053b342b13b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127886"
---
# <a name="deleting-a-client-from-an-interface"></a>Excluindo um cliente de uma interface

Para excluir um cliente, como um protocolo de roteamento, de uma interface específica, use [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) ou [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) para recuperar todas as informações do cliente para a interface. Use [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) para remover o bloco de informações para o cliente a ser excluído. Em seguida, [**use MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) para adicionar um bloco de comprimento zero para que o cliente seja excluído. Por fim, use [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) ou [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) para salvar as informações de volta no roteador em execução ou no Registro.

Se o gerenciador de roteador receber um bloco de informações de interface de comprimento zero para um cliente, ele saberá excluir esse cliente da interface. O gerenciador de roteador exclui o cliente chamando a implementação do cliente de [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface). Observe a distinção importante entre passar um header de informações que não contém um bloco de informações para um cliente e passar um título de informações que contém um bloco de informações de comprimento zero para o cliente. No primeiro caso, o gerenciador de roteador não toma nenhuma ação em relação ao cliente. No segundo caso, o gerenciador de roteador exclui o cliente da interface .

 

 





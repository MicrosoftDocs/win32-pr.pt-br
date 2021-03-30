---
title: Cliente do Gerenciador de grupos multicast
description: Um cliente é uma entidade que chama uma função MGM, como um protocolo de roteamento ou um aplicativo administrativo.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637090"
---
# <a name="multicast-group-manager-client"></a>Cliente do Gerenciador de grupos multicast

Um cliente é uma entidade que chama uma função MGM, como um protocolo de roteamento ou um aplicativo administrativo.

A API MGM é usada principalmente por protocolos de roteamento de multicast. Os desenvolvedores de protocolos de roteamento multicast usam a API MGM para:

-   Manter Associação de grupo
-   Propriedade da interface de controle
-   Receber notificações do Gerenciador do grupo de multicast sobre solicitações de outros protocolos de roteamento multicast para dados multicast

Aplicativos administrativos específicos que devem monitorar as entradas de encaminhamento de multicast (MFEs) podem fazer isso sem adicionar ou remover a associação de grupo. Os desenvolvedores de aplicativos administrativos usam funções MGM específicas para examinar informações no MFEs.

> [!Note]  
> Os protocolos de roteamento multicast também acessam MFEs.

 

Um MFE está encaminhando as informações que o Gerenciador do grupo de multicast cria com base na associação de grupo. Os MFEs que são recuperados do Gerenciador de grupos de multicast podem fornecer informações estatísticas. Um aplicativo administrativo pode usar essas informações para determinar as ações apropriadas. Por exemplo, um aplicativo administrativo pode executar ações baseadas no volume de pacotes em uma interface específica.

 

 





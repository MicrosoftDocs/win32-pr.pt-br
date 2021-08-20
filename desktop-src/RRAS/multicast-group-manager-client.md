---
title: Cliente do Gerenciador de grupos multicast
description: Um cliente é uma entidade que chama uma função MGM, como um protocolo de roteamento ou um aplicativo administrativo.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2fceda28404e20be5d2c3192b672b1d4e20cb1f95f238f8b561a989c564f6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790411"
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

 

 





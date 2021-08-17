---
title: Triagem de objetos desnecessários
description: Se você usar Inspecionar para examinar um controle simples, como um botão de push OK no acessórios do Microsoft WordPad, poderá ver que esses objetos de janela pai também contêm vários objetos filho invisíveis.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c52dc54f2c32be3aff3e535427668943cf1ee21423636e3be8c018f6e3257b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745279"
---
# <a name="screening-out-unnecessary-objects"></a>Triagem de objetos desnecessários

Se você usar [Inspecionar](inspect-objects.md) para examinar um controle simples, como um botão de push OK no acessórios do Microsoft WordPad, poderá ver que esses objetos de janela pai também contêm vários objetos filho invisíveis. Esses objetos invisíveis têm o mesmo nome de classe de janela que o controle e têm a [propriedade State](state-property.md) [**de STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md). A tabela a seguir lista os objetos filho invisíveis que Microsoft Active Accessibility cria para o controle .



| Name          | Função                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| "Sistema"      | [**BARRA DE \_ \_ MENUS DO SISTEMA DE FUNÇÕES**](object-roles.md)     | 0          |
| Nenhum          | [**BARRA DE \_ TÍTULO DO SISTEMA DE \_ FUNÇÃO**](object-roles.md)   | 5          |
| "Aplicativo" | [**BARRA DE \_ \_ MENUS DO SISTEMA DE FUNÇÕES**](object-roles.md)     | 0          |
| "Vertical"    | [**BARRA DE \_ ROLAGEM \_ DO SISTEMA DE FUNÇÃO**](object-roles.md) | 5          |
| "Horizontal"  | [**BARRA DE \_ ROLAGEM \_ DO SISTEMA DE FUNÇÃO**](object-roles.md) | 5          |
| "Caixa de tamanho"    | [**CONTROLE DE \_ CONTROLE DO SISTEMA DE \_ FUNÇÃO**](object-roles.md)           | 0          |



 

Os desenvolvedores cliente devem identificar e filtrar esses objetos de janela pai e objetos filho invisíveis porque eles não fornecem informações significativas para os usuários finais.

 

 





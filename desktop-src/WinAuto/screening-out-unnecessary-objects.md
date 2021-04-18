---
title: Triagem de objetos desnecessários
description: Se você usar inspecionar para examinar um controle simples, como um botão de ação OK no acessório do Microsoft WordPad, poderá ver que esses objetos de janela pai também contêm vários objetos filho invisíveis.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105786130"
---
# <a name="screening-out-unnecessary-objects"></a>Triagem de objetos desnecessários

Se você usar [inspecionar](inspect-objects.md) para examinar um controle simples, como um botão de ação OK no acessório do Microsoft WordPad, poderá ver que esses objetos de janela pai também contêm vários objetos filho invisíveis. Esses objetos invisíveis têm o mesmo nome de classe de janela que o controle e têm a [propriedade State](state-property.md) do [**sistema de estado \_ \_ invisível**](object-state-constants.md). A tabela a seguir lista os objetos filho invisíveis que o Microsoft Acessibilidade Ativa cria para o controle.



| Name          | Função                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| Sistema      | [**\_BarraDeMenu do sistema de funções \_**](object-roles.md)     | 0          |
| Nenhum          | [**\_TITLEBAR do sistema de funções \_**](object-roles.md)   | 5          |
| Aplicativo | [**\_BarraDeMenu do sistema de funções \_**](object-roles.md)     | 0          |
| Vertical    | [**\_barra de rolagem do sistema de funções \_**](object-roles.md) | 5          |
| Na  | [**\_barra de rolagem do sistema de funções \_**](object-roles.md) | 5          |
| "Dimensionar caixa"    | [**\_alça do sistema de função \_**](object-roles.md)           | 0          |



 

Os desenvolvedores de cliente devem identificar e filtrar esses objetos de janela pai e objetos filho invisíveis, pois eles não fornecem informações significativas para os usuários finais.

 

 





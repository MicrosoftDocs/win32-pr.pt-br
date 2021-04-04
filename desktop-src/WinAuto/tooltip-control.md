---
title: Controle ToolTip (referência de elemento de interface do usuário do MSAA)
description: Um controle ToolTip exibe uma pequena janela pop-up que contém uma linha de texto que descreve a finalidade de uma ferramenta, representada como um objeto gráfico, em um aplicativo.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822640"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a>Controle ToolTip (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve objetos de **controle de dica de ferramenta** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **controle de dica de ferramenta** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Um controle ToolTip exibe uma pequena janela pop-up que contém uma linha de texto que descreve a finalidade de uma ferramenta, representada como um objeto gráfico, em um aplicativo.

O nome da classe da janela para uma dica de ferramenta é a classe TOOLTIPs \_ , que é definida como "classe tooltips \_ " em commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um controle ToolTip dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Um controle ToolTip dá suporte às seguintes propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                 | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | A propriedade **ChildCount** é zero.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | A propriedade **Name** é o texto contido no controle ToolTip.                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.                                                                                                                                                                                                                                                               |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | A propriedade **role** é [**\_ \_ TOOLTIP do sistema de função**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






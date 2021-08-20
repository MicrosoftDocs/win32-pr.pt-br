---
title: Controle ToolTip (Referência de elemento de interface do usuário MSAA)
description: Um controle de dica de ferramenta exibe uma pequena janela pop-up que contém uma linha de texto que descreve a finalidade de uma ferramenta, representada como um objeto gráfico, em um aplicativo.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d6bdffd240d84043e95bcbc87046d2e74ea965ba18f3f03ad1a5177654eb8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928978"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a>Controle ToolTip (Referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve objetos **de Controle de Dica de** Ferramenta para fins de Referência de Elemento de Interface do Usuário da MSAA. Como criar objetos **de Controle de Dica de** Ferramenta em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência de API para a estrutura de interface do usuário que você está usando.

 

Um controle de dica de ferramenta exibe uma pequena janela pop-up que contém uma linha de texto que descreve a finalidade de uma ferramenta, representada como um objeto gráfico, em um aplicativo.

O nome da classe de janela para uma dica de ferramenta é TOOLTIPS CLASS, que é definido como \_ "classe tooltips" \_ em Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um controle de dica de ferramenta dá suporte aos seguintes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**Acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Acclocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**Accnavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**Accselect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades IAccessible

Um controle de dica de ferramenta dá suporte às [**seguintes propriedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propriedade                                                                 | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | A **propriedade ChildCount** é zero.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | A **propriedade Name** é o texto contido no controle de dica de ferramenta.                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | A **propriedade Parent** é uma janela ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que envolve o controle e tem a mesma propriedade **Name** e o mesmo nome de classe de janela que o controle.                                                                                                                                                                                                                                                               |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | A **propriedade Role** é ROLE SYSTEM [**\_ \_ TOOLTIP**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | A **propriedade State** é uma combinação de um ou mais dos seguintes valores: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE [](object-state-constants.md)SYSTEM UNAVAILABLE STATE SYSTEM FOCUSED STATE SYSTEM \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IAccessible Interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






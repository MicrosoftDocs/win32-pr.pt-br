---
title: Botão De push (Referência de elemento de interface do usuário da MSAA)
description: Um botão de push é um objeto retangular pequeno usado para executar uma ação. Por exemplo, os botões OK e CANCEL em uma caixa de diálogo são botões de push.
ms.assetid: 26dbe4a0-4110-4569-bac6-fa0a95c785dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4056b1b2bd8f80e79916db0056de176962bd7d3d86c2b62420deaf57f90e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644486"
---
# <a name="push-button-msaa-ui-element-reference"></a>Botão De push (Referência de elemento de interface do usuário da MSAA)

Um botão de push é um objeto retangular pequeno usado para executar uma ação. Por exemplo, os **botões OK** e **CANCEL** em uma caixa de diálogo são botões de push.

O nome da classe de janela para um botão de push é "BUTTON".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um botão de push dá suporte aos seguintes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Método                                                                    | Comentários                                                                                                     |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Accdodefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | O [**método accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) clica no botão de push. |
| [**Acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                              |
| [**Acclocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                              |
| [**Accnavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                              |
| [**Accselect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                              |



 

## <a name="iaccessible-properties"></a>Propriedades IAccessible

Um botão de push dá suporte às seguintes [**propriedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A **propriedade ChildCount** é zero ou mais.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | A **propriedade DefaultAction** é "Press".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A **propriedade KeyboardShortcut** é a chave de acesso do botão, que é um caractere sublinhado no texto do texto da janela do botão. Por exemplo, "Alt+o" é a **propriedade KeyboardShortcut** para um **botão OK.**                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A **propriedade** Name é obtida do texto da janela do controle (ou legenda), que é exibido no botão de push. Por exemplo, "OK" é a **propriedade Name** para um **botão OK.**                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A **propriedade Parent** é uma janela ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que envolve o controle e tem a mesma propriedade **Name** e o mesmo nome de classe de janela que o controle.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A **propriedade Role** é ROLE SYSTEM [**\_ \_ PUSHBUTTON.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A **propriedade State** é uma combinação de um ou mais dos seguintes valores: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE [](object-state-constants.md)SYSTEM UNAVAILABLE STATE SYSTEM FOCUSED STATE FOCUSABLE STATE SYSTEM \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ PRESSED**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ PRESSED**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ DEFAULT**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IAccessible Interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Caixa de seleção**](check-box.md)
</dt> <dt>

[**Caixa de grupo**](group-box.md)
</dt> <dt>

[**Botão de Opção**](radio-button.md)
</dt> </dl>

 

 






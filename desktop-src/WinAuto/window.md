---
title: Janela (Referência de elemento de interface do usuário MSAA)
description: Microsoft Active Accessibility cria um objeto de janela genérico como um contêiner para outro objeto. Os desenvolvedores cliente não transmitem as informações de objetos de janela para usuários finais porque esses objetos não contêm informações úteis.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881eb863c6b12f8e72a9f48ba5ea290a2ad2f2471fa60683ee17e70c6271dad3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413266"
---
# <a name="window-msaa-ui-element-reference"></a>Janela (Referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve os **objetos Window** para fins de Referência de Elemento de Interface do Usuário da MSAA. Como criar objetos **window** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência de API para a estrutura de interface do usuário que você está usando.

 

Microsoft Active Accessibility cria um objeto de janela genérico como um contêiner para outro objeto. Os desenvolvedores cliente não transmitem as informações de objetos de janela para usuários finais porque esses objetos não contêm informações úteis.

Se um aplicativo de servidor cria um controle personalizado, o Microsoft Active Accessibility cria um objeto de janela que contém o controle personalizado, mas o servidor cria um objeto acessível para fornecer informações sobre o conteúdo do controle. O sistema gera eventos de nível de objeto para o objeto de janela, mas o servidor deve enviar eventos para o objeto acessível que fornece informações sobre o controle.

## <a name="iaccessible-methods"></a>Métodos IAccessible

O objeto window dá suporte aos [**seguintes métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**Acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Acclocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**Accnavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**Accselect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades IAccessible

O objeto window dá suporte às seguintes [**propriedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera a interface [IDispatch](idispatch-interface.md) do filho especificado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A **propriedade ChildCount** é 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | O próprio objeto de janela não tem uma propriedade **Description.** A **propriedade Description** do objeto filho pode ser recuperada por meio do objeto de janela.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | O próprio objeto de janela não tem uma **propriedade KeyboardShortcut.** A **propriedade KeyboardShortcut** para o objeto filho é recuperada por meio do objeto de janela.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A **propriedade Name** do objeto de janela é a mesma que o objeto filho.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A **propriedade Role** é ROLE SYSTEM [**\_ \_ WINDOW.**](object-roles.md) A **Função** do objeto filho é recuperada por meio do objeto de janela.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A **propriedade State** é uma combinação de um ou mais dos seguintes valores: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE [](object-state-constants.md)SYSTEM UNAVAILABLE STATE SYSTEM SIZEABLE STATE SYSTEM \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ MOVEABLE STATE**](object-state-constants.md) SYSTEM \| [**\_ \_ FOCUSABLE**](object-state-constants.md) STATE \| [**\_ \_ SYSTEM**](object-state-constants.md) FOCUSED<br/> |



 

## <a name="notes"></a>Observações

Os eventos [**EVENT \_ SYSTEM \_ DRAGDROPSTART**](event-constants.md), [**EVENT SYSTEM \_ \_ DRAGDROPEND**](event-constants.md), [**EVENT OBJECT \_ \_ HIDE**](event-constants.md)e [**EVENT OBJECT \_ \_ PARENTCHANGE**](event-constants.md) não são enviados pelo objeto de janela. Esse é um problema conhecido e está sendo resolvido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IAccessible Interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






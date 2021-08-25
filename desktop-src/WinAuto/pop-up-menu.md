---
title: Menu pop-up (Referência de elemento de interface do usuário MSAA)
description: Um menu pop-up exibe uma lista de comandos de menu.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b578a6af66585e06c4d9392f7051a8ebf14c8c24865bac59bf0c4fa43c7deaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861386"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>Menu pop-up (Referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve objetos **de Menu Pop-up** para fins de Referência de Elemento de Interface do Usuário da MSAA. Como criar objetos **de Menu Pop-up** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência de API para a estrutura de interface do usuário que você está usando.

 

Um menu pop-up exibe uma lista de comandos de menu. Microsoft Active Accessibility cria um objeto pop-up de menu quando um item de menu em uma barra de menus é aberto. Microsoft Active Accessibility também cria objetos pop-up de menu para menus de contexto, que são exibidos quando o usuário clica com o botão direito do mouse em um elemento de interface do usuário.

O nome da classe de janela para um menu pop-up é " \# 32768".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um menu pop-up dá suporte aos seguintes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**Acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Acclocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**Accnavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**Accselect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades IAccessible

Um menu pop-up dá suporte às seguintes [**propriedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propriedade                                                                 | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Recupera o [**IDispatch para**](idispatch-interface.md) o item de menu especificado. As IDs filho dos itens de menu são numeradas sequencialmente de cima para baixo, começando com uma.                                                                                                                                                                                                                                                                                      |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | A **propriedade ChildCount** é o número de itens de menu no menu, incluindo separadores de menu.                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | A **propriedade** Nome de um menu pop-up é o mesmo nome que o menu. A **propriedade Nome** de um menu de contexto é "Contexto".                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | A **propriedade Pai** é uma janela ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que envolve o menu pop-up e tem a mesma propriedade **Name** e o mesmo nome de classe de janela que o menu pop-up .                                                                                                                                                                                                                                                      |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | A **propriedade Role** é ROLE SYSTEM [**\_ \_ MENUPOPUP.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | A **propriedade State** é uma combinação de um ou mais dos seguintes valores: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE [](object-state-constants.md)SYSTEM UNAVAILABLE STATE SYSTEM FOCUSED STATE SYSTEM \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Observações

-   Objetos de menu pop-up não disparam [**eventos EVENT \_ OBJECT \_ CREATE**](event-constants.md) e [**EVENT OBJECT \_ \_ DESTROY.**](event-constants.md)
-   Os menus de várias colunas não são suportados com os sinalizadores [**NAVDIR \_ LEFT**](navigation-constants.md) ou [**NAVDIR \_ RIGHT**](navigation-constants.md) do [**método accNavigate.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   Os eventos [**\_ EVENT SYSTEM \_ MENUPOPUPSTART**](event-constants.md) e [**EVENT SYSTEM \_ \_ MENUPOPUPEND**](event-constants.md) não são enviados de forma consistente. Esse é um problema conhecido e está sendo resolvido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IAccessible Interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de menus**](menu-bar.md)
</dt> <dt>

[**Menu Item**](menu-item.md)
</dt> </dl>

 

 






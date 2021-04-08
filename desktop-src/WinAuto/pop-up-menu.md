---
title: Menu pop-up (referência de elemento de interface do usuário do MSAA)
description: Um menu pop-up exibe uma lista de comandos de menu.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822808"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>Menu pop-up (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos de **menu pop-up** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **menu pop-up** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Um menu pop-up exibe uma lista de comandos de menu. O Microsoft Acessibilidade Ativa cria um objeto pop-up de menu quando um item de menu em uma barra de menus é aberto. O Microsoft Acessibilidade Ativa também cria objetos pop-up de menu para menus de contexto, que são exibidos quando o usuário clica com o botão direito do mouse em um elemento de interface do usuário.

O nome da classe de janela para um menu pop-up é " \# 32768".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um menu pop-up dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Um menu pop-up dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                 | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Recupera o [**IDispatch**](idispatch-interface.md) para o item de menu especificado. As IDs filho para os itens de menu são numeradas em sequência, de cima para baixo, começando com uma.                                                                                                                                                                                                                                                                                      |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | A propriedade **ChildCount** é o número de itens de menu no menu, incluindo separadores de menu.                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | A propriedade **Name** para um menu pop-up é o mesmo nome que o menu. A propriedade **Name** de um menu de contexto é "Context".                                                                                                                                                                                                                                                                                                                                              |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que envolve o menu pop-up e tem a mesma propriedade de **nome** e nome de classe de janela que o menu pop-up.                                                                                                                                                                                                                                                      |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | A propriedade **role** é [**\_ System role \_ MENUPOPUP**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Observações

-   Os objetos de menu pop-up não disparam eventos de [**\_ \_ criação de objeto de evento**](event-constants.md) e [**\_ \_ destruição de objeto de evento**](event-constants.md) .
-   Os menus de várias colunas não dão suporte aos sinalizadores [**NAVDIR \_ esquerdo**](navigation-constants.md) ou [**NAVDIR \_ direito**](navigation-constants.md) do método [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) .
-   O sistema de eventos de eventos [**\_ \_ MENUPOPUPSTART**](event-constants.md) e o [**sistema de eventos \_ \_ MENUPOPUPEND**](event-constants.md) não são enviados de forma consistente. Esse é um problema conhecido e está sendo resolvido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de menus**](menu-bar.md)
</dt> <dt>

[**Item de menu**](menu-item.md)
</dt> </dl>

 

 






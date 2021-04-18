---
title: Controle de Up-Down (referência de elemento de interface do usuário do MSAA)
description: Um controle de cima para baixo, também conhecido como controle de rotação, combina um par de botões exibidos como setas com um controle de edição Buddy. Clicar nas setas incrementa ou Decrementa o valor no controle de edição.
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd2d28acc4c14a89ec73f5994ed0af47202145a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771507"
---
# <a name="up-down-control-msaa-ui-element-reference"></a>Controle de Up-Down (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos de **controle de cima para baixo** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **controle de cima para baixo** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Um controle de cima para baixo, também conhecido como controle de rotação, combina um par de botões exibidos como setas com um controle de edição Buddy. Clicar nas setas incrementa ou Decrementa o valor no controle de edição.

O nome da classe da janela para um controle up up é a \_ classe upDown, que é definida como "msctls \_ updown32" em commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um controle de cima para baixo dá suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Um controle up dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                 | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | A propriedade **ChildCount** é "2" (os botões de seta para cima e para baixo).                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obter \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obter \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | A propriedade **Name** para o objeto de controle de cima para baixo é obtida no texto da janela do controle (ou legenda). Esse texto não é exibido com o controle up, portanto, os desenvolvedores de servidor devem fornecer um texto significativo na instrução de definição de recurso do controle para ajudar os usuários de utilitários cliente a identificar o controle. A propriedade **Name** para o botão de seta superior no controle acima-abaixo é "more", e a propriedade **Name** para o botão de seta inferior é "less". |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | A propriedade **Parent** do controle up-down é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que envolve o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle. A propriedade **Parent** dos botões de seta para cima e para baixo é o objeto de controle de cima para baixo.                                                                                                                                                    |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | A propriedade **role** do objeto de controle up é o [**\_ \_ SPINBUTTON do sistema de função**](object-roles.md). A propriedade **role** dos botões de seta é o botão de [**\_ \_ pressão do sistema de função**](object-roles.md).                                                                                                                                                                                                                          |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | A propriedade State para o objeto de controle de cima para baixo é um dos seguintes [valores](object-state-constants.md):[**estado sistema \_ \_ focalizado**](object-state-constants.md) no \| [**estado \_ \_**](object-state-constants.md) do sistema<br/>                                                                                                                                                                                      |
| [**obter \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Observações

O Microsoft Acessibilidade Ativa expõe o controle de edição Buddy como um objeto separado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






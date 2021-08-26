---
title: Controle da barra de status (referência de elemento da interface do usuário do MSAA)
description: Barras de status exibem informações de status em uma janela horizontal na parte inferior de uma janela de aplicativo.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6c4955bfe10bc7eb224213a8e2e262179d2b122ca4eae210d0d1e72e4635b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998056"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a>Controle da barra de status (referência de elemento da interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos de **controle da barra de status** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **controle da barra de status** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Barras de status exibem informações de status em uma janela horizontal na parte inferior de uma janela de aplicativo. As barras de status geralmente são divididas em partes, chamadas de painéis e cada painel exibe informações de status diferentes. Além disso, as barras de status podem conter objetos de tipos diferentes, incluindo botões e barras de progresso. O nome da classe de janela para um controle de barra de status é STATUSCLASSNAME, que é definido como "msctls \_ statusbar32" em commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Barras de status dão suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Barras de status dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                 | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | A propriedade **ChildCount** é o número de painéis na barra de status.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | O próprio objeto da barra de status não tem uma propriedade **Name** . A propriedade **Name** de cada painel na barra de status é igual ao texto exibido.                                                                                                                                                                                                                                                                                                                   |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | A propriedade **Parent** do objeto de barra de status é uma janela [**( \_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem o mesmo nome de classe de janela que o controle. A propriedade **Parent** dos painéis na barra de status é o objeto barra de status.                                                                                                                                                                           |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | A propriedade **role** do próprio objeto da barra de status é o [**sistema de funções \_ \_ STATUSBAR**](object-roles.md). O texto exibido em uma barra de status tem o [**sistema de função \_ \_ STATICTEXT**](object-roles.md) como sua propriedade de **função** .                                                                                                                                                                                                 |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Observações

Como os atalhos de teclado não têm suporte para controles de barra de status ou áreas de texto em barras de status, [**Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) não tem suporte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






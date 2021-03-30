---
title: Window (referência de elemento de interface do usuário do MSAA)
description: O Microsoft Acessibilidade Ativa cria um objeto de janela genérico como um contêiner para outro objeto. Os desenvolvedores de cliente não transmitem as informações de objetos de janela para os usuários finais porque esses objetos não contêm informações úteis.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87c8601ecd6344dc82bbdb416055c694687e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635492"
---
# <a name="window-msaa-ui-element-reference"></a>Window (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve objetos de **janela** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **janela** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

O Microsoft Acessibilidade Ativa cria um objeto de janela genérico como um contêiner para outro objeto. Os desenvolvedores de cliente não transmitem as informações de objetos de janela para os usuários finais porque esses objetos não contêm informações úteis.

Se um aplicativo de servidor criar um controle personalizado, o Microsoft Acessibilidade Ativa criará um objeto Window que contém o controle personalizado, mas o servidor criará um objeto acessível para fornecer informações sobre o conteúdo do controle. O sistema gera eventos de nível de objeto para o objeto Window, mas o servidor deve enviar eventos para o objeto acessível que fornece informações sobre o controle.

## <a name="iaccessible-methods"></a>Métodos IAccessible

O objeto Window dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

O objeto Window dá suporte às seguintes propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera a interface [IDispatch](idispatch-interface.md) do filho especificado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A propriedade **ChildCount** é 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | O objeto Window em si não tem uma propriedade **Description** . A propriedade **Description** do objeto filho pode ser recuperada por meio do objeto Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | O objeto Window em si não tem uma propriedade **KeyboardShortcut** . A propriedade **KeyboardShortcut** do objeto filho é recuperada por meio do objeto Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** do objeto Window é igual ao objeto filho.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é [**\_ \_ janela do sistema de funções**](object-roles.md). A **função** do objeto filho é recuperada por meio do objeto Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) estado do sistema \| [**\_ \_ considerável**](object-state-constants.md) \| [**estado sistema \_ \_ móvel**](object-state-constants.md) estado \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema estado do sistema focalizado<br/> |



 

## <a name="notes"></a>Observações

O sistema de eventos de eventos [**\_ \_ DRAGDROPSTART**](event-constants.md), o [**sistema de eventos \_ \_ DRAGDROPEND**](event-constants.md), o objeto de evento [**\_ \_ Hide**](event-constants.md)e o [**objeto de evento \_ \_ PARENTCHANGE**](event-constants.md) não são enviados pelo objeto Window. Esse é um problema conhecido e está sendo resolvido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






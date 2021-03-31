---
title: Controle de barra de progresso (referência de elemento de interface do usuário MSAA)
description: Os controles de barra de progresso indicam o progresso de uma operação demorada, como baixar um arquivo da Internet. Geralmente, o progresso é expresso como um percentual de zero (0) a 100 (100).
ms.assetid: 9165d00e-b3f3-41cd-812c-cd39313460fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9bbd9a648ee1c4d4f112577c8e41a5983f69038
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160182"
---
# <a name="progress-bar-control-msaa-ui-element-reference"></a>Controle de barra de progresso (referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve os objetos de **controle da barra de progresso** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **controle de barra de progresso** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Os controles de barra de progresso indicam o progresso de uma operação demorada, como baixar um arquivo da Internet. Geralmente, o progresso é expresso como um percentual de zero (0) a 100 (100).

O nome da classe de janela para um controle de barra de progresso é a \_ classe Progress, que é definida como "msctls \_ Progress" em commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Os controles de barra de progresso dão suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Os controles de barra de progresso dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A propriedade **ChildCount** é zero.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A propriedade **KeyboardShortcut** é a chave de acesso da barra de progresso, que é um caractere sublinhado no texto do rótulo da barra de progresso. A cadeia de caracteres retornada contém o caractere de chave de acesso anexado à cadeia de caracteres "Alt +".                                                                                                                                                                                                                                 |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** é o texto de um controle de texto estático que rotula a barra de progresso.                                                                                                                                                                                                                                                                                                                                                                               |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.                                                                                                                                                                                                                                                              |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é o [**sistema de função \_ \_ PROGRESSBAR**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md):[**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)<br/> |
| [**obter \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | A propriedade **Value** é uma cadeia de caracteres de "0%" a "100%" que descreve o progresso.                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






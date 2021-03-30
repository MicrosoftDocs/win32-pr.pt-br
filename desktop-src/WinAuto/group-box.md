---
title: Caixa de grupo (referência de elemento de interface do usuário do MSAA)
description: Uma caixa de grupo é um retângulo que circunda um conjunto de controles, como caixas de seleção ou botões de opção, e contém um texto definido pelo aplicativo (rótulo).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636592"
---
# <a name="group-box-msaa-ui-element-reference"></a>Caixa de grupo (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos da **caixa de grupo** para fins de referência de elemento da interface do usuário do MSAA. A criação de objetos de **caixa de grupo** em várias estruturas de interface do usuário não é descrita aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Uma caixa de grupo é um retângulo que circunda um conjunto de controles, como caixas de seleção ou botões de opção, e contém um texto definido pelo aplicativo (rótulo).

A única finalidade de uma caixa de grupo é organizar os controles relacionados por uma finalidade comum, indicada pelo rótulo.

O nome da classe de janela para uma caixa de grupo é "BUTTON".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Uma caixa de grupo dá suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Uma caixa de grupo dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A propriedade **ChildCount** é sempre zero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | As caixas de grupo não têm atalhos de teclado. No entanto, se o texto da janela da caixa de grupo contiver um caractere de e comercial (&), o Microsoft Acessibilidade Ativa retornará uma cadeia de caracteres não nula como a propriedade **KeyboardShortcut** .                                                                                                                                                                                                                                            |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** é obtida no texto da janela do controle (ou legenda), que é exibido com a caixa de grupo.                                                                                                                                                                                                                                                                                                                                                    |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.                                                                                                                                                                                                                                                              |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é [**\_ \_ agrupamento do sistema de funções**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                            |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md):[**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






---
title: Controle de cabeçalho (referência de elemento de interface do usuário do MSAA)
description: Um controle de cabeçalho exibe os títulos na parte superior das colunas de informações e permite que o usuário classifique as informações clicando nos títulos. Windows O Explorer usa um controle de cabeçalho quando a exibição detalhes é selecionada.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c378bb0244e94f4cb95c8b2ba90512d2b17542bdef7428197ee58479dbfde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994176"
---
# <a name="header-control-msaa-ui-element-reference"></a>Controle de cabeçalho (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve objetos de **controle de cabeçalho** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **controle de cabeçalho** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Um controle de cabeçalho exibe os títulos na parte superior das colunas de informações e permite que o usuário classifique as informações clicando nos títulos. Windows O Explorer usa um controle de cabeçalho quando a exibição detalhes é selecionada.

O nome de classe da janela para um controle de cabeçalho é WC \_ header, que é definido como "SysHeader32" em commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um controle de cabeçalho dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentários                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Esse método executa a ação padrão clicando no cabeçalho. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Um controle de cabeçalho dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                       | Comentários                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | A propriedade **ChildCount** é zero.                                                                                                                                                                                                   |
| [**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | A propriedade **DefaultAction** é "click".                                                                                                                                                                                             |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | A propriedade **Name** é igual ao nome do cabeçalho da coluna.                                                                                                                                                                    |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | A propriedade **Parent** é uma janela ( [**\_ \_ lista de sistema de funções**](object-roles.md) ) que circunda o controle e tem o mesmo nome de classe de janela que o controle.                                                      |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | A propriedade **role** é o [**sistema de função \_ \_ COLUMNHEADER**](object-roles.md).                                                                                                                                  |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | O valor da propriedade **estado** é sempre [**estado \_ sistema \_ ReadOnly**](object-state-constants.md) e também pode incluir o [**estado do \_ sistema \_ invisível**](object-state-constants.md). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





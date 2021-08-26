---
title: Botão de opção (referência de elemento de interface do usuário do MSAA)
description: Os botões de opção são usados para selecionar uma das várias opções, geralmente dentro de uma caixa de diálogo.
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c560e4efa57790980d852ab2716248d5b1d7faff535592f3f2ca892f3dff0715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998136"
---
# <a name="radio-button-msaa-ui-element-reference"></a>Botão de opção (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve objetos de **botão de opção** para fins de referência de elemento da interface do usuário do MSAA. A criação de objetos de **botão de opção** em várias estruturas de interface do usuário não é descrita aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Os botões de opção são usados para selecionar uma das várias opções, geralmente dentro de uma caixa de diálogo. Um botão de opção contém um círculo pequeno com texto ao lado dele. Quando selecionado, o círculo tem um círculo menor e preenchido dentro dele. A seleção de um botão em um conjunto anula a seleção do botão selecionado anteriormente, de modo que apenas uma das opções no conjunto é selecionada de cada vez.

O nome de classe da janela para um botão de opção é "BUTTON".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um botão de opção dá suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentários                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | O método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) clica no botão de opção. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Um botão de opção dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A propriedade **ChildCount** é zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | A propriedade **DefaultAction** para um botão de opção é "check".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A propriedade **KeyboardShortcut** é a tecla de acesso do botão de opção, que é um caractere sublinhado no texto da janela do controle. Essa cadeia de caracteres contém o caractere de chave de acesso anexado à cadeia de caracteres "Alt +".                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** é obtida no texto da janela do controle (ou legenda), que é exibido com o botão de opção.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é um [**botão de \_ \_ opção do sistema de função**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado sistema \_ \_ indisponível**](object-state-constants.md) sistema de \| [**estado \_ \_ focalizado**](object-state-constants.md) sistema estado \| com [**\_ \_ foco**](object-state-constants.md) sistemas \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) de estado marcado sistema de Estados marcados como sistema normal<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Caixa de seleção**](check-box.md)
</dt> <dt>

[**Caixa de grupo**](group-box.md)
</dt> <dt>

[**Botão de ação**](push-button.md)
</dt> </dl>

 

 






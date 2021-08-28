---
title: Controle de teclas de acesso (referência de elemento de interface do usuário do MSAA)
description: Os controles de teclas de acesso permitem que os usuários insiram uma combinação de pressionamentos de teclas usados como uma tecla de atalho, o que permite executar uma ação rapidamente. Um controle de tecla de atalho exibe os pressionamentos de teclas inseridos pelo usuário e garante que o usuário selecione uma combinação de teclas válida.
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53829b371ea026c92388e8ed0dac11ee0303514ff930ad1a64ada4b5583bfa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734436"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a>Controle de teclas de acesso (referência de elemento de interface do usuário do MSAA)

Os controles de teclas de acesso permitem que os usuários insiram uma combinação de pressionamentos de teclas usados como uma tecla de atalho, o que permite executar uma ação rapidamente. Um controle de tecla de atalho exibe os pressionamentos de teclas inseridos pelo usuário e garante que o usuário selecione uma combinação de teclas válida.

O nome da classe de janela para um controle de tecla de atalho é a classe de tecla de acesso \_ , que é definida como "msctls \_ hotkey32" em commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Os controles de tecla quente dão suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Os controles de tecla de acesso dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A propriedade **ChildCount** é sempre zero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A propriedade **KeyboardShortcut** é a tecla de acesso do controle de tecla quente, que é um caractere sublinhado no texto do rótulo do controle de tecla de atalho. A cadeia de caracteres retornada contém o caractere de chave de acesso anexado à cadeia de caracteres "Alt +".                                                                                                                                                                                                                                 |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** é o texto de um controle de texto estático que rotula o controle de tecla de acesso.                                                                                                                                                                                                                                                                                                                                                                            |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.                                                                                                                                                                                                                                                              |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é [**role do \_ sistema de \_ atalho**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md):[**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)<br/> |
| [**obter \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | A propriedade **Value** é uma cadeia de caracteres que contém o texto no campo de tecla de acesso.                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






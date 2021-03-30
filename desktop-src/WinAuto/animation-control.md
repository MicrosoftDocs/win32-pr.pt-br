---
title: Controle de animação (referência de elemento de interface do usuário do MSAA)
description: Os controles de animação exibem silenciosamente um clipe AVI (vídeo de áudio Intercalado). Os controles de animação são geralmente exibidos quando os arquivos estão sendo copiados ou quando alguma outra tarefa demorada está sendo executada.
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ca7cf7e4b8a2174dae81b1770b2d877f749502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635966"
---
# <a name="animation-control-msaa-ui-element-reference"></a>Controle de animação (referência de elemento de interface do usuário do MSAA)

Os controles de animação exibem silenciosamente um clipe AVI (vídeo de áudio Intercalado). Os controles de animação são geralmente exibidos quando os arquivos estão sendo copiados ou quando alguma outra tarefa demorada está sendo executada.

O nome da classe da janela para um controle de animação é a \_ classe Animate, que é definida como "SysAnimate32" em commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Os controles de animação dão suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Os controles de animação dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A propriedade **ChildCount** é zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Os controles de animação não têm atalhos de teclado. No entanto, se o rótulo do controle contiver uma tecla de acesso (um caractere sublinhado no texto do rótulo do controle), [**Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) retornará uma cadeia de caracteres não nula. Essa cadeia de caracteres contém o caractere de chave de acesso anexado à cadeia de caracteres "Alt +". Por exemplo, se o rótulo for "baixando arquivos", **KeyboardShortcut** será "Alt + d".                                                                                        |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** é obtida do controle de texto estático que rotula o controle de animação. Ao criar controles, os desenvolvedores de servidor devem garantir que um controle de texto estático preceda imediatamente o controle que ele rotula dentro da ordem de tabulação.                                                                                                                                                                                                                                                                                             |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é [**\_ \_ animação do sistema de funções**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade **State** é uma combinação de uma ou mais das seguintes constantes de estado do objeto: estado do sistema de estado [**\_ \_ invisível**](object-state-constants.md) do sistema \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema de estado com foco<br/> Para obter mais informações, consulte [constantes de estado de objeto](object-state-constants.md).<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






---
title: Como formatar texto em controles de edição avançados
description: Um aplicativo pode enviar mensagens para um controle de edição rico a fim de formatar caracteres e parágrafos e recuperar informações de formatação.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103640345"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a>Como formatar texto em controles de edição avançados

Um aplicativo pode enviar mensagens para um controle de edição rico a fim de formatar caracteres e parágrafos e recuperar informações de formatação. Os atributos de formatação de parágrafo incluem alinhamento, tabulações, recuos, numeração e tabelas simples. Para caracteres, você pode especificar o nome, o tamanho, a cor e os efeitos da fonte, como negrito, itálico e protegido.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="format-text-in-a-rich-edit-control"></a>Formatar texto em um controle de edição rico

Você pode aplicar a formatação de parágrafo usando a mensagem em [**\_ SETPARAFORMAT**](em-setparaformat.md) . Para determinar a formatação de parágrafo atual para o texto selecionado, use a mensagem em [**\_ GETPARAFORMAT**](em-getparaformat.md) . A estrutura [**PARAformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) ou [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) é usada com ambas as mensagens para especificar atributos de formatação de parágrafo.

Você pode aplicar a formatação de caracteres usando a mensagem em [**\_ SETCHARFORMAT**](em-setcharformat.md) . Para determinar a formatação de caractere atual para o texto selecionado, você pode usar a mensagem em [**\_ GETCHARFORMAT**](em-getcharformat.md) . A estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) ou [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) é usada com ambas as mensagens para especificar atributos de caractere.

Você também pode usar mensagens em [**\_ SETCHARFORMAT**](em-setcharformat.md) e em [**\_ GETCHARFORMAT**](em-getcharformat.md) para definir e recuperar a formatação de caracteres do ponto de inserção, que é a formatação aplicada a qualquer caractere inserido subsequentemente. Por exemplo, se um aplicativo definir a formatação de caractere padrão como negrito e o usuário digitar um caractere, esse caractere será negrito.

A formatação de caractere do ponto de inserção será aplicada somente ao texto inserido recentemente se a seleção atual estiver vazia (se a seleção atual for um ponto de inserção). Caso contrário, o novo texto assume a formatação de caractere do texto que ele substitui. Se a seleção for alterada, a formatação de caractere padrão será alterada para corresponder ao primeiro caractere na nova seleção.

O efeito de caractere protegido é exclusivo, pois não altera a aparência do texto. Se o usuário tentar modificar o texto protegido, um controle rich edit enviará a janela pai um código de notificação [ \_ protegido por en](en-protected.md) , permitindo que a janela pai permita ou impeça a alteração. Para receber esse código de notificação, você deve habilitá-lo usando a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

A cor de primeiro plano é sempre um atributo de caractere. No Microsoft Rich Edit 1,0, a cor do plano de fundo é apenas uma propriedade do controle rich edit. Para definir a cor do plano de fundo padrão, use a mensagem em [**\_ SETBKGNDCOLOR**](em-setbkgndcolor.md) . Observe que a edição rica não dá suporte à mensagem [**\_ CTLCOLOREDIT do WM**](wm-ctlcoloredit.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





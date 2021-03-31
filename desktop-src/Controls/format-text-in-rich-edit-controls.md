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
# <a name="how-to-format-text-in-rich-edit-controls"></a><span data-ttu-id="89ab3-103">Como formatar texto em controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="89ab3-103">How to Format Text in Rich Edit Controls</span></span>

<span data-ttu-id="89ab3-104">Um aplicativo pode enviar mensagens para um controle de edição rico a fim de formatar caracteres e parágrafos e recuperar informações de formatação.</span><span class="sxs-lookup"><span data-stu-id="89ab3-104">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="89ab3-105">Os atributos de formatação de parágrafo incluem alinhamento, tabulações, recuos, numeração e tabelas simples.</span><span class="sxs-lookup"><span data-stu-id="89ab3-105">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="89ab3-106">Para caracteres, você pode especificar o nome, o tamanho, a cor e os efeitos da fonte, como negrito, itálico e protegido.</span><span class="sxs-lookup"><span data-stu-id="89ab3-106">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="89ab3-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="89ab3-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="89ab3-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="89ab3-108">Technologies</span></span>

-   [<span data-ttu-id="89ab3-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="89ab3-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="89ab3-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="89ab3-110">Prerequisites</span></span>

-   <span data-ttu-id="89ab3-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="89ab3-111">C/C++</span></span>
-   <span data-ttu-id="89ab3-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="89ab3-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="89ab3-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="89ab3-113">Instructions</span></span>

### <a name="format-text-in-a-rich-edit-control"></a><span data-ttu-id="89ab3-114">Formatar texto em um controle de edição rico</span><span class="sxs-lookup"><span data-stu-id="89ab3-114">Format Text in a Rich Edit Control</span></span>

<span data-ttu-id="89ab3-115">Você pode aplicar a formatação de parágrafo usando a mensagem em [**\_ SETPARAFORMAT**](em-setparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="89ab3-115">You can apply paragraph formatting by using the [**EM\_SETPARAFORMAT**](em-setparaformat.md) message.</span></span> <span data-ttu-id="89ab3-116">Para determinar a formatação de parágrafo atual para o texto selecionado, use a mensagem em [**\_ GETPARAFORMAT**](em-getparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="89ab3-116">To determine the current paragraph formatting for the selected text, use the [**EM\_GETPARAFORMAT**](em-getparaformat.md) message.</span></span> <span data-ttu-id="89ab3-117">A estrutura [**PARAformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) ou [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) é usada com ambas as mensagens para especificar atributos de formatação de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="89ab3-117">The [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) or [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure is used with both messages to specify paragraph formatting attributes.</span></span>

<span data-ttu-id="89ab3-118">Você pode aplicar a formatação de caracteres usando a mensagem em [**\_ SETCHARFORMAT**](em-setcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="89ab3-118">You can apply character formatting by using the [**EM\_SETCHARFORMAT**](em-setcharformat.md) message.</span></span> <span data-ttu-id="89ab3-119">Para determinar a formatação de caractere atual para o texto selecionado, você pode usar a mensagem em [**\_ GETCHARFORMAT**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="89ab3-119">To determine the current character formatting for the selected text, you can use the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span> <span data-ttu-id="89ab3-120">A estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) ou [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) é usada com ambas as mensagens para especificar atributos de caractere.</span><span class="sxs-lookup"><span data-stu-id="89ab3-120">The [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) or [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure is used with both messages to specify character attributes.</span></span>

<span data-ttu-id="89ab3-121">Você também pode usar mensagens em [**\_ SETCHARFORMAT**](em-setcharformat.md) e em [**\_ GETCHARFORMAT**](em-getcharformat.md) para definir e recuperar a formatação de caracteres do ponto de inserção, que é a formatação aplicada a qualquer caractere inserido subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="89ab3-121">You can also use [**EM\_SETCHARFORMAT**](em-setcharformat.md) and [**EM\_GETCHARFORMAT**](em-getcharformat.md) messages to set and retrieve the character formatting of the insertion point, which is the formatting that is applied to any subsequently inserted characters.</span></span> <span data-ttu-id="89ab3-122">Por exemplo, se um aplicativo definir a formatação de caractere padrão como negrito e o usuário digitar um caractere, esse caractere será negrito.</span><span class="sxs-lookup"><span data-stu-id="89ab3-122">For example, if an application sets the default character formatting to bold and the user then types a character, that character is bold.</span></span>

<span data-ttu-id="89ab3-123">A formatação de caractere do ponto de inserção será aplicada somente ao texto inserido recentemente se a seleção atual estiver vazia (se a seleção atual for um ponto de inserção).</span><span class="sxs-lookup"><span data-stu-id="89ab3-123">The character formatting of the insertion point is applied to newly inserted text only if the current selection is empty (if the current selection is an insertion point).</span></span> <span data-ttu-id="89ab3-124">Caso contrário, o novo texto assume a formatação de caractere do texto que ele substitui.</span><span class="sxs-lookup"><span data-stu-id="89ab3-124">Otherwise, the new text assumes the character formatting of the text it replaces.</span></span> <span data-ttu-id="89ab3-125">Se a seleção for alterada, a formatação de caractere padrão será alterada para corresponder ao primeiro caractere na nova seleção.</span><span class="sxs-lookup"><span data-stu-id="89ab3-125">If the selection changes, the default character formatting changes to match the first character in the new selection.</span></span>

<span data-ttu-id="89ab3-126">O efeito de caractere protegido é exclusivo, pois não altera a aparência do texto.</span><span class="sxs-lookup"><span data-stu-id="89ab3-126">The protected character effect is unique in that it does not change the appearance of text.</span></span> <span data-ttu-id="89ab3-127">Se o usuário tentar modificar o texto protegido, um controle rich edit enviará a janela pai um código de notificação [ \_ protegido por en](en-protected.md) , permitindo que a janela pai permita ou impeça a alteração.</span><span class="sxs-lookup"><span data-stu-id="89ab3-127">If the user attempts to modify protected text, a rich edit control sends its parent window an [EN\_PROTECTED](en-protected.md) notification code, allowing the parent window to allow or prevent the change.</span></span> <span data-ttu-id="89ab3-128">Para receber esse código de notificação, você deve habilitá-lo usando a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="89ab3-128">To receive this notification code, you must enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="89ab3-129">A cor de primeiro plano é sempre um atributo de caractere.</span><span class="sxs-lookup"><span data-stu-id="89ab3-129">Foreground color is always a character attribute.</span></span> <span data-ttu-id="89ab3-130">No Microsoft Rich Edit 1,0, a cor do plano de fundo é apenas uma propriedade do controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="89ab3-130">In Microsoft Rich Edit 1.0, background color is only a property of the rich edit control.</span></span> <span data-ttu-id="89ab3-131">Para definir a cor do plano de fundo padrão, use a mensagem em [**\_ SETBKGNDCOLOR**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="89ab3-131">To set the default background color, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span> <span data-ttu-id="89ab3-132">Observe que a edição rica não dá suporte à mensagem [**\_ CTLCOLOREDIT do WM**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="89ab3-132">Note that Rich Edit does not support the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89ab3-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89ab3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89ab3-134">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="89ab3-134">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="89ab3-135">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="89ab3-135">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





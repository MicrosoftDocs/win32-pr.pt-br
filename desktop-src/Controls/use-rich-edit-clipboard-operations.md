---
title: Como usar operações de edição de área de transferência avançadas
description: Um aplicativo pode colar o conteúdo da área de transferência em um controle de edição rico usando o melhor formato de área de transferência disponível ou um formato de área de transferência específico.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917726"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a><span data-ttu-id="e07d5-103">Como usar operações de edição de área de transferência avançadas</span><span class="sxs-lookup"><span data-stu-id="e07d5-103">How to Use Rich Edit Clipboard Operations</span></span>

<span data-ttu-id="e07d5-104">Um aplicativo pode colar o conteúdo da área de transferência em um controle de edição rico usando o melhor formato de área de transferência disponível ou um formato de área de transferência específico.</span><span class="sxs-lookup"><span data-stu-id="e07d5-104">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="e07d5-105">Você também pode determinar se um controle de edição rico é capaz de colar um formato de área de transferência.</span><span class="sxs-lookup"><span data-stu-id="e07d5-105">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e07d5-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="e07d5-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e07d5-107">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="e07d5-107">Technologies</span></span>

-   [<span data-ttu-id="e07d5-108">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="e07d5-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e07d5-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e07d5-109">Prerequisites</span></span>

-   <span data-ttu-id="e07d5-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="e07d5-110">C/C++</span></span>
-   <span data-ttu-id="e07d5-111">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="e07d5-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e07d5-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="e07d5-112">Instructions</span></span>

### <a name="use-a-rich-edit-clipboard-operation"></a><span data-ttu-id="e07d5-113">Usar uma operação de edição rica da área de transferência</span><span class="sxs-lookup"><span data-stu-id="e07d5-113">Use a Rich Edit Clipboard Operation</span></span>

<span data-ttu-id="e07d5-114">Assim como com um controle de edição, você pode copiar ou recortar o conteúdo da seleção atual usando a mensagem do [**WM \_ Copy**](/windows/desktop/dataxchg/wm-copy) ou o [**\_ recortar do WM**](/windows/desktop/dataxchg/wm-cut) .</span><span class="sxs-lookup"><span data-stu-id="e07d5-114">As with an edit control, you can copy or cut the contents of the current selection by using the [**WM\_COPY**](/windows/desktop/dataxchg/wm-copy) or [**WM\_CUT**](/windows/desktop/dataxchg/wm-cut) message.</span></span> <span data-ttu-id="e07d5-115">Da mesma forma, você pode colar o conteúdo da área de transferência em um controle de edição rico usando a mensagem de [**\_ colagem do WM**](/windows/desktop/dataxchg/wm-paste) .</span><span class="sxs-lookup"><span data-stu-id="e07d5-115">Similarly, you can paste the contents of the clipboard into a rich edit control by using the [**WM\_PASTE**](/windows/desktop/dataxchg/wm-paste) message.</span></span> <span data-ttu-id="e07d5-116">O controle cola o primeiro formato disponível que ele reconhece, o que presumivelmente é o formato mais descritivo.</span><span class="sxs-lookup"><span data-stu-id="e07d5-116">The control pastes the first available format that it recognizes, which presumably is the most descriptive format.</span></span>

<span data-ttu-id="e07d5-117">Para colar um formato de área de transferência específico, você pode usar a mensagem em [**\_ PASTESPECIAL**](em-pastespecial.md) .</span><span class="sxs-lookup"><span data-stu-id="e07d5-117">To paste a specific clipboard format, you can use the [**EM\_PASTESPECIAL**](em-pastespecial.md) message.</span></span> <span data-ttu-id="e07d5-118">Essa mensagem é útil para aplicativos com um comando **colar especial** que permite ao usuário selecionar o formato da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="e07d5-118">This message is useful for applications with a **Paste Special** command that enables the user to select the clipboard format.</span></span> <span data-ttu-id="e07d5-119">Você pode usar a mensagem em [**\_ CanPaste**](em-canpaste.md) para determinar se um determinado formato é reconhecido pelo controle.</span><span class="sxs-lookup"><span data-stu-id="e07d5-119">You can use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether a given format is recognized by the control.</span></span>

<span data-ttu-id="e07d5-120">Você também pode usar a mensagem em [**\_ CanPaste**](em-canpaste.md) para determinar se qualquer formato de área de transferência disponível é reconhecido por um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="e07d5-120">You can also use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether any available clipboard format is recognized by a rich edit control.</span></span> <span data-ttu-id="e07d5-121">Essa mensagem é útil ao processar a [**mensagem \_ INITMENUPOPUP do WM**](/windows/desktop/menurc/wm-initmenupopup) .</span><span class="sxs-lookup"><span data-stu-id="e07d5-121">This message is useful when processing the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message.</span></span> <span data-ttu-id="e07d5-122">Um aplicativo pode habilitar ou cinza o comando **Paste** , dependendo se o controle pode colar qualquer formato disponível.</span><span class="sxs-lookup"><span data-stu-id="e07d5-122">An application might enable or gray its **Paste** command depending on whether the control can paste any available format.</span></span>

<span data-ttu-id="e07d5-123">Os controles de edição avançados registram dois formatos de área de transferência:</span><span class="sxs-lookup"><span data-stu-id="e07d5-123">Rich edit controls register two clipboard formats:</span></span>

-   <span data-ttu-id="e07d5-124">Formato de Rich Text</span><span class="sxs-lookup"><span data-stu-id="e07d5-124">Rich Text Format</span></span>
-   <span data-ttu-id="e07d5-125">Formato de Rich Text sem objetos</span><span class="sxs-lookup"><span data-stu-id="e07d5-125">Rich Text Format Without Objects</span></span>
-   <span data-ttu-id="e07d5-126">Texto e objetos RichEdit</span><span class="sxs-lookup"><span data-stu-id="e07d5-126">RichEdit Text and Objects</span></span>

<span data-ttu-id="e07d5-127">Um aplicativo pode registrar esses formatos usando a função [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) , especificando os valores do CF \_ RTF, CF \_ RTFNOOBJS e CF \_ RETEXTOBJ.</span><span class="sxs-lookup"><span data-stu-id="e07d5-127">An application can register these formats by using the [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) function, specifying the CF\_RTF, CF\_RTFNOOBJS, and CF\_RETEXTOBJ values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e07d5-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e07d5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e07d5-129">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="e07d5-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="e07d5-130">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="e07d5-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 
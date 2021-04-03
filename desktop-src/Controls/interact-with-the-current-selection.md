---
title: Como interagir com a seleção atual
description: O usuário pode selecionar o texto em um controle de edição rico usando o mouse ou o teclado.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103640344"
---
# <a name="how-to-interact-with-the-current-selection"></a><span data-ttu-id="2f838-103">Como interagir com a seleção atual</span><span class="sxs-lookup"><span data-stu-id="2f838-103">How to Interact with the Current Selection</span></span>

<span data-ttu-id="2f838-104">O usuário pode selecionar o texto em um controle de edição rico usando o mouse ou o teclado.</span><span class="sxs-lookup"><span data-stu-id="2f838-104">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="2f838-105">A *seleção atual* é o intervalo de caracteres selecionados ou a posição do ponto de inserção se nenhum caractere for selecionado.</span><span class="sxs-lookup"><span data-stu-id="2f838-105">The *current selection* is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="2f838-106">Um aplicativo pode obter informações sobre a seleção atual, defini-la, determinar quando ela é alterada e mostrar ou ocultar o realce de seleção.</span><span class="sxs-lookup"><span data-stu-id="2f838-106">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2f838-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="2f838-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2f838-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="2f838-108">Technologies</span></span>

-   [<span data-ttu-id="2f838-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="2f838-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2f838-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2f838-110">Prerequisites</span></span>

-   <span data-ttu-id="2f838-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="2f838-111">C/C++</span></span>
-   <span data-ttu-id="2f838-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="2f838-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2f838-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="2f838-113">Instructions</span></span>

### <a name="interact-with-the-current-selection"></a><span data-ttu-id="2f838-114">Interagir com a seleção atual</span><span class="sxs-lookup"><span data-stu-id="2f838-114">Interact with the Current Selection</span></span>

<span data-ttu-id="2f838-115">Para determinar a seleção atual em um controle de edição rico, use a mensagem em [**\_ EXGETSEL**](em-exgetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="2f838-115">To determine the current selection in a rich edit control, use the [**EM\_EXGETSEL**](em-exgetsel.md) message.</span></span> <span data-ttu-id="2f838-116">Para definir a seleção atual, use a mensagem em [**\_ EXSETSEL**](em-exsetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="2f838-116">To set the current selection, use the [**EM\_EXSETSEL**](em-exsetsel.md) message.</span></span> <span data-ttu-id="2f838-117">A estrutura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) é usada com as duas mensagens e especifica um intervalo de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2f838-117">The [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure is used with both messages and specifies a range of characters.</span></span> <span data-ttu-id="2f838-118">Para recuperar informações sobre o conteúdo da seleção atual, você pode usar a mensagem [**de \_ SelectionType**](em-selectiontype.md) em em.</span><span class="sxs-lookup"><span data-stu-id="2f838-118">To retrieve information about the contents of the current selection, you can use the [**EM\_SELECTIONTYPE**](em-selectiontype.md) message.</span></span>

<span data-ttu-id="2f838-119">Um aplicativo pode detectar quando a seleção atual muda processando o código de notificação [en \_ SELCHANGE](en-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="2f838-119">An application can detect when the current selection changes by processing the [EN\_SELCHANGE](en-selchange.md) notification code.</span></span> <span data-ttu-id="2f838-120">O código de notificação especifica uma estrutura [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que contém informações sobre a nova seleção.</span><span class="sxs-lookup"><span data-stu-id="2f838-120">The notification code specifies a [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that contains information about the new selection.</span></span> <span data-ttu-id="2f838-121">Um controle de edição rico envia esse código de notificação somente se você habilitá-lo usando a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="2f838-121">A rich edit control sends this notification code only if you enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="2f838-122">Por padrão, um controle rich edit mostra e oculta o realce de seleção quando ele ganha e perde o foco.</span><span class="sxs-lookup"><span data-stu-id="2f838-122">By default, a rich edit control shows and hides the selection highlight when it gains and loses the focus.</span></span> <span data-ttu-id="2f838-123">Você pode mostrar ou ocultar o realce de seleção a qualquer momento usando a mensagem em [**\_ HIDESELECTION**](em-hideselection.md) .</span><span class="sxs-lookup"><span data-stu-id="2f838-123">You can show or hide the selection highlight at any time by using the [**EM\_HIDESELECTION**](em-hideselection.md) message.</span></span> <span data-ttu-id="2f838-124">Por exemplo, um aplicativo pode fornecer uma caixa de diálogo de pesquisa para localizar texto em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="2f838-124">For example, an application might provide a Search dialog box to find text in a rich edit control.</span></span> <span data-ttu-id="2f838-125">O aplicativo pode selecionar texto correspondente sem fechar a caixa de diálogo; nesse caso, ele deve usar a mensagem em **\_ HIDESELECTION** para realçar a seleção.</span><span class="sxs-lookup"><span data-stu-id="2f838-125">The application might select matching text without closing the dialog box, in which case it must use the **EM\_HIDESELECTION** message to highlight the selection.</span></span>

<span data-ttu-id="2f838-126">Assim como com os controles de edição, você pode especificar o estilo de janela [**es \_ NOHIDESEL**](edit-control-styles.md) para impedir que um controle de edição rico oculte o realce de seleção quando ele perder o foco.</span><span class="sxs-lookup"><span data-stu-id="2f838-126">As with edit controls, you can specify the [**ES\_NOHIDESEL**](edit-control-styles.md) window style to prevent a rich edit control from hiding the selection highlight when it loses the focus.</span></span>

<span data-ttu-id="2f838-127">Como alternativa ao uso das mensagens [**em \_ EXGETSEL**](em-exgetsel.md) e [**em \_ EXSETSEL**](em-exsetsel.md) , você pode recuperar e definir a seleção atual usando as mensagens de controle de edição em [**\_ GETSEL**](em-getsel.md) e em [**\_ SETSEL**](em-setsel.md) .</span><span class="sxs-lookup"><span data-stu-id="2f838-127">As an alternative to using the [**EM\_EXGETSEL**](em-exgetsel.md) and [**EM\_EXSETSEL**](em-exsetsel.md) messages, you can retrieve and set the current selection by using the [**EM\_GETSEL**](em-getsel.md) and [**EM\_SETSEL**](em-setsel.md) edit control messages.</span></span> <span data-ttu-id="2f838-128">Os pacotes de mensagens em **\_ GETSEL** são índices de caracteres de 2 16 bits em seu valor de retorno de 32 bits e, portanto, funciona apenas para seleções que se enquadram inteiramente dentro dos primeiros 64K.</span><span class="sxs-lookup"><span data-stu-id="2f838-128">The **EM\_GETSEL** message packs two 16-bit character indexes into its 32-bit return value and therefore, works only for selections that fall entirely within the first 64K.</span></span> <span data-ttu-id="2f838-129">No entanto, um controle de edição rico nunca conterá mais de 32K caracteres de texto, a menos que você estenda esse limite usando a mensagem em [**\_ LIMITTEXT**](em-limittext.md) ou em [**\_ EXLIMITTEXT**](em-exlimittext.md) .</span><span class="sxs-lookup"><span data-stu-id="2f838-129">However, a rich edit control will never contain more than 32K characters of text, unless you extend this limit by using the [**EM\_LIMITTEXT**](em-limittext.md) or [**EM\_EXLIMITTEXT**](em-exlimittext.md) message.</span></span> <span data-ttu-id="2f838-130">Para seleções que se estendem além do primeiro 64 KB de texto, a mensagem em **\_ GETSEL** retorna – 1.</span><span class="sxs-lookup"><span data-stu-id="2f838-130">For selections that extend beyond the first 64 KB of text, the **EM\_GETSEL** message returns –1.</span></span> <span data-ttu-id="2f838-131">Nesse caso, você ainda pode usar os valores retornados em *wParam* e *lParam* para localizar os caracteres inicial e final da seleção.</span><span class="sxs-lookup"><span data-stu-id="2f838-131">In such a case you can still use the values that are returned in *wParam* and *lParam* to find the start and end characters of the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f838-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f838-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f838-133">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="2f838-133">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="2f838-134">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="2f838-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





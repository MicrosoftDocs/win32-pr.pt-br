---
title: Como usar operações de Rich Text de edição
description: Um aplicativo pode enviar mensagens para recuperar ou localizar texto em um controle de edição rico. Você pode recuperar o texto selecionado ou um intervalo de texto especificado.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917725"
---
# <a name="how-to-use-rich-edit-text-operations"></a><span data-ttu-id="ab499-104">Como usar operações de Rich Text de edição</span><span class="sxs-lookup"><span data-stu-id="ab499-104">How to Use Rich Edit Text Operations</span></span>

<span data-ttu-id="ab499-105">Um aplicativo pode enviar mensagens para recuperar ou localizar texto em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="ab499-105">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="ab499-106">Você pode recuperar o texto selecionado ou um intervalo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="ab499-106">You can retrieve either the selected text or a specified range of text.</span></span>

<span data-ttu-id="ab499-107">Para obter o texto selecionado em um controle de edição rico, use a mensagem em [**\_ GETSELTEXT**](em-getseltext.md) .</span><span class="sxs-lookup"><span data-stu-id="ab499-107">To get the selected text in a rich edit control, use the [**EM\_GETSELTEXT**](em-getseltext.md) message.</span></span> <span data-ttu-id="ab499-108">O texto é copiado para a matriz de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="ab499-108">The text is copied to the specified character array.</span></span> <span data-ttu-id="ab499-109">Você deve garantir que a matriz seja grande o suficiente para manter o texto selecionado mais um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="ab499-109">You must ensure that the array is large enough to hold the selected text plus a terminating null character.</span></span>

<span data-ttu-id="ab499-110">Para recuperar um intervalo de texto especificado, use a mensagem em [**\_ GetTextRange**](em-gettextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="ab499-110">To retrieve a specified range of text, use the [**EM\_GETTEXTRANGE**](em-gettextrange.md) message.</span></span> <span data-ttu-id="ab499-111">A estrutura [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) usada com essa mensagem Especifica o intervalo de texto a ser recuperado e aponta para uma matriz de caracteres que recebe o texto.</span><span class="sxs-lookup"><span data-stu-id="ab499-111">The [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure used with this message specifies the text range to retrieve and points to a character array that receives the text.</span></span> <span data-ttu-id="ab499-112">Novamente, o aplicativo deve garantir que a matriz seja grande o suficiente para o texto especificado, além de um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="ab499-112">Here again, the application must ensure that the array is large enough for the specified text plus a terminating null character.</span></span>

<span data-ttu-id="ab499-113">Você pode pesquisar uma cadeia de caracteres em um controle de edição rico usando as mensagens em [**\_ FINDTEXTEX**](em-findtextex.md) [**\_ LocalizarTexto**](em-findtext.md) ou em, ou seus equivalentes Unicode, em [**\_ FINDTEXTW**](em-findtextw.md) e em [**\_ FINDTEXTEXW**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="ab499-113">You can search for a string in a rich edit control by using the [**EM\_FINDTEXT**](em-findtext.md) or [**EM\_FINDTEXTEX**](em-findtextex.md) messages, or their Unicode equivalents, [**EM\_FINDTEXTW**](em-findtextw.md) and [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span> <span data-ttu-id="ab499-114">A estrutura [**LocalizarTexto**](/windows/win32/api/richedit/ns-richedit-findtexta) usada com as versões não estendidas especifica o intervalo de texto a ser pesquisado e a cadeia de caracteres a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="ab499-114">The [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure that is used with the nonextended versions specifies the text range to search and the string to search for.</span></span> <span data-ttu-id="ab499-115">As versões estendidas usam uma estrutura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , que especifica as mesmas informações e também recebe os pontos inicial e final do intervalo de caracteres do texto encontrado.</span><span class="sxs-lookup"><span data-stu-id="ab499-115">The extended versions use a [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, which specifies the same information and also receives the start and end points of the character range of the found text.</span></span> <span data-ttu-id="ab499-116">Você também pode especificar essas opções como se a pesquisa diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ab499-116">You can also specify such options as whether the search is case sensitive.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ab499-117">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="ab499-117">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ab499-118">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="ab499-118">Technologies</span></span>

-   [<span data-ttu-id="ab499-119">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="ab499-119">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ab499-120">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ab499-120">Prerequisites</span></span>

-   <span data-ttu-id="ab499-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="ab499-121">C/C++</span></span>
-   <span data-ttu-id="ab499-122">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="ab499-122">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ab499-123">Instruções</span><span class="sxs-lookup"><span data-stu-id="ab499-123">Instructions</span></span>

### <a name="use-a-rich-edit-text-operation"></a><span data-ttu-id="ab499-124">Usar uma operação Rich Text de edição</span><span class="sxs-lookup"><span data-stu-id="ab499-124">Use a Rich Edit Text Operation</span></span>

<span data-ttu-id="ab499-125">A função de exemplo a seguir localiza o texto especificado dentro do texto selecionado em um controle de edição rico que dá suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="ab499-125">The following example function finds the specified text within the selected text in a rich edit control that supports Unicode.</span></span> <span data-ttu-id="ab499-126">Se o destino for encontrado, ele se tornará a nova seleção.</span><span class="sxs-lookup"><span data-stu-id="ab499-126">If the target is found, it becomes the new selection.</span></span>


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a><span data-ttu-id="ab499-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab499-127">Remarks</span></span>

<span data-ttu-id="ab499-128">O Microsoft Rich Edit 3,0 também dá suporte à função IME (editor de método de entrada) HexToUnicode, que permite que um usuário converta entre hexadecimal e Unicode usando teclas de acesso.</span><span class="sxs-lookup"><span data-stu-id="ab499-128">Microsoft Rich Edit 3.0 also supports the HexToUnicode Input Method Editor (IME) function, which allows a user to convert between hexadecimal and Unicode by using hot keys.</span></span> <span data-ttu-id="ab499-129">Para obter mais informações, consulte [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime).</span><span class="sxs-lookup"><span data-stu-id="ab499-129">For more information, see [HexToUnicode IME](/windows/desktop/Intl/hextounicode-ime).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab499-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab499-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab499-131">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="ab499-131">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="ab499-132">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="ab499-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 
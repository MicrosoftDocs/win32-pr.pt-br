---
title: Como rotular botões da barra de ferramentas dinamicamente
description: Você pode atribuir texto a um botão existente usando a mensagem TB \_ SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104453892"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a><span data-ttu-id="aa7fc-103">Como rotular botões da barra de ferramentas dinamicamente</span><span class="sxs-lookup"><span data-stu-id="aa7fc-103">How to Dynamically Label Toolbar Buttons</span></span>

<span data-ttu-id="aa7fc-104">Você pode atribuir texto a um botão existente usando a mensagem [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="aa7fc-104">You can assign text to an existing button by using the [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="aa7fc-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="aa7fc-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="aa7fc-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="aa7fc-106">Technologies</span></span>

-   [<span data-ttu-id="aa7fc-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="aa7fc-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="aa7fc-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="aa7fc-108">Prerequisites</span></span>

-   <span data-ttu-id="aa7fc-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="aa7fc-109">C/C++</span></span>
-   <span data-ttu-id="aa7fc-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="aa7fc-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="aa7fc-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="aa7fc-111">Instructions</span></span>

### <a name="dynamically-label-a-toolbar-button"></a><span data-ttu-id="aa7fc-112">Rotular dinamicamente um botão da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="aa7fc-112">Dynamically Label a Toolbar Button</span></span>

<span data-ttu-id="aa7fc-113">O exemplo a seguir demonstra como alterar o texto do terceiro botão nos exemplos anteriores de **salvar** para **salvar como**.</span><span class="sxs-lookup"><span data-stu-id="aa7fc-113">The following example demonstrates how to change the text of the third button in the previous examples from **Save** to **Save As**.</span></span>


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a><span data-ttu-id="aa7fc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa7fc-114">Remarks</span></span>

<span data-ttu-id="aa7fc-115">Alterar o texto de um botão usando [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) não afeta a cadeia de caracteres atribuída a esse botão na lista de cadeias de caracteres internas.</span><span class="sxs-lookup"><span data-stu-id="aa7fc-115">Changing a button's text by using [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) does not affect the string that is assigned to that button in the internal string list.</span></span>

<span data-ttu-id="aa7fc-116">Se você adicionar uma cadeia de caracteres de botão da barra de ferramentas à lista de texto interna, não será possível recuperar o índice dessa cadeia de caracteres chamando [tbn \_ GETBUTTONINFO](tbn-getbuttoninfo.md)— você deve usar a mensagem de [**\_ SetButton de TB**](tb-getbutton.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="aa7fc-116">If you add a toolbar button string to the internal text list, you cannot retrieve the index of that string by calling [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md)—you must use the [**TB\_GETBUTTON**](tb-getbutton.md) message instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa7fc-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa7fc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa7fc-118">Usando controles da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="aa7fc-118">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="aa7fc-119">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="aa7fc-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





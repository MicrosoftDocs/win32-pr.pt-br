---
title: Como criar controles de edição avançados
description: Para criar um controle de edição rico, chame a função CreateWindowEx, especificando a classe da janela de edição rica.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008416"
---
# <a name="how-to-create-rich-edit-controls"></a><span data-ttu-id="c87f6-103">Como criar controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="c87f6-103">How to Create Rich Edit Controls</span></span>

<span data-ttu-id="c87f6-104">Para criar um controle de edição rico, chame a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe da janela de edição rica.</span><span class="sxs-lookup"><span data-stu-id="c87f6-104">To create a rich edit control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the rich edit window class.</span></span> <span data-ttu-id="c87f6-105">Para o Microsoft rich edit 4,1 (Msftedit.dll), especifique \_ a classe MSFTEDIT como a classe de janela.</span><span class="sxs-lookup"><span data-stu-id="c87f6-105">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT\_CLASS as the window class.</span></span> <span data-ttu-id="c87f6-106">Para todas as versões anteriores, especifique a \_ classe RichEdit.</span><span class="sxs-lookup"><span data-stu-id="c87f6-106">For all previous versions, specify RICHEDIT\_CLASS.</span></span> <span data-ttu-id="c87f6-107">Para obter mais informações, consulte [versões do rich edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c87f6-107">For more information, see [Versions of Rich Edit](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="c87f6-108">Os controles de edição avançados dão suporte à maioria dos estilos de janela usados com controles de edição, bem como estilos adicionais.</span><span class="sxs-lookup"><span data-stu-id="c87f6-108">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="c87f6-109">Você deve especificar o estilo de janela [**\_ multilinha es**](edit-control-styles.md) se desejar permitir mais de uma linha de texto no controle.</span><span class="sxs-lookup"><span data-stu-id="c87f6-109">You should specify the [**ES\_MULTILINE**](edit-control-styles.md) window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="c87f6-110">Para obter mais informações, consulte [Rich Edit Control Styles](rich-edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="c87f6-110">For more information, see [Rich Edit Control Styles](rich-edit-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c87f6-111">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="c87f6-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c87f6-112">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="c87f6-112">Technologies</span></span>

-   [<span data-ttu-id="c87f6-113">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="c87f6-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c87f6-114">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c87f6-114">Prerequisites</span></span>

-   <span data-ttu-id="c87f6-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="c87f6-115">C/C++</span></span>
-   <span data-ttu-id="c87f6-116">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="c87f6-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c87f6-117">Instruções</span><span class="sxs-lookup"><span data-stu-id="c87f6-117">Instructions</span></span>

### <a name="create-a-rich-edit-control"></a><span data-ttu-id="c87f6-118">Criar um controle de edição rico</span><span class="sxs-lookup"><span data-stu-id="c87f6-118">Create a Rich Edit Control</span></span>

<span data-ttu-id="c87f6-119">A função de exemplo a seguir cria um controle de edição rico e o inicializa com algum texto.</span><span class="sxs-lookup"><span data-stu-id="c87f6-119">The following example function creates a rich edit control and initializes it with some text.</span></span>


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



<span data-ttu-id="c87f6-120">No Microsoft Visual Studio 2005 e posterior, é possível adicionar um controle de edição rico em um modelo de caixa de diálogo arrastando o controle da caixa de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="c87f6-120">In Microsoft Visual Studio 2005 and later, it is possible to add a rich edit control into a dialog template by dragging the control from the toolbox.</span></span> <span data-ttu-id="c87f6-121">No entanto, fazer isso no editor de caixa de diálogo não garante que a biblioteca necessária será carregada antes de o controle ser criado.</span><span class="sxs-lookup"><span data-stu-id="c87f6-121">However, doing this in the dialog editor does not ensure that the required library will be loaded before the control is created.</span></span> <span data-ttu-id="c87f6-122">É necessário chamar a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar Riched32.dll, Riched20.dll ou Msftedit.dll antes de a caixa de diálogo ser criada.</span><span class="sxs-lookup"><span data-stu-id="c87f6-122">It is necessary to call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Riched32.dll, Riched20.dll, or Msftedit.dll before the dialog is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="c87f6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c87f6-123">Remarks</span></span>

<span data-ttu-id="c87f6-124">Para usar estilos visuais com esses controles, um aplicativo deve incluir um manifesto e deve chamar a função [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) no início do programa.</span><span class="sxs-lookup"><span data-stu-id="c87f6-124">To use visual styles with these controls, an application must include a manifest and must call the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function at the beginning of the program.</span></span> <span data-ttu-id="c87f6-125">Para obter informações sobre estilos visuais, consulte [estilos visuais](themes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c87f6-125">For information on visual styles, see [Visual Styles](themes-overview.md).</span></span> <span data-ttu-id="c87f6-126">Para obter informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c87f6-126">For information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c87f6-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c87f6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c87f6-128">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="c87f6-128">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="c87f6-129">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="c87f6-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 
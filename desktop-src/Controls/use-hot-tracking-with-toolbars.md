---
title: Como usar Hot-Tracking com barras de ferramentas
description: Quando um ponteiro do mouse passa sobre um item, o item fica quente. Se o acompanhamento de quente estiver habilitado, o item ativo será realçado. Uma barra de ferramentas criada com o \_ estilo simples TBSTYLE, ou uma que usa estilos visuais, dá suporte ao acompanhamento de acesso por padrão.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104007266"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a><span data-ttu-id="724e1-105">Como usar Hot-Tracking com barras de ferramentas</span><span class="sxs-lookup"><span data-stu-id="724e1-105">How to Use Hot-Tracking with Toolbars</span></span>

<span data-ttu-id="724e1-106">Quando um ponteiro do mouse passa sobre um item, o item fica quente.</span><span class="sxs-lookup"><span data-stu-id="724e1-106">When a mouse pointer hovers over an item, the item becomes hot.</span></span> <span data-ttu-id="724e1-107">Se o acompanhamento de quente estiver habilitado, o item ativo será realçado.</span><span class="sxs-lookup"><span data-stu-id="724e1-107">If hot-tracking is enabled, the hot item is highlighted.</span></span> <span data-ttu-id="724e1-108">Uma barra de ferramentas criada com o [**estilo \_ simples TBSTYLE**](toolbar-control-and-button-styles.md) , ou uma que usa [estilos visuais](themes-overview.md), dá suporte ao acompanhamento de acesso por padrão.</span><span class="sxs-lookup"><span data-stu-id="724e1-108">A toolbar that is created with the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style, or one that uses [Visual Styles](themes-overview.md), supports hot-tracking by default.</span></span>

<span data-ttu-id="724e1-109">O acompanhamento dinâmico exige que você crie listas de imagens; Portanto, você não pode usar a mensagem de [**TB \_ AddBitmap**](tb-addbitmap.md) ou a função [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) para criar sua barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="724e1-109">Hot-tracking requires that you create image lists; therefore, you cannot use the [**TB\_ADDBITMAP**](tb-addbitmap.md) message or the [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function to create your toolbar.</span></span>

<span data-ttu-id="724e1-110">Quando o mouse passa sobre um botão da barra de ferramentas, o botão é destacado para realçá-lo.</span><span class="sxs-lookup"><span data-stu-id="724e1-110">When the mouse hovers over a toolbar button, the button is outlined to highlight it.</span></span> <span data-ttu-id="724e1-111">A ilustração a seguir mostra uma barra de ferramentas com o controle de acesso habilitado; o ponteiro do mouse estava focalizando o botão salvar quando a captura de tela foi tomada.</span><span class="sxs-lookup"><span data-stu-id="724e1-111">The following illustration shows a toolbar with hot-tracking enabled; the mouse pointer was hovering on the Save button when the screen shot was taken.</span></span>

![captura de tela de uma caixa de diálogo com uma barra de ferramentas de três itens; o ícone selecionado é descrito](images/tb-withstyles.png)

<span data-ttu-id="724e1-113">Se você quiser que um bitmap de botão da barra de ferramentas seja alterado quando o estado do controle for alterado, armazene as diferentes imagens em [listas de imagens](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="724e1-113">If you want a toolbar button bitmap to change when the state of the control changes, store the different images in [image lists](image-lists.md).</span></span> <span data-ttu-id="724e1-114">Por exemplo, alguns aplicativos têm botões de barra de ferramentas pretos e brancos que se tornam coloridos quando são selecionados.</span><span class="sxs-lookup"><span data-stu-id="724e1-114">For example, some applications have black and white toolbar buttons that become colored when they are selected.</span></span> <span data-ttu-id="724e1-115">As duas imagens diferentes são armazenadas em listas de imagens.</span><span class="sxs-lookup"><span data-stu-id="724e1-115">The two different images are stored in image lists.</span></span> <span data-ttu-id="724e1-116">As barras de ferramentas dão suporte ao uso de até três listas de imagens.</span><span class="sxs-lookup"><span data-stu-id="724e1-116">Toolbars support using up to three image lists.</span></span> <span data-ttu-id="724e1-117">Normalmente, um aplicativo tem uma lista de imagens padrão, desabilitada e de rastreamento dinâmico.</span><span class="sxs-lookup"><span data-stu-id="724e1-117">Typically an application has a default, disabled, and hot-tracking list of images.</span></span> <span data-ttu-id="724e1-118">Para definir e recuperar listas de imagens para botões da barra de ferramentas quente, use as mensagens [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) e [**TB \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="724e1-118">To set and retrieve image lists for hot toolbar buttons, use the [**TB\_SETHOTIMAGELIST**](tb-sethotimagelist.md) and [**TB\_GETHOTIMAGELIST**](tb-gethotimagelist.md) messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="724e1-119">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="724e1-119">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="724e1-120">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="724e1-120">Technologies</span></span>

-   [<span data-ttu-id="724e1-121">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="724e1-121">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="724e1-122">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="724e1-122">Prerequisites</span></span>

-   <span data-ttu-id="724e1-123">C/C++</span><span class="sxs-lookup"><span data-stu-id="724e1-123">C/C++</span></span>
-   <span data-ttu-id="724e1-124">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="724e1-124">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="724e1-125">Instruções</span><span class="sxs-lookup"><span data-stu-id="724e1-125">Instructions</span></span>

### <a name="use-hot-tracking-with-a-toolbar"></a><span data-ttu-id="724e1-126">Usar Hot-Tracking com uma barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="724e1-126">Use Hot-Tracking with a Toolbar</span></span>

<span data-ttu-id="724e1-127">O exemplo de código a seguir cria, preenche e atribui uma lista de imagens para botões quentes.</span><span class="sxs-lookup"><span data-stu-id="724e1-127">The following code example creates, fills, and assigns an image list for hot buttons.</span></span>


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a><span data-ttu-id="724e1-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="724e1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="724e1-129">Usando controles da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="724e1-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="724e1-130">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="724e1-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





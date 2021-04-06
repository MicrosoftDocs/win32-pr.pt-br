---
title: Como criar uma lista de imagens
description: Este tópico demonstra como usar a função ImageList \_ Create para criar uma lista de imagens.
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c81ff3a46138c210474a1b00ddd2ba647d1368
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917804"
---
# <a name="how-to-create-an-image-list"></a><span data-ttu-id="0a5da-103">Como criar uma lista de imagens</span><span class="sxs-lookup"><span data-stu-id="0a5da-103">How to Create an Image List</span></span>

<span data-ttu-id="0a5da-104">Este tópico demonstra como usar a função [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) para criar uma lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="0a5da-104">This topic demonstrates how to use the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function to create an image list.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0a5da-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="0a5da-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0a5da-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="0a5da-106">Technologies</span></span>

-   [<span data-ttu-id="0a5da-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="0a5da-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0a5da-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="0a5da-108">Prerequisites</span></span>

-   <span data-ttu-id="0a5da-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="0a5da-109">C/C++</span></span>
-   <span data-ttu-id="0a5da-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="0a5da-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0a5da-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="0a5da-111">Instructions</span></span>


<span data-ttu-id="0a5da-112">Você cria uma lista de imagens chamando a função [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) .</span><span class="sxs-lookup"><span data-stu-id="0a5da-112">You create an image list by calling the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function.</span></span> <span data-ttu-id="0a5da-113">Os parâmetros incluem o tipo de lista de imagens a ser criado, as dimensões de cada imagem e o número de imagens que você pretende adicionar à lista.</span><span class="sxs-lookup"><span data-stu-id="0a5da-113">The parameters include the type of image list to create, the dimensions of each image, and the number of images that you intend to add to the list.</span></span>

<span data-ttu-id="0a5da-114">O exemplo a seguir cria uma lista de imagens mascaradas e usa a macro de [**\_ ícone**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) de exemplos ImageList para adicionar dois ícones à lista.</span><span class="sxs-lookup"><span data-stu-id="0a5da-114">The following example creates a masked image list and uses the [**ImageList\_AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) macro to add two icons to the list.</span></span>



```C++
// AddIconsToImageList - creates a masked image list and adds some 
// icons to it. 
// Returns the handle to the new image list. 
// hinst - handle to the application instance. 
// 
// Global variables and constants 
//     g_nBird and g_nTree - indexes of the images. 
//     cx_icon and cy_icon - width and height of the icon. 
//     num_icons - number of icons to add to the image list. 
extern int g_nBird, g_nTree; 
 
#define CX_ICON  32 
#define CY_ICON  32 
#define NUM_ICONS 3 
 
HIMAGELIST AddIconsToImageList(HINSTANCE hinst) 
{ 
    HIMAGELIST himlIcons;  // handle to new image list 
    HICON hicon;           // handle to icon 
 
    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Create a masked image list large enough to hold the icons. 
    himlIcons = ImageList_Create(CX_ICON, CY_ICON, ILC_MASK, NUM_ICONS, 0); 
 
    // Load the icon resources, and add the icons to the image list. 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_BIRD)); 
    g_nBird = ImageList_AddIcon(himlIcons, hicon); 
 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_TREE)); 
    g_nTree = ImageList_AddIcon(himlIcons, hicon); 
 
    return himlIcons; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="0a5da-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a5da-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a5da-116">Referência de listas de imagens</span><span class="sxs-lookup"><span data-stu-id="0a5da-116">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="0a5da-117">Sobre as listas de imagens</span><span class="sxs-lookup"><span data-stu-id="0a5da-117">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="0a5da-118">Usando listas de imagens</span><span class="sxs-lookup"><span data-stu-id="0a5da-118">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 





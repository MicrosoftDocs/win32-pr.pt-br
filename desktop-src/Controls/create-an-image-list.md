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
# <a name="how-to-create-an-image-list"></a>Como criar uma lista de imagens

Este tópico demonstra como usar a função [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) para criar uma lista de imagens.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Você cria uma lista de imagens chamando a função [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) . Os parâmetros incluem o tipo de lista de imagens a ser criado, as dimensões de cada imagem e o número de imagens que você pretende adicionar à lista.

O exemplo a seguir cria uma lista de imagens mascaradas e usa a macro de [**\_ ícone**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) de exemplos ImageList para adicionar dois ícones à lista.



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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de listas de imagens](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Sobre as listas de imagens](image-lists.md)
</dt> <dt>

[Usando listas de imagens](using-image-lists.md)
</dt> </dl>

 

 





---
description: Há sete pincéis de ações lógicas predefinidos mantidos pela interface gráfica do dispositivo (GDI). Também há 21 pincéis de estoque lógicos predefinidos mantidos pela interface de gerenciamento do Windows (usuário).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Pincel de ações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968144"
---
# <a name="stock-brush"></a><span data-ttu-id="1b182-104">Pincel de ações</span><span class="sxs-lookup"><span data-stu-id="1b182-104">Stock Brush</span></span>

<span data-ttu-id="1b182-105">Há sete pincéis de ações lógicas predefinidos mantidos pela interface gráfica do dispositivo (GDI).</span><span class="sxs-lookup"><span data-stu-id="1b182-105">There are seven predefined logical stock brushes maintained by the graphics device interface (GDI).</span></span> <span data-ttu-id="1b182-106">Também há 21 pincéis de estoque lógicos predefinidos mantidos pela interface de gerenciamento do Windows (usuário).</span><span class="sxs-lookup"><span data-stu-id="1b182-106">There are also 21 predefined logical stock brushes maintained by the window management interface (USER).</span></span>

<span data-ttu-id="1b182-107">A ilustração a seguir mostra retângulos pintados usando os sete pincéis de ações predefinidos.</span><span class="sxs-lookup"><span data-stu-id="1b182-107">The following illustration shows rectangles painted by using the seven predefined stock brushes.</span></span>

![ilustração mostrando sete caixas: uma preta, três tons de cinza e três que aparecem vazias](images/csbru-03.png)

<span data-ttu-id="1b182-109">Um aplicativo pode recuperar um identificador que identifica um dos sete pincéis de ações chamando a função [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) , especificando o tipo de pincel.</span><span class="sxs-lookup"><span data-stu-id="1b182-109">An application can retrieve a handle identifying one of the seven stock brushes by calling the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function, specifying the brush type.</span></span>

<span data-ttu-id="1b182-110">Os 21 pincéis de estoque mantidos pela interface de gerenciamento do Windows correspondem às cores dos elementos da janela, como menus, barras de rolagem e botões.</span><span class="sxs-lookup"><span data-stu-id="1b182-110">The 21 stock brushes maintained by the window management interface correspond to the colors of window elements such as menus, scroll bars, and buttons.</span></span> <span data-ttu-id="1b182-111">Um aplicativo pode obter um identificador que identifica um desses pincéis chamando a função [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) e especificando um valor de cor do sistema.</span><span class="sxs-lookup"><span data-stu-id="1b182-111">An application can obtain a handle identifying one of these brushes by calling the [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) function and specifying a system-color value.</span></span> <span data-ttu-id="1b182-112">Um aplicativo pode recuperar a cor correspondente a um determinado elemento de janela chamando a função [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) .</span><span class="sxs-lookup"><span data-stu-id="1b182-112">An application can retrieve the color corresponding to a particular window element by calling the [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) function.</span></span> <span data-ttu-id="1b182-113">Um aplicativo pode definir a cor correspondente a um elemento de janela chamando a função [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="1b182-113">An application can set the color corresponding to a window element by calling the [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) function.</span></span>

 

 

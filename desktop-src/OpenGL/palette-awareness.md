---
title: Reconhecimento de paleta
description: Seu aplicativo deve responder às mensagens do WM \_ paletachanged, do WM \_ QUERYNEWPALETTE e \_ do WM para que você esteja atento e use paletas. Projete seu aplicativo para selecionar e perceber as paletas em resposta a essas mensagens.
ms.assetid: 0670e929-dfdb-44d2-bda2-c532d1739d8e
keywords:
- OpenGL no Windows, reconhecimento de paleta
- reconhecimento de paleta OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ceab4c27f63c12977d072f84e789d1800b6557
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823958"
---
# <a name="palette-awareness"></a><span data-ttu-id="b46dc-106">Reconhecimento de paleta</span><span class="sxs-lookup"><span data-stu-id="b46dc-106">Palette Awareness</span></span>

<span data-ttu-id="b46dc-107">Seu aplicativo deve responder às mensagens do [WM \_ paletachanged](/windows/desktop/gdi/wm-palettechanged), do [WM \_ QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette)e do [WM \_ ](../inputdev/wm-activate.md) para que você esteja atento e use paletas.</span><span class="sxs-lookup"><span data-stu-id="b46dc-107">Your application must respond to the [WM\_PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged), [WM\_QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette), and [WM\_ACTIVATE](../inputdev/wm-activate.md) messages to be aware of and use palettes.</span></span> <span data-ttu-id="b46dc-108">Projete seu aplicativo para selecionar e perceber as paletas em resposta a essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="b46dc-108">Design your application to select and realize palettes in response to these messages.</span></span>

<span data-ttu-id="b46dc-109">Para obter mais informações sobre paletas e conscientização da paleta, consulte os artigos "reconhecimento da paleta" e "Gerenciador de paleta: como e por que" nos CDs da biblioteca de desenvolvimento do Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="b46dc-109">For more information on palettes and palette awareness, see the articles "Palette Awareness," and "The Palette Manager: How and Why" on the Microsoft Developer Network Development Library compact discs.</span></span>

 

 
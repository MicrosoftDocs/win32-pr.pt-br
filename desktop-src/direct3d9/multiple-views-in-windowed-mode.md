---
description: 'Além da cadeia de permuta que é proprietária e manipulada por meio do objeto Direct3DDevice, um aplicativo pode usar o método IDirect3DDevice9:: CreateAdditionalSwapChain para criar cadeias de permuta adicionais para apresentar várias exibições do mesmo dispositivo.'
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Várias exibições no modo de janela (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105802066"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="7f2a5-103">Várias exibições no modo de janela (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7f2a5-103">Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="7f2a5-104">Além da cadeia de permuta que é proprietária e manipulada por meio do objeto Direct3DDevice, um aplicativo pode usar o método [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) para criar cadeias de permuta adicionais para apresentar várias exibições do mesmo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f2a5-104">In addition to the swap chain that is owned and manipulated through the Direct3DDevice object, an application can use the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method to create additional swap chains to present multiple views from the same device.</span></span>

<span data-ttu-id="7f2a5-105">Normalmente, o aplicativo cria uma cadeia de permuta por exibição e associa cada cadeia de troca a uma determinada exibição.</span><span class="sxs-lookup"><span data-stu-id="7f2a5-105">Typically, the application creates one swap chain per view, and it associates each swap chain with a particular view.</span></span> <span data-ttu-id="7f2a5-106">O aplicativo renderiza as imagens nos buffers de fundo de cada cadeia de permuta e, em seguida, usa o método [**IDirect3DDevice9::P Resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para apresentá-las individualmente.</span><span class="sxs-lookup"><span data-stu-id="7f2a5-106">The application renders images in the back buffers of each swap chain, and then uses the [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method to present them individually.</span></span> <span data-ttu-id="7f2a5-107">Observe que apenas uma cadeia de permuta por vez pode ser de tela inteira em cada adaptador.</span><span class="sxs-lookup"><span data-stu-id="7f2a5-107">Note that only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f2a5-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f2a5-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f2a5-109">Apresentando uma cena</span><span class="sxs-lookup"><span data-stu-id="7f2a5-109">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 

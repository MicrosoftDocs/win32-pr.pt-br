---
description: Muitos aplicativos C++ limpam o buffer de profundidade antes de renderizar cada novo quadro.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Limpando buffers de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ad415b5c92e62da4f64eb590a0e202ffa3e0c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793635"
---
# <a name="clearing-depth-buffers-direct3d-9"></a><span data-ttu-id="96431-103">Limpando buffers de profundidade (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="96431-103">Clearing Depth Buffers (Direct3D 9)</span></span>

<span data-ttu-id="96431-104">Muitos aplicativos C++ limpam o buffer de profundidade antes de renderizar cada novo quadro.</span><span class="sxs-lookup"><span data-stu-id="96431-104">Many C++ applications clear the depth buffer before rendering each new frame.</span></span> <span data-ttu-id="96431-105">Você pode limpar explicitamente o buffer de profundidade por meio do Direct3D chamando [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) e especificando D3DCLEAR \_ ZBUFFER para o parâmetro flags.</span><span class="sxs-lookup"><span data-stu-id="96431-105">You can explicitly clear the depth buffer through Direct3D by calling [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) and specifying D3DCLEAR\_ZBUFFER for the Flags parameter.</span></span> <span data-ttu-id="96431-106">O método **IDirect3DDevice9:: Clear** permite que você especifique um valor de profundidade arbitrária no parâmetro Z.</span><span class="sxs-lookup"><span data-stu-id="96431-106">The **IDirect3DDevice9::Clear** method allows you to specify an arbitrary depth value in the Z parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96431-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96431-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96431-108">Buffers de profundidade</span><span class="sxs-lookup"><span data-stu-id="96431-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 

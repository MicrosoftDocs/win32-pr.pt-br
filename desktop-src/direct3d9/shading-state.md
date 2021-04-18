---
description: O Direct3D dá suporte a sombreamento simples e Gouraud. O padrão é sombreamento Gouraud. Para controlar o modo de sombreamento atual, seu aplicativo C++ especifica um membro do tipo enumerado D3DSHADEMODE para o \_ estado de RENDERIZAÇÃO D3DRS shadmode.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Estado de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105802065"
---
# <a name="shading-state-direct3d-9"></a><span data-ttu-id="e54c0-105">Estado de sombreamento (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e54c0-105">Shading State (Direct3D 9)</span></span>

<span data-ttu-id="e54c0-106">O Direct3D dá suporte a sombreamento simples e Gouraud.</span><span class="sxs-lookup"><span data-stu-id="e54c0-106">Direct3D supports both flat and Gouraud shading.</span></span> <span data-ttu-id="e54c0-107">O padrão é sombreamento Gouraud.</span><span class="sxs-lookup"><span data-stu-id="e54c0-107">The default is Gouraud shading.</span></span> <span data-ttu-id="e54c0-108">Para controlar o modo de sombreamento atual, seu aplicativo C++ especifica um membro do tipo enumerado [**D3DSHADEMODE**](./d3dshademode.md) para o \_ estado de renderização D3DRS shadmode.</span><span class="sxs-lookup"><span data-stu-id="e54c0-108">To control the current shading mode, your C++ application specifies a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type for the D3DRS\_SHADEMODE render state.</span></span>

<span data-ttu-id="e54c0-109">O exemplo de código C++ a seguir demonstra o processo de definir o estado de sombreamento para o modo de sombreamento simples.</span><span class="sxs-lookup"><span data-stu-id="e54c0-109">The following C++ code example demonstrates the process of setting the shading state to flat shading mode.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a><span data-ttu-id="e54c0-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e54c0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e54c0-111">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="e54c0-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 

---
description: A cor de neblina para sombra de pixel e Vertex é definida por meio do \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR. Os valores do estado de renderização podem ser qualquer cor RGB, especificada como uma cor RGBA. O componente alfa é ignorado.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Cor da neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009873"
---
# <a name="fog-color-direct3d-9"></a><span data-ttu-id="155a1-105">Cor da neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="155a1-105">Fog Color (Direct3D 9)</span></span>

<span data-ttu-id="155a1-106">A cor de neblina para sombra de pixel e Vertex é definida por meio do \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="155a1-106">Fog color for both pixel and vertex fog is set through the D3DRS\_FOGCOLOR render state.</span></span> <span data-ttu-id="155a1-107">Os valores do estado de renderização podem ser qualquer cor RGB, especificada como uma cor RGBA.</span><span class="sxs-lookup"><span data-stu-id="155a1-107">The render state values can be any RGB color, specified as an RGBA color.</span></span> <span data-ttu-id="155a1-108">O componente alfa é ignorado.</span><span class="sxs-lookup"><span data-stu-id="155a1-108">The alpha component is ignored.</span></span>

<span data-ttu-id="155a1-109">O exemplo de C++ a seguir define a cor de neblina como branco.</span><span class="sxs-lookup"><span data-stu-id="155a1-109">The following C++ example sets the fog color to white.</span></span>


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



<span data-ttu-id="155a1-110">A neblina é aplicada de forma diferente pelo pipeline de função fixa e pelo pipeline programável.</span><span class="sxs-lookup"><span data-stu-id="155a1-110">Fog is applied differently by the fixed function pipeline and the programmable pipeline.</span></span>

1.  <span data-ttu-id="155a1-111">Se o driver oferecer suporte a D3DPMISCCAPS \_ FOGANDSPECULARALPHA:</span><span class="sxs-lookup"><span data-stu-id="155a1-111">If the driver supports D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="155a1-112">Se o pipeline de função fixa for usado e D3DRS \_ FOGCOLOR for definido, v1. w (no sombreador de pixel) será igual ao valor definido em neblina RenderState.</span><span class="sxs-lookup"><span data-stu-id="155a1-112">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, v1.w (in the pixel shader) equals the value set in fog renderstate.</span></span>
    -   <span data-ttu-id="155a1-113">Se o pipeline programável for usado, v1. w (no sombreador de pixels) é igual a 0, mesmo que oD1. w seja explicitamente escrito em um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="155a1-113">If the programmable pipeline is used, then v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>
2.  <span data-ttu-id="155a1-114">Se o driver não oferecer suporte a D3DPMISCCAPS \_ FOGANDSPECULARALPHA:</span><span class="sxs-lookup"><span data-stu-id="155a1-114">If the driver does NOT support D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="155a1-115">Se o pipeline de função fixa for usado e D3DRS \_ FOGCOLOR for definido, então v1. w (no sombreador de pixel) é igual ao valor definido em neblina renderingstate.</span><span class="sxs-lookup"><span data-stu-id="155a1-115">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, then v1.w (in the pixel shader) equals value set in fog renderstate.</span></span>
    -   <span data-ttu-id="155a1-116">Se oFog for explicitamente gravado em um sombreador de vértice, v1. w (no sombreador de pixel) é igual a oFog, clamped entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="155a1-116">If oFog is explicitly written in a vertex shader, v1.w (in the pixel shader) equals oFog, clamped between 0 and 1.</span></span>
    -   <span data-ttu-id="155a1-117">Se nenhum dos dois casos acima se aplicar, v1. w (no sombreador de pixels) é igual a 0, mesmo se oD1. w for explicitamente escrito em um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="155a1-117">If neither of the above two cases applies, v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>

<span data-ttu-id="155a1-118">Para obter mais informações, consulte [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="155a1-118">For more information, see [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="155a1-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="155a1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="155a1-120">Tipos de neblina</span><span class="sxs-lookup"><span data-stu-id="155a1-120">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 




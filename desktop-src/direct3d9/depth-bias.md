---
description: Polígonos que são coplanar em seu espaço 3D podem ser feitos para aparecer como se não fossem coplanar adicionando um Bias z a cada um.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Tendência de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456585"
---
# <a name="depth-bias-direct3d-9"></a><span data-ttu-id="975f0-103">Tendência de profundidade (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="975f0-103">Depth Bias (Direct3D 9)</span></span>

<span data-ttu-id="975f0-104">Polígonos que são coplanar em seu espaço 3D podem ser feitos para aparecer como se não fossem coplanar adicionando um Bias z a cada um.</span><span class="sxs-lookup"><span data-stu-id="975f0-104">Polygons that are coplanar in your 3D space can be made to appear as if they are not coplanar by adding a z-bias to each one.</span></span> <span data-ttu-id="975f0-105">Essa é uma técnica comumente usada para garantir que as sombras em uma cena sejam exibidas corretamente.</span><span class="sxs-lookup"><span data-stu-id="975f0-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="975f0-106">Por exemplo, uma sombra em uma parede provavelmente terá o mesmo valor de profundidade que a parede.</span><span class="sxs-lookup"><span data-stu-id="975f0-106">For instance, a shadow on a wall will likely have the same depth value as the wall does.</span></span> <span data-ttu-id="975f0-107">Se você renderizar o mural primeiro e, em seguida, a sombra, a sombra pode não estar visível ou os artefatos de profundidade podem estar visíveis.</span><span class="sxs-lookup"><span data-stu-id="975f0-107">If you render the wall first and then the shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span> <span data-ttu-id="975f0-108">Você pode reverter a ordem na qual você renderiza os objetos Coplanar em espera de reversão do efeito, mas os artefatos de profundidade ainda são prováveis.</span><span class="sxs-lookup"><span data-stu-id="975f0-108">You can reverse the order in which you render the coplanar objects in hopes of reversing the effect, but depth artifacts are still likely.</span></span>

<span data-ttu-id="975f0-109">Um aplicativo pode ajudar a garantir que polígonos coplanar sejam renderizados corretamente adicionando uma tendência aos valores z que o sistema usa ao renderizar os conjuntos de polígonos coplanar.</span><span class="sxs-lookup"><span data-stu-id="975f0-109">An application can help ensure that coplanar polygons are rendered properly by adding a bias to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="975f0-110">Para adicionar um Bias z a um conjunto de polígonos, chame o método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) antes de processá-los, definindo o parâmetro *State* como D3DRS \_ DEPTHBIAS e o parâmetro *Value* para um valor float adequado (por exemplo, um valor adequado pode ser de-1,0 a 1,0); para passar esse valor para **setprocessstate**, você também deve converter o valor em um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="975f0-110">To add a z-bias to a set of polygons, call the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method just before rendering them, setting the *State* parameter to D3DRS\_DEPTHBIAS, and the *Value* parameter to a suitable float value (for example, a suitable value might be from -1.0 to 1.0); to pass this value to **SetRenderState**, you must also cast the value to a **DWORD**.</span></span> <span data-ttu-id="975f0-111">Um valor de tendência de z maior aumenta a probabilidade de que os polígonos processados sejam visíveis quando exibidos com outros polígonos coplanar.</span><span class="sxs-lookup"><span data-stu-id="975f0-111">A higher z-bias value increases the likelihood that the polygons you render will be visible when displayed with other coplanar polygons.</span></span>


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



<span data-ttu-id="975f0-112">onde m é a inclinação de profundidade máxima do triângulo que está sendo renderizado.</span><span class="sxs-lookup"><span data-stu-id="975f0-112">where m is the maximum depth slope of the triangle being rendered.</span></span>


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



<span data-ttu-id="975f0-113">As unidades dos Estados de \_ RENDERIZAÇÃO D3DRS DEPTHBIAS e D3DRS \_ SLOPESCALEDEPTHBIAS dependem de se o buffer z ou o w-buffer está habilitado.</span><span class="sxs-lookup"><span data-stu-id="975f0-113">The units for the D3DRS\_DEPTHBIAS and D3DRS\_SLOPESCALEDEPTHBIAS render states depend on whether z-buffering or w-buffering is enabled.</span></span> <span data-ttu-id="975f0-114">O aplicativo deve fornecer valores adequados.</span><span class="sxs-lookup"><span data-stu-id="975f0-114">The application must provide suitable values.</span></span>

<span data-ttu-id="975f0-115">A tendência não é aplicada a nenhum primitivo de linha e ponto.</span><span class="sxs-lookup"><span data-stu-id="975f0-115">The bias is not applied to any line and point primitive.</span></span> <span data-ttu-id="975f0-116">No entanto, essa tendência precisa ser aplicada a triângulos desenhados no modo de wireframe.</span><span class="sxs-lookup"><span data-stu-id="975f0-116">However, this bias needs to be applied to triangles drawn in wireframe mode.</span></span>


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a><span data-ttu-id="975f0-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="975f0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="975f0-118">Pipeline de pixel</span><span class="sxs-lookup"><span data-stu-id="975f0-118">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 

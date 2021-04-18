---
description: O buffer de profundidade é um método de remoção de linhas ocultas e superfícies. Por padrão, o Direct3D não usa o buffer de profundidade.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Estado de buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456583"
---
# <a name="depth-buffering-state-direct3d-9"></a><span data-ttu-id="faaa3-104">Estado de buffer de profundidade (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="faaa3-104">Depth Buffering State (Direct3D 9)</span></span>

<span data-ttu-id="faaa3-105">O buffer de profundidade é um método de remoção de linhas ocultas e superfícies.</span><span class="sxs-lookup"><span data-stu-id="faaa3-105">Depth buffering is a method of removing hidden lines and surfaces.</span></span> <span data-ttu-id="faaa3-106">Por padrão, o Direct3D não usa o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="faaa3-106">By default, Direct3D does not use depth buffering.</span></span>

<span data-ttu-id="faaa3-107">Para obter uma visão geral conceitual dos buffers de profundidade, consulte [buffers de profundidade (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="faaa3-107">For a conceptual overview of depth buffers, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="faaa3-108">Os aplicativos C++ atualizam o estado de buffer de profundidade com o \_ estado de RENDERIZAÇÃO D3DRS ZENABLE, usando um membro da enumeração [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) para especificar o novo valor de estado.</span><span class="sxs-lookup"><span data-stu-id="faaa3-108">C++ applications update the depth-buffering state with the D3DRS\_ZENABLE render state, using a member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumeration to specify the new state value.</span></span>

<span data-ttu-id="faaa3-109">Se seu aplicativo precisar impedir que o Direct3D grave no buffer de profundidade, ele poderá usar o \_ valor enumerado D3DRS ZWRITEENABLE, ESPECIFICANDO D3DZB \_ false como o segundo parâmetro para a chamada para [**IDirect3DDevice9:: setprocessstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="faaa3-109">If your application needs to prevent Direct3D from writing to the depth buffer, it can use the D3DRS\_ZWRITEENABLE enumerated value, specifying D3DZB\_FALSE as the second parameter for the call to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="faaa3-110">O exemplo de código a seguir mostra como o estado do buffer de profundidade é definido para habilitar o z-buffer.</span><span class="sxs-lookup"><span data-stu-id="faaa3-110">The following code example shows how the depth-buffer state is set to enable z-buffering.</span></span>


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



<span data-ttu-id="faaa3-111">Seu aplicativo também pode usar o \_ estado de RENDERIZAÇÃO D3DRS ZFUNC para controlar a função de comparação que o Direct3D usa ao executar o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="faaa3-111">Your application can also use the D3DRS\_ZFUNC render state to control the comparison function that Direct3D uses when performing depth buffering.</span></span>

<span data-ttu-id="faaa3-112">A tendência Z é um método de exibir uma superfície na frente de outra, mesmo que seus valores de profundidade sejam os mesmos.</span><span class="sxs-lookup"><span data-stu-id="faaa3-112">Z-biasing is a method of displaying one surface in front of another, even if their depth values are the same.</span></span> <span data-ttu-id="faaa3-113">Você pode usar essa técnica para uma variedade de efeitos.</span><span class="sxs-lookup"><span data-stu-id="faaa3-113">You can use this technique for a variety of effects.</span></span> <span data-ttu-id="faaa3-114">Um exemplo comum é A renderização de sombras em paredes.</span><span class="sxs-lookup"><span data-stu-id="faaa3-114">A common example is rendering shadows on walls.</span></span> <span data-ttu-id="faaa3-115">Tanto a sombra quanto a parede têm o mesmo valor de profundidade.</span><span class="sxs-lookup"><span data-stu-id="faaa3-115">Both the shadow and the wall have the same depth value.</span></span> <span data-ttu-id="faaa3-116">No entanto, você deseja que seu aplicativo mostre a sombra na parede.</span><span class="sxs-lookup"><span data-stu-id="faaa3-116">However, you want your application to show the shadow on the wall.</span></span> <span data-ttu-id="faaa3-117">Dar uma tendência z à sombra faz com que o Direct3D as exiba corretamente (Confira D3DRS \_ DEPTHBIAS).</span><span class="sxs-lookup"><span data-stu-id="faaa3-117">Giving a z-bias to the shadow makes Direct3D display them properly (see D3DRS\_DEPTHBIAS).</span></span>

## <a name="related-topics"></a><span data-ttu-id="faaa3-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="faaa3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faaa3-119">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="faaa3-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 

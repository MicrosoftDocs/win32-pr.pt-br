---
description: A interface ID3DXRenderToSurface é usada para generalizar o processo de renderização em superfícies.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Interface ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298814"
---
# <a name="id3dxrendertosurface-interface"></a><span data-ttu-id="aab14-103">Interface ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="aab14-103">ID3DXRenderToSurface interface</span></span>

<span data-ttu-id="aab14-104">A interface ID3DXRenderToSurface é usada para generalizar o processo de renderização em superfícies.</span><span class="sxs-lookup"><span data-stu-id="aab14-104">The ID3DXRenderToSurface interface is used to generalize the process of rendering to surfaces.</span></span>

## <a name="members"></a><span data-ttu-id="aab14-105">Membros</span><span class="sxs-lookup"><span data-stu-id="aab14-105">Members</span></span>

<span data-ttu-id="aab14-106">A interface **ID3DXRenderToSurface** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aab14-106">The **ID3DXRenderToSurface** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aab14-107">**ID3DXRenderToSurface** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aab14-107">**ID3DXRenderToSurface** also has these types of members:</span></span>

-   [<span data-ttu-id="aab14-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="aab14-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aab14-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="aab14-109">Methods</span></span>

<span data-ttu-id="aab14-110">A interface **ID3DXRenderToSurface** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="aab14-110">The **ID3DXRenderToSurface** interface has these methods.</span></span>



| <span data-ttu-id="aab14-111">Método</span><span class="sxs-lookup"><span data-stu-id="aab14-111">Method</span></span>                                                       | <span data-ttu-id="aab14-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="aab14-112">Description</span></span>                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aab14-113">**BeginScene**</span><span class="sxs-lookup"><span data-stu-id="aab14-113">**BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)       | <span data-ttu-id="aab14-114">Inicia uma cena.</span><span class="sxs-lookup"><span data-stu-id="aab14-114">Begins a scene.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="aab14-115">**Endcena**</span><span class="sxs-lookup"><span data-stu-id="aab14-115">**EndScene**</span></span>](id3dxrendertosurface--endscene.md)           | <span data-ttu-id="aab14-116">Encerra uma cena.</span><span class="sxs-lookup"><span data-stu-id="aab14-116">Ends a scene.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="aab14-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="aab14-117">**GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)             | <span data-ttu-id="aab14-118">Recupera os parâmetros da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="aab14-118">Retrieves the parameters of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="aab14-119">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="aab14-119">**GetDevice**</span></span>](id3dxrendertosurface--getdevice.md)         | <span data-ttu-id="aab14-120">Recupera o dispositivo Direct3D associado à superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="aab14-120">Retrieves the Direct3D device associated with the render surface.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="aab14-121">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="aab14-121">**OnLostDevice**</span></span>](id3dxrendertosurface--onlostdevice.md)   | <span data-ttu-id="aab14-122">Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks.</span><span class="sxs-lookup"><span data-stu-id="aab14-122">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="aab14-123">Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aab14-123">This method should be called whenever a device is lost or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="aab14-124">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="aab14-124">**OnResetDevice**</span></span>](id3dxrendertosurface--onresetdevice.md) | <span data-ttu-id="aab14-125">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="aab14-125">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="aab14-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="aab14-126">Remarks</span></span>

<span data-ttu-id="aab14-127">As superfícies podem ser usadas de várias maneiras, incluindo destinos de renderização, renderização fora da tela ou renderização para texturas.</span><span class="sxs-lookup"><span data-stu-id="aab14-127">Surfaces can be used in a variety of ways including render targets, off-screen rendering, or rendering to textures.</span></span>

<span data-ttu-id="aab14-128">Uma superfície pode ser configurada usando um visor separado usando o método [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md) , para fornecer uma exibição de renderização personalizada.</span><span class="sxs-lookup"><span data-stu-id="aab14-128">A surface can be configured using a separate viewport using the [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md) method, to provide a custom render view.</span></span> <span data-ttu-id="aab14-129">Se a superfície não for um destino de renderização, um destino de renderização compatível será usado e o resultado será copiado para a superfície no final da cena.</span><span class="sxs-lookup"><span data-stu-id="aab14-129">If the surface is not a render target, a compatible render target is used, and the result is copied to the surface at the end of the scene.</span></span>

<span data-ttu-id="aab14-130">A interface **ID3DXRenderToSurface** é obtida chamando a função [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .</span><span class="sxs-lookup"><span data-stu-id="aab14-130">The **ID3DXRenderToSurface** interface is obtained by calling the [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) function.</span></span>

<span data-ttu-id="aab14-131">O tipo LPD3DXRENDERTOSURFACE é definido como um ponteiro para a interface **ID3DXRenderToSurface** .</span><span class="sxs-lookup"><span data-stu-id="aab14-131">The LPD3DXRENDERTOSURFACE type is defined as a pointer to the **ID3DXRenderToSurface** interface.</span></span>


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a><span data-ttu-id="aab14-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aab14-132">Requirements</span></span>



| <span data-ttu-id="aab14-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="aab14-133">Requirement</span></span> | <span data-ttu-id="aab14-134">Valor</span><span class="sxs-lookup"><span data-stu-id="aab14-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aab14-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aab14-135">Header</span></span><br/>  | <dl> <span data-ttu-id="aab14-136"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="aab14-136"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="aab14-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aab14-137">Library</span></span><br/> | <dl> <span data-ttu-id="aab14-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aab14-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aab14-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="aab14-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab14-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="aab14-140">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

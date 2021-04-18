---
description: A interface ID3DXRenderToEnvMap é usada para generalizar o processo de renderização para mapas de ambiente.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Interface ID3DXRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752178"
---
# <a name="id3dxrendertoenvmap-interface"></a><span data-ttu-id="43edc-103">Interface ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="43edc-103">ID3DXRenderToEnvMap interface</span></span>

<span data-ttu-id="43edc-104">A interface ID3DXRenderToEnvMap é usada para generalizar o processo de renderização para mapas de ambiente.</span><span class="sxs-lookup"><span data-stu-id="43edc-104">The ID3DXRenderToEnvMap interface is used to generalize the process of rendering to environment maps.</span></span>

## <a name="members"></a><span data-ttu-id="43edc-105">Membros</span><span class="sxs-lookup"><span data-stu-id="43edc-105">Members</span></span>

<span data-ttu-id="43edc-106">A interface **ID3DXRenderToEnvMap** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="43edc-106">The **ID3DXRenderToEnvMap** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="43edc-107">**ID3DXRenderToEnvMap** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="43edc-107">**ID3DXRenderToEnvMap** also has these types of members:</span></span>

-   [<span data-ttu-id="43edc-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="43edc-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="43edc-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="43edc-109">Methods</span></span>

<span data-ttu-id="43edc-110">A interface **ID3DXRenderToEnvMap** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="43edc-110">The **ID3DXRenderToEnvMap** interface has these methods.</span></span>



| <span data-ttu-id="43edc-111">Método</span><span class="sxs-lookup"><span data-stu-id="43edc-111">Method</span></span>                                                          | <span data-ttu-id="43edc-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="43edc-112">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43edc-113">**BeginCube**</span><span class="sxs-lookup"><span data-stu-id="43edc-113">**BeginCube**</span></span>](id3dxrendertoenvmap--begincube.md)             | <span data-ttu-id="43edc-114">Inicie a renderização de um mapa de ambiente cúbico.</span><span class="sxs-lookup"><span data-stu-id="43edc-114">Initiate the rendering of a cubic environment map.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="43edc-115">**BeginHemisphere**</span><span class="sxs-lookup"><span data-stu-id="43edc-115">**BeginHemisphere**</span></span>](id3dxrendertoenvmap--beginhemisphere.md) | <span data-ttu-id="43edc-116">Inicie a renderização de um mapa de ambiente Hemispheric.</span><span class="sxs-lookup"><span data-stu-id="43edc-116">Initiate the rendering of a hemispheric environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="43edc-117">**BeginParabolic**</span><span class="sxs-lookup"><span data-stu-id="43edc-117">**BeginParabolic**</span></span>](id3dxrendertoenvmap--beginparabolic.md)   | <span data-ttu-id="43edc-118">Inicie a renderização de um mapa de ambiente parabólico.</span><span class="sxs-lookup"><span data-stu-id="43edc-118">Initiate the rendering of a parabolic environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="43edc-119">**BeginSphere**</span><span class="sxs-lookup"><span data-stu-id="43edc-119">**BeginSphere**</span></span>](id3dxrendertoenvmap--beginsphere.md)         | <span data-ttu-id="43edc-120">Inicie a renderização de um mapa de ambiente esférico.</span><span class="sxs-lookup"><span data-stu-id="43edc-120">Initiate the rendering of a spherical environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="43edc-121">**Completo**</span><span class="sxs-lookup"><span data-stu-id="43edc-121">**End**</span></span>](id3dxrendertoenvmap--end.md)                         | <span data-ttu-id="43edc-122">Restaurar todos os destinos de renderização e, se necessário, compor todas as faces renderizadas na superfície do mapa do ambiente.</span><span class="sxs-lookup"><span data-stu-id="43edc-122">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span><br/>                                                                           |
| [<span data-ttu-id="43edc-123">**Detecção Facial**</span><span class="sxs-lookup"><span data-stu-id="43edc-123">**Face**</span></span>](id3dxrendertoenvmap--face.md)                       | <span data-ttu-id="43edc-124">Inicie o desenho de cada face de um mapa de ambiente.</span><span class="sxs-lookup"><span data-stu-id="43edc-124">Initiate the drawing of each face of an environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="43edc-125">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="43edc-125">**GetDesc**</span></span>](id3dxrendertoenvmap--getdesc.md)                 | <span data-ttu-id="43edc-126">Recupera a descrição da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="43edc-126">Retrieves the description of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="43edc-127">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="43edc-127">**GetDevice**</span></span>](id3dxrendertoenvmap--getdevice.md)             | <span data-ttu-id="43edc-128">Recupera o dispositivo Direct3D associado ao mapa de ambiente.</span><span class="sxs-lookup"><span data-stu-id="43edc-128">Retrieves the Direct3D device associated with the environment map.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="43edc-129">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="43edc-129">**OnLostDevice**</span></span>](id3dxrendertoenvmap--onlostdevice.md)       | <span data-ttu-id="43edc-130">Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks.</span><span class="sxs-lookup"><span data-stu-id="43edc-130">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="43edc-131">Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43edc-131">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="43edc-132">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="43edc-132">**OnResetDevice**</span></span>](id3dxrendertoenvmap--onresetdevice.md)     | <span data-ttu-id="43edc-133">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="43edc-133">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="43edc-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="43edc-134">Remarks</span></span>

<span data-ttu-id="43edc-135">Um mapa de ambiente é usado para a geometria da cena de mapa de textura para fornecer uma cena mais sofisticada sem usar geometria complexa.</span><span class="sxs-lookup"><span data-stu-id="43edc-135">An environment map is used to texture-map scene geometry to provide a more sophisticated scene without using complex geometry.</span></span> <span data-ttu-id="43edc-136">Esta interface dá suporte à criação de superfícies para os seguintes tipos de geometria: Cube, meia Sphere ou Hemispheric, parabólico ou Sphere.</span><span class="sxs-lookup"><span data-stu-id="43edc-136">This interface supports creating surfaces for the following kinds of geometry: cube, half sphere or hemispheric, parabolic, or sphere.</span></span>

<span data-ttu-id="43edc-137">A interface **ID3DXRenderToEnvMap** é obtida chamando a função [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="43edc-137">The **ID3DXRenderToEnvMap** interface is obtained by calling the [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) function.</span></span>

<span data-ttu-id="43edc-138">O tipo LPD3DXRenderToEnvMap é definido como um ponteiro para a interface **ID3DXRenderToEnvMap** .</span><span class="sxs-lookup"><span data-stu-id="43edc-138">The LPD3DXRenderToEnvMap type is defined as a pointer to the **ID3DXRenderToEnvMap** interface.</span></span>


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a><span data-ttu-id="43edc-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43edc-139">Requirements</span></span>



| <span data-ttu-id="43edc-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="43edc-140">Requirement</span></span> | <span data-ttu-id="43edc-141">Valor</span><span class="sxs-lookup"><span data-stu-id="43edc-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43edc-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43edc-142">Header</span></span><br/>  | <dl> <span data-ttu-id="43edc-143"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="43edc-143"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="43edc-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43edc-144">Library</span></span><br/> | <dl> <span data-ttu-id="43edc-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43edc-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43edc-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="43edc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43edc-147">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="43edc-147">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

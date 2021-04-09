---
description: Habilita a decodificação acelerada por hardware de um dispositivo Direct3D 9, usando a versão 1,0 do DirectX Video Acceleration (DXVA).
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Interface IDirect3DVideoDevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090966"
---
# <a name="idirect3dvideodevice9-interface"></a><span data-ttu-id="addc5-103">Interface IDirect3DVideoDevice9</span><span class="sxs-lookup"><span data-stu-id="addc5-103">IDirect3DVideoDevice9 interface</span></span>

<span data-ttu-id="addc5-104">Habilita a decodificação acelerada por hardware de um dispositivo Direct3D 9, usando a versão 1,0 do DirectX Video Acceleration (DXVA).</span><span class="sxs-lookup"><span data-stu-id="addc5-104">Enables hardware-accelerated decoding from a Direct3D 9 device, using DirectX Video Acceleration (DXVA) version 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="addc5-105">Quando usar</span><span class="sxs-lookup"><span data-stu-id="addc5-105">When to use</span></span>

<span data-ttu-id="addc5-106">Essa interface não é destinada ao uso geral do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="addc5-106">This interface is not intended for general application use.</span></span> <span data-ttu-id="addc5-107">Os filtros do decodificador do DirectShow devem usar a interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , não **IDirect3DVideoDevice9**.</span><span class="sxs-lookup"><span data-stu-id="addc5-107">DirectShow decoder filters should use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, not **IDirect3DVideoDevice9**.</span></span> <span data-ttu-id="addc5-108">Os Pins de entrada do filtro de processador de mixagem de vídeo (VMR) e o filtro de mixagem de sobreposição expõem **IAMVideoAccelerator**.</span><span class="sxs-lookup"><span data-stu-id="addc5-108">The input pins of the Video Mixing Renderer (VMR) filter and the Overlay Mixer filter expose **IAMVideoAccelerator**.</span></span>

## <a name="members"></a><span data-ttu-id="addc5-109">Membros</span><span class="sxs-lookup"><span data-stu-id="addc5-109">Members</span></span>

<span data-ttu-id="addc5-110">A interface **IDirect3DVideoDevice9** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="addc5-110">The **IDirect3DVideoDevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="addc5-111">**IDirect3DVideoDevice9** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="addc5-111">**IDirect3DVideoDevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="addc5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="addc5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="addc5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="addc5-113">Methods</span></span>

<span data-ttu-id="addc5-114">A interface **IDirect3DVideoDevice9** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="addc5-114">The **IDirect3DVideoDevice9** interface has these methods.</span></span>



| <span data-ttu-id="addc5-115">Método</span><span class="sxs-lookup"><span data-stu-id="addc5-115">Method</span></span>                                                                                   | <span data-ttu-id="addc5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="addc5-116">Description</span></span>                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="addc5-117">**CreateDXVADevice**</span><span class="sxs-lookup"><span data-stu-id="addc5-117">**CreateDXVADevice**</span></span>](idirect3dvideodevice9-createdxvadevice.md)                       | <span data-ttu-id="addc5-118">Cria um dispositivo de decodificador DXVA.</span><span class="sxs-lookup"><span data-stu-id="addc5-118">Creates a DXVA decoder device.</span></span><br/>                                                                                         |
| [<span data-ttu-id="addc5-119">**CreateSurface**</span><span class="sxs-lookup"><span data-stu-id="addc5-119">**CreateSurface**</span></span>](idirect3dvideodevice9-createsurface.md)                             | <span data-ttu-id="addc5-120">Cria uma superfície compactada para a decodificação de DXVA.</span><span class="sxs-lookup"><span data-stu-id="addc5-120">Creates a compressed surface for DXVA decoding.</span></span><br/>                                                                        |
| [<span data-ttu-id="addc5-121">**GetDXVACompressedBufferInfo**</span><span class="sxs-lookup"><span data-stu-id="addc5-121">**GetDXVACompressedBufferInfo**</span></span>](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | <span data-ttu-id="addc5-122">Obtém informações sobre os buffers compactados necessários para a decodificação acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="addc5-122">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span><br/>                                |
| [<span data-ttu-id="addc5-123">**GetDXVAGuids**</span><span class="sxs-lookup"><span data-stu-id="addc5-123">**GetDXVAGuids**</span></span>](idirect3dvideodevice9-getdxvaguids.md)                               | <span data-ttu-id="addc5-124">Obtém uma lista dos perfis de DXVA com suporte no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="addc5-124">Gets a list of the DXVA profiles that are supported by the display driver.</span></span><br/>                                             |
| [<span data-ttu-id="addc5-125">**GetDXVAInternalInfo**</span><span class="sxs-lookup"><span data-stu-id="addc5-125">**GetDXVAInternalInfo**</span></span>](idirect3dvideodevice9-getdxvainternalinfo.md)                 | <span data-ttu-id="addc5-126">Consulta a quantidade de memória temporária que a HAL (camada de abstração de hardware) alocará para seu uso particular.</span><span class="sxs-lookup"><span data-stu-id="addc5-126">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span> <br/> |
| [<span data-ttu-id="addc5-127">**GetUncompressedDXVAFormats**</span><span class="sxs-lookup"><span data-stu-id="addc5-127">**GetUncompressedDXVAFormats**</span></span>](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | <span data-ttu-id="addc5-128">Obtém uma lista de formatos de pixel não compactados que podem ser renderizados usando um perfil de DXVA especificado.</span><span class="sxs-lookup"><span data-stu-id="addc5-128">Gets a list of uncompressed pixel formats that can be rendered using a specified DXVA profile.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="addc5-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="addc5-129">Remarks</span></span>

<span data-ttu-id="addc5-130">Para obter um ponteiro para essa interface, chame **QueryInterface** em um ponteiro [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) ou [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) .</span><span class="sxs-lookup"><span data-stu-id="addc5-130">To get a pointer to this interface, call **QueryInterface** on an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) or [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) pointer.</span></span>

<span data-ttu-id="addc5-131">Esta interface dá suporte apenas a DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="addc5-131">This interface supports DXVA 1.0 only.</span></span> <span data-ttu-id="addc5-132">Ele não dá suporte a DXVA 2,0.</span><span class="sxs-lookup"><span data-stu-id="addc5-132">It does not support DXVA 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="addc5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="addc5-133">Requirements</span></span>



| <span data-ttu-id="addc5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="addc5-134">Requirement</span></span> | <span data-ttu-id="addc5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="addc5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="addc5-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="addc5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="addc5-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="addc5-137">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="addc5-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="addc5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="addc5-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="addc5-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="addc5-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="addc5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="addc5-141"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="addc5-141"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="addc5-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="addc5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="addc5-143">Interfaces de vídeo Direct3D</span><span class="sxs-lookup"><span data-stu-id="addc5-143">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> <dt>

[<span data-ttu-id="addc5-144">Aceleração de vídeo do DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="addc5-144">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="addc5-145">Especificação de DXVA 1,0</span><span class="sxs-lookup"><span data-stu-id="addc5-145">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 

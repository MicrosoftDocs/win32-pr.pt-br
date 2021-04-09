---
description: Cria uma superfície compactada para a decodificação de aceleração de vídeo do DirectX (DXVA).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'Método IDirect3DVideoDevice9:: CreateSurface (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091460"
---
# <a name="idirect3dvideodevice9createsurface-method"></a><span data-ttu-id="73e69-103">Método IDirect3DVideoDevice9:: CreateSurface</span><span class="sxs-lookup"><span data-stu-id="73e69-103">IDirect3DVideoDevice9::CreateSurface method</span></span>

<span data-ttu-id="73e69-104">Cria uma superfície compactada para a decodificação de aceleração de vídeo do DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="73e69-104">Creates a compressed surface for DirectX Video Acceleration (DXVA) decoding.</span></span>

<span data-ttu-id="73e69-105">Para obter os requisitos de superfície, chame [**IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) e examine as estruturas [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) retornadas.</span><span class="sxs-lookup"><span data-stu-id="73e69-105">To get the surface requirements, call [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) and examine the returned [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e69-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73e69-106">Syntax</span></span>


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a><span data-ttu-id="73e69-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73e69-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e69-108">*Largura*</span><span class="sxs-lookup"><span data-stu-id="73e69-108">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="73e69-109">A largura da superfície, em pixels.</span><span class="sxs-lookup"><span data-stu-id="73e69-109">The width of the surface, in pixels.</span></span> <span data-ttu-id="73e69-110">Defina esse parâmetro como igual a **DXVACompBufferInfo. WidthToCreate**.</span><span class="sxs-lookup"><span data-stu-id="73e69-110">Set this parameter equal to **DXVACompBufferInfo.WidthToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="73e69-111">*Altura*</span><span class="sxs-lookup"><span data-stu-id="73e69-111">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="73e69-112">A altura da superfície, em pixels.</span><span class="sxs-lookup"><span data-stu-id="73e69-112">The height of the surface, in pixels.</span></span> <span data-ttu-id="73e69-113">Defina esse parâmetro como igual a **DXVACompBufferInfo. HeightToCreate**.</span><span class="sxs-lookup"><span data-stu-id="73e69-113">Set this parameter equal to **DXVACompBufferInfo.HeightToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="73e69-114">*Backbuffers*</span><span class="sxs-lookup"><span data-stu-id="73e69-114">*BackBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="73e69-115">O número de buffers de fundo.</span><span class="sxs-lookup"><span data-stu-id="73e69-115">The number of back buffers.</span></span> <span data-ttu-id="73e69-116">Esse parâmetro pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="73e69-116">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="73e69-117">*Formato*</span><span class="sxs-lookup"><span data-stu-id="73e69-117">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="73e69-118">O formato de pixel, especificado como um valor **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="73e69-118">The pixel format, specified as a **D3DFORMAT** value.</span></span> <span data-ttu-id="73e69-119">Defina esse parâmetro como igual a **DXVACompBufferInfo. Format**.</span><span class="sxs-lookup"><span data-stu-id="73e69-119">Set this parameter equal to **DXVACompBufferInfo.Format**.</span></span>

</dd> <dt>

<span data-ttu-id="73e69-120">*Pool*</span><span class="sxs-lookup"><span data-stu-id="73e69-120">*Pool*</span></span> 
</dt> <dd>

<span data-ttu-id="73e69-121">O pool de memória no qual criar a superfície, especificada como um valor **D3DPOOL** .</span><span class="sxs-lookup"><span data-stu-id="73e69-121">The memory pool in which to create the surface, specified as a **D3DPOOL** value.</span></span> <span data-ttu-id="73e69-122">Defina esse parâmetro como igual a **DXVACompBufferInfo. pool**.</span><span class="sxs-lookup"><span data-stu-id="73e69-122">Set this parameter equal to **DXVACompBufferInfo.Pool**.</span></span>

</dd> <dt>

<span data-ttu-id="73e69-123">*Usage*</span><span class="sxs-lookup"><span data-stu-id="73e69-123">*Usage*</span></span> 
</dt> <dd>

<span data-ttu-id="73e69-124">Uma ou **uma** ou mais constantes de **D3DUSAGE** .</span><span class="sxs-lookup"><span data-stu-id="73e69-124">A bitwise **OR** of one or more **D3DUSAGE** constants.</span></span> <span data-ttu-id="73e69-125">Defina esse parâmetro como igual a **DXVACompBufferInfo. Usage**.</span><span class="sxs-lookup"><span data-stu-id="73e69-125">Set this parameter equal to **DXVACompBufferInfo.Usage**.</span></span>

</dd> <dt>

<span data-ttu-id="73e69-126">*ppSurface*</span><span class="sxs-lookup"><span data-stu-id="73e69-126">*ppSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="73e69-127">Recebe um ponteiro para a interface **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="73e69-127">Receives a pointer to the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="73e69-128">O chamador deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="73e69-128">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="73e69-129">*pSharedHandle*</span><span class="sxs-lookup"><span data-stu-id="73e69-129">*pSharedHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="73e69-130">Reservado.</span><span class="sxs-lookup"><span data-stu-id="73e69-130">Reserved.</span></span> <span data-ttu-id="73e69-131">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="73e69-131">Set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e69-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73e69-132">Return value</span></span>

<span data-ttu-id="73e69-133">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="73e69-133">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73e69-134">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73e69-134">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73e69-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73e69-135">Requirements</span></span>



| <span data-ttu-id="73e69-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="73e69-136">Requirement</span></span> | <span data-ttu-id="73e69-137">Valor</span><span class="sxs-lookup"><span data-stu-id="73e69-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="73e69-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73e69-138">Minimum supported client</span></span><br/> | <span data-ttu-id="73e69-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73e69-139">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73e69-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73e69-140">Minimum supported server</span></span><br/> | <span data-ttu-id="73e69-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73e69-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="73e69-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73e69-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="73e69-143"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="73e69-143"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e69-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="73e69-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e69-145">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="73e69-145">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 





---
description: Função de proxy para o método CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: Função IWICImagingFactory_CreateBitmapFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753378"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a><span data-ttu-id="bc8c8-103">\_Função de \_ proxy IWICImagingFactory CreateBitmapFromMemory</span><span class="sxs-lookup"><span data-stu-id="bc8c8-103">IWICImagingFactory\_CreateBitmapFromMemory\_Proxy function</span></span>

<span data-ttu-id="bc8c8-104">Função de proxy para o método [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) .</span><span class="sxs-lookup"><span data-stu-id="bc8c8-104">Proxy function for the [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc8c8-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="bc8c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc8c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8c8-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8c8-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="bc8c8-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="bc8c8-109">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8c8-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="bc8c8-110">Type: **UINT**</span></span>

<span data-ttu-id="bc8c8-111">A largura do novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="bc8c8-111">The width of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="bc8c8-112">*uiHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8c8-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="bc8c8-113">Type: **UINT**</span></span>

<span data-ttu-id="bc8c8-114">A altura do novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="bc8c8-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="bc8c8-115">*PixelFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8c8-116">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="bc8c8-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="bc8c8-117">O formato de pixel do novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="bc8c8-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="bc8c8-118">*cbStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-118">*cbStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8c8-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="bc8c8-119">Type: **UINT**</span></span>

<span data-ttu-id="bc8c8-120">O [*Stride*](/windows) dos dados de pixel fornecidos.</span><span class="sxs-lookup"><span data-stu-id="bc8c8-120">The [*stride*](/windows) of the given pixel data.</span></span>

</dd> <dt>

<span data-ttu-id="bc8c8-121">*cbBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-121">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8c8-122">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="bc8c8-122">Type: **UINT**</span></span>

<span data-ttu-id="bc8c8-123">O tamanho de *pbBuffer*.</span><span class="sxs-lookup"><span data-stu-id="bc8c8-123">The size of *pbBuffer*.</span></span>

</dd> <dt>

<span data-ttu-id="bc8c8-124">*pbBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-124">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8c8-125">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="bc8c8-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="bc8c8-126">O buffer usado para criar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="bc8c8-126">The buffer used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="bc8c8-127">_ppIBitmap \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-127">_ppIBitmap\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8c8-128">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="bc8c8-128">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="bc8c8-129">Um ponteiro que recebe um ponteiro para o novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="bc8c8-129">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8c8-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc8c8-130">Return value</span></span>

<span data-ttu-id="bc8c8-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc8c8-131">Type: **HRESULT**</span></span>

<span data-ttu-id="bc8c8-132">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bc8c8-132">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc8c8-133">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc8c8-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc8c8-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc8c8-134">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8c8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc8c8-135">Requirements</span></span>



| <span data-ttu-id="bc8c8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc8c8-136">Requirement</span></span> | <span data-ttu-id="bc8c8-137">Valor</span><span class="sxs-lookup"><span data-stu-id="bc8c8-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8c8-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc8c8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bc8c8-139">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-139">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bc8c8-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc8c8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bc8c8-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc8c8-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bc8c8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bc8c8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc8c8-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc8c8-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


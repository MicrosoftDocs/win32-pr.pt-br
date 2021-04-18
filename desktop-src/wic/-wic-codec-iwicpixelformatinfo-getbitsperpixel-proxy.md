---
description: Função de proxy para o método GetBitsPerPixel.
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: Função IWICPixelFormatInfo_GetBitsPerPixel_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807947"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a><span data-ttu-id="3c34a-103">\_Função de \_ proxy IWICPixelFormatInfo GetBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="3c34a-103">IWICPixelFormatInfo\_GetBitsPerPixel\_Proxy function</span></span>

<span data-ttu-id="3c34a-104">Função de proxy para o método [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) .</span><span class="sxs-lookup"><span data-stu-id="3c34a-104">Proxy function for the [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c34a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c34a-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a><span data-ttu-id="3c34a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c34a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c34a-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="3c34a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c34a-108">Tipo: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="3c34a-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="3c34a-109">Ponteiro para este objeto [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="3c34a-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="3c34a-110">*puiBitsPerPixel* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3c34a-110">*puiBitsPerPixel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c34a-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="3c34a-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="3c34a-112">Ponteiro que recebe o BPP do formato de pixel.</span><span class="sxs-lookup"><span data-stu-id="3c34a-112">Pointer that receives the BPP of the pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c34a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c34a-113">Return value</span></span>

<span data-ttu-id="3c34a-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3c34a-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3c34a-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3c34a-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c34a-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c34a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c34a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c34a-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3c34a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c34a-118">Requirements</span></span>



| <span data-ttu-id="3c34a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c34a-119">Requirement</span></span> | <span data-ttu-id="3c34a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3c34a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c34a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c34a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3c34a-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c34a-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3c34a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c34a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3c34a-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c34a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3c34a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3c34a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c34a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c34a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: Função de proxy para o método CreateDecoderFromFileHandle.
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: Função IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 15c515bb17641e2e7b70b79552fe3bacf1f1c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921925"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a><span data-ttu-id="90838-103">\_Função de \_ proxy IWICImagingFactory CreateDecoderFromFileHandle</span><span class="sxs-lookup"><span data-stu-id="90838-103">IWICImagingFactory\_CreateDecoderFromFileHandle\_Proxy function</span></span>

<span data-ttu-id="90838-104">Função de proxy para o método [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) .</span><span class="sxs-lookup"><span data-stu-id="90838-104">Proxy function for the [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="90838-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90838-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="90838-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90838-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90838-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90838-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90838-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="90838-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="90838-109">_hFile \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90838-109">_hFile\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90838-110">Tipo: **ULONG \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="90838-110">Type: **ULONG\_PTR**</span></span>

<span data-ttu-id="90838-111">O identificador de arquivo do qual criar o decodificador.</span><span class="sxs-lookup"><span data-stu-id="90838-111">The file handle to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="90838-112">*pguidVendor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90838-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90838-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="90838-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="90838-114">O GUID do fornecedor para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="90838-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="90838-115">_metadataOptions \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90838-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90838-116">Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="90838-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="90838-117">O [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) a ser usado ao criar o decodificador.</span><span class="sxs-lookup"><span data-stu-id="90838-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="90838-118">*ppIDecoder* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="90838-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90838-119">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="90838-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="90838-120">Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="90838-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90838-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90838-121">Return value</span></span>

<span data-ttu-id="90838-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="90838-122">Type: **HRESULT**</span></span>

<span data-ttu-id="90838-123">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="90838-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="90838-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="90838-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="90838-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="90838-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="90838-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90838-126">Requirements</span></span>



| <span data-ttu-id="90838-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="90838-127">Requirement</span></span> | <span data-ttu-id="90838-128">Valor</span><span class="sxs-lookup"><span data-stu-id="90838-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90838-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90838-129">Minimum supported client</span></span><br/> | <span data-ttu-id="90838-130">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90838-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="90838-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90838-131">Minimum supported server</span></span><br/> | <span data-ttu-id="90838-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90838-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="90838-133">DLL</span><span class="sxs-lookup"><span data-stu-id="90838-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90838-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90838-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





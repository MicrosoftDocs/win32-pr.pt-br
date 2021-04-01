---
description: Função de proxy para o método CreateDecoderFromStream.
ms.assetid: 8395d647-c8c9-4715-b15d-a30755ae0a98
title: Função IWICImagingFactory_CreateDecoderFromStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1f6f84c9c29d10243f1b3bcb2cad43967547eeae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663385"
---
# <a name="iwicimagingfactory_createdecoderfromstream_proxy-function"></a><span data-ttu-id="5421c-103">\_Função de \_ proxy IWICImagingFactory CreateDecoderFromStream</span><span class="sxs-lookup"><span data-stu-id="5421c-103">IWICImagingFactory\_CreateDecoderFromStream\_Proxy function</span></span>

<span data-ttu-id="5421c-104">Função de proxy para o método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="5421c-104">Proxy function for the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5421c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5421c-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromStream_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        IStream            *pIStream,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="5421c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5421c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5421c-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5421c-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5421c-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="5421c-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="5421c-109">_pIStream \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5421c-109">_pIStream\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5421c-110">Tipo: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="5421c-110">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="5421c-111">O fluxo do qual criar o decodificador.</span><span class="sxs-lookup"><span data-stu-id="5421c-111">The stream to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="5421c-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5421c-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5421c-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="5421c-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="5421c-114">O GUID do fornecedor para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="5421c-114">The vendor GUID for the decoder .</span></span>

</dd> <dt>

<span data-ttu-id="5421c-115">_metadataOptions \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5421c-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5421c-116">Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="5421c-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="5421c-117">O [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) a ser usado ao criar o decodificador.</span><span class="sxs-lookup"><span data-stu-id="5421c-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="5421c-118">*ppIDecoder* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5421c-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5421c-119">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="5421c-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="5421c-120">Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="5421c-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5421c-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5421c-121">Return value</span></span>

<span data-ttu-id="5421c-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5421c-122">Type: **HRESULT**</span></span>

<span data-ttu-id="5421c-123">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5421c-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5421c-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5421c-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5421c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="5421c-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5421c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5421c-126">Requirements</span></span>



| <span data-ttu-id="5421c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5421c-127">Requirement</span></span> | <span data-ttu-id="5421c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5421c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5421c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5421c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5421c-130">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5421c-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5421c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5421c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5421c-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5421c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5421c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5421c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5421c-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5421c-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


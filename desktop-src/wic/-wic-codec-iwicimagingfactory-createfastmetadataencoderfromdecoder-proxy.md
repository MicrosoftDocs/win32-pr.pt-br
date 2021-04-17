---
description: Função de proxy para o método CreateFastMetadataEncoderFromDecoder.
ms.assetid: eae7ed9c-9205-4e41-91b2-461fd1f5d093
title: Função IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cdeb682139feb03c19cd66e999b6e3b8b7b366d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783782"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromdecoder_proxy-function"></a><span data-ttu-id="fa08e-103">\_Função de \_ proxy IWICImagingFactory CreateFastMetadataEncoderFromDecoder</span><span class="sxs-lookup"><span data-stu-id="fa08e-103">IWICImagingFactory\_CreateFastMetadataEncoderFromDecoder\_Proxy function</span></span>

<span data-ttu-id="fa08e-104">Função de proxy para o método [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) .</span><span class="sxs-lookup"><span data-stu-id="fa08e-104">Proxy function for the [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa08e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa08e-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapDecoder       *pIDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="fa08e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa08e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa08e-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa08e-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa08e-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="fa08e-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="fa08e-109">_pIDecoder \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa08e-109">_pIDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa08e-110">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="fa08e-110">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="fa08e-111">O decodificador do qual criar o [_ *IWICFastMetadataEncoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .</span><span class="sxs-lookup"><span data-stu-id="fa08e-111">The decoder to create the [_ *IWICFastMetadataEncoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="fa08e-112">*ppIFME* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fa08e-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa08e-113">Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="fa08e-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="fa08e-114">Um ponteiro que recebe um ponteiro para o novo [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="fa08e-114">A pointer that receives a pointer to the new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa08e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa08e-115">Return value</span></span>

<span data-ttu-id="fa08e-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fa08e-116">Type: **HRESULT**</span></span>

<span data-ttu-id="fa08e-117">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fa08e-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa08e-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa08e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa08e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa08e-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fa08e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa08e-120">Requirements</span></span>



| <span data-ttu-id="fa08e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa08e-121">Requirement</span></span> | <span data-ttu-id="fa08e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fa08e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa08e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa08e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fa08e-124">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa08e-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fa08e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa08e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fa08e-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa08e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fa08e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fa08e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa08e-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa08e-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





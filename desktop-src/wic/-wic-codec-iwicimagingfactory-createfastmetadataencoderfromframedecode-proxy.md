---
description: Função de proxy para o método CreateFastMetadataEncoderFromFrameDecode.
ms.assetid: 0edc3387-47e9-401c-9153-76c8c32b52de
title: Função IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 101bb6aca30f3511a8eb370afa8eb8fd6dda1c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808242"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromframedecode_proxy-function"></a><span data-ttu-id="11ad3-103">\_Função de \_ proxy IWICImagingFactory CreateFastMetadataEncoderFromFrameDecode</span><span class="sxs-lookup"><span data-stu-id="11ad3-103">IWICImagingFactory\_CreateFastMetadataEncoderFromFrameDecode\_Proxy function</span></span>

<span data-ttu-id="11ad3-104">Função de proxy para o método [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) .</span><span class="sxs-lookup"><span data-stu-id="11ad3-104">Proxy function for the [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ad3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11ad3-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapFrameDecode   *pIFrameDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="11ad3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11ad3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ad3-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11ad3-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11ad3-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="11ad3-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="11ad3-109">_pIFrameDecoder \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11ad3-109">_pIFrameDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11ad3-110">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="11ad3-110">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="11ad3-111">O [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) para criar o [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) de.</span><span class="sxs-lookup"><span data-stu-id="11ad3-111">The [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) to create the [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="11ad3-112">*ppIFME* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="11ad3-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11ad3-113">Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="11ad3-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="11ad3-114">Um ponteiro que recebe um ponteiro para um novo [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="11ad3-114">A pointer that receives a pointer to a new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ad3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11ad3-115">Return value</span></span>

<span data-ttu-id="11ad3-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="11ad3-116">Type: **HRESULT**</span></span>

<span data-ttu-id="11ad3-117">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="11ad3-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11ad3-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="11ad3-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="11ad3-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="11ad3-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="11ad3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11ad3-120">Requirements</span></span>



| <span data-ttu-id="11ad3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="11ad3-121">Requirement</span></span> | <span data-ttu-id="11ad3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="11ad3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11ad3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11ad3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="11ad3-124">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11ad3-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="11ad3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11ad3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="11ad3-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="11ad3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="11ad3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="11ad3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11ad3-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11ad3-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





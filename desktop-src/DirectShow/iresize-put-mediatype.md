---
description: O \_ método Put MediaType define o tipo de mídia de saída no filtro redimensionador.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'IResize: método de ut_MediaType de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810217"
---
# <a name="iresizeput_mediatype-method"></a><span data-ttu-id="38ee4-103">Método IResize::p UT \_ MediaType</span><span class="sxs-lookup"><span data-stu-id="38ee4-103">IResize::put\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="38ee4-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="38ee4-104">\[Deprecated.</span></span> <span data-ttu-id="38ee4-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38ee4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="38ee4-106">O `put_MediaType` método define o tipo de mídia de saída no filtro de redimensionador.</span><span class="sxs-lookup"><span data-stu-id="38ee4-106">The `put_MediaType` method sets the output media type on the resizer filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ee4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38ee4-107">Syntax</span></span>


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="38ee4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38ee4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ee4-109">*PGTO* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38ee4-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ee4-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contém o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="38ee4-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ee4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38ee4-111">Return value</span></span>

<span data-ttu-id="38ee4-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="38ee4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38ee4-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="38ee4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="38ee4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="38ee4-114">Remarks</span></span>

<span data-ttu-id="38ee4-115">O DES chama esse método antes de conectar o PIN de saída do filtro.</span><span class="sxs-lookup"><span data-stu-id="38ee4-115">DES calls this method before it connects the filter's output pin.</span></span> <span data-ttu-id="38ee4-116">Use o tipo de mídia como o tipo de mídia do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="38ee4-116">Use the media type as the output pin's media type.</span></span> <span data-ttu-id="38ee4-117">Retorne esse tipo de mídia no método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) e marque agsint deste tipo no método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="38ee4-117">Return this media type in the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method, and check agsint this type in the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span> <span data-ttu-id="38ee4-118">O DES nunca chama esse método depois que o pino de saída é conectado.</span><span class="sxs-lookup"><span data-stu-id="38ee4-118">DES never calls this method after the output pin is connected.</span></span>

<span data-ttu-id="38ee4-119">Atualmente, o DES sempre define o tipo de mídia de saída como um formato RGB descompactado com um bloco de formato **VIDEOINFOHEADER** (tipo de formato igual a VIDEOINFO de formato \_ ).</span><span class="sxs-lookup"><span data-stu-id="38ee4-119">Currently, DES always sets the output media type to an uncompressed RGB format with a **VIDEOINFOHEADER** format block (format type equals FORMAT\_VideoInfo).</span></span> <span data-ttu-id="38ee4-120">O subtipo pode ser MEDIASUBTYPE \_ ARGB32, que indica o RGB de 32 bits com um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="38ee4-120">The subtype might be MEDIASUBTYPE\_ARGB32, which indicates 32-bit RGB with an alpha channel.</span></span>

> [!Note]  
> <span data-ttu-id="38ee4-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="38ee4-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="38ee4-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="38ee4-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="38ee4-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="38ee4-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="38ee4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38ee4-124">Requirements</span></span>



| <span data-ttu-id="38ee4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ee4-125">Requirement</span></span> | <span data-ttu-id="38ee4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="38ee4-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38ee4-127">Versão</span><span class="sxs-lookup"><span data-stu-id="38ee4-127">Version</span></span><br/> | <span data-ttu-id="38ee4-128">DirectX 9,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="38ee4-128">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="38ee4-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38ee4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="38ee4-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="38ee4-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="38ee4-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38ee4-131">Library</span></span><br/> | <dl> <span data-ttu-id="38ee4-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38ee4-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ee4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="38ee4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ee4-134">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="38ee4-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="38ee4-135">**Interface IResize**</span><span class="sxs-lookup"><span data-stu-id="38ee4-135">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 





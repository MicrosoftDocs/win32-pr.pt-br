---
description: O método SetMediaType define o tipo de mídia descompactado para o grupo.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'Método IAMTimelineGroup:: SetMediaType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759551"
---
# <a name="iamtimelinegroupsetmediatype-method"></a><span data-ttu-id="d4644-103">Método IAMTimelineGroup:: SetMediaType</span><span class="sxs-lookup"><span data-stu-id="d4644-103">IAMTimelineGroup::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="d4644-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d4644-104">\[Deprecated.</span></span> <span data-ttu-id="d4644-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d4644-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d4644-106">O `SetMediaType` método define o tipo de mídia descompactado para o grupo.</span><span class="sxs-lookup"><span data-stu-id="d4644-106">The `SetMediaType` method sets the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4644-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4644-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="d4644-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4644-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4644-109">*PGTO* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4644-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4644-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que descreve o formato.</span><span class="sxs-lookup"><span data-stu-id="d4644-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure describing the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4644-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4644-111">Return value</span></span>

<span data-ttu-id="d4644-112">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="d4644-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="d4644-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d4644-113">Return code</span></span>                                                                                             | <span data-ttu-id="d4644-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4644-114">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="d4644-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4644-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="d4644-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="d4644-116">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="d4644-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d4644-117"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="d4644-118">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d4644-118">**NULL** pointer argument.</span></span><br/>           |
| <dl> <span data-ttu-id="d4644-119"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="d4644-119"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="d4644-120">O tipo de mídia especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="d4644-120">The specified media type is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4644-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4644-121">Remarks</span></span>

<span data-ttu-id="d4644-122">Há suporte para os seguintes tipos de mídia:</span><span class="sxs-lookup"><span data-stu-id="d4644-122">The following media types are supported:</span></span>

-   <span data-ttu-id="d4644-123">Vídeo RGB descompactado</span><span class="sxs-lookup"><span data-stu-id="d4644-123">Uncompressed RGB video</span></span>
-   <span data-ttu-id="d4644-124">16 bits por pixel, formato 555 (MEDIASUBTYPE \_ RGB555)</span><span class="sxs-lookup"><span data-stu-id="d4644-124">16 bits per pixel, 555 format (MEDIASUBTYPE\_RGB555)</span></span>
-   <span data-ttu-id="d4644-125">24 bits por pixel (MEDIASUBTYPE \_ RGB24)</span><span class="sxs-lookup"><span data-stu-id="d4644-125">24 bits per pixel (MEDIASUBTYPE\_RGB24)</span></span>
-   <span data-ttu-id="d4644-126">32 bits por pixel, com alfa (MEDIASUBTYPE \_ ARGB32, não MEDIASUBTYPE \_ RGB32)</span><span class="sxs-lookup"><span data-stu-id="d4644-126">32 bits per pixel, with alpha (MEDIASUBTYPE\_ARGB32, not MEDIASUBTYPE\_RGB32)</span></span>
-   <span data-ttu-id="d4644-127">áudio PCM estéreo de 16 bits (MEDIASUBTYPE \_ PCM)</span><span class="sxs-lookup"><span data-stu-id="d4644-127">16-bit stereo PCM audio (MEDIASUBTYPE\_PCM)</span></span>

<span data-ttu-id="d4644-128">Os tipos de vídeo devem usar \_ o formato VIDEOINFO para o tipo de formato e [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="d4644-128">Video types must use FORMAT\_VideoInfo for the format type and [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) for the format block.</span></span> <span data-ttu-id="d4644-129">Não há suporte para o formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="d4644-129">The [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format is not supported.</span></span> <span data-ttu-id="d4644-130">Além disso, os formatos de vídeo de cima para baixo (*biHeight* < 0) não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="d4644-130">Also, top-down video formats (*biHeight* < 0) are not supported.</span></span>

<span data-ttu-id="d4644-131">Para especificar um formato de compactação para o grupo, chame o método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="d4644-131">To specify a compression format for the group, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="d4644-132">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d4644-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d4644-133">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4644-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d4644-134">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d4644-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4644-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4644-135">Requirements</span></span>



| <span data-ttu-id="d4644-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4644-136">Requirement</span></span> | <span data-ttu-id="d4644-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d4644-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4644-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4644-138">Header</span></span><br/>  | <dl> <span data-ttu-id="d4644-139"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4644-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d4644-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4644-140">Library</span></span><br/> | <dl> <span data-ttu-id="d4644-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4644-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4644-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4644-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4644-143">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="d4644-143">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="d4644-144">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d4644-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





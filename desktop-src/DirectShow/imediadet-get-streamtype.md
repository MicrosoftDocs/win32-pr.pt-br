---
description: O \_ método Get streamtype recupera o GUID (identificador global exclusivo) para o tipo de mídia do fluxo atual.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'Método IMediaDet:: get_StreamType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780051"
---
# <a name="imediadetget_streamtype-method"></a><span data-ttu-id="5e820-103">Método streamtype de IMediaDet:: get \_</span><span class="sxs-lookup"><span data-stu-id="5e820-103">IMediaDet::get\_StreamType method</span></span>

> [!Note]  
> <span data-ttu-id="5e820-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5e820-104">\[Deprecated.</span></span> <span data-ttu-id="5e820-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5e820-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5e820-106">O `get_StreamType` método recupera o GUID (identificador global exclusivo) para o tipo de mídia do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="5e820-106">The `get_StreamType` method retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e820-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e820-107">Syntax</span></span>


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5e820-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e820-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e820-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5e820-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5e820-110">Recebe o GUID de tipo principal para o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="5e820-110">Receives the major type GUID for the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e820-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e820-111">Return value</span></span>

<span data-ttu-id="5e820-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5e820-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e820-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e820-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e820-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e820-114">Remarks</span></span>

<span data-ttu-id="5e820-115">Esse método recupera o membro **majortype** da estrutura [**do \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="5e820-115">This method retrieves the **majortype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="5e820-116">A estrutura do **\_ \_ tipo de mídia am** descreve o formato do fluxo, e o membro **majortype** é um GUID que indica a categoria geral, como áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e820-116">The **AM\_MEDIA\_TYPE** structure describes the format of the stream, and the **majortype** member is a GUID that indicates the general category, such as audio or video.</span></span> <span data-ttu-id="5e820-117">Para um fluxo de vídeo, o GUID é \_ vídeo de MediaType.</span><span class="sxs-lookup"><span data-stu-id="5e820-117">For a video stream, the GUID is MEDIATYPE\_Video.</span></span> <span data-ttu-id="5e820-118">Para áudio, é áudio de MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="5e820-118">For audio, it is MEDIATYPE\_Audio.</span></span> <span data-ttu-id="5e820-119">Para recuperar toda a estrutura do **\_ \_ tipo de mídia am** , chame o método [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="5e820-119">To retrieve the entire **AM\_MEDIA\_TYPE** structure, call the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method.</span></span>

<span data-ttu-id="5e820-120">Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="5e820-120">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="5e820-121">Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5e820-121">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="5e820-122">Para obter mais informações, consulte [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="5e820-122">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="5e820-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5e820-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5e820-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e820-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5e820-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5e820-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e820-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e820-126">Requirements</span></span>



| <span data-ttu-id="5e820-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e820-127">Requirement</span></span> | <span data-ttu-id="5e820-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5e820-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e820-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e820-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5e820-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e820-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5e820-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e820-131">Library</span></span><br/> | <dl> <span data-ttu-id="5e820-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e820-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e820-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e820-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e820-134">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="5e820-134">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="5e820-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="5e820-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





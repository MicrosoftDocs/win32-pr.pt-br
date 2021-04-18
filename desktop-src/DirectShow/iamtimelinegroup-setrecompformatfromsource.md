---
description: O método SetRecompFormatFromSource define o formato de recompactação de vídeo usando o formato de compactação de um arquivo de origem.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'Método IAMTimelineGroup:: SetRecompFormatFromSource (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810227"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a><span data-ttu-id="8da4a-103">Método IAMTimelineGroup:: SetRecompFormatFromSource</span><span class="sxs-lookup"><span data-stu-id="8da4a-103">IAMTimelineGroup::SetRecompFormatFromSource method</span></span>

> [!Note]  
> <span data-ttu-id="8da4a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="8da4a-104">\[Deprecated.</span></span> <span data-ttu-id="8da4a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8da4a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8da4a-106">O `SetRecompFormatFromSource` método define o formato de recompactação de vídeo usando o formato de compactação de um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="8da4a-106">The `SetRecompFormatFromSource` method sets the video recompression format using the compression format from a source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da4a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8da4a-107">Syntax</span></span>


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="8da4a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8da4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da4a-109">*pSource*</span><span class="sxs-lookup"><span data-stu-id="8da4a-109">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="8da4a-110">Ponteiro para a interface [**IAMTimelineSrc**](iamtimelinesrc.md) do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="8da4a-110">Pointer to the [**IAMTimelineSrc**](iamtimelinesrc.md) interface of the source object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8da4a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8da4a-111">Return value</span></span>

<span data-ttu-id="8da4a-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8da4a-112">Returns an **HRESULT** values.</span></span> <span data-ttu-id="8da4a-113">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="8da4a-113">Possible values include the following.</span></span>



| <span data-ttu-id="8da4a-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8da4a-114">Return code</span></span>                                                                                             | <span data-ttu-id="8da4a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8da4a-115">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8da4a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8da4a-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="8da4a-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="8da4a-117">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="8da4a-118"><dt>**E \_ sem \_ linha do tempo**</dt></span><span class="sxs-lookup"><span data-stu-id="8da4a-118"><dt>**E\_NO\_TIMELINE**</dt></span></span> </dl>          | <span data-ttu-id="8da4a-119">O grupo não está dentro de uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="8da4a-119">The group is not within a timeline.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="8da4a-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8da4a-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="8da4a-121">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="8da4a-121">Insufficient memory.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="8da4a-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="8da4a-122"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="8da4a-123">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="8da4a-123">**NULL** pointer argument.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="8da4a-124"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="8da4a-124"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="8da4a-125">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="8da4a-125">Invalid media type.</span></span> <span data-ttu-id="8da4a-126">O grupo não é um grupo de vídeos ou o arquivo de origem não tem nenhum fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8da4a-126">The group is not a video group, or the source file has no video stream.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8da4a-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="8da4a-127">Remarks</span></span>

<span data-ttu-id="8da4a-128">Esse método localiza o arquivo de origem associado a *pSource*, recupera o tipo de mídia do primeiro fluxo de vídeo no arquivo e define o formato de compactação de grupo usando esse tipo.</span><span class="sxs-lookup"><span data-stu-id="8da4a-128">This method finds the source file associated with *pSource*, retrieves the media type of the first video stream in the file, and sets the group compression format using that type.</span></span> <span data-ttu-id="8da4a-129">Para obter mais informações sobre formatos de compactação, consulte [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span><span class="sxs-lookup"><span data-stu-id="8da4a-129">For more information about compression formats, see [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span></span>

> [!Note]  
> <span data-ttu-id="8da4a-130">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="8da4a-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8da4a-131">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8da4a-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8da4a-132">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8da4a-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8da4a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8da4a-133">Requirements</span></span>



| <span data-ttu-id="8da4a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da4a-134">Requirement</span></span> | <span data-ttu-id="8da4a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8da4a-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8da4a-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8da4a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="8da4a-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8da4a-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8da4a-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8da4a-138">Library</span></span><br/> | <dl> <span data-ttu-id="8da4a-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8da4a-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da4a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8da4a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da4a-141">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="8da4a-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="8da4a-142">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="8da4a-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





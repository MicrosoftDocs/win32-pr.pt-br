---
description: O \_ método Get de taxa de quadros recupera a taxa de quadros do fluxo atual. O fluxo deve ser um fluxo de vídeo.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'Método IMediaDet:: get_FrameRate (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779524"
---
# <a name="imediadetget_framerate-method"></a><span data-ttu-id="7de08-104">Método IMediaDet:: obter a \_ taxa de quadros</span><span class="sxs-lookup"><span data-stu-id="7de08-104">IMediaDet::get\_FrameRate method</span></span>

> [!Note]  
> <span data-ttu-id="7de08-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="7de08-105">\[Deprecated.</span></span> <span data-ttu-id="7de08-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7de08-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7de08-107">O `get_FrameRate` método recupera a taxa de quadros do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="7de08-107">The `get_FrameRate` method retrieves the frame rate of the current stream.</span></span> <span data-ttu-id="7de08-108">O fluxo deve ser um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7de08-108">The stream must be a video stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="7de08-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7de08-109">Syntax</span></span>


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="7de08-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7de08-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de08-111">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7de08-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7de08-112">Recebe a taxa de quadros, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="7de08-112">Receives the frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de08-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7de08-113">Return value</span></span>

<span data-ttu-id="7de08-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7de08-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7de08-115">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7de08-115">Possible values include the following:</span></span>



| <span data-ttu-id="7de08-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7de08-116">Return code</span></span>                                                                                             | <span data-ttu-id="7de08-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7de08-117">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="7de08-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="7de08-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="7de08-119">O cabeçalho de formato de vídeo não especifica uma taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="7de08-119">Video format header does not specify a frame rate.</span></span><br/> |
| <dl> <span data-ttu-id="7de08-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7de08-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="7de08-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7de08-121">Success.</span></span><br/>                                           |
| <dl> <span data-ttu-id="7de08-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7de08-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="7de08-123">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="7de08-123">Invalid argument.</span></span><br/>                                  |
| <dl> <span data-ttu-id="7de08-124"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="7de08-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="7de08-125">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="7de08-125">**NULL** pointer argument.</span></span><br/>                         |
| <dl> <span data-ttu-id="7de08-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="7de08-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="7de08-127">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="7de08-127">Invalid media type.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="7de08-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="7de08-128">Remarks</span></span>

<span data-ttu-id="7de08-129">Esse método não pode recuperar a taxa de quadros de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="7de08-129">This method cannot retrieve the frame rate from an ASF file.</span></span>

<span data-ttu-id="7de08-130">Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="7de08-130">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="7de08-131">Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="7de08-131">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="7de08-132">Para obter mais informações, consulte [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="7de08-132">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="7de08-133">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="7de08-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7de08-134">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7de08-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7de08-135">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7de08-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7de08-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7de08-136">Requirements</span></span>



| <span data-ttu-id="7de08-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7de08-137">Requirement</span></span> | <span data-ttu-id="7de08-138">Valor</span><span class="sxs-lookup"><span data-stu-id="7de08-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7de08-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7de08-139">Header</span></span><br/>  | <dl> <span data-ttu-id="7de08-140"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7de08-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7de08-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7de08-141">Library</span></span><br/> | <dl> <span data-ttu-id="7de08-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7de08-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7de08-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="7de08-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de08-144">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="7de08-144">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="7de08-145">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="7de08-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





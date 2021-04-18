---
description: O método EnterBitmapGrabMode alterna o detector de mídia para o modo de captura de bitmap e busca o grafo de filtro em um horário especificado.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'Método IMediaDet:: EnterBitmapGrabMode (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768599"
---
# <a name="imediadetenterbitmapgrabmode-method"></a><span data-ttu-id="fb931-103">Método IMediaDet:: EnterBitmapGrabMode</span><span class="sxs-lookup"><span data-stu-id="fb931-103">IMediaDet::EnterBitmapGrabMode method</span></span>

> [!Note]  
> <span data-ttu-id="fb931-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="fb931-104">\[Deprecated.</span></span> <span data-ttu-id="fb931-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb931-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fb931-106">O `EnterBitmapGrabMode` método alterna o detector de mídia para o modo de captura de bitmap e procura o grafo de filtro em um horário especificado.</span><span class="sxs-lookup"><span data-stu-id="fb931-106">The `EnterBitmapGrabMode` method switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb931-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb931-107">Syntax</span></span>


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a><span data-ttu-id="fb931-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb931-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb931-109">*Fluxo de transmissão*</span><span class="sxs-lookup"><span data-stu-id="fb931-109">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="fb931-110">Tempo, em segundos, para o qual o grafo busca.</span><span class="sxs-lookup"><span data-stu-id="fb931-110">Time, in seconds, to which the graph seeks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb931-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb931-111">Return value</span></span>

<span data-ttu-id="fb931-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb931-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fb931-113">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="fb931-113">Possible values include the following:</span></span>



| <span data-ttu-id="fb931-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fb931-114">Return code</span></span>                                                                                             | <span data-ttu-id="fb931-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb931-115">Description</span></span>                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="fb931-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb931-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="fb931-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="fb931-117">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="fb931-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fb931-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="fb931-119">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="fb931-119">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="fb931-120"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="fb931-120"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="fb931-121">O arquivo de origem não tem um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fb931-121">The source file does not have a video stream.</span></span><br/> |
| <dl> <span data-ttu-id="fb931-122"><dt>**VFW \_ E \_ tempo \_ expirado**</dt></span><span class="sxs-lookup"><span data-stu-id="fb931-122"><dt>**VFW\_E\_TIME\_EXPIRED**</dt></span></span> </dl>    | <span data-ttu-id="fb931-123">O comando de busca expirou.</span><span class="sxs-lookup"><span data-stu-id="fb931-123">Seek command timed out.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="fb931-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb931-124">Remarks</span></span>

<span data-ttu-id="fb931-125">Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="fb931-125">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="fb931-126">Esse método insere o filtro de [**apoio de exemplo**](sample-grabber-filter.md) no gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="fb931-126">This method inserts the [**Sample Grabber**](sample-grabber-filter.md) filter into the filter graph.</span></span> <span data-ttu-id="fb931-127">Em seguida, você pode chamar [**IMediaDet:: GetSampleGrabber**](imediadet-getsamplegrabber.md) para obter um ponteiro para a interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="fb931-127">You can then call [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) to obtain a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span> <span data-ttu-id="fb931-128">Depois que o detector de mídia entrar no modo de captura de bitmap, os vários métodos informativos no **IMediaDet** não funcionarão.</span><span class="sxs-lookup"><span data-stu-id="fb931-128">Once the media detector enters bitmap grab mode, the various informational methods in **IMediaDet** do not work.</span></span>

<span data-ttu-id="fb931-129">Os métodos [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) ou [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md) também colocam o detector de mídia no modo de captura de bitmap.</span><span class="sxs-lookup"><span data-stu-id="fb931-129">The [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md) methods also put the media detector into bitmap grab mode.</span></span>

> [!Note]  
> <span data-ttu-id="fb931-130">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="fb931-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb931-131">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fb931-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fb931-132">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fb931-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb931-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb931-133">Requirements</span></span>



| <span data-ttu-id="fb931-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb931-134">Requirement</span></span> | <span data-ttu-id="fb931-135">Valor</span><span class="sxs-lookup"><span data-stu-id="fb931-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb931-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb931-136">Header</span></span><br/>  | <dl> <span data-ttu-id="fb931-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb931-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fb931-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb931-138">Library</span></span><br/> | <dl> <span data-ttu-id="fb931-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb931-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb931-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb931-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb931-141">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="fb931-141">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="fb931-142">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="fb931-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





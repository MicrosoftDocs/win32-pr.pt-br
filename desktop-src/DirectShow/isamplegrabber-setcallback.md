---
description: O método SetCallback especifica um método de retorno de chamada para chamar em exemplos de entrada.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'Método ISampleGrabber:: SetCallback (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810169"
---
# <a name="isamplegrabbersetcallback-method"></a><span data-ttu-id="44f9b-103">Método ISampleGrabber:: SetCallback</span><span class="sxs-lookup"><span data-stu-id="44f9b-103">ISampleGrabber::SetCallback method</span></span>

> [!Note]  
> <span data-ttu-id="44f9b-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="44f9b-104">\[Deprecated.</span></span> <span data-ttu-id="44f9b-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="44f9b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="44f9b-106">O método **SetCallback** especifica um método de retorno de chamada para chamar em exemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="44f9b-106">The **SetCallback** method specifies a callback method to call on incoming samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f9b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44f9b-107">Syntax</span></span>


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a><span data-ttu-id="44f9b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44f9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f9b-109">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="44f9b-109">*pCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="44f9b-110">Ponteiro para uma interface [**ISampleGrabberCB**](isamplegrabbercb.md) que contém o método de retorno de chamada ou **nulo** para cancelar o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="44f9b-110">Pointer to an [**ISampleGrabberCB**](isamplegrabbercb.md) interface containing the callback method, or **NULL** to cancel the callback.</span></span>

</dd> <dt>

<span data-ttu-id="44f9b-111">*WhichMethodToCallback*</span><span class="sxs-lookup"><span data-stu-id="44f9b-111">*WhichMethodToCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="44f9b-112">Índice que especifica o método de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="44f9b-112">Index specifying the callback method.</span></span> <span data-ttu-id="44f9b-113">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="44f9b-113">Must be one of the following values.</span></span>



| <span data-ttu-id="44f9b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="44f9b-114">Value</span></span> | <span data-ttu-id="44f9b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="44f9b-115">Description</span></span>                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44f9b-116">0</span><span class="sxs-lookup"><span data-stu-id="44f9b-116">0</span></span>     | <span data-ttu-id="44f9b-117">O filtro de apoio de exemplo chama o método [**ISampleGrabberCB:: SampleCB**](isamplegrabbercb-samplecb.md) .</span><span class="sxs-lookup"><span data-stu-id="44f9b-117">The Sample Grabber filter calls the [**ISampleGrabberCB::SampleCB**](isamplegrabbercb-samplecb.md) method.</span></span> <span data-ttu-id="44f9b-118">Esse método recebe um ponteiro [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="44f9b-118">This method receives an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer.</span></span>               |
| <span data-ttu-id="44f9b-119">1</span><span class="sxs-lookup"><span data-stu-id="44f9b-119">1</span></span>     | <span data-ttu-id="44f9b-120">O filtro de apoio de exemplo chama o método [**ISampleGrabberCB:: BufferCB**](isamplegrabbercb-buffercb.md) .</span><span class="sxs-lookup"><span data-stu-id="44f9b-120">The Sample Grabber filter calls the [**ISampleGrabberCB::BufferCB**](isamplegrabbercb-buffercb.md) method.</span></span> <span data-ttu-id="44f9b-121">Esse método recebe um ponteiro para o buffer que está contido no exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="44f9b-121">This method receives a pointer to the buffer that is contained in the media sample.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f9b-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44f9b-122">Return value</span></span>

<span data-ttu-id="44f9b-123">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="44f9b-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44f9b-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44f9b-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f9b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="44f9b-125">Remarks</span></span>

<span data-ttu-id="44f9b-126">O thread de processamento de dados é bloqueado até que o método de retorno de chamada seja retornado.</span><span class="sxs-lookup"><span data-stu-id="44f9b-126">The data processing thread blocks until the callback method returns.</span></span> <span data-ttu-id="44f9b-127">Se o retorno de chamada não retornar rapidamente, ele poderá interferir na reprodução.</span><span class="sxs-lookup"><span data-stu-id="44f9b-127">If the callback does not return quickly, it can interfere with playback.</span></span>

<span data-ttu-id="44f9b-128">O filtro não invoca a função de retorno de chamada para exemplos de prelance ou para exemplos nos quais o membro **dwStreamId** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) é algo diferente da \_ mídia de fluxo am \_ .</span><span class="sxs-lookup"><span data-stu-id="44f9b-128">The filter does not invoke the callback function for preroll samples, or for samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="44f9b-129">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="44f9b-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="44f9b-130">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="44f9b-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="44f9b-131">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="44f9b-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="44f9b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44f9b-132">Requirements</span></span>



| <span data-ttu-id="44f9b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="44f9b-133">Requirement</span></span> | <span data-ttu-id="44f9b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="44f9b-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44f9b-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44f9b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="44f9b-136"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="44f9b-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="44f9b-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44f9b-137">Library</span></span><br/> | <dl> <span data-ttu-id="44f9b-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44f9b-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44f9b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="44f9b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f9b-140">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="44f9b-140">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="44f9b-141">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="44f9b-141">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 





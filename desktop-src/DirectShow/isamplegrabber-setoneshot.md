---
description: O método SetOneShot especifica se o filtro de apoio de exemplo é interrompido depois que o filtro recebe um exemplo.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'Método ISampleGrabber:: SetOneShot (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757010"
---
# <a name="isamplegrabbersetoneshot-method"></a><span data-ttu-id="e125e-103">Método ISampleGrabber:: SetOneShot</span><span class="sxs-lookup"><span data-stu-id="e125e-103">ISampleGrabber::SetOneShot method</span></span>

> [!Note]  
> <span data-ttu-id="e125e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e125e-104">\[Deprecated.</span></span> <span data-ttu-id="e125e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e125e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e125e-106">O método **SetOneShot** especifica se o filtro de [**apoio de exemplo**](sample-grabber-filter.md) é interrompido depois que o filtro recebe um exemplo.</span><span class="sxs-lookup"><span data-stu-id="e125e-106">The **SetOneShot** method specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e125e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e125e-107">Syntax</span></span>


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a><span data-ttu-id="e125e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e125e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e125e-109">*OneShot*</span><span class="sxs-lookup"><span data-stu-id="e125e-109">*OneShot*</span></span> 
</dt> <dd>

<span data-ttu-id="e125e-110">Um valor booliano que especifica se o filtro de apoio de exemplo é interrompido depois de receber um exemplo.</span><span class="sxs-lookup"><span data-stu-id="e125e-110">A Boolean value that specifies whether the Sample Grabber filter halts after receiving a sample.</span></span>



| <span data-ttu-id="e125e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e125e-111">Value</span></span>                                                                                                                                    | <span data-ttu-id="e125e-112">Significado</span><span class="sxs-lookup"><span data-stu-id="e125e-112">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="e125e-113"><dt>VERDADEIRO \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e125e-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="e125e-114">O exemplo de apoio é interrompido após o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="e125e-114">The Sample Grabber halts after the first sample.</span></span> <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="e125e-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e125e-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="e125e-116">Após o primeiro exemplo, o exemplo de apoio continua a processar exemplos.</span><span class="sxs-lookup"><span data-stu-id="e125e-116">After the first sample, the Sample Grabber continues to process samples.</span></span> <span data-ttu-id="e125e-117">Esse é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e125e-117">This is the default behavior.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e125e-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e125e-118">Return value</span></span>

<span data-ttu-id="e125e-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e125e-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e125e-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e125e-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e125e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e125e-121">Remarks</span></span>

<span data-ttu-id="e125e-122">Use este método para obter uma única amostra do fluxo, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e125e-122">Use this method to get a single sample from the stream, as follows:</span></span>

1.  <span data-ttu-id="e125e-123">Chame **SetOneShot** com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="e125e-123">Call **SetOneShot** with the value **TRUE**.</span></span>
2.  <span data-ttu-id="e125e-124">Opcionalmente, use a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) para buscar uma posição no fluxo.</span><span class="sxs-lookup"><span data-stu-id="e125e-124">Optionally, use the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface to seek to a position in the stream.</span></span>
3.  <span data-ttu-id="e125e-125">Chame [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para executar o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="e125e-125">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph.</span></span>
4.  <span data-ttu-id="e125e-126">Chame [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) para aguardar a parada do grafo.</span><span class="sxs-lookup"><span data-stu-id="e125e-126">Call [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) to wait for the graph to halt.</span></span> <span data-ttu-id="e125e-127">Como alternativa, chame [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obter eventos de grafo, até que você receba o evento [**EC \_ Complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="e125e-127">Alternatively, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get graph events, until you receive the [**EC\_COMPLETE**](ec-complete.md) event.</span></span>

<span data-ttu-id="e125e-128">Depois que o exemplo de apoio for interrompido, o gráfico de filtro ainda estará em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="e125e-128">After the Sample Grabber halts, the filter graph is still in a running state.</span></span> <span data-ttu-id="e125e-129">Você pode buscar ou pausar o grafo para obter outra amostra.</span><span class="sxs-lookup"><span data-stu-id="e125e-129">You can seek or pause the graph to get another sample.</span></span>

> [!Note]  
> <span data-ttu-id="e125e-130">Uma versão anterior da documentação declarava que o gráfico de filtro é interrompido depois que o exemplo é recebido.</span><span class="sxs-lookup"><span data-stu-id="e125e-130">An earlier version of the documentation stated that the filter graph stops after the sample is received.</span></span> <span data-ttu-id="e125e-131">Isso não é preciso.</span><span class="sxs-lookup"><span data-stu-id="e125e-131">That is not accurate.</span></span> <span data-ttu-id="e125e-132">O fluxo termina, mas o grafo permanece no estado executando.</span><span class="sxs-lookup"><span data-stu-id="e125e-132">The stream ends, but the graph remains in the running state.</span></span>

 

<span data-ttu-id="e125e-133">O exemplo de apoio implementa o modo One-Shot chamando [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no filtro downstream e retornando S \_ false do método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) dele.</span><span class="sxs-lookup"><span data-stu-id="e125e-133">The Sample Grabber implements one-shot mode by calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream filter and returning S\_FALSE from the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method of it.</span></span>

> [!Note]  
> <span data-ttu-id="e125e-134">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e125e-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e125e-135">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e125e-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e125e-136">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e125e-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e125e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e125e-137">Requirements</span></span>



| <span data-ttu-id="e125e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e125e-138">Requirement</span></span> | <span data-ttu-id="e125e-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e125e-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e125e-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e125e-140">Header</span></span><br/>  | <dl> <span data-ttu-id="e125e-141"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e125e-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e125e-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e125e-142">Library</span></span><br/> | <dl> <span data-ttu-id="e125e-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e125e-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e125e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e125e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e125e-145">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="e125e-145">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="e125e-146">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="e125e-146">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 





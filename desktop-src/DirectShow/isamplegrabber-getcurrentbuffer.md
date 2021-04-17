---
description: O método GetCurrentBuffer recupera uma cópia do buffer associado ao exemplo mais recente.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'Método ISampleGrabber:: GetCurrentBuffer (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766303"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a><span data-ttu-id="3ac0a-103">Método ISampleGrabber:: GetCurrentBuffer</span><span class="sxs-lookup"><span data-stu-id="3ac0a-103">ISampleGrabber::GetCurrentBuffer method</span></span>

> [!Note]  
> <span data-ttu-id="3ac0a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-104">\[Deprecated.</span></span> <span data-ttu-id="3ac0a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3ac0a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3ac0a-106">O método **GetCurrentBuffer** recupera uma cópia do buffer associado ao exemplo mais recente.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-106">The **GetCurrentBuffer** method retrieves a copy of the buffer associated with the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac0a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ac0a-107">Syntax</span></span>


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="3ac0a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ac0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ac0a-109">*pBufferSize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3ac0a-109">*pBufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac0a-110">Ponteiro para o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-110">Pointer to the size of the buffer.</span></span> <span data-ttu-id="3ac0a-111">Se *pBuffer* for **NULL**, esse parâmetro receberá o tamanho de buffer necessário, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-111">If *pBuffer* is **NULL**, this parameter receives the required buffer size, in bytes.</span></span> <span data-ttu-id="3ac0a-112">Se *pBuffer* não for **NULL**, defina esse parâmetro como igual ao tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-112">If *pBuffer* is not **NULL**, set this parameter equal to the size of the buffer, in bytes.</span></span> <span data-ttu-id="3ac0a-113">Na saída, o parâmetro recebe o número de bytes que foram copiados no buffer.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-113">On output, the parameter receives the number of bytes that were copied into the buffer.</span></span> <span data-ttu-id="3ac0a-114">Esse valor pode ser menor do que o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-114">This value might be smaller than the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3ac0a-115">*pBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ac0a-115">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac0a-116">Ponteiro para uma matriz de bytes de tamanho *pBufferSize* ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-116">Pointer to an array of bytes of size *pBufferSize*, or **NULL**.</span></span> <span data-ttu-id="3ac0a-117">Se esse parâmetro não for **nulo**, o buffer atual será copiado para a matriz.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-117">If this parameter is not **NULL**, the current buffer is copied into the array.</span></span> <span data-ttu-id="3ac0a-118">Se esse parâmetro for **nulo**, o parâmetro *pBufferSize* receberá o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-118">If this parameter is **NULL**, the *pBufferSize* parameter receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ac0a-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ac0a-119">Return value</span></span>

<span data-ttu-id="3ac0a-120">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-120">Returns one of the following values.</span></span>



| <span data-ttu-id="3ac0a-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3ac0a-121">Return code</span></span>                                                                                           | <span data-ttu-id="3ac0a-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ac0a-122">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ac0a-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac0a-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="3ac0a-124">Os exemplos não estão sendo armazenados em buffer.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-124">Samples are not being buffered.</span></span> <span data-ttu-id="3ac0a-125">Chame [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span><span class="sxs-lookup"><span data-stu-id="3ac0a-125">Call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span></span><br/> |
| <dl> <span data-ttu-id="3ac0a-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac0a-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="3ac0a-127">O buffer especificado não é grande o suficiente.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-127">The specified buffer is not large enough.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="3ac0a-128"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac0a-128"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="3ac0a-129">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="3ac0a-129">**NULL** pointer argument.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="3ac0a-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac0a-130"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="3ac0a-131">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-131">Success.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="3ac0a-132"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac0a-132"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3ac0a-133">O filtro não está conectado.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-133">The filter is not connected.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="3ac0a-134"><dt>**VFW \_ E \_ estado incorreto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac0a-134"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="3ac0a-135">O filtro ainda não recebeu amostras.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-135">The filter has not received any samples yet.</span></span> <span data-ttu-id="3ac0a-136">Para entregar um exemplo, execute ou Pause o grafo.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-136">To deliver a sample, run or pause the graph.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="3ac0a-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ac0a-137">Remarks</span></span>

<span data-ttu-id="3ac0a-138">Para ativar o buffer, chame [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) com um valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-138">To activate buffering, call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with a value of **TRUE**.</span></span>

<span data-ttu-id="3ac0a-139">Chame esse método duas vezes.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-139">Call this method twice.</span></span> <span data-ttu-id="3ac0a-140">Na primeira chamada, defina *pBuffer* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-140">On the first call, set *pBuffer* to **NULL**.</span></span> <span data-ttu-id="3ac0a-141">O tamanho do buffer é retornado em *pBufferSize*.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-141">The size of the buffer is returned in *pBufferSize*.</span></span> <span data-ttu-id="3ac0a-142">Em seguida, aloque uma matriz e chame o método novamente.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-142">Then allocate an array and call the method again.</span></span> <span data-ttu-id="3ac0a-143">Na segunda chamada, passe o tamanho da matriz em *pBufferSize* e passe o endereço da matriz em *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-143">On the second call, pass the size of the array in *pBufferSize*, and pass the address of the array in *pBuffer*.</span></span> <span data-ttu-id="3ac0a-144">Se a matriz não for grande o suficiente, o método retornará E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-144">If the array is not large enough, the method returns E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="3ac0a-145">O parâmetro *pBuffer* é digitado como um ponteiro **longo** , mas o conteúdo do buffer depende do formato dos dados.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-145">The *pBuffer* parameter is typed as a **long** pointer, but the contents of the buffer depend on the format of the data.</span></span> <span data-ttu-id="3ac0a-146">Chame [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) para obter o tipo de mídia do formato.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-146">Call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) to get the media type of the format.</span></span>

<span data-ttu-id="3ac0a-147">Não chame esse método enquanto o grafo de filtro estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-147">Do not call this method while the filter graph is running.</span></span> <span data-ttu-id="3ac0a-148">Enquanto o grafo de filtro está em execução, o filtro de apoio de exemplo substitui o conteúdo do buffer sempre que recebe um novo exemplo.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-148">While the filter graph is running, the Sample Grabber filter overwrites the contents of the buffer whenever it receives a new sample.</span></span> <span data-ttu-id="3ac0a-149">A melhor maneira de usar esse método é usar o "modo One-shot", que interrompe o grafo depois de receber o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-149">The best way to use this method is to use "one-shot mode," which stops the graph after receiving the first sample.</span></span> <span data-ttu-id="3ac0a-150">Para definir o modo One-shot, chame [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md).</span><span class="sxs-lookup"><span data-stu-id="3ac0a-150">To set one-shot mode, call [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md).</span></span>

<span data-ttu-id="3ac0a-151">O filtro não armazena amostras de registro em buffer ou exemplos em que o membro **dwStreamId** da estrutura [**de \_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) é algo diferente da mídia de fluxo am \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3ac0a-151">The filter does not buffer preroll samples, or samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="3ac0a-152">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3ac0a-153">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ac0a-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3ac0a-154">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3ac0a-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3ac0a-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac0a-155">Requirements</span></span>



| <span data-ttu-id="3ac0a-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac0a-156">Requirement</span></span> | <span data-ttu-id="3ac0a-157">Valor</span><span class="sxs-lookup"><span data-stu-id="3ac0a-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac0a-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ac0a-158">Header</span></span><br/>  | <dl> <span data-ttu-id="3ac0a-159"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ac0a-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3ac0a-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ac0a-160">Library</span></span><br/> | <dl> <span data-ttu-id="3ac0a-161"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ac0a-161"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ac0a-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ac0a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac0a-163">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="3ac0a-163">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="3ac0a-164">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="3ac0a-164">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 





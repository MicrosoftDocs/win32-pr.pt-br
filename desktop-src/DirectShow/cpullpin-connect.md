---
description: O método Connect conclui uma conexão com o pino de saída.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: Método CPullPin. Connect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768650"
---
# <a name="cpullpinconnect-method"></a><span data-ttu-id="87a1a-103">Método CPullPin. Connect</span><span class="sxs-lookup"><span data-stu-id="87a1a-103">CPullPin.Connect method</span></span>

<span data-ttu-id="87a1a-104">O `Connect` método conclui uma conexão com o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="87a1a-104">The `Connect` method completes a connection to the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a1a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87a1a-105">Syntax</span></span>


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a><span data-ttu-id="87a1a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87a1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a1a-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="87a1a-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="87a1a-108">Ponteiro para a interface **IUnknown** do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="87a1a-108">Pointer to the **IUnknown** interface of the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="87a1a-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="87a1a-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="87a1a-110">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador preferencial do pino de entrada ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="87a1a-110">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87a1a-111">*bSync*</span><span class="sxs-lookup"><span data-stu-id="87a1a-111">*bSync*</span></span> 
</dt> <dd>

<span data-ttu-id="87a1a-112">Valor booliano que especifica se as leituras síncronas devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="87a1a-112">Boolean value that specifies whether to use synchronous reads.</span></span> <span data-ttu-id="87a1a-113">Se **for true**, o PIN executará operações de leitura síncronas no pino de saída.</span><span class="sxs-lookup"><span data-stu-id="87a1a-113">If **TRUE**, the pin performs synchronous read operations on the output pin.</span></span> <span data-ttu-id="87a1a-114">Se **for false**, o PIN fará solicitações de leitura assíncronas.</span><span class="sxs-lookup"><span data-stu-id="87a1a-114">If **FALSE**, the pin makes asynchronous read requests.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a1a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87a1a-115">Return value</span></span>

<span data-ttu-id="87a1a-116">Retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="87a1a-116">Returns an **HRESULT**.</span></span> <span data-ttu-id="87a1a-117">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="87a1a-117">Possible values include the following.</span></span>



| <span data-ttu-id="87a1a-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="87a1a-118">Return code</span></span>                                                                                               | <span data-ttu-id="87a1a-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="87a1a-119">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87a1a-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87a1a-120"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="87a1a-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="87a1a-121">Success.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="87a1a-122"><dt>**VFW \_ E \_ já \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="87a1a-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="87a1a-123">O pino de entrada já está conectado.</span><span class="sxs-lookup"><span data-stu-id="87a1a-123">The input pin is already connected.</span></span><br/>                                  |
| <dl> <span data-ttu-id="87a1a-124"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="87a1a-124"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="87a1a-125">O pino de saída não expõe [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span><span class="sxs-lookup"><span data-stu-id="87a1a-125">The output pin does not expose [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87a1a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="87a1a-126">Remarks</span></span>

<span data-ttu-id="87a1a-127">Chame esse método durante o processo de conexão do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="87a1a-127">Call this method during the input pin's connection process.</span></span> <span data-ttu-id="87a1a-128">Se o método falhar, o PIN deverá falhar na conexão.</span><span class="sxs-lookup"><span data-stu-id="87a1a-128">If the method fails, the pin should fail the connection.</span></span>

<span data-ttu-id="87a1a-129">Esse método consulta o pino de saída para a interface **IAsyncReader** .</span><span class="sxs-lookup"><span data-stu-id="87a1a-129">This method queries the output pin for the **IAsyncReader** interface.</span></span> <span data-ttu-id="87a1a-130">Se for bem-sucedido, ele chamará [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) para negociar o alocador para a conexão.</span><span class="sxs-lookup"><span data-stu-id="87a1a-130">If successful, it calls [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) to negotiate the allocator for the connection.</span></span> <span data-ttu-id="87a1a-131">Se o PIN de entrada tiver um alocador preferencial, especifique-o no parâmetro *pAlloc* ; o método **DecideAllocator** passa esse ponteiro para o método [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="87a1a-131">If your input pin has a preferred allocator, specify it in the *pAlloc* parameter; the **DecideAllocator** method passes this pointer to the output pin's [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method.</span></span> <span data-ttu-id="87a1a-132">Caso contrário, defina *pAlloc* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="87a1a-132">Otherwise, set *pAlloc* to **NULL**.</span></span>

<span data-ttu-id="87a1a-133">Se o valor de *bSync* for **true**, o objeto **CPullPin** fará solicitações de leitura síncronas chamando o [**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="87a1a-133">If the value of *bSync* is **TRUE**, the **CPullPin** object makes synchronous read requests, by calling the output pin's [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span> <span data-ttu-id="87a1a-134">Caso contrário, ele chama o método [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) para fazer solicitações de leitura sobrepostas.</span><span class="sxs-lookup"><span data-stu-id="87a1a-134">Otherwise, it calls the [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) method to make overlapping read requests.</span></span>

## <a name="requirements"></a><span data-ttu-id="87a1a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87a1a-135">Requirements</span></span>



| <span data-ttu-id="87a1a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="87a1a-136">Requirement</span></span> | <span data-ttu-id="87a1a-137">Valor</span><span class="sxs-lookup"><span data-stu-id="87a1a-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a1a-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87a1a-138">Header</span></span><br/>  | <dl> <span data-ttu-id="87a1a-139"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="87a1a-139"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="87a1a-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87a1a-140">Library</span></span><br/> | <dl> <span data-ttu-id="87a1a-141"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="87a1a-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87a1a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="87a1a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a1a-143">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="87a1a-143">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 





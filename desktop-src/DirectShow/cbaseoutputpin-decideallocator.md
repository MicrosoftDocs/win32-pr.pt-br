---
description: O método DecideAllocator seleciona um alocador de memória.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Método CBaseOutputPin. DecideAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751267"
---
# <a name="cbaseoutputpindecideallocator-method"></a><span data-ttu-id="98023-103">Método CBaseOutputPin. DecideAllocator</span><span class="sxs-lookup"><span data-stu-id="98023-103">CBaseOutputPin.DecideAllocator method</span></span>

<span data-ttu-id="98023-104">O `DecideAllocator` método seleciona um alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="98023-104">The `DecideAllocator` method selects a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="98023-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98023-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="98023-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98023-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98023-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="98023-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="98023-108">Ponteiro para a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="98023-108">Pointer to the input pin's [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="98023-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="98023-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="98023-110">Endereço de uma variável que recebe um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="98023-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98023-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98023-111">Return value</span></span>

<span data-ttu-id="98023-112">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="98023-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="98023-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="98023-113">Remarks</span></span>

<span data-ttu-id="98023-114">Esse método é chamado no final do processo de conexão do PIN.</span><span class="sxs-lookup"><span data-stu-id="98023-114">This method is called at the end of the pin connection process.</span></span> <span data-ttu-id="98023-115">Ele executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="98023-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="98023-116">Chama o método [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) para recuperar os requisitos de buffer do pino de entrada, se houver.</span><span class="sxs-lookup"><span data-stu-id="98023-116">Calls the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method to retrieve the input pin's buffer requirements, if any.</span></span>
2.  <span data-ttu-id="98023-117">Chama o método [**IMemInputPin:: Getalocador**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) para solicitar um alocador do PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="98023-117">Calls the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method to request an allocator from the input pin.</span></span> <span data-ttu-id="98023-118">Se o pino de entrada não fornecer um alocador, o pino de saída criará um chamando o método de classe [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="98023-118">If the input pin does not provide an allocator, the output pin creates one by calling the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) class method.</span></span>
3.  <span data-ttu-id="98023-119">Chama o método de classe [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , que define as propriedades do alocador.</span><span class="sxs-lookup"><span data-stu-id="98023-119">Calls the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) class method, which sets the allocator properties.</span></span> <span data-ttu-id="98023-120">Esse é um método virtual puro; a classe derivada deve implementá-la.</span><span class="sxs-lookup"><span data-stu-id="98023-120">This is a pure virtual method; the derived class must implement it.</span></span>
4.  <span data-ttu-id="98023-121">Chama o método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , que notifica o pino de entrada do alocador que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="98023-121">Calls the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method, which notifies the input pin of the allocator being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="98023-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98023-122">Requirements</span></span>



| <span data-ttu-id="98023-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="98023-123">Requirement</span></span> | <span data-ttu-id="98023-124">Valor</span><span class="sxs-lookup"><span data-stu-id="98023-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98023-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98023-125">Header</span></span><br/>  | <dl> <span data-ttu-id="98023-126"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98023-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="98023-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98023-127">Library</span></span><br/> | <dl> <span data-ttu-id="98023-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="98023-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98023-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="98023-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98023-130">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="98023-130">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





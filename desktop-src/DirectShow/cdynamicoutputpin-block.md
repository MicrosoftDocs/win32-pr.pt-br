---
description: 'O método Block bloqueia ou desbloqueia o fluxo de dados do PIN. Esse método implementa o método IPinFlowControl:: Block.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Método CDynamicOutputPin. Block (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756600"
---
# <a name="cdynamicoutputpinblock-method"></a><span data-ttu-id="721e9-104">Método CDynamicOutputPin. Block</span><span class="sxs-lookup"><span data-stu-id="721e9-104">CDynamicOutputPin.Block method</span></span>

<span data-ttu-id="721e9-105">O `Block` método bloqueia ou desbloqueia o fluxo de dados do PIN.</span><span class="sxs-lookup"><span data-stu-id="721e9-105">The `Block` method blocks or unblocks the flow of data from the pin.</span></span> <span data-ttu-id="721e9-106">Esse método implementa o método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) .</span><span class="sxs-lookup"><span data-stu-id="721e9-106">This method implements the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="721e9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="721e9-107">Syntax</span></span>


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="721e9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="721e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="721e9-109">*dwBlockFlags*</span><span class="sxs-lookup"><span data-stu-id="721e9-109">*dwBlockFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="721e9-110">Sinalizador que indica se deve bloquear ou desbloquear o PIN.</span><span class="sxs-lookup"><span data-stu-id="721e9-110">Flag that indicates whether to block or unblock the pin.</span></span> <span data-ttu-id="721e9-111">Deve ser um dos seguintes valores: </span><span class="sxs-lookup"><span data-stu-id="721e9-111">Must be one of the following values:</span></span>

<span data-ttu-id="721e9-112">Zero: desbloquear o fluxo de dados do PIN.</span><span class="sxs-lookup"><span data-stu-id="721e9-112">Zero: Unblock data flow from the pin.</span></span>

<span data-ttu-id="721e9-113">\_Bloco de \_ controle de fluxo am-PIN \_ \_ : bloqueia o fluxo de dados do PIN.</span><span class="sxs-lookup"><span data-stu-id="721e9-113">AM\_PIN\_FLOW\_CONTROL\_BLOCK: Block data flow from the pin.</span></span>

</dd> <dt>

<span data-ttu-id="721e9-114">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="721e9-114">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="721e9-115">Identificador para um objeto de evento ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="721e9-115">Handle to an event object, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="721e9-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="721e9-116">Return value</span></span>

<span data-ttu-id="721e9-117">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="721e9-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="721e9-118">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="721e9-118">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="721e9-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="721e9-119">Return code</span></span>                                                                                                                    | <span data-ttu-id="721e9-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="721e9-120">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="721e9-121"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="721e9-121"><dt>**S\_FALSE**</dt></span></span> </dl>                                        | <span data-ttu-id="721e9-122">O PIN já está desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="721e9-122">Pin is already unblocked.</span></span><br/>                     |
| <dl> <span data-ttu-id="721e9-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="721e9-123"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="721e9-124">Êxito.</span><span class="sxs-lookup"><span data-stu-id="721e9-124">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="721e9-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="721e9-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                   | <span data-ttu-id="721e9-126">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="721e9-126">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="721e9-127"><dt>**VFW \_ E \_ PIN \_ já \_ bloqueados**</dt></span><span class="sxs-lookup"><span data-stu-id="721e9-127"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="721e9-128">O PIN já está bloqueado em outro thread.</span><span class="sxs-lookup"><span data-stu-id="721e9-128">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="721e9-129"><dt>**VFW \_ E \_ PIN \_ já \_ bloqueados neste \_ \_ \_ thread**</dt></span><span class="sxs-lookup"><span data-stu-id="721e9-129"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="721e9-130">O PIN já está bloqueado no thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="721e9-130">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="721e9-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="721e9-131">Remarks</span></span>

<span data-ttu-id="721e9-132">Para obter mais informações sobre esse método, consulte [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span><span class="sxs-lookup"><span data-stu-id="721e9-132">For more information about this method, see [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span></span> <span data-ttu-id="721e9-133">Internamente, esse método chama um dos seguintes métodos protegidos:</span><span class="sxs-lookup"><span data-stu-id="721e9-133">Internally, this method calls one of the following protected methods:</span></span>

-   <span data-ttu-id="721e9-134">Bloquear (assíncrono): [ **CDynamicOutputPin:: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="721e9-134">Block (asynchronous): [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="721e9-135">Bloco (síncrono): [ **CDynamicOutputPin:: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="721e9-135">Block (synchronous): [**CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="721e9-136">Desbloquear: [ **CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="721e9-136">Unblock: [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span></span>

<span data-ttu-id="721e9-137">O desbloqueio é sempre executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="721e9-137">Unblocking is always performed synchronously.</span></span>

## <a name="requirements"></a><span data-ttu-id="721e9-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="721e9-138">Requirements</span></span>



| <span data-ttu-id="721e9-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="721e9-139">Requirement</span></span> | <span data-ttu-id="721e9-140">Valor</span><span class="sxs-lookup"><span data-stu-id="721e9-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="721e9-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="721e9-141">Header</span></span><br/>  | <dl> <span data-ttu-id="721e9-142"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="721e9-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="721e9-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="721e9-143">Library</span></span><br/> | <dl> <span data-ttu-id="721e9-144"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="721e9-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="721e9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="721e9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="721e9-146">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="721e9-146">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





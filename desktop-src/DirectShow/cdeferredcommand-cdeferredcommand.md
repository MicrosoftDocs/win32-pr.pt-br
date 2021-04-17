---
description: Método de construtor.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Construtor CDeferredCommand. CDeferredCommand (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e92a2ffc5129ee38fc5061b28ea7ffef49da0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754268"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a><span data-ttu-id="433a9-103">Construtor CDeferredCommand. CDeferredCommand</span><span class="sxs-lookup"><span data-stu-id="433a9-103">CDeferredCommand.CDeferredCommand constructor</span></span>

<span data-ttu-id="433a9-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="433a9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="433a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="433a9-105">Syntax</span></span>


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a><span data-ttu-id="433a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="433a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="433a9-107">*pQ*</span><span class="sxs-lookup"><span data-stu-id="433a9-107">*pQ*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-108">Ponteiro para um objeto que expõe a interface [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) .</span><span class="sxs-lookup"><span data-stu-id="433a9-108">Pointer to an object that exposes the [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) interface.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="433a9-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-110">Ponteiro para a interface **IUnknown** externa para agregação.</span><span class="sxs-lookup"><span data-stu-id="433a9-110">Pointer to the outer **IUnknown** interface for aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="433a9-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-112">Ponteiro para um valor **HRESULT** retornado.</span><span class="sxs-lookup"><span data-stu-id="433a9-112">Pointer to a returned **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-113">*pUnkExecutor*</span><span class="sxs-lookup"><span data-stu-id="433a9-113">*pUnkExecutor*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-114">Ponteiro para o objeto que executará esse comando.</span><span class="sxs-lookup"><span data-stu-id="433a9-114">Pointer to the object that will carry out this command.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-115">*time*</span><span class="sxs-lookup"><span data-stu-id="433a9-115">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-116">Hora em que o comando será executado.</span><span class="sxs-lookup"><span data-stu-id="433a9-116">Time at which the command will be run.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-117">*IID*</span><span class="sxs-lookup"><span data-stu-id="433a9-117">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-118">Ponteiro para o identificador global exclusivo (**GUID**) da interface que contém o método.</span><span class="sxs-lookup"><span data-stu-id="433a9-118">Pointer to the globally unique identifier (**GUID**) of the interface that contains the method.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-119">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="433a9-119">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-120">Método na interface a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="433a9-120">Method on the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-121">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="433a9-121">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-122">Contexto da invocação.</span><span class="sxs-lookup"><span data-stu-id="433a9-122">Context of the invocation.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-123">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="433a9-123">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-124">Número de argumentos passados.</span><span class="sxs-lookup"><span data-stu-id="433a9-124">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-125">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="433a9-125">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-126">Ponteiro para uma lista de tipos de variante de argumento.</span><span class="sxs-lookup"><span data-stu-id="433a9-126">Pointer to a list of argument variant types.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-127">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="433a9-127">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-128">Ponteiro para uma lista de tipo Variant retornada, se houver.</span><span class="sxs-lookup"><span data-stu-id="433a9-128">Pointer to a returned variant type list, if any.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-129">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="433a9-129">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-130">Ponteiro para o último argumento na lista de parâmetros *pDispParams* com um erro.</span><span class="sxs-lookup"><span data-stu-id="433a9-130">Pointer to the last argument in the *pDispParams* parameter list with an error.</span></span>

</dd> <dt>

<span data-ttu-id="433a9-131">*bStream*</span><span class="sxs-lookup"><span data-stu-id="433a9-131">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="433a9-132">Valor que indica se o tempo de comando adiado está em tempo de fluxo (**true**) ou tempo de apresentação (**false**).</span><span class="sxs-lookup"><span data-stu-id="433a9-132">Value indicating whether the deferred command time is in stream time (**TRUE**) or presentation time (**FALSE**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="433a9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="433a9-133">Requirements</span></span>



| <span data-ttu-id="433a9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="433a9-134">Requirement</span></span> | <span data-ttu-id="433a9-135">Valor</span><span class="sxs-lookup"><span data-stu-id="433a9-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="433a9-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="433a9-136">Header</span></span><br/>  | <dl> <span data-ttu-id="433a9-137"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="433a9-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="433a9-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="433a9-138">Library</span></span><br/> | <dl> <span data-ttu-id="433a9-139"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="433a9-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="433a9-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="433a9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433a9-141">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="433a9-141">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 





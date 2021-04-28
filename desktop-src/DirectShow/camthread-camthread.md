---
description: Construtor de CAMThread. CAMThread-método de construtor.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Construtor CAMThread. CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096404"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="d09fc-103">Construtor CAMThread. CAMThread</span><span class="sxs-lookup"><span data-stu-id="d09fc-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="d09fc-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="d09fc-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09fc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d09fc-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="d09fc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d09fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d09fc-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="d09fc-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d09fc-108">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d09fc-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="d09fc-109">Se o Construtor falhar, esse parâmetro receberá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="d09fc-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="d09fc-110">Se isso ocorrer, o objeto não está em um estado válido.</span><span class="sxs-lookup"><span data-stu-id="d09fc-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="d09fc-111">Para compatibilidade com versões anteriores do Strmbase. lib, esse parâmetro assume **nulo** como padrão.</span><span class="sxs-lookup"><span data-stu-id="d09fc-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="d09fc-112">No entanto, a passagem de um valor não **nulo** é preferida, para que o chamador possa verificar o status do objeto.</span><span class="sxs-lookup"><span data-stu-id="d09fc-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d09fc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d09fc-113">Remarks</span></span>

<span data-ttu-id="d09fc-114">O método de construtor não cria o thread.</span><span class="sxs-lookup"><span data-stu-id="d09fc-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="d09fc-115">Para criar o thread, chame o método [**CAMThread:: Create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="d09fc-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d09fc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d09fc-116">Requirements</span></span>



| <span data-ttu-id="d09fc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d09fc-117">Requirement</span></span> | <span data-ttu-id="d09fc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d09fc-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d09fc-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d09fc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d09fc-120"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d09fc-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d09fc-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d09fc-121">Library</span></span><br/> | <dl> <span data-ttu-id="d09fc-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d09fc-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09fc-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d09fc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09fc-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="d09fc-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 





---
description: Método de construtor.
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
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756001"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="9ddf7-103">Construtor CAMThread. CAMThread</span><span class="sxs-lookup"><span data-stu-id="9ddf7-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="9ddf7-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ddf7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ddf7-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="9ddf7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ddf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ddf7-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="9ddf7-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="9ddf7-108">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ddf7-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="9ddf7-109">Se o Construtor falhar, esse parâmetro receberá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="9ddf7-110">Se isso ocorrer, o objeto não está em um estado válido.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="9ddf7-111">Para compatibilidade com versões anteriores do Strmbase. lib, esse parâmetro assume **nulo** como padrão.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="9ddf7-112">No entanto, a passagem de um valor não **nulo** é preferida, para que o chamador possa verificar o status do objeto.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ddf7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ddf7-113">Remarks</span></span>

<span data-ttu-id="9ddf7-114">O método de construtor não cria o thread.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="9ddf7-115">Para criar o thread, chame o método [**CAMThread:: Create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="9ddf7-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ddf7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ddf7-116">Requirements</span></span>



| <span data-ttu-id="9ddf7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ddf7-117">Requirement</span></span> | <span data-ttu-id="9ddf7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9ddf7-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ddf7-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ddf7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9ddf7-120"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ddf7-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9ddf7-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ddf7-121">Library</span></span><br/> | <dl> <span data-ttu-id="9ddf7-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9ddf7-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ddf7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ddf7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ddf7-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="9ddf7-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 





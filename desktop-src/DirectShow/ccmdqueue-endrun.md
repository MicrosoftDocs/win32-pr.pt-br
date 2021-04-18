---
description: O método EndRun alterna para o modo parado ou pausado.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Método CCmdQueue. EndRun (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755598"
---
# <a name="ccmdqueueendrun-method"></a><span data-ttu-id="0ef60-103">Método CCmdQueue. EndRun</span><span class="sxs-lookup"><span data-stu-id="0ef60-103">CCmdQueue.EndRun method</span></span>

<span data-ttu-id="0ef60-104">O `EndRun` método alterna para o modo parado ou pausado.</span><span class="sxs-lookup"><span data-stu-id="0ef60-104">The `EndRun` method switches to the stopped or paused mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef60-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ef60-105">Syntax</span></span>


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a><span data-ttu-id="0ef60-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ef60-106">Parameters</span></span>

<span data-ttu-id="0ef60-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0ef60-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ef60-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ef60-108">Return value</span></span>

<span data-ttu-id="0ef60-109">Retorna um valor **HRESULT** que depende da implementação.</span><span class="sxs-lookup"><span data-stu-id="0ef60-109">Returns an **HRESULT** value that depends on the implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef60-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ef60-110">Remarks</span></span>

<span data-ttu-id="0ef60-111">O mapeamento de tempo entre a hora do fluxo e o tempo de apresentação não é conhecido depois que essa função de membro é chamada.</span><span class="sxs-lookup"><span data-stu-id="0ef60-111">Time mapping between stream time and presentation time is not known after this member function has been called.</span></span> <span data-ttu-id="0ef60-112">Chame a função de membro [**CCmdQueue:: Run**](ccmdqueue-run.md) para executar esse mapeamento.</span><span class="sxs-lookup"><span data-stu-id="0ef60-112">Call the [**CCmdQueue::Run**](ccmdqueue-run.md) member function to carry out this mapping.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef60-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ef60-113">Requirements</span></span>



| <span data-ttu-id="0ef60-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ef60-114">Requirement</span></span> | <span data-ttu-id="0ef60-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0ef60-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef60-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ef60-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef60-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef60-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ef60-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ef60-118">Library</span></span><br/> | <dl> <span data-ttu-id="0ef60-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef60-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef60-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ef60-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef60-121">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="0ef60-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 





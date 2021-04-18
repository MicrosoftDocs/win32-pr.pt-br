---
description: O método GetDueCommand recupera um ponteiro para o próximo comando que é devido.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Método CCmdQueue. GetDueCommand (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751253"
---
# <a name="ccmdqueuegetduecommand-method"></a><span data-ttu-id="a7d5d-103">Método CCmdQueue. GetDueCommand</span><span class="sxs-lookup"><span data-stu-id="a7d5d-103">CCmdQueue.GetDueCommand method</span></span>

<span data-ttu-id="a7d5d-104">O `GetDueCommand` método recupera um ponteiro para o próximo comando que está vencido.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-104">The `GetDueCommand` method retrieves a pointer to the next command that is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7d5d-105">Syntax</span></span>


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="a7d5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7d5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d5d-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="a7d5d-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d5d-108">Endereço de um ponteiro para o comando adiado.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-108">Address of a pointer to the deferred command.</span></span>

</dd> <dt>

<span data-ttu-id="a7d5d-109">*msTimeout*</span><span class="sxs-lookup"><span data-stu-id="a7d5d-109">*msTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d5d-110">Tempo de espera antes da realização do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-110">Amount of time to wait before carrying out the time-out.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d5d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7d5d-111">Return value</span></span>

<span data-ttu-id="a7d5d-112">Retorna E \_ anula se ocorrer um tempo limite.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-112">Returns E\_ABORT if a time-out occurs.</span></span> <span data-ttu-id="a7d5d-113">Retornará S \_ OK se for bem-sucedido; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-113">Returns S\_OK if successful; otherwise, returns an error.</span></span> <span data-ttu-id="a7d5d-114">Retorna um objeto que foi incrementado usando **IUnknown:: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-114">Returns an object that has been incremented using **IUnknown::AddRef**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7d5d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7d5d-115">Remarks</span></span>

<span data-ttu-id="a7d5d-116">Essa função de membro é bloqueada até que um comando pendente seja devido.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-116">This member function blocks until a pending command is due.</span></span> <span data-ttu-id="a7d5d-117">A função de membro é bloqueada para o período de tempo, em milissegundos, especificado no parâmetro *msTimeout* .</span><span class="sxs-lookup"><span data-stu-id="a7d5d-117">The member function blocks for the amount of time, in milliseconds, specified in the *msTimeout* parameter.</span></span> <span data-ttu-id="a7d5d-118">Os comandos de tempo de transmissão se tornam devido somente às funções de membro [**CCmdQueue:: Run**](ccmdqueue-run.md) e [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) .</span><span class="sxs-lookup"><span data-stu-id="a7d5d-118">Stream-time commands become due only between the [**CCmdQueue::Run**](ccmdqueue-run.md) and [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) member functions.</span></span> <span data-ttu-id="a7d5d-119">O comando permanece na fila até ser executado ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-119">The command remains queued until run or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d5d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7d5d-120">Requirements</span></span>



| <span data-ttu-id="a7d5d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d5d-121">Requirement</span></span> | <span data-ttu-id="a7d5d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a7d5d-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d5d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7d5d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a7d5d-124"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d5d-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7d5d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7d5d-125">Library</span></span><br/> | <dl> <span data-ttu-id="a7d5d-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d5d-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7d5d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7d5d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d5d-128">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="a7d5d-128">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 





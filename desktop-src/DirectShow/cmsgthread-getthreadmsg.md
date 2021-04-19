---
description: Recupera um objeto CMsg enfileirado que contém uma solicitação.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Método CMsgThread. GetThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770092"
---
# <a name="cmsgthreadgetthreadmsg-method"></a><span data-ttu-id="9e159-103">Método CMsgThread. GetThreadMsg</span><span class="sxs-lookup"><span data-stu-id="9e159-103">CMsgThread.GetThreadMsg method</span></span>

<span data-ttu-id="9e159-104">Recupera um objeto [**CMsg**](cmsg.md) enfileirado que contém uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9e159-104">Retrieves a queued [**CMsg**](cmsg.md) object containing a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e159-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e159-105">Syntax</span></span>


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a><span data-ttu-id="9e159-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e159-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e159-107">*msg*</span><span class="sxs-lookup"><span data-stu-id="9e159-107">*msg*</span></span> 
</dt> <dd>

<span data-ttu-id="9e159-108">Ponteiro para um objeto [**CMsg**](cmsg.md) alocado.</span><span class="sxs-lookup"><span data-stu-id="9e159-108">Pointer to an allocated [**CMsg**](cmsg.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e159-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e159-109">Return value</span></span>

<span data-ttu-id="9e159-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9e159-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e159-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e159-111">Remarks</span></span>

<span data-ttu-id="9e159-112">Essa função de membro é chamada da função [**ThreadProc**](camthread-threadproc.md) privada do thread de trabalho para recuperar a próxima função de membro.</span><span class="sxs-lookup"><span data-stu-id="9e159-112">This member function is called from the worker thread's private [**ThreadProc**](camthread-threadproc.md) function to retrieve the next member function.</span></span> <span data-ttu-id="9e159-113">O parâmetro *msg* deve apontar para um objeto [**CMsg**](cmsg.md) alocado que será preenchido com os parâmetros para a próxima solicitação na fila.</span><span class="sxs-lookup"><span data-stu-id="9e159-113">The *msg* parameter should point to an allocated [**CMsg**](cmsg.md) object that will be filled with the parameters to the next request in the queue.</span></span> <span data-ttu-id="9e159-114">Se não houver nenhuma solicitação em fila, essa função de membro será bloqueada até que a próxima solicitação seja enfileirada (por uma chamada para a função de membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ).</span><span class="sxs-lookup"><span data-stu-id="9e159-114">If there are no queued requests, this member function blocks until the next request is queued (by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e159-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e159-115">Requirements</span></span>



| <span data-ttu-id="9e159-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e159-116">Requirement</span></span> | <span data-ttu-id="9e159-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9e159-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e159-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e159-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9e159-119"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e159-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9e159-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e159-120">Library</span></span><br/> | <dl> <span data-ttu-id="9e159-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9e159-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e159-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e159-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e159-123">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="9e159-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 





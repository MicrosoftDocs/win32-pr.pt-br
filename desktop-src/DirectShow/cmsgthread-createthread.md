---
description: Cria um thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Método CMsgThread. CreateThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749248"
---
# <a name="cmsgthreadcreatethread-method"></a><span data-ttu-id="8c402-103">Método CMsgThread. CreateThread</span><span class="sxs-lookup"><span data-stu-id="8c402-103">CMsgThread.CreateThread method</span></span>

<span data-ttu-id="8c402-104">Cria um thread.</span><span class="sxs-lookup"><span data-stu-id="8c402-104">Creates a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c402-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c402-105">Syntax</span></span>


```C++
BOOL CreateThread();
```



## <a name="parameters"></a><span data-ttu-id="8c402-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c402-106">Parameters</span></span>

<span data-ttu-id="8c402-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8c402-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c402-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c402-108">Return value</span></span>

<span data-ttu-id="8c402-109">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c402-109">Returns one of the following values.</span></span>



| <span data-ttu-id="8c402-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8c402-110">Return code</span></span>                                                                              | <span data-ttu-id="8c402-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c402-111">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="8c402-112"><dt>VERDADEIRO \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8c402-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="8c402-113">O thread foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="8c402-113">Thread was successfully created.</span></span><br/>     |
| <dl> <span data-ttu-id="8c402-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8c402-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="8c402-115">O thread não foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="8c402-115">Thread was not successfully created.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8c402-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c402-116">Remarks</span></span>

<span data-ttu-id="8c402-117">O thread fará um loop, bloqueando até que uma solicitação seja enfileirada (por meio da função de membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) e, em seguida, chamando a função de membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) com cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="8c402-117">The thread will loop, blocking until a request is queued (through the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then calling the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function with each message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c402-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c402-118">Requirements</span></span>



| <span data-ttu-id="8c402-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c402-119">Requirement</span></span> | <span data-ttu-id="8c402-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8c402-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c402-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c402-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8c402-122"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c402-122"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c402-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c402-123">Library</span></span><br/> | <dl> <span data-ttu-id="8c402-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8c402-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c402-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c402-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c402-126">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="8c402-126">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 





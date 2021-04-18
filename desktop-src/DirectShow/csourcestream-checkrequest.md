---
description: O método CheckRequest verifica se há uma solicitação de thread, sem bloqueio.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Método CSourceStream. CheckRequest (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768795"
---
# <a name="csourcestreamcheckrequest-method"></a><span data-ttu-id="d8cf1-103">Método CSourceStream. CheckRequest</span><span class="sxs-lookup"><span data-stu-id="d8cf1-103">CSourceStream.CheckRequest method</span></span>

<span data-ttu-id="d8cf1-104">O `CheckRequest` método verifica se há uma solicitação de thread, sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="d8cf1-104">The `CheckRequest` method checks if there is a thread request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8cf1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8cf1-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a><span data-ttu-id="d8cf1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8cf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8cf1-107">*pCom*</span><span class="sxs-lookup"><span data-stu-id="d8cf1-107">*pCom*</span></span> 
</dt> <dd>

<span data-ttu-id="d8cf1-108">Ponteiro para uma variável que recebe o valor passado na última chamada para o método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="d8cf1-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8cf1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8cf1-109">Return value</span></span>

<span data-ttu-id="d8cf1-110">Retorna **true** se houver uma solicitação pendente ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d8cf1-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8cf1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8cf1-111">Remarks</span></span>

<span data-ttu-id="d8cf1-112">Esse método substitui o método [**CAMThread:: CheckRequest**](camthread-checkrequest.md) para executar a verificação de tipo.</span><span class="sxs-lookup"><span data-stu-id="d8cf1-112">This method overrides the [**CAMThread::CheckRequest**](camthread-checkrequest.md) method to perform type-checking.</span></span> <span data-ttu-id="d8cf1-113">A classe **CSourceStream** define o seguinte tipo enumerado para o parâmetro *Pcom* :</span><span class="sxs-lookup"><span data-stu-id="d8cf1-113">The **CSourceStream** class defines the following enumerated type for the *pCom* parameter:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="d8cf1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8cf1-114">Requirements</span></span>



| <span data-ttu-id="d8cf1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8cf1-115">Requirement</span></span> | <span data-ttu-id="d8cf1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d8cf1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8cf1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8cf1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d8cf1-118"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8cf1-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d8cf1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8cf1-119">Library</span></span><br/> | <dl> <span data-ttu-id="d8cf1-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d8cf1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8cf1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8cf1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8cf1-122">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="d8cf1-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





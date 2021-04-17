---
description: O método Run alterna para o modo de execução para que os comandos adiados pelo tempo do fluxo possam ser executados.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Método CCmdQueue. Run (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758698"
---
# <a name="ccmdqueuerun-method"></a><span data-ttu-id="bf9b2-103">Método CCmdQueue. Run</span><span class="sxs-lookup"><span data-stu-id="bf9b2-103">CCmdQueue.Run method</span></span>

<span data-ttu-id="bf9b2-104">O `Run` método alterna para o modo de execução para que os comandos adiados pelo tempo do fluxo possam ser executados.</span><span class="sxs-lookup"><span data-stu-id="bf9b2-104">The `Run` method switches to running mode so that commands that are deferred by the stream time can be run.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf9b2-105">Syntax</span></span>


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a><span data-ttu-id="bf9b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf9b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf9b2-107">*tStreamTimeOffset*</span><span class="sxs-lookup"><span data-stu-id="bf9b2-107">*tStreamTimeOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="bf9b2-108">Tempo de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="bf9b2-108">Offset time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf9b2-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf9b2-109">Return value</span></span>

<span data-ttu-id="bf9b2-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bf9b2-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf9b2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf9b2-111">Remarks</span></span>

<span data-ttu-id="bf9b2-112">Durante o modo de execução, o mapeamento de tempo para apresentação do fluxo é conhecido.</span><span class="sxs-lookup"><span data-stu-id="bf9b2-112">During running mode, stream-time-to-presentation-time mapping is known.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf9b2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf9b2-113">Requirements</span></span>



| <span data-ttu-id="bf9b2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf9b2-114">Requirement</span></span> | <span data-ttu-id="bf9b2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bf9b2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9b2-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf9b2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bf9b2-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf9b2-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf9b2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf9b2-118">Library</span></span><br/> | <dl> <span data-ttu-id="bf9b2-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bf9b2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf9b2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf9b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf9b2-121">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="bf9b2-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 





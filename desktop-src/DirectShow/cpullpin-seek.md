---
description: O método Seek define as posições de início e parada do fluxo.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Método CPullPin. Seek (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754147"
---
# <a name="cpullpinseek-method"></a><span data-ttu-id="cfa86-103">Método CPullPin. Seek</span><span class="sxs-lookup"><span data-stu-id="cfa86-103">CPullPin.Seek method</span></span>

<span data-ttu-id="cfa86-104">O `Seek` método define as posições de início e parada do fluxo.</span><span class="sxs-lookup"><span data-stu-id="cfa86-104">The `Seek` method sets the start and stop positions of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa86-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfa86-105">Syntax</span></span>


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a><span data-ttu-id="cfa86-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfa86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa86-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="cfa86-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="cfa86-108">Especifica a posição inicial, em bytes multiplicada por 10 milhões.</span><span class="sxs-lookup"><span data-stu-id="cfa86-108">Specifies the start position, in bytes multiplied by 10,000,000.</span></span>

</dd> <dt>

<span data-ttu-id="cfa86-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="cfa86-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="cfa86-110">Especifica a posição de parada, em bytes multiplicada por 10 milhões.</span><span class="sxs-lookup"><span data-stu-id="cfa86-110">Specifies the stop position, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa86-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfa86-111">Return value</span></span>

<span data-ttu-id="cfa86-112">Retorna S \_ OK se o método for bem sucedido ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="cfa86-112">Returns S\_OK if the method succeeds, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa86-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfa86-113">Remarks</span></span>

<span data-ttu-id="cfa86-114">Se o thread de trabalho estiver em execução, o método pausará o thread, liberará o gráfico de filtro e retomará o thread.</span><span class="sxs-lookup"><span data-stu-id="cfa86-114">If the worker thread is running, the method pauses the thread, flushes the filter graph, and resumes the thread.</span></span> <span data-ttu-id="cfa86-115">O thread começa a extrair dados da nova posição inicial.</span><span class="sxs-lookup"><span data-stu-id="cfa86-115">The thread begins pulling data from the new start position.</span></span> <span data-ttu-id="cfa86-116">Caso contrário, os novos valores de posição entram em vigor sempre que o thread for iniciado.</span><span class="sxs-lookup"><span data-stu-id="cfa86-116">Otherwise, the new position values become effective whenever the thread is started.</span></span>

<span data-ttu-id="cfa86-117">As posições são relativas ao início da fonte original.</span><span class="sxs-lookup"><span data-stu-id="cfa86-117">Positions are relative to the start of the original source.</span></span> <span data-ttu-id="cfa86-118">Multiplique os deslocamentos de bytes desejados pelas unidades constantes, que são definidas na biblioteca de classes base como 10 milhões.</span><span class="sxs-lookup"><span data-stu-id="cfa86-118">Multiply the desired byte offsets by the constant UNITS, which is defined in the base class library as 10,000,000.</span></span>

<span data-ttu-id="cfa86-119">Quando o PIN se conecta pela primeira vez, as posições de parar e iniciar padrão para o início e o fim do fluxo.</span><span class="sxs-lookup"><span data-stu-id="cfa86-119">When the pin first connects, the stop and start positions default to the beginning and end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa86-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfa86-120">Requirements</span></span>



| <span data-ttu-id="cfa86-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfa86-121">Requirement</span></span> | <span data-ttu-id="cfa86-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cfa86-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa86-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfa86-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cfa86-124"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfa86-124"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="cfa86-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cfa86-125">Library</span></span><br/> | <dl> <span data-ttu-id="cfa86-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cfa86-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa86-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfa86-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa86-128">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="cfa86-128">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 





---
description: O método SetTimeAdvise configura um evento de temporizador com o relógio de referência.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Método CCmdQueue. SetTimeAdvise (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768667"
---
# <a name="ccmdqueuesettimeadvise-method"></a><span data-ttu-id="2c42e-103">Método CCmdQueue. SetTimeAdvise</span><span class="sxs-lookup"><span data-stu-id="2c42e-103">CCmdQueue.SetTimeAdvise method</span></span>

<span data-ttu-id="2c42e-104">O `SetTimeAdvise` método configura um evento de temporizador com o relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="2c42e-104">The `SetTimeAdvise` method sets up a timer event with the reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c42e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c42e-105">Syntax</span></span>


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a><span data-ttu-id="2c42e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c42e-106">Parameters</span></span>

<span data-ttu-id="2c42e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2c42e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c42e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c42e-108">Return value</span></span>

<span data-ttu-id="2c42e-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2c42e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c42e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c42e-110">Remarks</span></span>

<span data-ttu-id="2c42e-111">Essa função de membro chama o método [**IReferenceClock:: aconselhetime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para configurar uma notificação para a hora mais antiga necessária na fila.</span><span class="sxs-lookup"><span data-stu-id="2c42e-111">This member function calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method to set up a notification for the earliest time required in the queue.</span></span> <span data-ttu-id="2c42e-112">Os comandos de tempo de apresentação que são adiados sempre são verificados.</span><span class="sxs-lookup"><span data-stu-id="2c42e-112">Presentation-time commands that are deferred are always checked.</span></span> <span data-ttu-id="2c42e-113">Se o gráfico de filtro estiver no modo de execução, os comandos adiados usando o tempo de transmissão também serão verificados.</span><span class="sxs-lookup"><span data-stu-id="2c42e-113">If the filter graph is in running mode, deferred commands using stream time are also checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c42e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c42e-114">Requirements</span></span>



| <span data-ttu-id="2c42e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c42e-115">Requirement</span></span> | <span data-ttu-id="2c42e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2c42e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c42e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c42e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2c42e-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c42e-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2c42e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c42e-119">Library</span></span><br/> | <dl> <span data-ttu-id="2c42e-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2c42e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c42e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c42e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c42e-122">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="2c42e-122">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 





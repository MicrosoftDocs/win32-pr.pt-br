---
description: O método de redefinição redefine o objeto para que ele possa receber mais dados.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Método COutputQueue. Reset (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754259"
---
# <a name="coutputqueuereset-method"></a><span data-ttu-id="5afa2-103">Método COutputQueue. Reset</span><span class="sxs-lookup"><span data-stu-id="5afa2-103">COutputQueue.Reset method</span></span>

<span data-ttu-id="5afa2-104">O `Reset` método redefine o objeto para que ele possa receber mais dados.</span><span class="sxs-lookup"><span data-stu-id="5afa2-104">The `Reset` method resets the object so that it can receive more data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5afa2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5afa2-105">Syntax</span></span>


```C++
void Reset();
```



## <a name="parameters"></a><span data-ttu-id="5afa2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5afa2-106">Parameters</span></span>

<span data-ttu-id="5afa2-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5afa2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5afa2-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5afa2-108">Return value</span></span>

<span data-ttu-id="5afa2-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5afa2-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5afa2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5afa2-110">Remarks</span></span>

<span data-ttu-id="5afa2-111">Esse método redefine a variável de membro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) para S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5afa2-111">This method resets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_OK.</span></span> <span data-ttu-id="5afa2-112">O objeto pode receber amostras de mídia novamente; por exemplo, após uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="5afa2-112">The object can receive media samples again; for example, after a flush operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5afa2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5afa2-113">Requirements</span></span>



| <span data-ttu-id="5afa2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5afa2-114">Requirement</span></span> | <span data-ttu-id="5afa2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5afa2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5afa2-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5afa2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5afa2-117"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5afa2-117"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5afa2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5afa2-118">Library</span></span><br/> | <dl> <span data-ttu-id="5afa2-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5afa2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5afa2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5afa2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5afa2-121">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="5afa2-121">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





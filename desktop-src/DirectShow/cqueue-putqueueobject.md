---
description: Coloca um item na fila.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Método CQueue. PutQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770278"
---
# <a name="cqueueputqueueobject-method"></a><span data-ttu-id="792f0-103">Método CQueue. PutQueueObject</span><span class="sxs-lookup"><span data-stu-id="792f0-103">CQueue.PutQueueObject method</span></span>

<span data-ttu-id="792f0-104">Coloca um item na fila.</span><span class="sxs-lookup"><span data-stu-id="792f0-104">Puts an item onto the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="792f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="792f0-105">Syntax</span></span>


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a><span data-ttu-id="792f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="792f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="792f0-107">*object*</span><span class="sxs-lookup"><span data-stu-id="792f0-107">*object*</span></span> 
</dt> <dd>

<span data-ttu-id="792f0-108">Objeto do tipo **T** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="792f0-108">Object of type **T** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="792f0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="792f0-109">Return value</span></span>

<span data-ttu-id="792f0-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="792f0-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="792f0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="792f0-111">Remarks</span></span>

<span data-ttu-id="792f0-112">Esse método é bloqueado até que haja espaço na fila para o item.</span><span class="sxs-lookup"><span data-stu-id="792f0-112">This method blocks until there is space in the queue for the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="792f0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="792f0-113">Requirements</span></span>



| <span data-ttu-id="792f0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="792f0-114">Requirement</span></span> | <span data-ttu-id="792f0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="792f0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="792f0-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="792f0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="792f0-117"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="792f0-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="792f0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="792f0-118">Library</span></span><br/> | <dl> <span data-ttu-id="792f0-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="792f0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="792f0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="792f0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792f0-121">**Classe CQueue**</span><span class="sxs-lookup"><span data-stu-id="792f0-121">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 





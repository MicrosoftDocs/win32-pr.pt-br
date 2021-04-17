---
description: O método remove remove o objeto CDeferredCommand da fila.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Método CCmdQueue. Remove (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748207"
---
# <a name="ccmdqueueremove-method"></a><span data-ttu-id="c73c5-103">Método CCmdQueue. Remove</span><span class="sxs-lookup"><span data-stu-id="c73c5-103">CCmdQueue.Remove method</span></span>

<span data-ttu-id="c73c5-104">O `Remove` método remove o objeto [**CDeferredCommand**](cdeferredcommand.md) da fila.</span><span class="sxs-lookup"><span data-stu-id="c73c5-104">The `Remove` method removes the [**CDeferredCommand**](cdeferredcommand.md) object from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="c73c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c73c5-105">Syntax</span></span>


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="c73c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c73c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c73c5-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="c73c5-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="c73c5-108">Ponteiro para o objeto **CDeferredCommand** a ser removido da fila.</span><span class="sxs-lookup"><span data-stu-id="c73c5-108">Pointer to the **CDeferredCommand** object to remove from the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c73c5-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c73c5-109">Return value</span></span>

<span data-ttu-id="c73c5-110">Retorna VFW \_ E \_ não \_ encontrado se o objeto não for encontrado na fila.</span><span class="sxs-lookup"><span data-stu-id="c73c5-110">Returns VFW\_E\_NOT\_FOUND if the object is not found in the queue.</span></span> <span data-ttu-id="c73c5-111">Caso contrário, retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c73c5-111">Otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="c73c5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c73c5-112">Requirements</span></span>



| <span data-ttu-id="c73c5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c73c5-113">Requirement</span></span> | <span data-ttu-id="c73c5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c73c5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c73c5-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c73c5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c73c5-116"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c73c5-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c73c5-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c73c5-117">Library</span></span><br/> | <dl> <span data-ttu-id="c73c5-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c73c5-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c73c5-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c73c5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c73c5-120">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="c73c5-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 





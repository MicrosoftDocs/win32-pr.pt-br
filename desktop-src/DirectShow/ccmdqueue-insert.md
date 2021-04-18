---
description: O método Insert adiciona um objeto CDeferredCommand à fila.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Método CCmdQueue. Insert (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749023"
---
# <a name="ccmdqueueinsert-method"></a><span data-ttu-id="4cae1-103">Método CCmdQueue. Insert</span><span class="sxs-lookup"><span data-stu-id="4cae1-103">CCmdQueue.Insert method</span></span>

<span data-ttu-id="4cae1-104">O `Insert` método adiciona um objeto [**CDeferredCommand**](cdeferredcommand.md) à fila.</span><span class="sxs-lookup"><span data-stu-id="4cae1-104">The `Insert` method adds a [**CDeferredCommand**](cdeferredcommand.md) object to the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cae1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cae1-105">Syntax</span></span>


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="4cae1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cae1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cae1-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="4cae1-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-108">Ponteiro para o objeto **CDeferredCommand** a ser adicionado à fila.</span><span class="sxs-lookup"><span data-stu-id="4cae1-108">Pointer to the **CDeferredCommand** object to add to the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cae1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4cae1-109">Return value</span></span>

<span data-ttu-id="4cae1-110">Retorna S \_ OK na implementação padrão.</span><span class="sxs-lookup"><span data-stu-id="4cae1-110">Returns S\_OK in the default implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cae1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cae1-111">Requirements</span></span>



| <span data-ttu-id="4cae1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cae1-112">Requirement</span></span> | <span data-ttu-id="4cae1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4cae1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cae1-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cae1-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4cae1-115"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cae1-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4cae1-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4cae1-116">Library</span></span><br/> | <dl> <span data-ttu-id="4cae1-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4cae1-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cae1-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cae1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cae1-119">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="4cae1-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 





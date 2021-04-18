---
description: O método addantes insere uma lista antes da posição especificada.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Método CBaseList. AddBefore (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751913"
---
# <a name="cbaselistaddbefore-method"></a><span data-ttu-id="a794a-103">Método CBaseList. AddBefore</span><span class="sxs-lookup"><span data-stu-id="a794a-103">CBaseList.AddBefore method</span></span>

<span data-ttu-id="a794a-104">O `AddBefore` método insere uma lista antes da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="a794a-104">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="a794a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a794a-105">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="a794a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a794a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a794a-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="a794a-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="a794a-108">Posição antes da qual inserir a lista.</span><span class="sxs-lookup"><span data-stu-id="a794a-108">Position before which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="a794a-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="a794a-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="a794a-110">Ponteiro para a lista a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="a794a-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a794a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a794a-111">Return value</span></span>

<span data-ttu-id="a794a-112">Retornará **true** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a794a-112">Returns **TRUE** if successful.</span></span> <span data-ttu-id="a794a-113">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="a794a-113">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a794a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a794a-114">Remarks</span></span>

<span data-ttu-id="a794a-115">Os indicadores de posição existentes, incluindo aquele especificado no parâmetro *pos* , permanecem válidos.</span><span class="sxs-lookup"><span data-stu-id="a794a-115">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="a794a-116">Se o método falhar, alguns dos itens podem ter sido adicionados.</span><span class="sxs-lookup"><span data-stu-id="a794a-116">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="a794a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a794a-117">Requirements</span></span>



| <span data-ttu-id="a794a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a794a-118">Requirement</span></span> | <span data-ttu-id="a794a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a794a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a794a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a794a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a794a-121"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a794a-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a794a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a794a-122">Library</span></span><br/> | <dl> <span data-ttu-id="a794a-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a794a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a794a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a794a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a794a-125">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="a794a-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





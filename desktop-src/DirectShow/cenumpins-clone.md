---
description: 'O método clone faz uma cópia do enumerador com o mesmo estado de enumeração. Esse método implementa o método IEnumPins:: clone.'
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Método CEnumPins. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2aa3e4604b260779a5d203e75e8e0790a7378b11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752701"
---
# <a name="cenumpinsclone-method"></a><span data-ttu-id="9ed0d-104">Método CEnumPins. Clone</span><span class="sxs-lookup"><span data-stu-id="9ed0d-104">CEnumPins.Clone method</span></span>

<span data-ttu-id="9ed0d-105">O `Clone` método faz uma cópia do enumerador com o mesmo estado de enumeração.</span><span class="sxs-lookup"><span data-stu-id="9ed0d-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="9ed0d-106">Esse método implementa o método [**IEnumPins:: clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) .</span><span class="sxs-lookup"><span data-stu-id="9ed0d-106">This method implements the [**IEnumPins::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed0d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ed0d-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="9ed0d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ed0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed0d-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="9ed0d-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed0d-110">Endereço de uma variável que recebe um ponteiro para a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) do novo enumerador.</span><span class="sxs-lookup"><span data-stu-id="9ed0d-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed0d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ed0d-111">Return value</span></span>

<span data-ttu-id="9ed0d-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ed0d-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="9ed0d-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9ed0d-113">Return code</span></span>                                                                                                | <span data-ttu-id="9ed0d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ed0d-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ed0d-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9ed0d-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="9ed0d-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="9ed0d-116">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="9ed0d-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9ed0d-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="9ed0d-118">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="9ed0d-118">Insufficient memory.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9ed0d-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="9ed0d-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="9ed0d-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="9ed0d-120">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="9ed0d-121"><dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt></span><span class="sxs-lookup"><span data-stu-id="9ed0d-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="9ed0d-122">O estado do filtro foi alterado e agora está inconsistente com o enumerador.</span><span class="sxs-lookup"><span data-stu-id="9ed0d-122">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9ed0d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ed0d-123">Requirements</span></span>



| <span data-ttu-id="9ed0d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ed0d-124">Requirement</span></span> | <span data-ttu-id="9ed0d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9ed0d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed0d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ed0d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9ed0d-127"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed0d-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9ed0d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ed0d-128">Library</span></span><br/> | <dl> <span data-ttu-id="9ed0d-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed0d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed0d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ed0d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed0d-131">**Classe CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="9ed0d-131">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 





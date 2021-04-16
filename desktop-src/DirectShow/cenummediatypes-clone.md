---
description: 'O método clone faz uma cópia do enumerador com o mesmo estado de enumeração. Esse método implementa o método IEnumMediaTypes:: clone.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Método CEnumMediaTypes. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750483"
---
# <a name="cenummediatypesclone-method"></a><span data-ttu-id="ca108-104">Método CEnumMediaTypes. Clone</span><span class="sxs-lookup"><span data-stu-id="ca108-104">CEnumMediaTypes.Clone method</span></span>

<span data-ttu-id="ca108-105">O `Clone` método faz uma cópia do enumerador com o mesmo estado de enumeração.</span><span class="sxs-lookup"><span data-stu-id="ca108-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="ca108-106">Esse método implementa o método [**IEnumMediaTypes:: clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .</span><span class="sxs-lookup"><span data-stu-id="ca108-106">This method implements the [**IEnumMediaTypes::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca108-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca108-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="ca108-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca108-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca108-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="ca108-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="ca108-110">Endereço de uma variável que recebe um ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) do novo enumerador.</span><span class="sxs-lookup"><span data-stu-id="ca108-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca108-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca108-111">Return value</span></span>

<span data-ttu-id="ca108-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca108-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ca108-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ca108-113">Return code</span></span>                                                                                                | <span data-ttu-id="ca108-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca108-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca108-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca108-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="ca108-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ca108-116">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="ca108-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ca108-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="ca108-118">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="ca108-118">Insufficient memory.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="ca108-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ca108-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="ca108-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ca108-120">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="ca108-121"><dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt></span><span class="sxs-lookup"><span data-stu-id="ca108-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="ca108-122">O estado do PIN foi alterado e agora está inconsistente com o enumerador.</span><span class="sxs-lookup"><span data-stu-id="ca108-122">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ca108-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca108-123">Requirements</span></span>



| <span data-ttu-id="ca108-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca108-124">Requirement</span></span> | <span data-ttu-id="ca108-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ca108-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca108-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca108-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ca108-127"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca108-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca108-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca108-128">Library</span></span><br/> | <dl> <span data-ttu-id="ca108-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ca108-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca108-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca108-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca108-131">**Classe CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="ca108-131">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 





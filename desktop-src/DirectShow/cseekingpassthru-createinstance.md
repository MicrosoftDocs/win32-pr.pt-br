---
description: O método CreateInstance cria uma instância do objeto. Esse método dá suporte à criação do objeto por meio de uma fábrica de classes. Para obter mais informações, consulte CFactoryTemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Método CSeekingPassThru. CreateInstance (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751486"
---
# <a name="cseekingpassthrucreateinstance-method"></a><span data-ttu-id="138b0-105">Método CSeekingPassThru. CreateInstance</span><span class="sxs-lookup"><span data-stu-id="138b0-105">CSeekingPassThru.CreateInstance method</span></span>

<span data-ttu-id="138b0-106">O `CreateInstance` método cria uma instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="138b0-106">The `CreateInstance` method creates an instance of the object.</span></span> <span data-ttu-id="138b0-107">Esse método dá suporte à criação do objeto por meio de uma fábrica de classes.</span><span class="sxs-lookup"><span data-stu-id="138b0-107">This method supports creation of the object through a class factory.</span></span> <span data-ttu-id="138b0-108">Para obter mais informações, consulte [**CFactoryTemplate**](cfactorytemplate.md).</span><span class="sxs-lookup"><span data-stu-id="138b0-108">For more information, see [**CFactoryTemplate**](cfactorytemplate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="138b0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="138b0-109">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="138b0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="138b0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="138b0-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="138b0-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="138b0-112">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="138b0-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="138b0-113">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="138b0-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="138b0-114">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="138b0-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="138b0-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="138b0-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="138b0-116">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="138b0-116">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="138b0-117">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="138b0-117">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="138b0-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="138b0-118">Return value</span></span>

<span data-ttu-id="138b0-119">Retorna um ponteiro para um novo objeto **CSeekingPassThru** .</span><span class="sxs-lookup"><span data-stu-id="138b0-119">Returns a pointer to a new **CSeekingPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="138b0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="138b0-120">Requirements</span></span>



| <span data-ttu-id="138b0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="138b0-121">Requirement</span></span> | <span data-ttu-id="138b0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="138b0-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="138b0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="138b0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="138b0-124"><dt>Seekpt. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="138b0-124"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="138b0-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="138b0-125">Library</span></span><br/> | <dl> <span data-ttu-id="138b0-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="138b0-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="138b0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="138b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="138b0-128">**Classe CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="138b0-128">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 





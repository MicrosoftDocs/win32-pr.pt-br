---
description: O método GetPin recupera um PIN. A classe CEnumPins chama esse método para enumerar Pins no filtro.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Método CBaseFilter. GetPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755392"
---
# <a name="cbasefiltergetpin-method"></a><span data-ttu-id="62407-104">Método CBaseFilter. GetPin</span><span class="sxs-lookup"><span data-stu-id="62407-104">CBaseFilter.GetPin method</span></span>

<span data-ttu-id="62407-105">O método **GetPin** recupera um PIN.</span><span class="sxs-lookup"><span data-stu-id="62407-105">The **GetPin** method retrieves a pin.</span></span> <span data-ttu-id="62407-106">A classe [**CEnumPins**](cenumpins.md) chama esse método para enumerar Pins no filtro.</span><span class="sxs-lookup"><span data-stu-id="62407-106">The [**CEnumPins**](cenumpins.md) class calls this method to enumerate pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="62407-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62407-107">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="62407-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62407-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62407-109">*n*</span><span class="sxs-lookup"><span data-stu-id="62407-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="62407-110">O índice de base zero do PIN.</span><span class="sxs-lookup"><span data-stu-id="62407-110">The zero-based index of the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62407-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62407-111">Return value</span></span>

<span data-ttu-id="62407-112">Retorna um ponteiro para o objeto [**CBasePin**](cbasepin.md) que implementa o PIN.</span><span class="sxs-lookup"><span data-stu-id="62407-112">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="62407-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="62407-113">Remarks</span></span>

<span data-ttu-id="62407-114">Você deve implementar esse método virtual puro em sua classe derivada.</span><span class="sxs-lookup"><span data-stu-id="62407-114">You must implement this pure virtual method in your derived class.</span></span> <span data-ttu-id="62407-115">Retornar um ponteiro para o *n* º PIN neste filtro, indexado de zero.</span><span class="sxs-lookup"><span data-stu-id="62407-115">Return a pointer to the *n* th pin on this filter, indexed from zero.</span></span> <span data-ttu-id="62407-116">Você pode escolher uma ordem de indexação arbitrária, desde que a ordem seja fixa.</span><span class="sxs-lookup"><span data-stu-id="62407-116">You can choose an arbitrary indexing order, as long as the ordering is fixed.</span></span> <span data-ttu-id="62407-117">Se o filtro Adicionar ou excluir Pins ou a ordenação for alterada por algum outro motivo em tempo de execução, chame o método [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="62407-117">If the filter adds or deletes pins, or the ordering changes for some other reason at run time, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="62407-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62407-118">Requirements</span></span>



| <span data-ttu-id="62407-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="62407-119">Requirement</span></span> | <span data-ttu-id="62407-120">Valor</span><span class="sxs-lookup"><span data-stu-id="62407-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62407-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62407-121">Header</span></span><br/>  | <dl> <span data-ttu-id="62407-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62407-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="62407-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62407-123">Library</span></span><br/> | <dl> <span data-ttu-id="62407-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="62407-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62407-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="62407-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62407-126">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="62407-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





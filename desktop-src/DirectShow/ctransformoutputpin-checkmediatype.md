---
description: O método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Método CTransformOutputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c2bc617a5ff56a8b82184700af85e2634960ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752683"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="5877c-103">Método CTransformOutputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="5877c-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="5877c-104">O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="5877c-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5877c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5877c-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="5877c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5877c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5877c-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="5877c-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="5877c-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="5877c-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5877c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5877c-109">Return value</span></span>

<span data-ttu-id="5877c-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5877c-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5877c-111">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="5877c-111">Possible values include the following.</span></span>



| <span data-ttu-id="5877c-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5877c-112">Return code</span></span>                                                                                  | <span data-ttu-id="5877c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="5877c-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="5877c-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5877c-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5877c-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="5877c-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="5877c-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5877c-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5877c-117">O pino de entrada do filtro não está conectado.</span><span class="sxs-lookup"><span data-stu-id="5877c-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5877c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5877c-118">Remarks</span></span>

<span data-ttu-id="5877c-119">Esse método implementa o método puramente virtual [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="5877c-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="5877c-120">O método falhará se o PIN de entrada do filtro não estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="5877c-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="5877c-121">Caso contrário, ele chama o método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) do filtro, que também é virtual puro.</span><span class="sxs-lookup"><span data-stu-id="5877c-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="5877c-122">A classe derivada do filtro deve implementar **CheckTransform**, que determina se o tipo de mídia de saída proposto é compatível com o tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="5877c-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5877c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5877c-123">Requirements</span></span>



| <span data-ttu-id="5877c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5877c-124">Requirement</span></span> | <span data-ttu-id="5877c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5877c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5877c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5877c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5877c-127"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5877c-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5877c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5877c-128">Library</span></span><br/> | <dl> <span data-ttu-id="5877c-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5877c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





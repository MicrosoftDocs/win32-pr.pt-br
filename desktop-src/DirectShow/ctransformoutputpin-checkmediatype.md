---
description: Método CTransformOutputPin. CheckMediaType – o método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
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
ms.openlocfilehash: 7dc0edc642687518979eab1d47c69af039bc3173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084904"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="87ae2-103">Método CTransformOutputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="87ae2-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="87ae2-104">O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="87ae2-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ae2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87ae2-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="87ae2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87ae2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ae2-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="87ae2-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="87ae2-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="87ae2-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ae2-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="87ae2-109">Return value</span></span>

<span data-ttu-id="87ae2-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87ae2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="87ae2-111">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="87ae2-111">Possible values include the following.</span></span>



| <span data-ttu-id="87ae2-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="87ae2-112">Return code</span></span>                                                                                  | <span data-ttu-id="87ae2-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="87ae2-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="87ae2-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87ae2-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="87ae2-115">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="87ae2-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="87ae2-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="87ae2-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="87ae2-117">O pino de entrada do filtro não está conectado.</span><span class="sxs-lookup"><span data-stu-id="87ae2-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87ae2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="87ae2-118">Remarks</span></span>

<span data-ttu-id="87ae2-119">Esse método implementa o método puramente virtual [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="87ae2-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="87ae2-120">O método falhará se o PIN de entrada do filtro não estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="87ae2-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="87ae2-121">Caso contrário, ele chama o método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) do filtro, que também é virtual puro.</span><span class="sxs-lookup"><span data-stu-id="87ae2-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="87ae2-122">A classe derivada do filtro deve implementar **CheckTransform**, que determina se o tipo de mídia de saída proposto é compatível com o tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="87ae2-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ae2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87ae2-123">Requirements</span></span>



| <span data-ttu-id="87ae2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ae2-124">Requirement</span></span> | <span data-ttu-id="87ae2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="87ae2-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ae2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87ae2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="87ae2-127"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87ae2-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="87ae2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87ae2-128">Library</span></span><br/> | <dl> <span data-ttu-id="87ae2-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="87ae2-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





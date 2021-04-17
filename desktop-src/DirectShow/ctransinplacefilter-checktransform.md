---
description: 'O método CheckTransform verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída. Esse método substitui o método CTransformFilter:: CheckTransform.'
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Método CTransInPlaceFilter. CheckTransform (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775567"
---
# <a name="ctransinplacefilterchecktransform-method"></a><span data-ttu-id="c0208-104">Método CTransInPlaceFilter. CheckTransform</span><span class="sxs-lookup"><span data-stu-id="c0208-104">CTransInPlaceFilter.CheckTransform method</span></span>

<span data-ttu-id="c0208-105">O `CheckTransform` método verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="c0208-105">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span> <span data-ttu-id="c0208-106">Esse método substitui o método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="c0208-106">This method overrides the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0208-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0208-107">Syntax</span></span>


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a><span data-ttu-id="c0208-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0208-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0208-109">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="c0208-109">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="c0208-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0208-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="c0208-111">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="c0208-111">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="c0208-112">Ponteiro para um objeto **CMediaType** que especifica o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="c0208-112">Pointer to a **CMediaType** object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0208-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0208-113">Return value</span></span>

<span data-ttu-id="c0208-114">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0208-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0208-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0208-115">Remarks</span></span>

<span data-ttu-id="c0208-116">O filtro **CTransInPlace** nunca chama `CheckTransform` .</span><span class="sxs-lookup"><span data-stu-id="c0208-116">The **CTransInPlace** filter never calls `CheckTransform`.</span></span> <span data-ttu-id="c0208-117">Em vez disso, toda a conexão de PIN usa [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) para verificar o tipo de mídia, com a suposição de que os tipos de entrada e saída sempre correspondem.</span><span class="sxs-lookup"><span data-stu-id="c0208-117">Instead, all pin connection use [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) to check the media type, with the assumption that the input and output types always match.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0208-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0208-118">Requirements</span></span>



| <span data-ttu-id="c0208-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0208-119">Requirement</span></span> | <span data-ttu-id="c0208-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c0208-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0208-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0208-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c0208-122"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0208-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0208-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0208-123">Library</span></span><br/> | <dl> <span data-ttu-id="c0208-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c0208-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0208-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0208-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0208-126">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="c0208-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 





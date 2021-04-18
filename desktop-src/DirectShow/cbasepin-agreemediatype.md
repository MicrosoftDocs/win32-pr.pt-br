---
description: O método AgreeMediaType procura um tipo de mídia para fazer uma conexão de PIN.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Método CBasePin. AgreeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753358"
---
# <a name="cbasepinagreemediatype-method"></a><span data-ttu-id="bf1f2-103">Método CBasePin. AgreeMediaType</span><span class="sxs-lookup"><span data-stu-id="bf1f2-103">CBasePin.AgreeMediaType method</span></span>

<span data-ttu-id="bf1f2-104">O `AgreeMediaType` método procura um tipo de mídia para fazer uma conexão de PIN.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-104">The `AgreeMediaType` method searches for a media type to make a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf1f2-105">Syntax</span></span>


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="bf1f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf1f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf1f2-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="bf1f2-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="bf1f2-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de recebimento.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="bf1f2-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="bf1f2-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="bf1f2-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica um tipo de mídia ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies a media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf1f2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf1f2-111">Return value</span></span>

<span data-ttu-id="bf1f2-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf1f2-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bf1f2-113">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="bf1f2-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bf1f2-114">Return code</span></span>                                                                                                  | <span data-ttu-id="bf1f2-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf1f2-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="bf1f2-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bf1f2-116"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="bf1f2-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="bf1f2-118"><dt>**VFW \_ E \_ nenhum \_ \_ tipo aceitável**</dt></span><span class="sxs-lookup"><span data-stu-id="bf1f2-118"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="bf1f2-119">Nenhum tipo de mídia aceitável foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-119">No acceptable media type was found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf1f2-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf1f2-120">Remarks</span></span>

<span data-ttu-id="bf1f2-121">Se o parâmetro *PGTO* for não **nulo** e especificar totalmente um tipo de mídia, esse método tentará uma conexão usando esse tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-121">If the *pmt* parameter is non-**NULL** and fully specifies a media type, this method attempts a connection using that media type.</span></span> <span data-ttu-id="bf1f2-122">Se a tentativa falhar, o método retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-122">If the attempt fails, the method returns an error.</span></span>

<span data-ttu-id="bf1f2-123">Se o parâmetro *PGTO* for **nulo** ou especificar um tipo de mídia parcial, esse método tentará os tipos de mídia na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="bf1f2-123">If the *pmt* parameter is **NULL** or specifies a partial media type, this method tries media types in the following order:</span></span>

1.  <span data-ttu-id="bf1f2-124">Os tipos de mídia preferenciais do pino de recebimento.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-124">The receiving pin's preferred media types.</span></span>
2.  <span data-ttu-id="bf1f2-125">Os tipos de mídia preferenciais deste PIN.</span><span class="sxs-lookup"><span data-stu-id="bf1f2-125">This pin's preferred media types.</span></span>

<span data-ttu-id="bf1f2-126">Os tipos de mídia preferenciais são enumerados com o método [**CBasePin:: EnumMediaTypes**](cbasepin-enummediatypes.md) e o enumerador resultante é passado para o método [**CBasePin:: TryMediaTypes**](cbasepin-trymediatypes.md) .</span><span class="sxs-lookup"><span data-stu-id="bf1f2-126">Preferred media types are enumerated with the [**CBasePin::EnumMediaTypes**](cbasepin-enummediatypes.md) method, and the resulting enumerator is passed to the [**CBasePin::TryMediaTypes**](cbasepin-trymediatypes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf1f2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf1f2-127">Requirements</span></span>



| <span data-ttu-id="bf1f2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf1f2-128">Requirement</span></span> | <span data-ttu-id="bf1f2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="bf1f2-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1f2-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf1f2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="bf1f2-131"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf1f2-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bf1f2-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf1f2-132">Library</span></span><br/> | <dl> <span data-ttu-id="bf1f2-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bf1f2-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf1f2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf1f2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1f2-135">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="bf1f2-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





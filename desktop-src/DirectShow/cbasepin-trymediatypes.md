---
description: Dada uma lista de tipos de mídia, o método TryMediaTypes tenta concluir uma conexão usando um desses tipos.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Método CBasePin. TryMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19b8da39d07b8aae9401bdc6ccf2eecb5d3a1e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750065"
---
# <a name="cbasepintrymediatypes-method"></a><span data-ttu-id="7d8e2-103">Método CBasePin. TryMediaTypes</span><span class="sxs-lookup"><span data-stu-id="7d8e2-103">CBasePin.TryMediaTypes method</span></span>

<span data-ttu-id="7d8e2-104">Dada uma lista de tipos de mídia, o `TryMediaTypes` método tenta concluir uma conexão usando um desses tipos.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-104">Given a list of media types, the `TryMediaTypes` method tries to complete a connection using one of those types.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d8e2-105">Syntax</span></span>


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="7d8e2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d8e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8e2-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="7d8e2-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="7d8e2-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de recebimento.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7d8e2-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="7d8e2-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7d8e2-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que limita os tipos de mídia possíveis, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-110">Pointer to a [**CMediaType**](cmediatype.md) object that limits the possible media types, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7d8e2-111">*pEnum*</span><span class="sxs-lookup"><span data-stu-id="7d8e2-111">*pEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="7d8e2-112">Ponteiro para uma interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) , usado para enumerar a lista de tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-112">Pointer to an [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface, used to enumerate the list of media types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8e2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d8e2-113">Return value</span></span>

<span data-ttu-id="7d8e2-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7d8e2-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7d8e2-115">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="7d8e2-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7d8e2-116">Return code</span></span>                                                                                                  | <span data-ttu-id="7d8e2-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d8e2-117">Description</span></span>                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="7d8e2-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7d8e2-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="7d8e2-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-119">Success.</span></span><br/>                               |
| <dl> <span data-ttu-id="7d8e2-120"><dt>**VFW \_ E \_ nenhum \_ \_ tipo aceitável**</dt></span><span class="sxs-lookup"><span data-stu-id="7d8e2-120"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="7d8e2-121">Não foi possível encontrar um tipo de mídia aceitável.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-121">Did not find an acceptable media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d8e2-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d8e2-122">Remarks</span></span>

<span data-ttu-id="7d8e2-123">Para cada tipo de mídia retornado pela interface **IEnumMediaTypes** , esse método tenta uma conexão chamando o método [**CBasePin:: AttemptConnection**](cbasepin-attemptconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="7d8e2-123">For each media type returned by the **IEnumMediaTypes** interface, this method attempts a connection by calling the [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) method.</span></span>

<span data-ttu-id="7d8e2-124">Se o parâmetro *PGTO* for não **nulo**, o PIN ignorará os tipos de mídia que não correspondem a esse tipo.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-124">If the *pmt* parameter is non-**NULL**, the pin skips media types that do not match this type.</span></span> <span data-ttu-id="7d8e2-125">O parâmetro *PGTO* pode especificar um tipo de mídia parcial.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-125">The *pmt* parameter can specify a partial media type.</span></span> <span data-ttu-id="7d8e2-126">Um tipo de mídia parcial tem um valor de GUID \_ NULL para o tipo principal, o subtipo ou o formato.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-126">A partial media type has a value of GUID\_NULL for either the major type, the subtype, or the format.</span></span> <span data-ttu-id="7d8e2-127">O \_ valor NULL de GUID corresponde a qualquer tipo, semelhante a um valor "curinga".</span><span class="sxs-lookup"><span data-stu-id="7d8e2-127">The GUID\_NULL value matches any type, similar to a "wildcard" value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8e2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d8e2-128">Requirements</span></span>



| <span data-ttu-id="7d8e2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d8e2-129">Requirement</span></span> | <span data-ttu-id="7d8e2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7d8e2-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8e2-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d8e2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7d8e2-132"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d8e2-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7d8e2-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d8e2-133">Library</span></span><br/> | <dl> <span data-ttu-id="7d8e2-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7d8e2-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d8e2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d8e2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8e2-136">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="7d8e2-136">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





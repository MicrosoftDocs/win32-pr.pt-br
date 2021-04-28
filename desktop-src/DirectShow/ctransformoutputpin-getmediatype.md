---
description: Método CTransformOutputPin. GetMediaType – o método GetMediaType recupera um tipo de mídia preferencial, por valor de índice.
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Método CTransformOutputPin. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dd0bf38f2fa3be0e077f2509001680bbfc84e15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094894"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="a50b8-103">Método CTransformOutputPin. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="a50b8-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="a50b8-104">O `GetMediaType` método recupera um tipo de mídia preferencial, por valor de índice.</span><span class="sxs-lookup"><span data-stu-id="a50b8-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a50b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a50b8-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="a50b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a50b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a50b8-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="a50b8-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="a50b8-108">Valor de índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="a50b8-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="a50b8-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="a50b8-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="a50b8-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="a50b8-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a50b8-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a50b8-111">Return value</span></span>

<span data-ttu-id="a50b8-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a50b8-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a50b8-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a50b8-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a50b8-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a50b8-114">Return code</span></span>                                                                                            | <span data-ttu-id="a50b8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a50b8-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="a50b8-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a50b8-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="a50b8-117">Êxito</span><span class="sxs-lookup"><span data-stu-id="a50b8-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="a50b8-118"><dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt></span><span class="sxs-lookup"><span data-stu-id="a50b8-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="a50b8-119">Índice fora do intervalo</span><span class="sxs-lookup"><span data-stu-id="a50b8-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a50b8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a50b8-120">Remarks</span></span>

<span data-ttu-id="a50b8-121">Esse método substitui o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="a50b8-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="a50b8-122">Se o pino de entrada do filtro não estiver conectado, o método retornará VFW \_ s \_ não \_ mais \_ itens.</span><span class="sxs-lookup"><span data-stu-id="a50b8-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="a50b8-123">Caso contrário, ele chama o método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) do filtro para recuperar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="a50b8-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="a50b8-124">O método **CTransformFilter:: GetMediaType** é virtual puro; a classe derivada do filtro deve substituí-la.</span><span class="sxs-lookup"><span data-stu-id="a50b8-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a50b8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a50b8-125">Requirements</span></span>



| <span data-ttu-id="a50b8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a50b8-126">Requirement</span></span> | <span data-ttu-id="a50b8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a50b8-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a50b8-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a50b8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a50b8-129"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a50b8-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a50b8-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a50b8-130">Library</span></span><br/> | <dl> <span data-ttu-id="a50b8-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a50b8-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





---
description: O método GetMediaType recupera um tipo de mídia preferencial, por valor de índice.
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
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758651"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="de6c7-103">Método CTransformOutputPin. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="de6c7-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="de6c7-104">O `GetMediaType` método recupera um tipo de mídia preferencial, por valor de índice.</span><span class="sxs-lookup"><span data-stu-id="de6c7-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="de6c7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de6c7-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="de6c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de6c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de6c7-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="de6c7-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="de6c7-108">Valor de índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="de6c7-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="de6c7-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="de6c7-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="de6c7-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="de6c7-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de6c7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de6c7-111">Return value</span></span>

<span data-ttu-id="de6c7-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de6c7-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="de6c7-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="de6c7-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="de6c7-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="de6c7-114">Return code</span></span>                                                                                            | <span data-ttu-id="de6c7-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="de6c7-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="de6c7-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de6c7-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="de6c7-117">Sucesso</span><span class="sxs-lookup"><span data-stu-id="de6c7-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="de6c7-118"><dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt></span><span class="sxs-lookup"><span data-stu-id="de6c7-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="de6c7-119">Índice fora do intervalo</span><span class="sxs-lookup"><span data-stu-id="de6c7-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de6c7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="de6c7-120">Remarks</span></span>

<span data-ttu-id="de6c7-121">Esse método substitui o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="de6c7-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="de6c7-122">Se o pino de entrada do filtro não estiver conectado, o método retornará VFW \_ s \_ não \_ mais \_ itens.</span><span class="sxs-lookup"><span data-stu-id="de6c7-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="de6c7-123">Caso contrário, ele chama o método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) do filtro para recuperar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="de6c7-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="de6c7-124">O método **CTransformFilter:: GetMediaType** é virtual puro; a classe derivada do filtro deve substituí-la.</span><span class="sxs-lookup"><span data-stu-id="de6c7-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="de6c7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de6c7-125">Requirements</span></span>



| <span data-ttu-id="de6c7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="de6c7-126">Requirement</span></span> | <span data-ttu-id="de6c7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="de6c7-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de6c7-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de6c7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="de6c7-129"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de6c7-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="de6c7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de6c7-130">Library</span></span><br/> | <dl> <span data-ttu-id="de6c7-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="de6c7-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





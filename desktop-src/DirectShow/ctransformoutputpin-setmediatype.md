---
description: O método SetMediaType define o tipo de mídia para a conexão.
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: Método CTransformOutputPin. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45bd16f0c0e5ea9cd1e719518fab15180177fd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748188"
---
# <a name="ctransformoutputpinsetmediatype-method"></a><span data-ttu-id="4467f-103">Método CTransformOutputPin. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="4467f-103">CTransformOutputPin.SetMediaType method</span></span>

<span data-ttu-id="4467f-104">O `SetMediaType` método define o tipo de mídia para a conexão.</span><span class="sxs-lookup"><span data-stu-id="4467f-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4467f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4467f-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="4467f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4467f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4467f-107">*MT*</span><span class="sxs-lookup"><span data-stu-id="4467f-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="4467f-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="4467f-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4467f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4467f-109">Return value</span></span>

<span data-ttu-id="4467f-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4467f-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4467f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4467f-111">Remarks</span></span>

<span data-ttu-id="4467f-112">Esse método substitui o método [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="4467f-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="4467f-113">Ele chama o método [**CTransformFilter:: SetMediaType**](ctransformfilter-setmediatype.md) do filtro para informar o filtro.</span><span class="sxs-lookup"><span data-stu-id="4467f-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="4467f-114">O PIN deve verificar se o tipo de mídia é aceitável antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="4467f-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4467f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4467f-115">Requirements</span></span>



| <span data-ttu-id="4467f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4467f-116">Requirement</span></span> | <span data-ttu-id="4467f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4467f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4467f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4467f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4467f-119"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4467f-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4467f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4467f-120">Library</span></span><br/> | <dl> <span data-ttu-id="4467f-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4467f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





---
description: O método SetMediaType define o tipo de mídia para a conexão.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Método CTransformInputPin. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b42531a003fbad1a2a08864390a512296c440e64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778444"
---
# <a name="ctransforminputpinsetmediatype-method"></a><span data-ttu-id="49598-103">Método CTransformInputPin. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="49598-103">CTransformInputPin.SetMediaType method</span></span>

<span data-ttu-id="49598-104">O `SetMediaType` método define o tipo de mídia para a conexão.</span><span class="sxs-lookup"><span data-stu-id="49598-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="49598-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49598-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="49598-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49598-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49598-107">*MT*</span><span class="sxs-lookup"><span data-stu-id="49598-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="49598-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="49598-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49598-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49598-109">Return value</span></span>

<span data-ttu-id="49598-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49598-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="49598-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="49598-111">Remarks</span></span>

<span data-ttu-id="49598-112">Esse método substitui o método [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="49598-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="49598-113">Ele chama o método [**CTransformFilter:: SetMediaType**](ctransformfilter-setmediatype.md) do filtro para informar o filtro.</span><span class="sxs-lookup"><span data-stu-id="49598-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="49598-114">O PIN deve verificar se o tipo de mídia é aceitável antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="49598-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="49598-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49598-115">Requirements</span></span>



| <span data-ttu-id="49598-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="49598-116">Requirement</span></span> | <span data-ttu-id="49598-117">Valor</span><span class="sxs-lookup"><span data-stu-id="49598-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49598-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49598-118">Header</span></span><br/>  | <dl> <span data-ttu-id="49598-119"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49598-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="49598-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49598-120">Library</span></span><br/> | <dl> <span data-ttu-id="49598-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="49598-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





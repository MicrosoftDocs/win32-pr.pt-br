---
description: O método SetMediaType é chamado quando o tipo de mídia é definido em um dos Pins do filtro.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Método CTransformFilter. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789652"
---
# <a name="ctransformfiltersetmediatype-method"></a><span data-ttu-id="83278-103">Método CTransformFilter. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="83278-103">CTransformFilter.SetMediaType method</span></span>

<span data-ttu-id="83278-104">O `SetMediaType` método é chamado quando o tipo de mídia é definido em um dos Pins do filtro.</span><span class="sxs-lookup"><span data-stu-id="83278-104">The `SetMediaType` method is called when the media type is set on one of the filter's pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="83278-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83278-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="83278-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83278-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83278-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="83278-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="83278-108">Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando um PIN no filtro (entrada ou saída).</span><span class="sxs-lookup"><span data-stu-id="83278-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying a pin on the filter (input or output).</span></span>

</dd> <dt>

<span data-ttu-id="83278-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="83278-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="83278-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="83278-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83278-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83278-111">Return value</span></span>

<span data-ttu-id="83278-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83278-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="83278-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="83278-113">Remarks</span></span>

<span data-ttu-id="83278-114">Os métodos [**CTransformInputPin:: SetMediaType**](ctransforminputpin-setmediatype.md) e [**CTransformOutputPin:: SetMediaType**](ctransformoutputpin-setmediatype.md) chamam esse método quando o tipo de mídia de um PIN é definido.</span><span class="sxs-lookup"><span data-stu-id="83278-114">The [**CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) and [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) methods call this method when a pin's media type is set.</span></span> <span data-ttu-id="83278-115">Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="83278-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="83278-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83278-116">Requirements</span></span>



| <span data-ttu-id="83278-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="83278-117">Requirement</span></span> | <span data-ttu-id="83278-118">Valor</span><span class="sxs-lookup"><span data-stu-id="83278-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83278-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83278-119">Header</span></span><br/>  | <dl> <span data-ttu-id="83278-120"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83278-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="83278-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83278-121">Library</span></span><br/> | <dl> <span data-ttu-id="83278-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="83278-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83278-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="83278-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83278-124">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="83278-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





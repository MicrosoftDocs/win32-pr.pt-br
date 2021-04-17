---
description: O método BreakConnect libera um PIN de uma conexão.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Método CTransformFilter. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749011"
---
# <a name="ctransformfilterbreakconnect-method"></a><span data-ttu-id="d08c4-103">Método CTransformFilter. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="d08c4-103">CTransformFilter.BreakConnect method</span></span>

<span data-ttu-id="d08c4-104">O `BreakConnect` método libera um PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="d08c4-104">The `BreakConnect` method releases a pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d08c4-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="d08c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d08c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08c4-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="d08c4-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="d08c4-108">Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando qual conexão de PIN foi quebrada (entrada ou saída).</span><span class="sxs-lookup"><span data-stu-id="d08c4-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin connection was broken (input or output).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d08c4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d08c4-109">Return value</span></span>

<span data-ttu-id="d08c4-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d08c4-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d08c4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08c4-111">Remarks</span></span>

<span data-ttu-id="d08c4-112">Os métodos [**CTransformInputPin:: BreakConnect**](ctransforminputpin-breakconnect.md) e [**CTransformOutputPin:: BreakConnect**](ctransformoutputpin-breakconnect.md) chamam esse método quando uma conexão de PIN é quebrada.</span><span class="sxs-lookup"><span data-stu-id="d08c4-112">The [**CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) and [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) methods call this method when a pin connection is broken.</span></span> <span data-ttu-id="d08c4-113">Esse método não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="d08c4-113">This method does nothing in the base class.</span></span> <span data-ttu-id="d08c4-114">Se você substituir o método [**CheckConnect**](ctransformfilter-checkconnect.md) , substitua esse método para liberar todos os recursos obtidos no método **CheckConnect** , incluindo ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="d08c4-114">If you override the [**CheckConnect**](ctransformfilter-checkconnect.md) method, override this method to release any resources obtained in the **CheckConnect** method, including interface pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d08c4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d08c4-115">Requirements</span></span>



| <span data-ttu-id="d08c4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d08c4-116">Requirement</span></span> | <span data-ttu-id="d08c4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d08c4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d08c4-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d08c4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d08c4-119"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d08c4-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d08c4-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d08c4-120">Library</span></span><br/> | <dl> <span data-ttu-id="d08c4-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d08c4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d08c4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d08c4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08c4-123">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="d08c4-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





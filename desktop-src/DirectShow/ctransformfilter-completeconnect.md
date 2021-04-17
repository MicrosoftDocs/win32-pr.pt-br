---
description: O método CompleteConnect conclui uma conexão de PIN.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Método CTransformFilter. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751239"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="74405-103">Método CTransformFilter. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="74405-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="74405-104">O `CompleteConnect` método conclui uma conexão de PIN.</span><span class="sxs-lookup"><span data-stu-id="74405-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="74405-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74405-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="74405-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74405-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74405-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="74405-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="74405-108">Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando qual Pin no filtro está fazendo a conexão.</span><span class="sxs-lookup"><span data-stu-id="74405-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="74405-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="74405-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="74405-110">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN nesta tentativa de conexão.</span><span class="sxs-lookup"><span data-stu-id="74405-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74405-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74405-111">Return value</span></span>

<span data-ttu-id="74405-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74405-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="74405-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="74405-113">Remarks</span></span>

<span data-ttu-id="74405-114">Os métodos [**CTransformInputPin:: CompleteConnect**](ctransforminputpin-completeconnect.md) e [**CTransformOutputPin:: CompleteConnect**](ctransformoutputpin-completeconnect.md) chamam esse método durante o processo de conexão do PIN.</span><span class="sxs-lookup"><span data-stu-id="74405-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="74405-115">Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="74405-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="74405-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74405-116">Requirements</span></span>



| <span data-ttu-id="74405-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="74405-117">Requirement</span></span> | <span data-ttu-id="74405-118">Valor</span><span class="sxs-lookup"><span data-stu-id="74405-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74405-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74405-119">Header</span></span><br/>  | <dl> <span data-ttu-id="74405-120"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74405-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="74405-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74405-121">Library</span></span><br/> | <dl> <span data-ttu-id="74405-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="74405-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74405-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="74405-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74405-124">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="74405-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





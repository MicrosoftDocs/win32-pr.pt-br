---
description: Método CTransformFilter. CompleteConnect – o método CompleteConnect conclui uma conexão de PIN.
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
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095164"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="4fc5b-103">Método CTransformFilter. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="4fc5b-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="4fc5b-104">O `CompleteConnect` método conclui uma conexão de PIN.</span><span class="sxs-lookup"><span data-stu-id="4fc5b-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc5b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4fc5b-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="4fc5b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4fc5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc5b-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="4fc5b-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc5b-108">Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando qual Pin no filtro está fazendo a conexão.</span><span class="sxs-lookup"><span data-stu-id="4fc5b-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="4fc5b-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="4fc5b-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc5b-110">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN nesta tentativa de conexão.</span><span class="sxs-lookup"><span data-stu-id="4fc5b-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc5b-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4fc5b-111">Return value</span></span>

<span data-ttu-id="4fc5b-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4fc5b-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fc5b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4fc5b-113">Remarks</span></span>

<span data-ttu-id="4fc5b-114">Os métodos [**CTransformInputPin:: CompleteConnect**](ctransforminputpin-completeconnect.md) e [**CTransformOutputPin:: CompleteConnect**](ctransformoutputpin-completeconnect.md) chamam esse método durante o processo de conexão do PIN.</span><span class="sxs-lookup"><span data-stu-id="4fc5b-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="4fc5b-115">Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="4fc5b-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc5b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fc5b-116">Requirements</span></span>



| <span data-ttu-id="4fc5b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fc5b-117">Requirement</span></span> | <span data-ttu-id="4fc5b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4fc5b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc5b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4fc5b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4fc5b-120"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fc5b-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4fc5b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4fc5b-121">Library</span></span><br/> | <dl> <span data-ttu-id="4fc5b-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4fc5b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc5b-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4fc5b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc5b-124">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="4fc5b-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





---
description: O método CheckConnect determina se uma conexão de PIN é adequada.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Método CTransformFilter. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751482"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="31101-103">Método CTransformFilter. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="31101-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="31101-104">O `CheckConnect` método determina se uma conexão de PIN é adequada.</span><span class="sxs-lookup"><span data-stu-id="31101-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="31101-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31101-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="31101-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31101-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="31101-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="31101-108">Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando qual Pin no filtro está fazendo a conexão.</span><span class="sxs-lookup"><span data-stu-id="31101-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="31101-109">*pPin*</span><span class="sxs-lookup"><span data-stu-id="31101-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="31101-110">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN nesta tentativa de conexão.</span><span class="sxs-lookup"><span data-stu-id="31101-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31101-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31101-111">Return value</span></span>

<span data-ttu-id="31101-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31101-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="31101-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="31101-113">Remarks</span></span>

<span data-ttu-id="31101-114">Os métodos [**CTransformInputPin:: CheckConnect**](ctransforminputpin-checkconnect.md) e [**CTransformOutputPin:: CheckConnect**](ctransformoutputpin-checkconnect.md) chamam esse método durante o processo de conexão do PIN.</span><span class="sxs-lookup"><span data-stu-id="31101-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="31101-115">Esse método não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="31101-115">This method does nothing in the base class.</span></span> <span data-ttu-id="31101-116">A classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="31101-116">The derived class can override it.</span></span> <span data-ttu-id="31101-117">Por exemplo, a classe derivada pode consultar o outro PIN para uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="31101-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="31101-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31101-118">Requirements</span></span>



| <span data-ttu-id="31101-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="31101-119">Requirement</span></span> | <span data-ttu-id="31101-120">Valor</span><span class="sxs-lookup"><span data-stu-id="31101-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31101-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31101-121">Header</span></span><br/>  | <dl> <span data-ttu-id="31101-122"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31101-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="31101-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31101-123">Library</span></span><br/> | <dl> <span data-ttu-id="31101-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="31101-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31101-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="31101-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31101-126">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="31101-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





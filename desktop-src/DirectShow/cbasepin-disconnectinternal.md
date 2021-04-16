---
description: O método DisconnectInternal quebra a conexão do PIN atual.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Método CBasePin. DisconnectInternal (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752512"
---
# <a name="cbasepindisconnectinternal-method"></a><span data-ttu-id="ffc01-103">Método CBasePin. DisconnectInternal</span><span class="sxs-lookup"><span data-stu-id="ffc01-103">CBasePin.DisconnectInternal method</span></span>

<span data-ttu-id="ffc01-104">O `DisconnectInternal` método quebra a conexão do PIN atual.</span><span class="sxs-lookup"><span data-stu-id="ffc01-104">The `DisconnectInternal` method breaks the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffc01-105">Syntax</span></span>


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a><span data-ttu-id="ffc01-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffc01-106">Parameters</span></span>

<span data-ttu-id="ffc01-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ffc01-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ffc01-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ffc01-108">Return value</span></span>

<span data-ttu-id="ffc01-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ffc01-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ffc01-110">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ffc01-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="ffc01-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ffc01-111">Return code</span></span>                                                                                         | <span data-ttu-id="ffc01-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ffc01-112">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ffc01-113"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="ffc01-113"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="ffc01-114">O PIN não foi conectado.</span><span class="sxs-lookup"><span data-stu-id="ffc01-114">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="ffc01-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ffc01-115"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="ffc01-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ffc01-116">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ffc01-117"><dt>**VFW \_ E \_ não \_ parado**</dt></span><span class="sxs-lookup"><span data-stu-id="ffc01-117"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="ffc01-118">O filtro está ativo e o PIN não dá suporte à reconexão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="ffc01-118">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ffc01-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffc01-119">Remarks</span></span>

<span data-ttu-id="ffc01-120">O método [**CBasePin::D isconnect**](cbasepin-disconnect.md) delega o processo de desconexão para esse método.</span><span class="sxs-lookup"><span data-stu-id="ffc01-120">The [**CBasePin::Disconnect**](cbasepin-disconnect.md) method delegates the disconnect process to this method.</span></span> <span data-ttu-id="ffc01-121">Esse método chama o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc01-121">This method calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="ffc01-122">Ele também libera a contagem de referência no outro PIN, que é mantido pela variável de membro [**\_ conectado CBasePin:: m**](cbasepin-m-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc01-122">It also releases the reference count on the other pin, which is held by the [**CBasePin::m\_Connected**](cbasepin-m-connected.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffc01-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffc01-123">Requirements</span></span>



| <span data-ttu-id="ffc01-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffc01-124">Requirement</span></span> | <span data-ttu-id="ffc01-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ffc01-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc01-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ffc01-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ffc01-127"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc01-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ffc01-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ffc01-128">Library</span></span><br/> | <dl> <span data-ttu-id="ffc01-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc01-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffc01-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffc01-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc01-131">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="ffc01-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





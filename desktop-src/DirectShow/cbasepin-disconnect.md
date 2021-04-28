---
description: Método CBasePin. Disconnect – o método Disconnect quebra a conexão do PIN atual. Esse método implementa o método IPin::D isconnect.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Método CBasePin. Disconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bda01d02db2a93a90c63f206b723a55df2373418
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096004"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="806ab-104">Método CBasePin. Disconnect</span><span class="sxs-lookup"><span data-stu-id="806ab-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="806ab-105">O `Disconnect` método quebra a conexão do PIN atual.</span><span class="sxs-lookup"><span data-stu-id="806ab-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="806ab-106">Esse método implementa o método [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="806ab-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="806ab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="806ab-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="806ab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="806ab-108">Parameters</span></span>

<span data-ttu-id="806ab-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="806ab-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="806ab-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="806ab-110">Return value</span></span>

<span data-ttu-id="806ab-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="806ab-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="806ab-112">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="806ab-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="806ab-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="806ab-113">Return code</span></span>                                                                                         | <span data-ttu-id="806ab-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="806ab-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="806ab-115"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="806ab-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="806ab-116">O PIN não foi conectado.</span><span class="sxs-lookup"><span data-stu-id="806ab-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="806ab-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="806ab-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="806ab-118">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="806ab-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="806ab-119"><dt>**VFW \_ E \_ não \_ parado**</dt></span><span class="sxs-lookup"><span data-stu-id="806ab-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="806ab-120">O filtro está ativo e o PIN não dá suporte à reconexão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="806ab-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="806ab-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="806ab-121">Remarks</span></span>

<span data-ttu-id="806ab-122">A classe base delega a maior parte do trabalho para o método [**CBasePin::D isconnectinternal**](cbasepin-disconnectinternal.md) .</span><span class="sxs-lookup"><span data-stu-id="806ab-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="806ab-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="806ab-123">Requirements</span></span>



| <span data-ttu-id="806ab-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="806ab-124">Requirement</span></span> | <span data-ttu-id="806ab-125">Valor</span><span class="sxs-lookup"><span data-stu-id="806ab-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="806ab-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="806ab-126">Header</span></span><br/>  | <dl> <span data-ttu-id="806ab-127"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="806ab-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="806ab-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="806ab-128">Library</span></span><br/> | <dl> <span data-ttu-id="806ab-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="806ab-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="806ab-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="806ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="806ab-131">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="806ab-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





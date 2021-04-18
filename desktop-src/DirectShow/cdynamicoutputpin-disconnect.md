---
description: O método Disconnect quebra a conexão do PIN atual. Esse método implementa o método IPin::D isconnect.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Método CDynamicOutputPin. Disconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754989"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="e4322-104">Método CDynamicOutputPin. Disconnect</span><span class="sxs-lookup"><span data-stu-id="e4322-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="e4322-105">O `Disconnect` método quebra a conexão do PIN atual.</span><span class="sxs-lookup"><span data-stu-id="e4322-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="e4322-106">Esse método implementa o método [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="e4322-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4322-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4322-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="e4322-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4322-108">Parameters</span></span>

<span data-ttu-id="e4322-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e4322-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4322-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4322-110">Return value</span></span>

<span data-ttu-id="e4322-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4322-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e4322-112">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4322-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e4322-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e4322-113">Return code</span></span>                                                                             | <span data-ttu-id="e4322-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4322-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e4322-115"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="e4322-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e4322-116">O PIN não foi conectado.</span><span class="sxs-lookup"><span data-stu-id="e4322-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="e4322-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4322-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e4322-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="e4322-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="e4322-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4322-119">Remarks</span></span>

<span data-ttu-id="e4322-120">Esse método substitui o método [**CBasePin::D isconnect**](cbasepin-disconnect.md) para habilitar a desconexão enquanto o filtro está ativo.</span><span class="sxs-lookup"><span data-stu-id="e4322-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4322-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4322-121">Requirements</span></span>



| <span data-ttu-id="e4322-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4322-122">Requirement</span></span> | <span data-ttu-id="e4322-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e4322-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4322-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4322-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e4322-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4322-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4322-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4322-126">Library</span></span><br/> | <dl> <span data-ttu-id="e4322-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e4322-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4322-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4322-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4322-129">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="e4322-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





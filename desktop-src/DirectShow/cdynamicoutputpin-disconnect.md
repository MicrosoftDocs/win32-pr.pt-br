---
description: Método CDynamicOutputPin. Disconnect – o método Disconnect quebra a conexão do PIN atual. Esse método implementa o método IPin::D isconnect.
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
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099294"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="d53f1-104">Método CDynamicOutputPin. Disconnect</span><span class="sxs-lookup"><span data-stu-id="d53f1-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="d53f1-105">O `Disconnect` método quebra a conexão do PIN atual.</span><span class="sxs-lookup"><span data-stu-id="d53f1-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="d53f1-106">Esse método implementa o método [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="d53f1-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d53f1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d53f1-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="d53f1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d53f1-108">Parameters</span></span>

<span data-ttu-id="d53f1-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d53f1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d53f1-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d53f1-110">Return value</span></span>

<span data-ttu-id="d53f1-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d53f1-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d53f1-112">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d53f1-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d53f1-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d53f1-113">Return code</span></span>                                                                             | <span data-ttu-id="d53f1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d53f1-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d53f1-115"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="d53f1-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d53f1-116">O PIN não foi conectado.</span><span class="sxs-lookup"><span data-stu-id="d53f1-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="d53f1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d53f1-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d53f1-118">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="d53f1-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="d53f1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d53f1-119">Remarks</span></span>

<span data-ttu-id="d53f1-120">Esse método substitui o método [**CBasePin::D isconnect**](cbasepin-disconnect.md) para habilitar a desconexão enquanto o filtro está ativo.</span><span class="sxs-lookup"><span data-stu-id="d53f1-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="d53f1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d53f1-121">Requirements</span></span>



| <span data-ttu-id="d53f1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d53f1-122">Requirement</span></span> | <span data-ttu-id="d53f1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d53f1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d53f1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d53f1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d53f1-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d53f1-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d53f1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d53f1-126">Library</span></span><br/> | <dl> <span data-ttu-id="d53f1-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d53f1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d53f1-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d53f1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d53f1-129">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="d53f1-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





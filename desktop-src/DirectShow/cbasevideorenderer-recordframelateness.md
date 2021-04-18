---
description: O método RecordFrameLateness registra a hora em que a renderização ocorreu e coleta estatísticas para a página de propriedades.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Método CBaseVideoRenderer. RecordFrameLateness (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789717"
---
# <a name="cbasevideorendererrecordframelateness-method"></a><span data-ttu-id="c4aae-103">Método CBaseVideoRenderer. RecordFrameLateness</span><span class="sxs-lookup"><span data-stu-id="c4aae-103">CBaseVideoRenderer.RecordFrameLateness method</span></span>

<span data-ttu-id="c4aae-104">O `RecordFrameLateness` método registra a hora em que a renderização ocorreu e coleta estatísticas para a página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c4aae-104">The `RecordFrameLateness` method records how timely the rendering occurred and gathers statistics for the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4aae-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4aae-105">Syntax</span></span>


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="c4aae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4aae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4aae-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="c4aae-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="c4aae-108">Valor que indica o quão tarde o exemplo estava além do tempo de vida, em unidades de tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="c4aae-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="c4aae-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="c4aae-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="c4aae-110">Tempo entre quadros, em unidades de tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="c4aae-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4aae-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4aae-111">Return value</span></span>

<span data-ttu-id="c4aae-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c4aae-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4aae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4aae-113">Requirements</span></span>



| <span data-ttu-id="c4aae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4aae-114">Requirement</span></span> | <span data-ttu-id="c4aae-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c4aae-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4aae-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4aae-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c4aae-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4aae-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c4aae-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4aae-118">Library</span></span><br/> | <dl> <span data-ttu-id="c4aae-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c4aae-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4aae-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4aae-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4aae-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="c4aae-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





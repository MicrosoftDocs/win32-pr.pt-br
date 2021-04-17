---
description: Sinalizador que indica se o filtro enviou uma notificação de fim de fluxo.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Membro CTransformFilter:: m_bEOSDelivered (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747373"
---
# <a name="ctransformfilterm_beosdelivered-member"></a><span data-ttu-id="5eaaf-103">Membro de CTransformFilter:: m \_ bEOSDelivered</span><span class="sxs-lookup"><span data-stu-id="5eaaf-103">CTransformFilter::m\_bEOSDelivered member</span></span>

<span data-ttu-id="5eaaf-104">Sinalizador que indica se o filtro enviou uma notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="5eaaf-104">Flag that indicates whether the filter has sent an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eaaf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5eaaf-105">Syntax</span></span>


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a><span data-ttu-id="5eaaf-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="5eaaf-106">Remarks</span></span>

<span data-ttu-id="5eaaf-107">Se o filtro for pausado quando não tiver uma conexão de entrada, ele enviará um downstream de notificação de fim de fluxo e definirá esse sinalizador como **true**.</span><span class="sxs-lookup"><span data-stu-id="5eaaf-107">If the filter pauses when it does not have an input connection, it sends an end-of-stream notification downstream and sets this flag to **TRUE**.</span></span> <span data-ttu-id="5eaaf-108">A notificação de fim de fluxo garante que o filtro downstream não espere por exemplos.</span><span class="sxs-lookup"><span data-stu-id="5eaaf-108">The end-of-stream notification ensures that the downstream filter does not wait for samples.</span></span> <span data-ttu-id="5eaaf-109">Observe que o método [**EndOfStream**](ctransformfilter-endofstream.md) do filtro não define esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="5eaaf-109">Note that the filter's [**EndOfStream**](ctransformfilter-endofstream.md) method does not set this flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eaaf-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eaaf-110">Requirements</span></span>



| <span data-ttu-id="5eaaf-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eaaf-111">Requirement</span></span> | <span data-ttu-id="5eaaf-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5eaaf-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eaaf-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5eaaf-113">Header</span></span><br/>  | <dl> <span data-ttu-id="5eaaf-114"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5eaaf-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5eaaf-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5eaaf-115">Library</span></span><br/> | <dl> <span data-ttu-id="5eaaf-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5eaaf-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eaaf-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5eaaf-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eaaf-118">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="5eaaf-118">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





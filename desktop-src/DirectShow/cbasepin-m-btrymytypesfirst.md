---
description: Sinalizador que indica se o PIN tenta seus próprios tipos de mídia preferenciais antes daqueles do PIN de recebimento.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Membro CBasePin:: m_bTryMyTypesFirst (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754561"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a><span data-ttu-id="6e7a1-103">Membro de CBasePin:: m \_ bTryMyTypesFirst</span><span class="sxs-lookup"><span data-stu-id="6e7a1-103">CBasePin::m\_bTryMyTypesFirst member</span></span>

<span data-ttu-id="6e7a1-104">Sinalizador que indica se o PIN tenta seus próprios tipos de mídia preferenciais antes daqueles do PIN de recebimento.</span><span class="sxs-lookup"><span data-stu-id="6e7a1-104">Flag that indicates whether the pin tries its own preferred media types before those of the receiving pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e7a1-105">Syntax</span></span>


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a><span data-ttu-id="6e7a1-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e7a1-106">Remarks</span></span>

<span data-ttu-id="6e7a1-107">Esse sinalizador assume como padrão **false**.</span><span class="sxs-lookup"><span data-stu-id="6e7a1-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="6e7a1-108">Se o sinalizador for **true**, o método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) inverterá a ordem em que ele tenta os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="6e7a1-108">If the flag is **TRUE**, the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method reverses the order in which it tries media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e7a1-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e7a1-109">Requirements</span></span>



| <span data-ttu-id="6e7a1-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e7a1-110">Requirement</span></span> | <span data-ttu-id="6e7a1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="6e7a1-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7a1-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e7a1-112">Header</span></span><br/>  | <dl> <span data-ttu-id="6e7a1-113"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e7a1-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6e7a1-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e7a1-114">Library</span></span><br/> | <dl> <span data-ttu-id="6e7a1-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6e7a1-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e7a1-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e7a1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e7a1-117">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="6e7a1-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





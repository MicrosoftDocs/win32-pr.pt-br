---
description: O método CurrentMediaType recupera o tipo de mídia para a conexão do PIN atual.
ms.assetid: d46f4d8e-9e9d-49d3-b823-f2f0fcf25383
title: Método CTransformInputPin. CurrentMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59feca88e896b2a81a352b693e57ceaa5388d452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810179"
---
# <a name="ctransforminputpincurrentmediatype-method"></a><span data-ttu-id="66b6e-103">Método CTransformInputPin. CurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="66b6e-103">CTransformInputPin.CurrentMediaType method</span></span>

<span data-ttu-id="66b6e-104">O `CurrentMediaType` método recupera o tipo de mídia para a conexão do PIN atual.</span><span class="sxs-lookup"><span data-stu-id="66b6e-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="66b6e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66b6e-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="66b6e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66b6e-106">Parameters</span></span>

<span data-ttu-id="66b6e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="66b6e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66b6e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66b6e-108">Return value</span></span>

<span data-ttu-id="66b6e-109">Retorna uma referência à variável de membro [**CBasePin:: m \_ MT**](cbasepin-m-mt.md) .</span><span class="sxs-lookup"><span data-stu-id="66b6e-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b6e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66b6e-110">Requirements</span></span>



| <span data-ttu-id="66b6e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="66b6e-111">Requirement</span></span> | <span data-ttu-id="66b6e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="66b6e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66b6e-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66b6e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="66b6e-114"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66b6e-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66b6e-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66b6e-115">Library</span></span><br/> | <dl> <span data-ttu-id="66b6e-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="66b6e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





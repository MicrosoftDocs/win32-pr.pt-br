---
description: O \_ método Put CurrentPosition define a posição atual, em relação à duração total do fluxo. Esse método implementa o método IMediaPosition::p UT \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: Método de CPosPassThru.put_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770084"
---
# <a name="cpospassthruput_currentposition-method"></a><span data-ttu-id="6e379-104">Método CPosPassThru. put \_ CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="6e379-104">CPosPassThru.put\_CurrentPosition method</span></span>

<span data-ttu-id="6e379-105">O `put_CurrentPosition` método define a posição atual, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="6e379-105">The `put_CurrentPosition` method sets the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="6e379-106">Esse método implementa o método [**IMediaPosition::p UT \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="6e379-106">This method implements the [**IMediaPosition::put\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e379-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e379-107">Syntax</span></span>


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="6e379-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e379-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e379-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="6e379-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="6e379-110">Nova posição, em segundos.</span><span class="sxs-lookup"><span data-stu-id="6e379-110">New position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e379-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e379-111">Return value</span></span>

<span data-ttu-id="6e379-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="6e379-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e379-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e379-113">Requirements</span></span>



| <span data-ttu-id="6e379-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e379-114">Requirement</span></span> | <span data-ttu-id="6e379-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6e379-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e379-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e379-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6e379-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e379-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6e379-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e379-118">Library</span></span><br/> | <dl> <span data-ttu-id="6e379-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6e379-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e379-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e379-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e379-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="6e379-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





---
description: Método CMediaEvent. GetTypeInfoCount – recupera o número de interfaces de informações de tipo fornecidas por um objeto.
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Método CMediaEvent. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099114"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="c21dc-103">Método CMediaEvent. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="c21dc-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="c21dc-104">Recupera o número de interfaces de informações de tipo fornecidas por um objeto.</span><span class="sxs-lookup"><span data-stu-id="c21dc-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c21dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c21dc-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="c21dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c21dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c21dc-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="c21dc-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c21dc-108">Ponteiro para o número de interfaces de informações de tipo que o objeto fornece.</span><span class="sxs-lookup"><span data-stu-id="c21dc-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="c21dc-109">Se o objeto fornecer informações de tipo, esse número será 1; caso contrário, o número será 0.</span><span class="sxs-lookup"><span data-stu-id="c21dc-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c21dc-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c21dc-110">Return value</span></span>

<span data-ttu-id="c21dc-111">Retorna o \_ ponteiro E se *pctinfo* for inválido; caso contrário, retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c21dc-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="c21dc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c21dc-112">Requirements</span></span>



| <span data-ttu-id="c21dc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c21dc-113">Requirement</span></span> | <span data-ttu-id="c21dc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c21dc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21dc-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c21dc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c21dc-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c21dc-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c21dc-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c21dc-117">Library</span></span><br/> | <dl> <span data-ttu-id="c21dc-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c21dc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c21dc-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c21dc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c21dc-120">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="c21dc-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 





---
description: Recupera o número de interfaces de informações de tipo fornecidas por um objeto.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Método CMediaControl. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764564"
---
# <a name="cmediacontrolgettypeinfocount-method"></a><span data-ttu-id="d2ca5-103">Método CMediaControl. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="d2ca5-103">CMediaControl.GetTypeInfoCount method</span></span>

<span data-ttu-id="d2ca5-104">Recupera o número de interfaces de informações de tipo fornecidas por um objeto.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ca5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2ca5-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="d2ca5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2ca5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ca5-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="d2ca5-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d2ca5-108">Aponta para o número de interfaces de informações de tipo que o objeto fornece.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-108">Pointer to the number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="d2ca5-109">Se o objeto fornecer informações de tipo, esse número será 1; caso contrário, o número será 0.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ca5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2ca5-110">Return value</span></span>

<span data-ttu-id="d2ca5-111">Retorna o \_ ponteiro E se *pctinfo* for inválido; caso contrário, retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ca5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2ca5-112">Requirements</span></span>



| <span data-ttu-id="d2ca5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2ca5-113">Requirement</span></span> | <span data-ttu-id="d2ca5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d2ca5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ca5-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2ca5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d2ca5-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2ca5-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d2ca5-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2ca5-117">Library</span></span><br/> | <dl> <span data-ttu-id="d2ca5-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d2ca5-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2ca5-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2ca5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ca5-120">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="d2ca5-120">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 





---
description: O método GetTypeInfoCount recupera o número de interfaces de informações de tipo que o objeto fornece.
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: Método CMediaPosition. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cac543c49b7f2f6b9dc3357bbb1c691477d9b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775636"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="ff53b-103">Método CMediaPosition. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="ff53b-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="ff53b-104">O `GetTypeInfoCount` método recupera o número de interfaces de informações de tipo que o objeto fornece.</span><span class="sxs-lookup"><span data-stu-id="ff53b-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff53b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff53b-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="ff53b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff53b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff53b-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="ff53b-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ff53b-108">Ponteiro para uma variável que recebe o número de interfaces de informações de tipo fornecidas pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="ff53b-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="ff53b-109">Quando o método retorna, o valor é 1.</span><span class="sxs-lookup"><span data-stu-id="ff53b-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff53b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff53b-110">Return value</span></span>

<span data-ttu-id="ff53b-111">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff53b-111">Returns one of the following values.</span></span>



| <span data-ttu-id="ff53b-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ff53b-112">Return code</span></span>                                                                               | <span data-ttu-id="ff53b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff53b-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ff53b-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ff53b-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="ff53b-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ff53b-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="ff53b-116"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ff53b-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="ff53b-117">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ff53b-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ff53b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff53b-118">Requirements</span></span>



| <span data-ttu-id="ff53b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff53b-119">Requirement</span></span> | <span data-ttu-id="ff53b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ff53b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff53b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff53b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ff53b-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff53b-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff53b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff53b-123">Library</span></span><br/> | <dl> <span data-ttu-id="ff53b-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ff53b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff53b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff53b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff53b-126">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="ff53b-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 





---
description: Método CMediaPosition. GetTypeInfoCount – o método GetTypeInfoCount recupera o número de interfaces de informações de tipo que o objeto fornece.
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
ms.openlocfilehash: 8cfc54f414a6722f7f69a0330fad2d1a0cfab425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095474"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="6cc80-103">Método CMediaPosition. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="6cc80-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="6cc80-104">O `GetTypeInfoCount` método recupera o número de interfaces de informações de tipo que o objeto fornece.</span><span class="sxs-lookup"><span data-stu-id="6cc80-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc80-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cc80-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="6cc80-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cc80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc80-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="6cc80-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc80-108">Ponteiro para uma variável que recebe o número de interfaces de informações de tipo fornecidas pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="6cc80-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="6cc80-109">Quando o método retorna, o valor é 1.</span><span class="sxs-lookup"><span data-stu-id="6cc80-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc80-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6cc80-110">Return value</span></span>

<span data-ttu-id="6cc80-111">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6cc80-111">Returns one of the following values.</span></span>



| <span data-ttu-id="6cc80-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6cc80-112">Return code</span></span>                                                                               | <span data-ttu-id="6cc80-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cc80-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6cc80-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6cc80-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="6cc80-115">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="6cc80-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="6cc80-116"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="6cc80-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="6cc80-117">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="6cc80-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6cc80-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cc80-118">Requirements</span></span>



| <span data-ttu-id="6cc80-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cc80-119">Requirement</span></span> | <span data-ttu-id="6cc80-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6cc80-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc80-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cc80-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6cc80-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cc80-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6cc80-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cc80-123">Library</span></span><br/> | <dl> <span data-ttu-id="6cc80-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6cc80-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cc80-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6cc80-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc80-126">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="6cc80-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 





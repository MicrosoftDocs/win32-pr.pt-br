---
description: Método CBaseDispatch. GetTypeInfoCount – o método GetTypeInfoCount recupera o número de interfaces de informações de tipo que o objeto fornece.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Método CBaseDispatch. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e68c94420b3d7715845f8d6bd14e26b770b44f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099884"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="95f07-103">Método CBaseDispatch. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="95f07-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="95f07-104">O `GetTypeInfoCount` método recupera o número de interfaces de informações de tipo que o objeto fornece.</span><span class="sxs-lookup"><span data-stu-id="95f07-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95f07-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="95f07-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95f07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95f07-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="95f07-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="95f07-108">Ponteiro para uma variável que recebe o número de interfaces de informações de tipo fornecidas pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="95f07-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="95f07-109">Quando o método retorna, o valor é 1.</span><span class="sxs-lookup"><span data-stu-id="95f07-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95f07-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="95f07-110">Return value</span></span>

<span data-ttu-id="95f07-111">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="95f07-111">Returns one of the following values.</span></span>



| <span data-ttu-id="95f07-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="95f07-112">Return code</span></span>                                                                               | <span data-ttu-id="95f07-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="95f07-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="95f07-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95f07-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="95f07-115">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="95f07-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="95f07-116"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="95f07-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="95f07-117">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="95f07-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="95f07-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95f07-118">Requirements</span></span>



| <span data-ttu-id="95f07-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="95f07-119">Requirement</span></span> | <span data-ttu-id="95f07-120">Valor</span><span class="sxs-lookup"><span data-stu-id="95f07-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f07-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95f07-121">Header</span></span><br/>  | <dl> <span data-ttu-id="95f07-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95f07-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95f07-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95f07-123">Library</span></span><br/> | <dl> <span data-ttu-id="95f07-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="95f07-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95f07-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="95f07-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f07-126">**Classe CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="95f07-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 





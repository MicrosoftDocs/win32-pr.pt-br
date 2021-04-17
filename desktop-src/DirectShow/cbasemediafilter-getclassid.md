---
description: 'O método GetClassID recupera o identificador de classe. Esse método implementa o método IPersist:: GetClassID.'
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Método CBaseMediaFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748226"
---
# <a name="cbasemediafiltergetclassid-method"></a><span data-ttu-id="3b978-104">Método CBaseMediaFilter. GetClassID</span><span class="sxs-lookup"><span data-stu-id="3b978-104">CBaseMediaFilter.GetClassID method</span></span>

<span data-ttu-id="3b978-105">O `GetClassID` método recupera o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="3b978-105">The `GetClassID` method retrieves the class identifier.</span></span> <span data-ttu-id="3b978-106">Esse método implementa o método **IPersist:: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="3b978-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b978-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b978-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="3b978-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b978-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b978-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="3b978-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="3b978-110">Ponteiro para uma variável que recebe o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="3b978-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b978-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b978-111">Return value</span></span>

<span data-ttu-id="3b978-112">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3b978-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b978-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b978-113">Requirements</span></span>



| <span data-ttu-id="3b978-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b978-114">Requirement</span></span> | <span data-ttu-id="3b978-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3b978-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b978-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b978-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3b978-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b978-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3b978-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b978-118">Library</span></span><br/> | <dl> <span data-ttu-id="3b978-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3b978-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b978-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b978-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b978-121">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="3b978-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 





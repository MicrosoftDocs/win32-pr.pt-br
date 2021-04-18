---
description: O método GetOwner Recupera um ponteiro para a interface IUnknown do componente proprietário. Para um componente agregado, o proprietário é o componente externo. Caso contrário, o componente pertence a si mesmo.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Método CUnknown. getproprietário (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749609"
---
# <a name="cunknowngetowner-method"></a><span data-ttu-id="91c33-105">Método CUnknown. GetOwner</span><span class="sxs-lookup"><span data-stu-id="91c33-105">CUnknown.GetOwner method</span></span>

<span data-ttu-id="91c33-106">O `GetOwner` método recupera um ponteiro para a interface **IUnknown** do componente proprietário.</span><span class="sxs-lookup"><span data-stu-id="91c33-106">The `GetOwner` method retrieves a pointer to the **IUnknown** interface of the owning component.</span></span> <span data-ttu-id="91c33-107">Para um componente agregado, o proprietário é o componente externo.</span><span class="sxs-lookup"><span data-stu-id="91c33-107">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="91c33-108">Caso contrário, o componente pertence a si mesmo.</span><span class="sxs-lookup"><span data-stu-id="91c33-108">Otherwise, the component owns itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c33-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91c33-109">Syntax</span></span>


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a><span data-ttu-id="91c33-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91c33-110">Parameters</span></span>

<span data-ttu-id="91c33-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="91c33-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91c33-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91c33-112">Return value</span></span>

<span data-ttu-id="91c33-113">Retorna um ponteiro para a interface **IUnknown** de controle.</span><span class="sxs-lookup"><span data-stu-id="91c33-113">Returns a pointer to the controlling **IUnknown** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c33-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91c33-114">Requirements</span></span>



| <span data-ttu-id="91c33-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="91c33-115">Requirement</span></span> | <span data-ttu-id="91c33-116">Valor</span><span class="sxs-lookup"><span data-stu-id="91c33-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c33-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91c33-117">Header</span></span><br/>  | <dl> <span data-ttu-id="91c33-118"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91c33-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="91c33-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91c33-119">Library</span></span><br/> | <dl> <span data-ttu-id="91c33-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="91c33-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





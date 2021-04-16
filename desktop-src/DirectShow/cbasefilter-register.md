---
description: O método Register adiciona o filtro ao registro.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: Método CBaseFilter. Register (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750898"
---
# <a name="cbasefilterregister-method"></a><span data-ttu-id="93cd9-103">Método CBaseFilter. Register</span><span class="sxs-lookup"><span data-stu-id="93cd9-103">CBaseFilter.Register method</span></span>

<span data-ttu-id="93cd9-104">O `Register` método adiciona o filtro ao registro.</span><span class="sxs-lookup"><span data-stu-id="93cd9-104">The `Register` method adds the filter to the registry.</span></span>

> [!Note]  
> <span data-ttu-id="93cd9-105">Esse método é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="93cd9-105">This method is obsolete.</span></span> <span data-ttu-id="93cd9-106">Novos filtros devem ser registrados usando a função [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="93cd9-106">New filters should be registered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="93cd9-107">Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="93cd9-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="93cd9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93cd9-108">Syntax</span></span>


```C++
HRESULT Register();
```



## <a name="parameters"></a><span data-ttu-id="93cd9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93cd9-109">Parameters</span></span>

<span data-ttu-id="93cd9-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="93cd9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93cd9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93cd9-111">Return value</span></span>

<span data-ttu-id="93cd9-112">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="93cd9-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="93cd9-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="93cd9-113">Return code</span></span>                                                                             | <span data-ttu-id="93cd9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="93cd9-114">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="93cd9-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="93cd9-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="93cd9-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="93cd9-116">Success.</span></span><br/>                                  |
| <dl> <span data-ttu-id="93cd9-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="93cd9-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="93cd9-118">Não há informações de registro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="93cd9-118">No registration information is available.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="93cd9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93cd9-119">Requirements</span></span>



| <span data-ttu-id="93cd9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="93cd9-120">Requirement</span></span> | <span data-ttu-id="93cd9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="93cd9-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93cd9-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93cd9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="93cd9-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93cd9-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="93cd9-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93cd9-124">Library</span></span><br/> | <dl> <span data-ttu-id="93cd9-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="93cd9-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93cd9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="93cd9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93cd9-127">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="93cd9-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





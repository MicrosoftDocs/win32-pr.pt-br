---
description: Obsoleto. Use AMovieSetupRegisterFilter2 em vez disso.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Função AMovieSetupRegisterFilter (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785506"
---
# <a name="amoviesetupregisterfilter-function"></a><span data-ttu-id="802d8-104">Função AMovieSetupRegisterFilter</span><span class="sxs-lookup"><span data-stu-id="802d8-104">AMovieSetupRegisterFilter function</span></span>

<span data-ttu-id="802d8-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="802d8-105">Obsolete.</span></span> <span data-ttu-id="802d8-106">Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="802d8-106">Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="802d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="802d8-107">Syntax</span></span>


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="802d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="802d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="802d8-109">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="802d8-109">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="802d8-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="802d8-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="802d8-111">*pIFM*</span><span class="sxs-lookup"><span data-stu-id="802d8-111">*pIFM*</span></span> 
</dt> <dd>

<span data-ttu-id="802d8-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="802d8-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="802d8-113">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="802d8-113">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="802d8-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="802d8-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="802d8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="802d8-115">Return value</span></span>

<span data-ttu-id="802d8-116">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="802d8-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="802d8-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="802d8-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="802d8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="802d8-118">Requirements</span></span>



| <span data-ttu-id="802d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="802d8-119">Requirement</span></span> | <span data-ttu-id="802d8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="802d8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="802d8-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="802d8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="802d8-122"><dt>Dllsetup. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="802d8-122"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="802d8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="802d8-123">Library</span></span><br/> | <dl> <span data-ttu-id="802d8-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="802d8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="802d8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="802d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="802d8-126">**Funções de instalação de DLL**</span><span class="sxs-lookup"><span data-stu-id="802d8-126">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 





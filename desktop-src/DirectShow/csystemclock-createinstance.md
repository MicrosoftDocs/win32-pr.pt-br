---
description: O método CreateInstance cria uma nova instância desse objeto.
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Método CSystemClock. CreateInstance (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 264997448aea028c5725d207ce4b301d369a092c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752887"
---
# <a name="csystemclockcreateinstance-method"></a><span data-ttu-id="7203e-103">Método CSystemClock. CreateInstance</span><span class="sxs-lookup"><span data-stu-id="7203e-103">CSystemClock.CreateInstance method</span></span>

<span data-ttu-id="7203e-104">O `CreateInstance` método cria uma nova instância desse objeto.</span><span class="sxs-lookup"><span data-stu-id="7203e-104">The `CreateInstance` method creates a new instance of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7203e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7203e-105">Syntax</span></span>


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="7203e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7203e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7203e-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="7203e-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="7203e-108">Ponteiro para a interface **IUnknown** de agregação.</span><span class="sxs-lookup"><span data-stu-id="7203e-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="7203e-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="7203e-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7203e-110">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="7203e-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7203e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7203e-111">Return value</span></span>

<span data-ttu-id="7203e-112">Retorna um ponteiro para uma nova instância desse objeto.</span><span class="sxs-lookup"><span data-stu-id="7203e-112">Returns a pointer to a new instance of this object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7203e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7203e-113">Remarks</span></span>

<span data-ttu-id="7203e-114">A fábrica de classes chama esse método para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="7203e-114">The class factory calls this method to create the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7203e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7203e-115">Requirements</span></span>



| <span data-ttu-id="7203e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7203e-116">Requirement</span></span> | <span data-ttu-id="7203e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7203e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7203e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7203e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7203e-119"><dt>Sysclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7203e-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7203e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7203e-120">Library</span></span><br/> | <dl> <span data-ttu-id="7203e-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7203e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





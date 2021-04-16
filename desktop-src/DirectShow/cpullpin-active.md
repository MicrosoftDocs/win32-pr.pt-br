---
description: O método ativo cria um thread de trabalho que efetua pull dos dados do pino de saída. Esse método também confirma o alocador.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Método CPullPin. Active (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750467"
---
# <a name="cpullpinactive-method"></a><span data-ttu-id="0eccb-104">Método CPullPin. active</span><span class="sxs-lookup"><span data-stu-id="0eccb-104">CPullPin.Active method</span></span>

<span data-ttu-id="0eccb-105">O método **ativo** cria um thread de trabalho que efetua pull dos dados do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="0eccb-105">The **Active** method creates a worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="0eccb-106">Esse método também confirma o alocador.</span><span class="sxs-lookup"><span data-stu-id="0eccb-106">This method also commits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eccb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0eccb-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="0eccb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0eccb-108">Parameters</span></span>

<span data-ttu-id="0eccb-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0eccb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0eccb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0eccb-110">Return value</span></span>

<span data-ttu-id="0eccb-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0eccb-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0eccb-112">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="0eccb-112">Possible values include the following.</span></span>



| <span data-ttu-id="0eccb-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0eccb-113">Return code</span></span>                                                                                  | <span data-ttu-id="0eccb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0eccb-114">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="0eccb-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0eccb-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0eccb-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0eccb-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="0eccb-117"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="0eccb-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="0eccb-118">A conexão do PIN não foi estabelecida corretamente.</span><span class="sxs-lookup"><span data-stu-id="0eccb-118">The pin connection was not established correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="0eccb-119"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="0eccb-119"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="0eccb-120">Não foi possível criar o thread ou o thread já existe.</span><span class="sxs-lookup"><span data-stu-id="0eccb-120">Could not create the thread, or the thread already exists.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0eccb-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0eccb-121">Remarks</span></span>

<span data-ttu-id="0eccb-122">Chame esse método quando o filtro proprietário se tornar ativo.</span><span class="sxs-lookup"><span data-stu-id="0eccb-122">Call this method when the owning filter becomes active.</span></span> <span data-ttu-id="0eccb-123">(Se o PIN de entrada deriva de [**CBasePin**](cbasepin.md), substitua o método [**CBasePin:: active**](cbasepin-active.md) .)</span><span class="sxs-lookup"><span data-stu-id="0eccb-123">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Active**](cbasepin-active.md) method.)</span></span>

<span data-ttu-id="0eccb-124">Antes de chamar esse método, chame o método [**CPullPin:: Connect**](cpullpin-connect.md) para estabelecer a conexão com o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="0eccb-124">Before calling this method, call the [**CPullPin::Connect**](cpullpin-connect.md) method to establish the connection with the output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eccb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0eccb-125">Requirements</span></span>



| <span data-ttu-id="0eccb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eccb-126">Requirement</span></span> | <span data-ttu-id="0eccb-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0eccb-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eccb-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0eccb-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0eccb-129"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eccb-129"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="0eccb-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0eccb-130">Library</span></span><br/> | <dl> <span data-ttu-id="0eccb-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0eccb-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eccb-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0eccb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eccb-133">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="0eccb-133">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 





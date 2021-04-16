---
description: O método Invoke fornece acesso a métodos e propriedades expostas por um objeto.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Método CDeferredCommand. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759144"
---
# <a name="cdeferredcommandinvoke-method"></a><span data-ttu-id="3f2fd-103">Método CDeferredCommand. Invoke</span><span class="sxs-lookup"><span data-stu-id="3f2fd-103">CDeferredCommand.Invoke method</span></span>

<span data-ttu-id="3f2fd-104">O `Invoke` método fornece acesso a métodos e propriedades expostas por um objeto.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-104">The `Invoke` method provides access to methods and properties exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f2fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f2fd-105">Syntax</span></span>


```C++
HRESULT Invoke();
```



## <a name="parameters"></a><span data-ttu-id="3f2fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f2fd-106">Parameters</span></span>

<span data-ttu-id="3f2fd-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f2fd-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f2fd-108">Return value</span></span>

<span data-ttu-id="3f2fd-109">Retornará VFW \_ E \_ já \_ cancelado se **m \_ pQueue** for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="3f2fd-110">Caso contrário, retorna o **HRESULT** resultante de uma chamada para **IDispatch:: GetTypeInfo** ou **IUnknown:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-110">Otherwise, returns the **HRESULT** resulting from a call to **IDispatch::GetTypeInfo** or **IUnknown::QueryInterface**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f2fd-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f2fd-111">Requirements</span></span>



| <span data-ttu-id="3f2fd-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f2fd-112">Requirement</span></span> | <span data-ttu-id="3f2fd-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3f2fd-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f2fd-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f2fd-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3f2fd-115"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f2fd-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3f2fd-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f2fd-116">Library</span></span><br/> | <dl> <span data-ttu-id="3f2fd-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3f2fd-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f2fd-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f2fd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2fd-119">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="3f2fd-119">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 





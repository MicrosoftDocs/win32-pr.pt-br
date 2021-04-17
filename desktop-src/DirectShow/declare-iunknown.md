---
description: A \_ macro declare IUnknown declara os três métodos da interface base para uma nova interface.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747577"
---
# <a name="declare_iunknown"></a><span data-ttu-id="ce41f-103">DECLARAR \_ IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce41f-103">DECLARE\_IUNKNOWN</span></span>

<span data-ttu-id="ce41f-104">A macro **Declare \_ IUnknown** declara os três métodos da interface base para uma nova interface.</span><span class="sxs-lookup"><span data-stu-id="ce41f-104">The **DECLARE\_IUNKNOWN** macro declares the three methods of the base interface for a new interface.</span></span>

<span data-ttu-id="ce41f-105">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="ce41f-105">**Syntax**</span></span>

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a><span data-ttu-id="ce41f-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce41f-106">Remarks</span></span>

<span data-ttu-id="ce41f-107">Quando você cria uma nova interface, ela deve derivar de **IUnknown**, que tem três métodos: **QueryInterface**, **AddRef** e **Release**.</span><span class="sxs-lookup"><span data-stu-id="ce41f-107">When you create a new interface, it must derive from **IUnknown**, which has three methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="ce41f-108">Essa macro simplifica o processo de declaração declarando cada um desses métodos para a nova interface.</span><span class="sxs-lookup"><span data-stu-id="ce41f-108">This macro simplifies the declaration process by declaring each of these methods for the new interface.</span></span>

<span data-ttu-id="ce41f-109">Essa macro funciona apenas com classes que derivam, direta ou indiretamente, da classe [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ce41f-109">This macro works only with classes that derive, directly or indirectly, from the [**CUnknown**](cunknown.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce41f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce41f-110">Requirements</span></span>



| <span data-ttu-id="ce41f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce41f-111">Requirement</span></span> | <span data-ttu-id="ce41f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ce41f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce41f-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce41f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ce41f-114"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce41f-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce41f-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce41f-115">Library</span></span><br/> | <dl> <span data-ttu-id="ce41f-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ce41f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce41f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce41f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce41f-118">**Funções auxiliares COM**</span><span class="sxs-lookup"><span data-stu-id="ce41f-118">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="ce41f-119">**CUnknown:: GetOwner**</span><span class="sxs-lookup"><span data-stu-id="ce41f-119">**CUnknown::GetOwner**</span></span>](cunknown-getowner.md)
</dt> <dt>

[<span data-ttu-id="ce41f-120">Como implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce41f-120">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 





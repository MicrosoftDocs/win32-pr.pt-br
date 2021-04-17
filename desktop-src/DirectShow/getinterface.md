---
description: A função GetInterface recupera um ponteiro de interface.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: Função GetInterface (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785345"
---
# <a name="getinterface-function"></a><span data-ttu-id="ac211-103">Função GetInterface</span><span class="sxs-lookup"><span data-stu-id="ac211-103">GetInterface function</span></span>

<span data-ttu-id="ac211-104">A `GetInterface` função recupera um ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="ac211-104">The `GetInterface` function retrieves an interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac211-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac211-105">Syntax</span></span>


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="ac211-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac211-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac211-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ac211-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ac211-108">Ponteiro para a interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="ac211-108">Pointer to the **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="ac211-109">*ppv*</span><span class="sxs-lookup"><span data-stu-id="ac211-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="ac211-110">Endereço de um ponteiro para a interface recuperada.</span><span class="sxs-lookup"><span data-stu-id="ac211-110">Address of a pointer to the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac211-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac211-111">Return value</span></span>

<span data-ttu-id="ac211-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac211-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac211-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac211-113">Remarks</span></span>

<span data-ttu-id="ac211-114">Essa função de membro executa um incremento thread-safe da contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="ac211-114">This member function performs a thread-safe increment of the reference count.</span></span> <span data-ttu-id="ac211-115">Para recuperar a interface e adicionar uma referência, chame essa função de sua implementação de substituição do método **INonDelegatingUnknown:: NonDelegatingQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="ac211-115">To retrieve the interface and add a reference, call this function from your overriding implementation of the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac211-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac211-116">Requirements</span></span>



| <span data-ttu-id="ac211-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac211-117">Requirement</span></span> | <span data-ttu-id="ac211-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ac211-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac211-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac211-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ac211-120"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac211-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ac211-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac211-121">Library</span></span><br/> | <dl> <span data-ttu-id="ac211-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ac211-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac211-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac211-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac211-124">**Funções auxiliares COM**</span><span class="sxs-lookup"><span data-stu-id="ac211-124">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="ac211-125">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="ac211-125">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md)
</dt> </dl>

 

 





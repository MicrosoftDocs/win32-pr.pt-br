---
description: Ponteiro para uma função que cria uma instância do objeto.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Ponteiro de função LPFNNewCOMObject (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759434"
---
# <a name="lpfnnewcomobject-function-pointer"></a><span data-ttu-id="d540e-103">Ponteiro de função LPFNNewCOMObject</span><span class="sxs-lookup"><span data-stu-id="d540e-103">LPFNNewCOMObject function pointer</span></span>

<span data-ttu-id="d540e-104">Ponteiro para uma função que cria uma instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="d540e-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d540e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d540e-105">Syntax</span></span>


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="d540e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d540e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d540e-107">*pUnkOuter*</span><span class="sxs-lookup"><span data-stu-id="d540e-107">*pUnkOuter*</span></span> 
</dt> <dd>

<span data-ttu-id="d540e-108">Ponteiro para a interface **IUnknown** do objeto que agrega o novo objeto, se houver.</span><span class="sxs-lookup"><span data-stu-id="d540e-108">Pointer to the **IUnknown** interface of the object that aggregates the new object, if any.</span></span> <span data-ttu-id="d540e-109">Esse ponteiro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d540e-109">This pointer can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d540e-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="d540e-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d540e-111">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d540e-111">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="d540e-112">Se o Construtor falhar, esse parâmetro receberá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="d540e-112">If the constructor fails, this parameter receives an error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d540e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d540e-113">Return value</span></span>

<span data-ttu-id="d540e-114">Retorna um ponteiro para uma nova instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="d540e-114">Returns a pointer to a new instance of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d540e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d540e-115">Requirements</span></span>



| <span data-ttu-id="d540e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d540e-116">Requirement</span></span> | <span data-ttu-id="d540e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d540e-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d540e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d540e-118">Header</span></span><br/> | <dl> <span data-ttu-id="d540e-119"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d540e-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d540e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d540e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d540e-121">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="d540e-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 





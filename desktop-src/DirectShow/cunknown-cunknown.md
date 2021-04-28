---
description: Construtor de CUnknown. CUnknown-método de construtor.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Construtor CUnknown. CUnknown (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084604"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="4361f-103">Construtor CUnknown. CUnknown</span><span class="sxs-lookup"><span data-stu-id="4361f-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="4361f-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="4361f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4361f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4361f-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="4361f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4361f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4361f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="4361f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="4361f-108">Cadeia de caracteres que contém o nome do objeto; usado no construtor [**CBaseObject**](cbaseobject.md) para depuração.</span><span class="sxs-lookup"><span data-stu-id="4361f-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="4361f-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="4361f-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4361f-110">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="4361f-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="4361f-111">Se o objeto for agregado, passe um ponteiro para a interface IUnknown do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="4361f-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="4361f-112">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4361f-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4361f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4361f-113">Remarks</span></span>

<span data-ttu-id="4361f-114">O objeto é inicializado com uma contagem de referência igual a zero.</span><span class="sxs-lookup"><span data-stu-id="4361f-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4361f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4361f-115">Requirements</span></span>



| <span data-ttu-id="4361f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4361f-116">Requirement</span></span> | <span data-ttu-id="4361f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4361f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4361f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4361f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4361f-119"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4361f-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4361f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4361f-120">Library</span></span><br/> | <dl> <span data-ttu-id="4361f-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4361f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





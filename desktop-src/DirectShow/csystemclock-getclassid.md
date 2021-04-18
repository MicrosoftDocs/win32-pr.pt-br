---
description: 'O método GetClassID recupera o identificador de classe (CLSID) do objeto. Esse método implementa o método IPersist:: GetClassID.'
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Método CSystemClock. GetClassID (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749828"
---
# <a name="csystemclockgetclassid-method"></a><span data-ttu-id="918fe-104">Método CSystemClock. GetClassID</span><span class="sxs-lookup"><span data-stu-id="918fe-104">CSystemClock.GetClassID method</span></span>

<span data-ttu-id="918fe-105">O `GetClassID` método recupera o identificador de classe (CLSID) do objeto.</span><span class="sxs-lookup"><span data-stu-id="918fe-105">The `GetClassID` method retrieves the class identifier (CLSID) of the object.</span></span> <span data-ttu-id="918fe-106">Esse método implementa o método **IPersist:: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="918fe-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="918fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="918fe-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="918fe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="918fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="918fe-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="918fe-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="918fe-110">Ponteiro para uma variável que recebe o valor CLSID \_ SystemClock.</span><span class="sxs-lookup"><span data-stu-id="918fe-110">Pointer to a variable that receives the value CLSID\_SystemClock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="918fe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="918fe-111">Return value</span></span>

<span data-ttu-id="918fe-112">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="918fe-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="918fe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="918fe-113">Requirements</span></span>



| <span data-ttu-id="918fe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="918fe-114">Requirement</span></span> | <span data-ttu-id="918fe-115">Valor</span><span class="sxs-lookup"><span data-stu-id="918fe-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="918fe-116">Versão</span><span class="sxs-lookup"><span data-stu-id="918fe-116">Version</span></span><br/> | <span data-ttu-id="918fe-117">Classe CSystemClock</span><span class="sxs-lookup"><span data-stu-id="918fe-117">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="918fe-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="918fe-118">Header</span></span><br/>  | <dl> <span data-ttu-id="918fe-119"><dt>Sysclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="918fe-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="918fe-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="918fe-120">Library</span></span><br/> | <dl> <span data-ttu-id="918fe-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="918fe-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





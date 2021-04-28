---
description: Construtor de CSeekingPassThru. CSeekingPassThru-método de construtor.
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Construtor CSeekingPassThru. CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cab9d6329f5175c96a3bfc5962ca5a555fe62b5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085374"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="8663f-103">Construtor CSeekingPassThru. CSeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="8663f-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="8663f-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="8663f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8663f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8663f-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="8663f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8663f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8663f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="8663f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="8663f-108">Cadeia de caracteres que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="8663f-108">String containing the name of the object.</span></span> <span data-ttu-id="8663f-109">Consulte [**CBaseObject**](cbaseobject.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8663f-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="8663f-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="8663f-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8663f-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="8663f-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="8663f-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="8663f-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="8663f-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8663f-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8663f-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="8663f-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8663f-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8663f-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="8663f-116">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="8663f-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8663f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8663f-117">Requirements</span></span>



| <span data-ttu-id="8663f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8663f-118">Requirement</span></span> | <span data-ttu-id="8663f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8663f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8663f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8663f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8663f-121"><dt>Seekpt. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8663f-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8663f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8663f-122">Library</span></span><br/> | <dl> <span data-ttu-id="8663f-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8663f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8663f-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8663f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8663f-125">**Classe CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="8663f-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 





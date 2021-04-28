---
description: Construtor de CMediaEvent. CMediaEvent-método de construtor.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Construtor CMediaEvent. CMediaEvent (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095554"
---
# <a name="cmediaeventcmediaevent-constructor"></a><span data-ttu-id="331fa-103">Construtor CMediaEvent. CMediaEvent</span><span class="sxs-lookup"><span data-stu-id="331fa-103">CMediaEvent.CMediaEvent constructor</span></span>

<span data-ttu-id="331fa-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="331fa-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="331fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="331fa-105">Syntax</span></span>


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="331fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="331fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="331fa-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="331fa-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="331fa-108">Ponteiro para o nome do objeto para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="331fa-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="331fa-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="331fa-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="331fa-110">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="331fa-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="331fa-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="331fa-111">Remarks</span></span>

<span data-ttu-id="331fa-112">Aloque o parâmetro *pname* na memória estática.</span><span class="sxs-lookup"><span data-stu-id="331fa-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="331fa-113">Esse nome aparece no terminal de depuração após a criação e a exclusão do objeto.</span><span class="sxs-lookup"><span data-stu-id="331fa-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="331fa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="331fa-114">Requirements</span></span>



| <span data-ttu-id="331fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="331fa-115">Requirement</span></span> | <span data-ttu-id="331fa-116">Valor</span><span class="sxs-lookup"><span data-stu-id="331fa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="331fa-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="331fa-117">Header</span></span><br/>  | <dl> <span data-ttu-id="331fa-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="331fa-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="331fa-119">Library</span></span><br/> | <dl> <span data-ttu-id="331fa-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="331fa-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="331fa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="331fa-122">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="331fa-122">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 





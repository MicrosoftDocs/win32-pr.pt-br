---
description: Método de construtor.
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Construtor CMediaControl. CMediaControl (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63b965ff2484d4db7f7de41d8d524bc74c31ac73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770095"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a><span data-ttu-id="369d6-103">Construtor CMediaControl. CMediaControl</span><span class="sxs-lookup"><span data-stu-id="369d6-103">CMediaControl.CMediaControl constructor</span></span>

<span data-ttu-id="369d6-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="369d6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="369d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="369d6-105">Syntax</span></span>


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="369d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="369d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="369d6-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="369d6-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="369d6-108">Ponteiro para o nome do objeto para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="369d6-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="369d6-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="369d6-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="369d6-110">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="369d6-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="369d6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="369d6-111">Remarks</span></span>

<span data-ttu-id="369d6-112">Aloque o parâmetro *pname* na memória estática.</span><span class="sxs-lookup"><span data-stu-id="369d6-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="369d6-113">Esse nome aparece no terminal de depuração após a criação e a exclusão do objeto.</span><span class="sxs-lookup"><span data-stu-id="369d6-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="369d6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="369d6-114">Requirements</span></span>



| <span data-ttu-id="369d6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="369d6-115">Requirement</span></span> | <span data-ttu-id="369d6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="369d6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="369d6-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="369d6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="369d6-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="369d6-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="369d6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="369d6-119">Library</span></span><br/> | <dl> <span data-ttu-id="369d6-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="369d6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="369d6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="369d6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="369d6-122">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="369d6-122">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 





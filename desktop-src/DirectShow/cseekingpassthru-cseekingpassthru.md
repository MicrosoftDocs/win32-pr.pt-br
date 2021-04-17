---
description: Método de construtor.
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
ms.openlocfilehash: a93ed9706762b9a1672bfae85550ee4c2aceeead
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787393"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="c3d8d-103">Construtor CSeekingPassThru. CSeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="c3d8d-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="c3d8d-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d8d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3d8d-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="c3d8d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3d8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d8d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="c3d8d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c3d8d-108">Cadeia de caracteres que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-108">String containing the name of the object.</span></span> <span data-ttu-id="c3d8d-109">Consulte [**CBaseObject**](cbaseobject.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c3d8d-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="c3d8d-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c3d8d-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="c3d8d-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="c3d8d-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3d8d-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="c3d8d-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c3d8d-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="c3d8d-116">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3d8d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3d8d-117">Requirements</span></span>



| <span data-ttu-id="c3d8d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3d8d-118">Requirement</span></span> | <span data-ttu-id="c3d8d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c3d8d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d8d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3d8d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c3d8d-121"><dt>Seekpt. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d8d-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c3d8d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3d8d-122">Library</span></span><br/> | <dl> <span data-ttu-id="c3d8d-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d8d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d8d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3d8d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d8d-125">**Classe CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="c3d8d-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 





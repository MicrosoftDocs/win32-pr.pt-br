---
description: Método de construtor.
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: Construtor CRendererPosPassThru. CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97b21ba3ad9438189f97c3e0bb9f011b210a0195
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756185"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a><span data-ttu-id="12f1a-103">Construtor CRendererPosPassThru. CRendererPosPassThru</span><span class="sxs-lookup"><span data-stu-id="12f1a-103">CRendererPosPassThru.CRendererPosPassThru constructor</span></span>

<span data-ttu-id="12f1a-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="12f1a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f1a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12f1a-105">Syntax</span></span>


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="12f1a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12f1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f1a-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="12f1a-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="12f1a-108">Ponteiro para o nome do objeto, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="12f1a-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="12f1a-109">Aloque esse parâmetro na memória estática.</span><span class="sxs-lookup"><span data-stu-id="12f1a-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="12f1a-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="12f1a-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="12f1a-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="12f1a-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="12f1a-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="12f1a-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="12f1a-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="12f1a-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="12f1a-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="12f1a-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="12f1a-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12f1a-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="12f1a-116">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="12f1a-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="12f1a-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="12f1a-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="12f1a-118">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN de entrada do filtro.</span><span class="sxs-lookup"><span data-stu-id="12f1a-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12f1a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12f1a-119">Requirements</span></span>



| <span data-ttu-id="12f1a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12f1a-120">Requirement</span></span> | <span data-ttu-id="12f1a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="12f1a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f1a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12f1a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12f1a-123"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12f1a-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12f1a-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12f1a-124">Library</span></span><br/> | <dl> <span data-ttu-id="12f1a-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="12f1a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





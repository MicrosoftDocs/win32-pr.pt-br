---
description: 'O método SetTimeFormat define o formato de hora. Esse método implementa o método IMediaSeeking:: SetTimeFormat.'
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: Método CPosPassThru. SetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b843e67a827e4bbd7471bb42df31033e314d9158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747381"
---
# <a name="cpospassthrusettimeformat-method"></a><span data-ttu-id="3dfe0-104">Método CPosPassThru. SetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3dfe0-104">CPosPassThru.SetTimeFormat method</span></span>

<span data-ttu-id="3dfe0-105">O método SetTimeFormat define o formato de hora.</span><span class="sxs-lookup"><span data-stu-id="3dfe0-105">The SetTimeFormat method sets the time format.</span></span> <span data-ttu-id="3dfe0-106">Esse método implementa o método [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="3dfe0-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dfe0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3dfe0-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="3dfe0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dfe0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dfe0-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="3dfe0-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3dfe0-110">Ponteiro para um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="3dfe0-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dfe0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3dfe0-111">Return value</span></span>

<span data-ttu-id="3dfe0-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="3dfe0-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dfe0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dfe0-113">Requirements</span></span>



| <span data-ttu-id="3dfe0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dfe0-114">Requirement</span></span> | <span data-ttu-id="3dfe0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3dfe0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dfe0-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3dfe0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3dfe0-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3dfe0-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3dfe0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3dfe0-118">Library</span></span><br/> | <dl> <span data-ttu-id="3dfe0-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3dfe0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dfe0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dfe0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dfe0-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="3dfe0-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="3dfe0-122">**GUIDs de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="3dfe0-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





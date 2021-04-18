---
description: 'O método IsUsingTimeFormat determina se um formato de hora especificado é o formato em uso no momento. Esse método implementa o método IMediaSeeking:: IsUsingTimeFormat.'
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Método CPosPassThru. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 012a9487f5840117edb9f8bc0afa1d9388b4bce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752083"
---
# <a name="cpospassthruisusingtimeformat-method"></a><span data-ttu-id="7ceca-104">Método CPosPassThru. IsUsingTimeFormat</span><span class="sxs-lookup"><span data-stu-id="7ceca-104">CPosPassThru.IsUsingTimeFormat method</span></span>

<span data-ttu-id="7ceca-105">O `IsUsingTimeFormat` método determina se um formato de hora especificado é o formato em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="7ceca-105">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span> <span data-ttu-id="7ceca-106">Esse método implementa o método [**IMediaSeeking:: IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) .</span><span class="sxs-lookup"><span data-stu-id="7ceca-106">This method implements the [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ceca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ceca-107">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="7ceca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ceca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ceca-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="7ceca-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="7ceca-110">Ponteiro para um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="7ceca-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ceca-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ceca-111">Return value</span></span>

<span data-ttu-id="7ceca-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="7ceca-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ceca-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ceca-113">Requirements</span></span>



| <span data-ttu-id="7ceca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ceca-114">Requirement</span></span> | <span data-ttu-id="7ceca-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7ceca-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ceca-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ceca-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7ceca-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ceca-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7ceca-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ceca-118">Library</span></span><br/> | <dl> <span data-ttu-id="7ceca-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7ceca-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ceca-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ceca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ceca-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="7ceca-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="7ceca-122">**GUIDs de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="7ceca-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





---
description: 'O método GetTimeFormat recupera o formato de hora atual. Esse método implementa o método IMediaSeeking:: GetTimeFormat.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Método CPosPassThru. GetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7db1b46cfe2ac06dc43b52009043ae32676f154
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747818"
---
# <a name="cpospassthrugettimeformat-method"></a><span data-ttu-id="c0937-104">Método CPosPassThru. GetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c0937-104">CPosPassThru.GetTimeFormat method</span></span>

<span data-ttu-id="c0937-105">O `GetTimeFormat` método recupera o formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="c0937-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="c0937-106">Esse método implementa o método [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="c0937-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0937-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0937-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="c0937-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0937-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0937-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="c0937-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c0937-110">Ponteiro para uma variável que recebe um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="c0937-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0937-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0937-111">Return value</span></span>

<span data-ttu-id="c0937-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="c0937-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0937-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0937-113">Requirements</span></span>



| <span data-ttu-id="c0937-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0937-114">Requirement</span></span> | <span data-ttu-id="c0937-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c0937-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0937-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0937-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c0937-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0937-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0937-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0937-118">Library</span></span><br/> | <dl> <span data-ttu-id="c0937-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c0937-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0937-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0937-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0937-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="c0937-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="c0937-122">**GUIDs de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="c0937-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





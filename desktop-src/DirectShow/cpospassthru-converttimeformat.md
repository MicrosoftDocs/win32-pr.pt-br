---
description: 'Método CPosPassThru. ConvertTimeFormat-o método ConvertTimeFormat converte de um formato de tempo para outro. Esse método implementa o método IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Método CPosPassThru. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098954"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="18f81-104">Método CPosPassThru. ConvertTimeFormat</span><span class="sxs-lookup"><span data-stu-id="18f81-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="18f81-105">O `ConvertTimeFormat` método converte de um formato de tempo para outro.</span><span class="sxs-lookup"><span data-stu-id="18f81-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="18f81-106">Esse método implementa o método [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="18f81-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f81-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18f81-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="18f81-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18f81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18f81-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="18f81-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="18f81-110">Ponteiro para uma variável que recebe a hora convertida.</span><span class="sxs-lookup"><span data-stu-id="18f81-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="18f81-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="18f81-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="18f81-112">Ponteiro para o GUID de formato de hora do formato de destino.</span><span class="sxs-lookup"><span data-stu-id="18f81-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="18f81-113">Se for **NULL**, o formato atual será usado.</span><span class="sxs-lookup"><span data-stu-id="18f81-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="18f81-114">*Origem*</span><span class="sxs-lookup"><span data-stu-id="18f81-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="18f81-115">Valor de tempo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="18f81-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="18f81-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="18f81-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="18f81-117">Ponteiro para o GUID de formato de hora do formato a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="18f81-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="18f81-118">Se for **NULL**, o formato atual será usado.</span><span class="sxs-lookup"><span data-stu-id="18f81-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18f81-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="18f81-119">Return value</span></span>

<span data-ttu-id="18f81-120">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="18f81-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="18f81-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18f81-121">Requirements</span></span>



| <span data-ttu-id="18f81-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="18f81-122">Requirement</span></span> | <span data-ttu-id="18f81-123">Valor</span><span class="sxs-lookup"><span data-stu-id="18f81-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f81-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18f81-124">Header</span></span><br/>  | <dl> <span data-ttu-id="18f81-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18f81-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="18f81-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18f81-126">Library</span></span><br/> | <dl> <span data-ttu-id="18f81-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="18f81-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18f81-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="18f81-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f81-129">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="18f81-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="18f81-130">**GUIDs de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="18f81-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





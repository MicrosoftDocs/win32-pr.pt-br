---
description: 'O método ConvertTimeFormat converte de um formato de tempo para outro. Esse método implementa o método IMediaSeeking:: ConvertTimeFormat.'
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
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754257"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="aafe9-104">Método CPosPassThru. ConvertTimeFormat</span><span class="sxs-lookup"><span data-stu-id="aafe9-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="aafe9-105">O `ConvertTimeFormat` método converte de um formato de tempo para outro.</span><span class="sxs-lookup"><span data-stu-id="aafe9-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="aafe9-106">Esse método implementa o método [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="aafe9-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aafe9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aafe9-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="aafe9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aafe9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aafe9-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="aafe9-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="aafe9-110">Ponteiro para uma variável que recebe a hora convertida.</span><span class="sxs-lookup"><span data-stu-id="aafe9-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="aafe9-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="aafe9-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="aafe9-112">Ponteiro para o GUID de formato de hora do formato de destino.</span><span class="sxs-lookup"><span data-stu-id="aafe9-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="aafe9-113">Se for **NULL**, o formato atual será usado.</span><span class="sxs-lookup"><span data-stu-id="aafe9-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="aafe9-114">*Origem*</span><span class="sxs-lookup"><span data-stu-id="aafe9-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="aafe9-115">Valor de tempo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="aafe9-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="aafe9-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="aafe9-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="aafe9-117">Ponteiro para o GUID de formato de hora do formato a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="aafe9-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="aafe9-118">Se for **NULL**, o formato atual será usado.</span><span class="sxs-lookup"><span data-stu-id="aafe9-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aafe9-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aafe9-119">Return value</span></span>

<span data-ttu-id="aafe9-120">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="aafe9-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="aafe9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aafe9-121">Requirements</span></span>



| <span data-ttu-id="aafe9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aafe9-122">Requirement</span></span> | <span data-ttu-id="aafe9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="aafe9-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aafe9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aafe9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="aafe9-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aafe9-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aafe9-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aafe9-126">Library</span></span><br/> | <dl> <span data-ttu-id="aafe9-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="aafe9-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aafe9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="aafe9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aafe9-129">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="aafe9-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="aafe9-130">**GUIDs de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="aafe9-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





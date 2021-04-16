---
description: 'O método ConvertTimeFormat converte de um formato de tempo para outro. Esse método implementa o método IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Método CSourceSeeking. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758072"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="33777-104">Método CSourceSeeking. ConvertTimeFormat</span><span class="sxs-lookup"><span data-stu-id="33777-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="33777-105">O `ConvertTimeFormat` método converte de um formato de tempo para outro.</span><span class="sxs-lookup"><span data-stu-id="33777-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="33777-106">Esse método implementa o método [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="33777-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33777-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33777-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="33777-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33777-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33777-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="33777-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="33777-110">Ponteiro para uma variável que recebe a hora convertida.</span><span class="sxs-lookup"><span data-stu-id="33777-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="33777-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="33777-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="33777-112">Ponteiro para o GUID do formato de destino.</span><span class="sxs-lookup"><span data-stu-id="33777-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="33777-113">Se for **NULL**, o formato atual será usado.</span><span class="sxs-lookup"><span data-stu-id="33777-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="33777-114">Consulte [**GUIDs de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="33777-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="33777-115">*Origem*</span><span class="sxs-lookup"><span data-stu-id="33777-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="33777-116">Valor de tempo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="33777-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="33777-117">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="33777-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="33777-118">Ponteiro para o GUID de formato de hora do formato a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="33777-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="33777-119">Se for **NULL**, o formato atual será usado.</span><span class="sxs-lookup"><span data-stu-id="33777-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33777-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33777-120">Return value</span></span>

<span data-ttu-id="33777-121">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="33777-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="33777-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="33777-122">Return code</span></span>                                                                                  | <span data-ttu-id="33777-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="33777-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="33777-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33777-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="33777-125">Sucesso</span><span class="sxs-lookup"><span data-stu-id="33777-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="33777-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="33777-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="33777-127">Argumento inválido</span><span class="sxs-lookup"><span data-stu-id="33777-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="33777-128"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="33777-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="33777-129">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="33777-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33777-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="33777-130">Remarks</span></span>

<span data-ttu-id="33777-131">O único formato de tempo com suporte da classe base é \_ o \_ tempo de mídia de formato de hora \_ (unidades de 100 nanossegundos).</span><span class="sxs-lookup"><span data-stu-id="33777-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="33777-132">Esse método retorna E \_ INVALIDARG, exceto no caso trivial, em que *PTargetFormat* e *pSourceFormat* especificam o tempo de mídia de formato de hora \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="33777-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="33777-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33777-133">Requirements</span></span>



| <span data-ttu-id="33777-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="33777-134">Requirement</span></span> | <span data-ttu-id="33777-135">Valor</span><span class="sxs-lookup"><span data-stu-id="33777-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33777-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33777-136">Header</span></span><br/>  | <dl> <span data-ttu-id="33777-137"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33777-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="33777-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33777-138">Library</span></span><br/> | <dl> <span data-ttu-id="33777-139"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="33777-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33777-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="33777-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33777-141">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="33777-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





---
description: 'Método CSourceSeeking. setpositiones – o método SetPositions define a posição atual e a posição de parada. Esse método implementa o método IMediaSeeking:: setposicionations.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Método CSourceSeeking. setpositiones (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085164"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="506f6-104">Método CSourceSeeking. setpositiones</span><span class="sxs-lookup"><span data-stu-id="506f6-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="506f6-105">O `SetPositions` método define a posição atual e a posição de parada.</span><span class="sxs-lookup"><span data-stu-id="506f6-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="506f6-106">Esse método implementa o método [**IMediaSeeking:: Setposicionations**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="506f6-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="506f6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="506f6-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="506f6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="506f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="506f6-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="506f6-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="506f6-110">Ponteiro para uma variável que especifica a posição atual.</span><span class="sxs-lookup"><span data-stu-id="506f6-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="506f6-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="506f6-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="506f6-112">Combinação bit-a-de de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="506f6-112">Bitwise combination of flags.</span></span> <span data-ttu-id="506f6-113">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="506f6-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="506f6-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="506f6-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="506f6-115">Ponteiro para uma variável que especifica a hora de parada, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="506f6-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="506f6-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="506f6-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="506f6-117">Combinação bit-a-de de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="506f6-117">Bitwise combination of flags.</span></span> <span data-ttu-id="506f6-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="506f6-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="506f6-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="506f6-119">Return value</span></span>

<span data-ttu-id="506f6-120">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="506f6-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="506f6-121">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="506f6-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="506f6-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="506f6-122">Return code</span></span>                                                                                  | <span data-ttu-id="506f6-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="506f6-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="506f6-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="506f6-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="506f6-125">Êxito</span><span class="sxs-lookup"><span data-stu-id="506f6-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="506f6-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="506f6-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="506f6-127">Sinalizadores inválidos</span><span class="sxs-lookup"><span data-stu-id="506f6-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="506f6-128"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="506f6-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="506f6-129">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="506f6-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="506f6-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="506f6-130">Remarks</span></span>

<span data-ttu-id="506f6-131">Há suporte para os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="506f6-131">The following flags are supported:</span></span>

-   <span data-ttu-id="506f6-132">Está \_ procurando \_ noposição</span><span class="sxs-lookup"><span data-stu-id="506f6-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="506f6-133">Estou \_ procurando \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="506f6-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="506f6-134">Estou \_ procurando \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="506f6-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="506f6-135">Estou \_ procurando \_ IncrementalPositioning (somente *pStop* )</span><span class="sxs-lookup"><span data-stu-id="506f6-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="506f6-136">Para obter mais informações, consulte [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="506f6-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="506f6-137">Esse método atualiza os valores das variáveis de membro [**CSourceSeeking:: m \_ RtStart**](csourceseeking-m-rtstart.md) e [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) e, em seguida, chama os métodos virtuais puros [**CSourceSeeking:: altere**](csourceseeking-changestart.md) e [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="506f6-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="506f6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="506f6-138">Requirements</span></span>



| <span data-ttu-id="506f6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="506f6-139">Requirement</span></span> | <span data-ttu-id="506f6-140">Valor</span><span class="sxs-lookup"><span data-stu-id="506f6-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="506f6-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="506f6-141">Header</span></span><br/>  | <dl> <span data-ttu-id="506f6-142"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="506f6-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="506f6-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="506f6-143">Library</span></span><br/> | <dl> <span data-ttu-id="506f6-144"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="506f6-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="506f6-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="506f6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506f6-146">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="506f6-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





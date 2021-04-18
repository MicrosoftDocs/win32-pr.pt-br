---
description: 'O método setpositiones define a posição atual e a posição de parada. Esse método implementa o método IMediaSeeking:: setposicionations.'
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
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751887"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="218b3-104">Método CSourceSeeking. setpositiones</span><span class="sxs-lookup"><span data-stu-id="218b3-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="218b3-105">O `SetPositions` método define a posição atual e a posição de parada.</span><span class="sxs-lookup"><span data-stu-id="218b3-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="218b3-106">Esse método implementa o método [**IMediaSeeking:: Setposicionations**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="218b3-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="218b3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="218b3-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="218b3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="218b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="218b3-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="218b3-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="218b3-110">Ponteiro para uma variável que especifica a posição atual.</span><span class="sxs-lookup"><span data-stu-id="218b3-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="218b3-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="218b3-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="218b3-112">Combinação bit-a-de de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="218b3-112">Bitwise combination of flags.</span></span> <span data-ttu-id="218b3-113">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="218b3-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="218b3-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="218b3-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="218b3-115">Ponteiro para uma variável que especifica a hora de parada, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="218b3-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="218b3-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="218b3-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="218b3-117">Combinação bit-a-de de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="218b3-117">Bitwise combination of flags.</span></span> <span data-ttu-id="218b3-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="218b3-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="218b3-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="218b3-119">Return value</span></span>

<span data-ttu-id="218b3-120">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="218b3-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="218b3-121">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="218b3-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="218b3-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="218b3-122">Return code</span></span>                                                                                  | <span data-ttu-id="218b3-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="218b3-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="218b3-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="218b3-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="218b3-125">Sucesso</span><span class="sxs-lookup"><span data-stu-id="218b3-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="218b3-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="218b3-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="218b3-127">Sinalizadores inválidos</span><span class="sxs-lookup"><span data-stu-id="218b3-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="218b3-128"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="218b3-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="218b3-129">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="218b3-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="218b3-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="218b3-130">Remarks</span></span>

<span data-ttu-id="218b3-131">Há suporte para os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="218b3-131">The following flags are supported:</span></span>

-   <span data-ttu-id="218b3-132">Está \_ procurando \_ noposição</span><span class="sxs-lookup"><span data-stu-id="218b3-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="218b3-133">Estou \_ procurando \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="218b3-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="218b3-134">Estou \_ procurando \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="218b3-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="218b3-135">Estou \_ procurando \_ IncrementalPositioning (somente *pStop* )</span><span class="sxs-lookup"><span data-stu-id="218b3-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="218b3-136">Para obter mais informações, consulte [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="218b3-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="218b3-137">Esse método atualiza os valores das variáveis de membro [**CSourceSeeking:: m \_ RtStart**](csourceseeking-m-rtstart.md) e [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) e, em seguida, chama os métodos virtuais puros [**CSourceSeeking:: altere**](csourceseeking-changestart.md) e [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="218b3-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="218b3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="218b3-138">Requirements</span></span>



| <span data-ttu-id="218b3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="218b3-139">Requirement</span></span> | <span data-ttu-id="218b3-140">Valor</span><span class="sxs-lookup"><span data-stu-id="218b3-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="218b3-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="218b3-141">Header</span></span><br/>  | <dl> <span data-ttu-id="218b3-142"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="218b3-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="218b3-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="218b3-143">Library</span></span><br/> | <dl> <span data-ttu-id="218b3-144"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="218b3-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="218b3-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="218b3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="218b3-146">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="218b3-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





---
description: O método GetMediaTime recupera os carimbos de data/hora no exemplo atual.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Método CRendererPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 628c0f0c65dad4e00dd259edbeee97fd8f6f13ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755341"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="901b8-103">Método CRendererPosPassThru. GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="901b8-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="901b8-104">O `GetMediaTime` método recupera os carimbos de data/hora no exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="901b8-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="901b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="901b8-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="901b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="901b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="901b8-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="901b8-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="901b8-108">Ponteiro para uma variável que recebe a hora de início, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="901b8-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="901b8-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="901b8-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="901b8-110">Ponteiro para uma variável que recebe a hora de término, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="901b8-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="901b8-111">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="901b8-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="901b8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="901b8-112">Return value</span></span>

<span data-ttu-id="901b8-113">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="901b8-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="901b8-114">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="901b8-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="901b8-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="901b8-115">Return code</span></span>                                                                                  | <span data-ttu-id="901b8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="901b8-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="901b8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="901b8-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="901b8-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="901b8-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="901b8-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="901b8-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="901b8-120">Não há suporte para a conversão para esse formato.</span><span class="sxs-lookup"><span data-stu-id="901b8-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="901b8-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="901b8-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="901b8-122">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="901b8-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="901b8-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="901b8-123">Remarks</span></span>

<span data-ttu-id="901b8-124">Esse método substitui o método [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="901b8-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="901b8-125">Os valores de carimbo de data/hora são convertidos no formato de hora atual chamando o método [**CPosPassThru:: ConvertTimeFormat**](cpospassthru-converttimeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="901b8-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="901b8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="901b8-126">Requirements</span></span>



| <span data-ttu-id="901b8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="901b8-127">Requirement</span></span> | <span data-ttu-id="901b8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="901b8-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="901b8-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="901b8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="901b8-130"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="901b8-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="901b8-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="901b8-131">Library</span></span><br/> | <dl> <span data-ttu-id="901b8-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="901b8-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





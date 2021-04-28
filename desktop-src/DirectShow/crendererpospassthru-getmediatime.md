---
description: Método CRendererPosPassThru. GetMediaTime – o método GetMediaTime recupera os carimbos de data/hora no exemplo atual.
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
ms.openlocfilehash: 588c92faec6b68cfa51392d4df00567c4e881460
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085364"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="d6e4f-103">Método CRendererPosPassThru. GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="d6e4f-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="d6e4f-104">O `GetMediaTime` método recupera os carimbos de data/hora no exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="d6e4f-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e4f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6e4f-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="d6e4f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6e4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e4f-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="d6e4f-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d6e4f-108">Ponteiro para uma variável que recebe a hora de início, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="d6e4f-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="d6e4f-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="d6e4f-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d6e4f-110">Ponteiro para uma variável que recebe a hora de término, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="d6e4f-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="d6e4f-111">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d6e4f-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6e4f-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d6e4f-112">Return value</span></span>

<span data-ttu-id="d6e4f-113">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6e4f-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d6e4f-114">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6e4f-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="d6e4f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d6e4f-115">Return code</span></span>                                                                                  | <span data-ttu-id="d6e4f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6e4f-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="d6e4f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d6e4f-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d6e4f-118">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="d6e4f-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d6e4f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d6e4f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d6e4f-120">Não há suporte para a conversão para esse formato.</span><span class="sxs-lookup"><span data-stu-id="d6e4f-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="d6e4f-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d6e4f-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="d6e4f-122">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d6e4f-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="d6e4f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6e4f-123">Remarks</span></span>

<span data-ttu-id="d6e4f-124">Esse método substitui o método [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="d6e4f-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="d6e4f-125">Os valores de carimbo de data/hora são convertidos no formato de hora atual chamando o método [**CPosPassThru:: ConvertTimeFormat**](cpospassthru-converttimeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="d6e4f-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e4f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6e4f-126">Requirements</span></span>



| <span data-ttu-id="d6e4f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6e4f-127">Requirement</span></span> | <span data-ttu-id="d6e4f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d6e4f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e4f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6e4f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d6e4f-130"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6e4f-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d6e4f-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6e4f-131">Library</span></span><br/> | <dl> <span data-ttu-id="d6e4f-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d6e4f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





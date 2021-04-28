---
description: 'Método CSourceSeeking. SetTimeFormat – o método SetTimeFormat define o formato de hora. Esse método implementa o método IMediaSeeking:: SetTimeFormat.'
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Método CSourceSeeking. SetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdb3889ecfa5bdcd49b4054822a2b2d09df58fa6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085194"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="817ff-104">Método CSourceSeeking. SetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="817ff-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="817ff-105">O `SetTimeFormat` método define o formato de hora.</span><span class="sxs-lookup"><span data-stu-id="817ff-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="817ff-106">Esse método implementa o método [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="817ff-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="817ff-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="817ff-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="817ff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="817ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="817ff-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="817ff-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="817ff-110">Ponteiro para um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="817ff-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="817ff-111">Consulte [**GUIDs de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="817ff-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="817ff-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="817ff-112">Return value</span></span>

<span data-ttu-id="817ff-113">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="817ff-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="817ff-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="817ff-114">Return code</span></span>                                                                                  | <span data-ttu-id="817ff-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="817ff-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="817ff-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="817ff-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="817ff-117">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="817ff-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="817ff-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="817ff-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="817ff-119">Não há suporte para o formato especificado.</span><span class="sxs-lookup"><span data-stu-id="817ff-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="817ff-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="817ff-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="817ff-121">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="817ff-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="817ff-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="817ff-122">Remarks</span></span>

<span data-ttu-id="817ff-123">O único formato de tempo com suporte da classe base é \_ o \_ tempo de mídia de formato de hora \_ (unidades de 100 nanossegundos).</span><span class="sxs-lookup"><span data-stu-id="817ff-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="817ff-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="817ff-124">Requirements</span></span>



| <span data-ttu-id="817ff-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="817ff-125">Requirement</span></span> | <span data-ttu-id="817ff-126">Valor</span><span class="sxs-lookup"><span data-stu-id="817ff-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="817ff-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="817ff-127">Header</span></span><br/>  | <dl> <span data-ttu-id="817ff-128"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="817ff-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="817ff-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="817ff-129">Library</span></span><br/> | <dl> <span data-ttu-id="817ff-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="817ff-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="817ff-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="817ff-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="817ff-132">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="817ff-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





---
description: 'Método CPosPassThru. GetDuration – o método GetDuration recupera a duração do fluxo. Esse método implementa o método IMediaSeeking:: getDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Método CPosPassThru. getDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b0af7bfaca405ed52a4e3c5a63c18b4bc087ba3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085574"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="51cc1-104">Método CPosPassThru. GetDuration</span><span class="sxs-lookup"><span data-stu-id="51cc1-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="51cc1-105">O `GetDuration` método recupera a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="51cc1-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="51cc1-106">Esse método implementa o método [**IMediaSeeking:: getDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="51cc1-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51cc1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51cc1-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="51cc1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51cc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51cc1-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="51cc1-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="51cc1-110">Ponteiro para uma variável que recebe a duração, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="51cc1-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51cc1-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="51cc1-111">Return value</span></span>

<span data-ttu-id="51cc1-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="51cc1-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cc1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51cc1-113">Requirements</span></span>



| <span data-ttu-id="51cc1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="51cc1-114">Requirement</span></span> | <span data-ttu-id="51cc1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="51cc1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51cc1-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51cc1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="51cc1-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51cc1-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="51cc1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51cc1-118">Library</span></span><br/> | <dl> <span data-ttu-id="51cc1-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="51cc1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51cc1-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="51cc1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cc1-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="51cc1-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





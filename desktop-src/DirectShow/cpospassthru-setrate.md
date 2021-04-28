---
description: 'Método CPosPassThru. SetRate-o método SetRate define a taxa de reprodução. Esse método implementa o método IMediaSeeking:: SetRate.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Método CPosPassThru. SetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bccc0d7044ccf17ac1c97e4fc5a185bdf6c7f0be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095214"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="dae01-104">Método CPosPassThru. SetRate</span><span class="sxs-lookup"><span data-stu-id="dae01-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="dae01-105">O `SetRate` método define a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="dae01-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="dae01-106">Esse método implementa o método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="dae01-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae01-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dae01-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="dae01-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dae01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae01-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="dae01-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="dae01-110">Taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="dae01-110">Playback rate.</span></span> <span data-ttu-id="dae01-111">Não deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dae01-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae01-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dae01-112">Return value</span></span>

<span data-ttu-id="dae01-113">Retorna E \_ INVALIDARG se *drate* for zero.</span><span class="sxs-lookup"><span data-stu-id="dae01-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="dae01-114">Caso contrário, retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="dae01-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae01-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae01-115">Requirements</span></span>



| <span data-ttu-id="dae01-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae01-116">Requirement</span></span> | <span data-ttu-id="dae01-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dae01-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae01-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dae01-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dae01-119"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dae01-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dae01-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dae01-120">Library</span></span><br/> | <dl> <span data-ttu-id="dae01-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dae01-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae01-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dae01-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae01-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="dae01-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





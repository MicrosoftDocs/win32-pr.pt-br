---
description: 'O método StopAt informa o PIN quando parar de entregar dados. Esse método implementa o método IAMStreamControl:: StopAt.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Método CBaseStreamControl. StopAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778513"
---
# <a name="cbasestreamcontrolstopat-method"></a><span data-ttu-id="989b3-104">Método CBaseStreamControl. StopAt</span><span class="sxs-lookup"><span data-stu-id="989b3-104">CBaseStreamControl.StopAt method</span></span>

<span data-ttu-id="989b3-105">O `StopAt` método informa o PIN quando parar de entregar dados.</span><span class="sxs-lookup"><span data-stu-id="989b3-105">The `StopAt` method informs the pin when to stop delivering data.</span></span> <span data-ttu-id="989b3-106">Esse método implementa o método [**IAMStreamControl:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="989b3-106">This method implements the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="989b3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="989b3-107">Syntax</span></span>


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="989b3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="989b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="989b3-109">*ptStop*</span><span class="sxs-lookup"><span data-stu-id="989b3-109">*ptStop*</span></span> 
</dt> <dd>

<span data-ttu-id="989b3-110">Ponteiro para um valor de [**\_ tempo de referência**](reference-time.md) que especifica quando o PIN deve parar de entregar dados.</span><span class="sxs-lookup"><span data-stu-id="989b3-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should stop delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="989b3-111">*bSendExtra*</span><span class="sxs-lookup"><span data-stu-id="989b3-111">*bSendExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="989b3-112">Especifica um valor booliano que indica se um exemplo extra deve ser enviado após a hora de término agendada.</span><span class="sxs-lookup"><span data-stu-id="989b3-112">Specifies a Boolean value that indicates whether to send an extra sample after the scheduled stop time.</span></span> <span data-ttu-id="989b3-113">Se **for true**, o PIN enviará um exemplo extra.</span><span class="sxs-lookup"><span data-stu-id="989b3-113">If **TRUE**, the pin sends one extra sample.</span></span>

</dd> <dt>

<span data-ttu-id="989b3-114">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="989b3-114">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="989b3-115">Especifica um valor a ser enviado junto com a notificação de início.</span><span class="sxs-lookup"><span data-stu-id="989b3-115">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="989b3-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="989b3-116">Return value</span></span>

<span data-ttu-id="989b3-117">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="989b3-117">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="989b3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="989b3-118">Requirements</span></span>



| <span data-ttu-id="989b3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="989b3-119">Requirement</span></span> | <span data-ttu-id="989b3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="989b3-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="989b3-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="989b3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="989b3-122"><dt>Strmctl. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="989b3-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="989b3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="989b3-123">Library</span></span><br/> | <dl> <span data-ttu-id="989b3-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="989b3-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="989b3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="989b3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="989b3-126">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="989b3-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 





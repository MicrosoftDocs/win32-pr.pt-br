---
description: 'O método StartAt informa o PIN quando iniciar a entrega de dados. Esse método implementa o método IAMStreamControl:: StartAt.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Método CBaseStreamControl. StartAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752297"
---
# <a name="cbasestreamcontrolstartat-method"></a><span data-ttu-id="24b38-104">Método CBaseStreamControl. StartAt</span><span class="sxs-lookup"><span data-stu-id="24b38-104">CBaseStreamControl.StartAt method</span></span>

<span data-ttu-id="24b38-105">O `StartAt` método informa o PIN quando iniciar a entrega de dados.</span><span class="sxs-lookup"><span data-stu-id="24b38-105">The `StartAt` method informs the pin when to start delivering data.</span></span> <span data-ttu-id="24b38-106">Esse método implementa o método [**IAMStreamControl:: StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="24b38-106">This method implements the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b38-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24b38-107">Syntax</span></span>


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="24b38-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24b38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24b38-109">*ptStart*</span><span class="sxs-lookup"><span data-stu-id="24b38-109">*ptStart*</span></span> 
</dt> <dd>

<span data-ttu-id="24b38-110">Ponteiro para um valor de [**\_ tempo de referência**](reference-time.md) que especifica quando o PIN deve começar a entregar dados.</span><span class="sxs-lookup"><span data-stu-id="24b38-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should start delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="24b38-111">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="24b38-111">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="24b38-112">Especifica um valor a ser enviado junto com a notificação de início.</span><span class="sxs-lookup"><span data-stu-id="24b38-112">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24b38-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24b38-113">Return value</span></span>

<span data-ttu-id="24b38-114">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="24b38-114">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="24b38-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24b38-115">Requirements</span></span>



| <span data-ttu-id="24b38-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b38-116">Requirement</span></span> | <span data-ttu-id="24b38-117">Valor</span><span class="sxs-lookup"><span data-stu-id="24b38-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b38-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24b38-118">Header</span></span><br/>  | <dl> <span data-ttu-id="24b38-119"><dt>Strmctl. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24b38-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24b38-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24b38-120">Library</span></span><br/> | <dl> <span data-ttu-id="24b38-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="24b38-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b38-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="24b38-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b38-123">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="24b38-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 





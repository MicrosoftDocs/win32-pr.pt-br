---
description: 'O método GetDuration recupera a duração do fluxo. Esse método implementa o método IMediaSeeking:: getDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Método CSourceSeeking. getDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747377"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="71422-104">Método CSourceSeeking. GetDuration</span><span class="sxs-lookup"><span data-stu-id="71422-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="71422-105">O `GetDuration` método recupera a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="71422-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="71422-106">Esse método implementa o método [**IMediaSeeking:: getDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="71422-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="71422-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71422-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="71422-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71422-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71422-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="71422-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="71422-110">Ponteiro para uma variável que recebe a duração, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="71422-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71422-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71422-111">Return value</span></span>

<span data-ttu-id="71422-112">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="71422-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="71422-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="71422-113">Return code</span></span>                                                                               | <span data-ttu-id="71422-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="71422-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="71422-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71422-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="71422-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="71422-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="71422-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="71422-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="71422-118">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="71422-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71422-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="71422-119">Remarks</span></span>

<span data-ttu-id="71422-120">A duração é especificada pela variável de membro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="71422-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="71422-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71422-121">Requirements</span></span>



| <span data-ttu-id="71422-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="71422-122">Requirement</span></span> | <span data-ttu-id="71422-123">Valor</span><span class="sxs-lookup"><span data-stu-id="71422-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71422-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71422-124">Header</span></span><br/>  | <dl> <span data-ttu-id="71422-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71422-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71422-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71422-126">Library</span></span><br/> | <dl> <span data-ttu-id="71422-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="71422-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71422-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="71422-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71422-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="71422-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





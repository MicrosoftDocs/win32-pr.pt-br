---
description: 'O método GetPreroll recupera o tempo de preversão. Esse método implementa o método IMediaSeeking:: GetPreroll.'
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Método CSourceSeeking. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097af089a7221f005cf7f3aac74953166af3cb2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787998"
---
# <a name="csourceseekinggetpreroll-method"></a><span data-ttu-id="1c721-104">Método CSourceSeeking. GetPreroll</span><span class="sxs-lookup"><span data-stu-id="1c721-104">CSourceSeeking.GetPreroll method</span></span>

<span data-ttu-id="1c721-105">O `GetPreroll` método recupera o tempo de preversão.</span><span class="sxs-lookup"><span data-stu-id="1c721-105">The `GetPreroll` method retrieves the preroll time.</span></span> <span data-ttu-id="1c721-106">Esse método implementa o método [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="1c721-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c721-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c721-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="1c721-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c721-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c721-109">*pPreroll*</span><span class="sxs-lookup"><span data-stu-id="1c721-109">*pPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="1c721-110">Ponteiro para uma variável que recebe a hora de preversão.</span><span class="sxs-lookup"><span data-stu-id="1c721-110">Pointer to a variable that receives the preroll time.</span></span> <span data-ttu-id="1c721-111">O valor é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="1c721-111">The value is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c721-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c721-112">Return value</span></span>

<span data-ttu-id="1c721-113">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c721-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="1c721-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1c721-114">Return code</span></span>                                                                               | <span data-ttu-id="1c721-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c721-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="1c721-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c721-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="1c721-117">Sucesso</span><span class="sxs-lookup"><span data-stu-id="1c721-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="1c721-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1c721-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="1c721-119">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="1c721-119">**NULL** pointer value</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1c721-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c721-120">Requirements</span></span>



| <span data-ttu-id="1c721-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c721-121">Requirement</span></span> | <span data-ttu-id="1c721-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1c721-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c721-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c721-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1c721-124"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c721-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c721-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c721-125">Library</span></span><br/> | <dl> <span data-ttu-id="1c721-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1c721-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c721-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c721-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c721-128">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="1c721-128">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





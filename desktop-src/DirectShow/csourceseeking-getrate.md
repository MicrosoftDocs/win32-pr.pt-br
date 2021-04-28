---
description: 'Método CSourceSeeking. GetRate – o método GetRate recupera a taxa de reprodução. Esse método implementa o método IMediaSeeking:: GetRate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Método CSourceSeeking. GetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085224"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="83ece-104">Método CSourceSeeking. GetRate</span><span class="sxs-lookup"><span data-stu-id="83ece-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="83ece-105">O `GetRate` método recupera a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="83ece-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="83ece-106">Esse método implementa o método [**IMediaSeeking:: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="83ece-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="83ece-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83ece-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="83ece-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83ece-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83ece-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="83ece-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="83ece-110">Ponteiro para uma variável que recebe a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="83ece-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83ece-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="83ece-111">Return value</span></span>

<span data-ttu-id="83ece-112">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="83ece-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="83ece-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="83ece-113">Return code</span></span>                                                                               | <span data-ttu-id="83ece-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="83ece-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="83ece-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83ece-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="83ece-116">Êxito</span><span class="sxs-lookup"><span data-stu-id="83ece-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="83ece-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="83ece-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="83ece-118">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="83ece-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="83ece-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="83ece-119">Remarks</span></span>

<span data-ttu-id="83ece-120">A taxa de reprodução é especificada pela variável de membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) .</span><span class="sxs-lookup"><span data-stu-id="83ece-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="83ece-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83ece-121">Requirements</span></span>



| <span data-ttu-id="83ece-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="83ece-122">Requirement</span></span> | <span data-ttu-id="83ece-123">Valor</span><span class="sxs-lookup"><span data-stu-id="83ece-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83ece-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83ece-124">Header</span></span><br/>  | <dl> <span data-ttu-id="83ece-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83ece-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="83ece-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83ece-126">Library</span></span><br/> | <dl> <span data-ttu-id="83ece-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="83ece-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83ece-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="83ece-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83ece-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="83ece-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





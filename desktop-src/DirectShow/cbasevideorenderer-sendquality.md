---
description: O método SendQuality envia uma mensagem de qualidade para indicar o que o fornecedor deve fazer sobre a qualidade.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Método CBaseVideoRenderer. SendQuality (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751496"
---
# <a name="cbasevideorenderersendquality-method"></a><span data-ttu-id="4582f-103">Método CBaseVideoRenderer. SendQuality</span><span class="sxs-lookup"><span data-stu-id="4582f-103">CBaseVideoRenderer.SendQuality method</span></span>

<span data-ttu-id="4582f-104">O `SendQuality` método envia uma mensagem de qualidade para indicar o que o fornecedor deve fazer sobre a qualidade.</span><span class="sxs-lookup"><span data-stu-id="4582f-104">The `SendQuality` method sends a quality message to indicate what the supplier should do about quality.</span></span>

## <a name="syntax"></a><span data-ttu-id="4582f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4582f-105">Syntax</span></span>


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a><span data-ttu-id="4582f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4582f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4582f-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="4582f-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="4582f-108">Período de tempo pelo qual o quadro está atrasado.</span><span class="sxs-lookup"><span data-stu-id="4582f-108">Amount of time by which the frame is late.</span></span>

</dd> <dt>

<span data-ttu-id="4582f-109">*trRealStream*</span><span class="sxs-lookup"><span data-stu-id="4582f-109">*trRealStream*</span></span> 
</dt> <dd>

<span data-ttu-id="4582f-110">Tempo de Currentstream.</span><span class="sxs-lookup"><span data-stu-id="4582f-110">Currentstream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4582f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4582f-111">Return value</span></span>

<span data-ttu-id="4582f-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4582f-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4582f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4582f-113">Remarks</span></span>

<span data-ttu-id="4582f-114">Essa função de membro envia uma mensagem de controle de qualidade upstream para controlar o gerenciamento de qualidade.</span><span class="sxs-lookup"><span data-stu-id="4582f-114">This member function sends a quality control message upstream to control quality management.</span></span> <span data-ttu-id="4582f-115">A natureza da mensagem de qualidade (ou seja, se deseja reduzir ou aumentar o número de amostras) é determinada na implementação de gerenciamento de qualidade nessa classe derivada (consulte [**CBaseVideoRenderer:: ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span><span class="sxs-lookup"><span data-stu-id="4582f-115">The nature of the quality message (that is, whether to reduce or increase the number of samples) is determined in the quality management implementation in this derived class (see [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4582f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4582f-116">Requirements</span></span>



| <span data-ttu-id="4582f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4582f-117">Requirement</span></span> | <span data-ttu-id="4582f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4582f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4582f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4582f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4582f-120"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4582f-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4582f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4582f-121">Library</span></span><br/> | <dl> <span data-ttu-id="4582f-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4582f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4582f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4582f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4582f-124">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="4582f-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





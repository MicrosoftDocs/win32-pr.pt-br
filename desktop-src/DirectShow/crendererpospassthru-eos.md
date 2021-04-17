---
description: O método EOS atualiza os carimbos de data/hora em cache após uma notificação de fim de fluxo.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Método CRendererPosPassThru. EOS (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752694"
---
# <a name="crendererpospassthrueos-method"></a><span data-ttu-id="ae7e8-103">Método CRendererPosPassThru. EOS</span><span class="sxs-lookup"><span data-stu-id="ae7e8-103">CRendererPosPassThru.EOS method</span></span>

<span data-ttu-id="ae7e8-104">O `EOS` método atualiza os carimbos de data/hora em cache após uma notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ae7e8-104">The `EOS` method updates the cached time stamps after an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae7e8-105">Syntax</span></span>


```C++
HRESULT EOS();
```



## <a name="parameters"></a><span data-ttu-id="ae7e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae7e8-106">Parameters</span></span>

<span data-ttu-id="ae7e8-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ae7e8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae7e8-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae7e8-108">Return value</span></span>

<span data-ttu-id="ae7e8-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae7e8-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ae7e8-110">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae7e8-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="ae7e8-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ae7e8-111">Return code</span></span>                                                                            | <span data-ttu-id="ae7e8-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae7e8-112">Description</span></span>                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="ae7e8-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae7e8-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ae7e8-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ae7e8-114">Success.</span></span><br/>                                       |
| <dl> <span data-ttu-id="ae7e8-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="ae7e8-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ae7e8-116">Falha.</span><span class="sxs-lookup"><span data-stu-id="ae7e8-116">Failure.</span></span> <span data-ttu-id="ae7e8-117">Possivelmente, o filtro não é transmitido.</span><span class="sxs-lookup"><span data-stu-id="ae7e8-117">Possibly the filter is not streaming.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ae7e8-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae7e8-118">Remarks</span></span>

<span data-ttu-id="ae7e8-119">O filtro deve chamar esse método quando ele recebe uma notificação de fim de fluxo ([**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span><span class="sxs-lookup"><span data-stu-id="ae7e8-119">The filter should call this method when it receives an end-of-stream notification ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span></span> <span data-ttu-id="ae7e8-120">O método define os carimbos de data/hora em cache iguais à posição de parada, garantindo que o método [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retorne os valores corretos no final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="ae7e8-120">The method sets both cached time stamps equal to the stop position, ensuring that the [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the correct values at the end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae7e8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae7e8-121">Requirements</span></span>



| <span data-ttu-id="ae7e8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae7e8-122">Requirement</span></span> | <span data-ttu-id="ae7e8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ae7e8-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7e8-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae7e8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ae7e8-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae7e8-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ae7e8-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae7e8-126">Library</span></span><br/> | <dl> <span data-ttu-id="ae7e8-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ae7e8-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





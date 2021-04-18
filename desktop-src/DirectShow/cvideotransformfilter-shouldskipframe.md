---
description: O método ShouldSkipFrame determina se o filtro deve descartar um exemplo especificado.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Método CVideoTransformFilter. ShouldSkipFrame (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749819"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a><span data-ttu-id="a80a0-103">Método CVideoTransformFilter. ShouldSkipFrame</span><span class="sxs-lookup"><span data-stu-id="a80a0-103">CVideoTransformFilter.ShouldSkipFrame method</span></span>

<span data-ttu-id="a80a0-104">O `ShouldSkipFrame` método determina se o filtro deve descartar um exemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="a80a0-104">The `ShouldSkipFrame` method determines whether the filter should drop a specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a80a0-105">Syntax</span></span>


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="a80a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a80a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80a0-107">*Afixa*</span><span class="sxs-lookup"><span data-stu-id="a80a0-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="a80a0-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="a80a0-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80a0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a80a0-109">Return value</span></span>

<span data-ttu-id="a80a0-110">Retorna **true** se o filtro deve descartar este exemplo ou **false** se o filtro deve processar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="a80a0-110">Returns **TRUE** if the filter should drop this sample, or **FALSE** if the filter should process this sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="a80a0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a80a0-111">Remarks</span></span>

<span data-ttu-id="a80a0-112">Esse método retornará **true** se as seguintes condições forem atendidas:</span><span class="sxs-lookup"><span data-stu-id="a80a0-112">This method returns **TRUE** if the following conditions are met:</span></span>

-   <span data-ttu-id="a80a0-113">O exemplo tem carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="a80a0-113">The sample has time stamps.</span></span>
-   <span data-ttu-id="a80a0-114">O tempo médio de decodificação é de, pelo menos, 25% da duração do quadro.</span><span class="sxs-lookup"><span data-stu-id="a80a0-114">The average decoding time is at least 25% of the frame duration.</span></span>
-   <span data-ttu-id="a80a0-115">No momento, o renderizador é pelo menos um quadro atrasado, conforme relatado por meio de mensagens de qualidade.</span><span class="sxs-lookup"><span data-stu-id="a80a0-115">The renderer is currently at least one frame late, as reported through quality messages.</span></span>
-   <span data-ttu-id="a80a0-116">Ignorar para o próximo quadro chave não fará com que o quadro chegue mais de um quadro no início.</span><span class="sxs-lookup"><span data-stu-id="a80a0-116">Skipping to the next key frame would not cause the frame to arrive more than one frame early.</span></span>

<span data-ttu-id="a80a0-117">Para fins deste cálculo, o filtro registra as seguintes informações conforme processa os dados:</span><span class="sxs-lookup"><span data-stu-id="a80a0-117">For purposes of this calculation, the filter records the following information as it processes data:</span></span>

-   <span data-ttu-id="a80a0-118">O tempo médio de decodificação nos últimos 20 quadros (**m \_ itrAvgDecode**)</span><span class="sxs-lookup"><span data-stu-id="a80a0-118">The average decoding time over the past 20 frames (**m\_itrAvgDecode**)</span></span>
-   <span data-ttu-id="a80a0-119">O número de quadros desde o último quadro chave (**m \_ nFramesSinceKeyFrame**)</span><span class="sxs-lookup"><span data-stu-id="a80a0-119">The number of frames since the last key frame (**m\_nFramesSinceKeyFrame**)</span></span>
-   <span data-ttu-id="a80a0-120">Uma estimativa de quantos quadros existem entre quadros-chave (**m \_ nKeyFramePeriod**)</span><span class="sxs-lookup"><span data-stu-id="a80a0-120">An estimate of how many frames there are between key frames (**m\_nKeyFramePeriod**)</span></span>

<span data-ttu-id="a80a0-121">Depois que o filtro soltar um quadro, ele continuará a descartar os quadros até atingir o próximo quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="a80a0-121">Once the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="a80a0-122">Se esse método retornar **true**, ele também enviará um evento de [**\_ \_ alteração de qualidade do EC**](ec-quality-change.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="a80a0-122">If this method returns **TRUE**, it also sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the Filter Graph Manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="a80a0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a80a0-123">Requirements</span></span>



| <span data-ttu-id="a80a0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80a0-124">Requirement</span></span> | <span data-ttu-id="a80a0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a80a0-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a80a0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a80a0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a80a0-127"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a80a0-127"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a80a0-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a80a0-128">Library</span></span><br/> | <dl> <span data-ttu-id="a80a0-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a80a0-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a80a0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a80a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80a0-131">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="a80a0-131">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 





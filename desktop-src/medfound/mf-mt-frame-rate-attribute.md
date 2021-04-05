---
description: Taxa de quadros de um tipo de mídia de vídeo, em quadros por segundo.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: Atributo MF_MT_FRAME_RATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370752"
---
# <a name="mf_mt_frame_rate-attribute"></a><span data-ttu-id="212de-103">\_Atributo de \_ taxa de quadros MF MT \_</span><span class="sxs-lookup"><span data-stu-id="212de-103">MF\_MT\_FRAME\_RATE attribute</span></span>

<span data-ttu-id="212de-104">Taxa de quadros de um tipo de mídia de vídeo, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="212de-104">Frame rate of a video media type, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="212de-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="212de-105">Data type</span></span>

<span data-ttu-id="212de-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="212de-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="212de-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="212de-107">Remarks</span></span>

<span data-ttu-id="212de-108">A taxa de quadros é expressa como uma taxa.</span><span class="sxs-lookup"><span data-stu-id="212de-108">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="212de-109">Os bits superiores de 32 do valor do atributo contêm o numerador e os bits inferiores de 32 contêm o denominador.</span><span class="sxs-lookup"><span data-stu-id="212de-109">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="212de-110">Por exemplo, se a taxa de quadros for de 30 quadros por segundo (FPS), a taxa será 30/1.</span><span class="sxs-lookup"><span data-stu-id="212de-110">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="212de-111">Se a taxa de quadros for de 29,97 fps, a taxa será 30.000/1001.</span><span class="sxs-lookup"><span data-stu-id="212de-111">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

<span data-ttu-id="212de-112">Para definir o valor, use a função [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="212de-112">To set the value, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="212de-113">Para obter o valor, use a função [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="212de-113">To get the value, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="212de-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="212de-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="212de-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="212de-115">Examples</span></span>

<span data-ttu-id="212de-116">O exemplo a seguir define a taxa de quadros em um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="212de-116">The following example sets the frame rate on a video media type.</span></span>


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



<span data-ttu-id="212de-117">O exemplo a seguir obtém a taxa de quadros de um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="212de-117">The following example gets the frame rate from a video media type.</span></span>


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a><span data-ttu-id="212de-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="212de-118">Requirements</span></span>



| <span data-ttu-id="212de-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="212de-119">Requirement</span></span> | <span data-ttu-id="212de-120">Valor</span><span class="sxs-lookup"><span data-stu-id="212de-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="212de-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="212de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="212de-122">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="212de-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="212de-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="212de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="212de-124">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="212de-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="212de-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="212de-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="212de-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="212de-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="212de-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="212de-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="212de-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="212de-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="212de-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="212de-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="212de-130">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="212de-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="212de-131">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="212de-131">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[<span data-ttu-id="212de-132">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="212de-132">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 





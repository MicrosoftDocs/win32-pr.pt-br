---
description: Especifica o retângulo de origem para o mixer de vídeo do processador de vídeo avançado (EVR). O retângulo de origem é a parte do quadro de vídeo que o mixer blits para a superfície de destino.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: Atributo VIDEO_ZOOM_RECT (EVR. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759017"
---
# <a name="video_zoom_rect-attribute"></a><span data-ttu-id="c6723-104">\_Atributo Rect de zoom de vídeo \_</span><span class="sxs-lookup"><span data-stu-id="c6723-104">VIDEO\_ZOOM\_RECT attribute</span></span>

<span data-ttu-id="c6723-105">Especifica o retângulo de origem para o mixer de vídeo do [processador de vídeo avançado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="c6723-105">Specifies the source rectangle for video mixer of the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="c6723-106">O retângulo de origem é a parte do quadro de vídeo que o mixer blits para a superfície de destino.</span><span class="sxs-lookup"><span data-stu-id="c6723-106">The source rectangle is the portion of the video frame that the mixer blits to the destination surface.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6723-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c6723-107">Data type</span></span>

<span data-ttu-id="c6723-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="c6723-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="c6723-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6723-109">Remarks</span></span>

<span data-ttu-id="c6723-110">O valor desse atributo é uma estrutura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="c6723-110">The value of this attribute is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="c6723-111">O retângulo de origem é definido em relação a um sistema de coordenadas normalizado, no qual todo o quadro de vídeo ocupa um retângulo com coordenadas {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="c6723-111">The source rectangle is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="c6723-112">O retângulo de origem deve caber no quadro de vídeo; as coordenadas do retângulo de origem têm um intervalo de (0... 1).</span><span class="sxs-lookup"><span data-stu-id="c6723-112">The source rectangle must fit within the video frame; the coordinates of the source rectangle have a range of (0...1).</span></span>

<span data-ttu-id="c6723-113">O apresentador EVR padrão define esse atributo no mixer.</span><span class="sxs-lookup"><span data-stu-id="c6723-113">The standard EVR presenter sets this attribute on the mixer.</span></span> <span data-ttu-id="c6723-114">Para definir o atributo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c6723-114">To set the attribute, do the following:</span></span>

1.  <span data-ttu-id="c6723-115">Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no mixer para obter o repositório de atributos do mixer.</span><span class="sxs-lookup"><span data-stu-id="c6723-115">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the mixer, to get the mixer's attribute store.</span></span>
2.  <span data-ttu-id="c6723-116">Chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) para definir o atributo de **\_ \_ retângulo de zoom de vídeo** no mixer.</span><span class="sxs-lookup"><span data-stu-id="c6723-116">Call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) to set the **VIDEO\_ZOOM\_RECT** attribute on the mixer.</span></span> <span data-ttu-id="c6723-117">O valor é uma estrutura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="c6723-117">The value is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="c6723-118">Em um apresentador personalizado do EVR, você pode usar esse atributo para implementar o método [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="c6723-118">In a custom EVR presenter, you can use this attribute to implement the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method.</span></span> <span data-ttu-id="c6723-119">Para obter mais informações, consulte [retângulos de origem e de destino](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="c6723-119">For more information, see [Source and Destination Rectangles](how-to-write-an-evr-presenter.md).</span></span>

<span data-ttu-id="c6723-120">A constante de GUID para esse atributo é exportada de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="c6723-120">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="c6723-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6723-121">Examples</span></span>

<span data-ttu-id="c6723-122">O exemplo a seguir define o retângulo de origem no mixer.</span><span class="sxs-lookup"><span data-stu-id="c6723-122">The following example sets the source rectangle on the mixer.</span></span>


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c6723-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6723-123">Requirements</span></span>



| <span data-ttu-id="c6723-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6723-124">Requirement</span></span> | <span data-ttu-id="c6723-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c6723-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c6723-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6723-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c6723-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6723-127">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c6723-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6723-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c6723-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6723-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c6723-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6723-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6723-131"><dt>EVR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6723-131"><dt>Evr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6723-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6723-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6723-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6723-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6723-134">Atributos avançados de processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="c6723-134">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6723-135">Como escrever um apresentador EVR</span><span class="sxs-lookup"><span data-stu-id="c6723-135">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="c6723-136">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="c6723-136">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="c6723-137">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="c6723-137">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 





---
description: Largura e altura de um quadro de vídeo, em pixels.
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: Atributo MF_MT_FRAME_SIZE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3d6278cdbd4c279c498839cb183b3331fe1efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756287"
---
# <a name="mf_mt_frame_size-attribute"></a><span data-ttu-id="4e38d-103">\_Atributo de \_ tamanho de quadro MF MT \_</span><span class="sxs-lookup"><span data-stu-id="4e38d-103">MF\_MT\_FRAME\_SIZE attribute</span></span>

<span data-ttu-id="4e38d-104">Largura e altura de um quadro de vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="4e38d-104">Width and height of a video frame, in pixels.</span></span>

## <a name="data-type"></a><span data-ttu-id="4e38d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4e38d-105">Data type</span></span>

<span data-ttu-id="4e38d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4e38d-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="4e38d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e38d-107">Remarks</span></span>

<span data-ttu-id="4e38d-108">Os bits superiores de 32 contêm a largura e os bits de 32 inferiores contêm a altura.</span><span class="sxs-lookup"><span data-stu-id="4e38d-108">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="4e38d-109">Para definir esse atributo, use a função [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) .</span><span class="sxs-lookup"><span data-stu-id="4e38d-109">To set this attribute, use the [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) function.</span></span> <span data-ttu-id="4e38d-110">Para obter esse atributo, use a função [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) .</span><span class="sxs-lookup"><span data-stu-id="4e38d-110">To get this attribute, use the [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) function.</span></span>

<span data-ttu-id="4e38d-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4e38d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="4e38d-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e38d-112">Examples</span></span>


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## <a name="requirements"></a><span data-ttu-id="4e38d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e38d-113">Requirements</span></span>



| <span data-ttu-id="4e38d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e38d-114">Requirement</span></span> | <span data-ttu-id="4e38d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4e38d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e38d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e38d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4e38d-117">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="4e38d-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4e38d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e38d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4e38d-119">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e38d-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4e38d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e38d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e38d-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e38d-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e38d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e38d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e38d-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4e38d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e38d-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4e38d-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="4e38d-125">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="4e38d-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 





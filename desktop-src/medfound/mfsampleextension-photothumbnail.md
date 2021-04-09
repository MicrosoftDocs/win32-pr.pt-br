---
description: Contém a miniatura da foto de um IMFSample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: Atributo MFSampleExtension_PhotoThumbnail (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091354"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a><span data-ttu-id="1b9a9-103">\_Atributo MFSampleExtension Fotominiatura</span><span class="sxs-lookup"><span data-stu-id="1b9a9-103">MFSampleExtension\_PhotoThumbnail attribute</span></span>

<span data-ttu-id="1b9a9-104">Contém a miniatura da foto de um [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="1b9a9-104">Contains the photo thumbnail of a [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span>

## <a name="data-type"></a><span data-ttu-id="1b9a9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1b9a9-105">Data type</span></span>

<span data-ttu-id="1b9a9-106">**IUnknown** armazenado como **IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="1b9a9-106">**IUnknown** stored as **IMFMediaBuffer**</span></span>

<span data-ttu-id="1b9a9-107">A miniatura é configurada usando o **KSPROPERTYSETID \_ ExtendedCameraControl**.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-107">The thumbnail is configured using the **KSPROPERTYSETID\_ExtendedCameraControl**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b9a9-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b9a9-108">Remarks</span></span>

<span data-ttu-id="1b9a9-109">Esse atributo é definido no [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) fornecido pelo MFT0 e é a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associado à miniatura da foto.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-109">This attribute is set on the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) provided by the MFT0 and is the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associated with the photo thumbnail.</span></span>

<span data-ttu-id="1b9a9-110">O formato da miniatura da foto pode ser JPEG (imagem do tipo principal), NV12 ou ARGB32.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-110">The format of the photo thumbnail can be JPEG (major type image), NV12 or ARGB32.</span></span>

<span data-ttu-id="1b9a9-111">O [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) é necessário para miniaturas para descrever o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-111">The [MFSampleExtension\_PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) is required for thumbnails to describe the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b9a9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b9a9-112">Requirements</span></span>



| <span data-ttu-id="1b9a9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b9a9-113">Requirement</span></span> | <span data-ttu-id="1b9a9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1b9a9-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9a9-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b9a9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1b9a9-116">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1b9a9-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="1b9a9-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b9a9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1b9a9-118">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="1b9a9-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1b9a9-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b9a9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b9a9-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b9a9-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b9a9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b9a9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b9a9-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b9a9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b9a9-123">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="1b9a9-123">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 

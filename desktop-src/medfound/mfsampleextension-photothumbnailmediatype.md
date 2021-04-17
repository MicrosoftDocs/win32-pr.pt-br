---
description: Contém o IMFMediaType que descreve o tipo de formato de imagem contido no \_ atributo Keythumbnail MFSampleExtension.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Atributo MFSampleExtension_PhotoThumbnailMediaType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105762189"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a><span data-ttu-id="d6edc-103">\_Atributo MFSampleExtension PhotoThumbnailMediaType</span><span class="sxs-lookup"><span data-stu-id="d6edc-103">MFSampleExtension\_PhotoThumbnailMediaType attribute</span></span>

<span data-ttu-id="d6edc-104">Contém o [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que descreve o tipo de formato de imagem contido no atributo [ \_ keythumbnail MFSampleExtension](mfsampleextension-photothumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="d6edc-104">Contains the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) which describes the image format type contained in the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6edc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d6edc-105">Data type</span></span>

<span data-ttu-id="d6edc-106">**IUnknown** armazenado como **IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d6edc-106">**IUnknown** stored as **IMFMediaType**</span></span>

## <a name="remarks"></a><span data-ttu-id="d6edc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6edc-107">Remarks</span></span>

<span data-ttu-id="d6edc-108">Se o [atributo MFSampleExtension \_ keythumbnail](mfsampleextension-photothumbnail.md) estiver presente no exemplo de foto, o MFSampleExtension \_ PhotoThumbnailMediaType será necessário e deverá conter, no mínimo, o [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md), o [ \_ \_ subtipo de MF MT](mf-mt-subtype-attribute.md) e o [ \_ \_ \_ tamanho do quadro MF MT](mf-mt-frame-size-attribute.md) que descrevem a miniatura.</span><span class="sxs-lookup"><span data-stu-id="d6edc-108">If the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute is present on the photo sample, the MFSampleExtension\_PhotoThumbnailMediaType is required and must contain, at a minimum, [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md), [MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md) and [MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md) which describe the thumbnail.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6edc-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6edc-109">Requirements</span></span>



| <span data-ttu-id="d6edc-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6edc-110">Requirement</span></span> | <span data-ttu-id="d6edc-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d6edc-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6edc-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6edc-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d6edc-113">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6edc-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="d6edc-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6edc-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d6edc-115">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d6edc-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d6edc-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6edc-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6edc-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6edc-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6edc-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6edc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6edc-119">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6edc-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d6edc-120">MFSampleExtension \_ Fotominiatura</span><span class="sxs-lookup"><span data-stu-id="d6edc-120">MFSampleExtension\_PhotoThumbnail</span></span>](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 





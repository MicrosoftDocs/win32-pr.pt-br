---
description: Requisitos de codec BRUTOs para o Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Requisitos de codec BRUTOs para o Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759674"
---
# <a name="raw-codec-requirements-for-windows-7"></a><span data-ttu-id="4d01e-103">Requisitos de codec BRUTOs para o Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d01e-103">RAW Codec Requirements for Windows 7</span></span>

<span data-ttu-id="4d01e-104">Os seguintes recursos de codec são necessários no mínimo:</span><span class="sxs-lookup"><span data-stu-id="4d01e-104">The following codec features are required at a minimum:</span></span>

<span data-ttu-id="4d01e-105">Todas as funcionalidades necessárias para o Shell do Windows Vista e para o suporte da Galeria de fotos: miniatura, visualização e rotação (persistente).</span><span class="sxs-lookup"><span data-stu-id="4d01e-105">All functionality that is required for Windows Vista shell and Photo Gallery support: thumbnail, preview, and (persisted) rotation.</span></span> <span data-ttu-id="4d01e-106">O processamento bruto deve padronizar para as configurações do as shot apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4d01e-106">RAW processing should default to appropriate as-shot settings.</span></span>

<span data-ttu-id="4d01e-107">O suporte para metadados principais (leitura e gravação), metadados não EXIF, bem como metadados de EXIF, deve persistir dentro de formatos de arquivo BRUTOs sem o uso de arquivos sidecar.</span><span class="sxs-lookup"><span data-stu-id="4d01e-107">Support for core metadata (both read and write), Non-EXIF metadata, as well as EXIF metadata, should be persisted inside RAW file formats without use of sidecar files.</span></span>

<span data-ttu-id="4d01e-108">Suporte para a interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="4d01e-108">Support for the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="4d01e-109">Para o Windows 7, o WIC do Windows Imaging Component (WIC) requer que todas as interfaces de parâmetro expostas por [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) sejam implementadas.</span><span class="sxs-lookup"><span data-stu-id="4d01e-109">For Windows 7, Windows Imaging Component (WIC)WIC requires that all parameter interfaces exposed by [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) be implemented.</span></span>

<span data-ttu-id="4d01e-110">Suporte ao estado de orientação:</span><span class="sxs-lookup"><span data-stu-id="4d01e-110">Orientation state support:</span></span>

-   <span data-ttu-id="4d01e-111">90 as rotações de imagem de etapa de grau devem ser aplicadas usando o método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) .</span><span class="sxs-lookup"><span data-stu-id="4d01e-111">90 degree-step Image rotations should be applied by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) method.</span></span> <span data-ttu-id="4d01e-112">Aplicativos e Windows Use esse método para girar as imagens (e as miniaturas e visualizações em cache).</span><span class="sxs-lookup"><span data-stu-id="4d01e-112">Applications and Windows use this method to rotate the images (and cached thumbnails and previews).</span></span>
-   <span data-ttu-id="4d01e-113">A aplicação de rotação usando essa API também deve persistir pelo codec (veja anteriormente neste documento).</span><span class="sxs-lookup"><span data-stu-id="4d01e-113">Application of rotation by using this API should also be persisted by the codec (see earlier in this paper).</span></span>
-   <span data-ttu-id="4d01e-114">Os aplicativos podem usar os recursos de rotação da API [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , mas o codec não serializará nenhuma configuração de rotação nessa API, portanto, as rotações feitas usando o [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) não serão persistidas.</span><span class="sxs-lookup"><span data-stu-id="4d01e-114">Applications can use the rotation capabilities of the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) API, but the codec will not serialize any rotation settings on this API, so rotations done using [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) will not be persisted.</span></span>

<span data-ttu-id="4d01e-115">Suporte à extração de miniatura e visualização de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="4d01e-115">High-speed thumbnail and preview extraction support.</span></span> <span data-ttu-id="4d01e-116">Se a dimensão de pixel de visualização máxima (largura ou altura) tiver menos de 1024 pixels de tamanho, o Windows Vista solicitará um processamento para visualização de tela:</span><span class="sxs-lookup"><span data-stu-id="4d01e-116">If the preview maximum pixel dimension (width or height) is less than 1024 pixels in size, Windows Vista will request a render for screen preview:</span></span>

-   <span data-ttu-id="4d01e-117">O método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**setprocessmode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) deve dar suporte a pelo menos os modos [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) e [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) para permitir renderização mais rápida de miniaturas e visualizações do que o modo de qualidade total.</span><span class="sxs-lookup"><span data-stu-id="4d01e-117">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) method should support at least the [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) and [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) modes to allow faster rendering of thumbnails and previews than the full-quality mode.</span></span>
-   <span data-ttu-id="4d01e-118">O Windows chamará [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) com o tamanho de resolução de tela solicitado.</span><span class="sxs-lookup"><span data-stu-id="4d01e-118">Windows will call [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the requested screen resolution size.</span></span>
-   <span data-ttu-id="4d01e-119">Os tamanhos de resolução de tela devem ter suporte na API acima.</span><span class="sxs-lookup"><span data-stu-id="4d01e-119">Screen resolution sizes must be supported in the above API.</span></span>
-   <span data-ttu-id="4d01e-120">É necessário um processamento de imagem consistente de miniatura, visualização e bits de imagem completa do [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) .</span><span class="sxs-lookup"><span data-stu-id="4d01e-120">Consistent image processing of thumbnail, preview, and full-image bits from [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) is required.</span></span>

<span data-ttu-id="4d01e-121">Formatos de pixel de intervalo dinâmico alto (HDR).</span><span class="sxs-lookup"><span data-stu-id="4d01e-121">High dynamic range (HDR) pixel formats.</span></span>

<span data-ttu-id="4d01e-122">Impressão de XML Paper Specification (XPS).</span><span class="sxs-lookup"><span data-stu-id="4d01e-122">XML Paper Specification (XPS) printing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d01e-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d01e-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4d01e-124">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4d01e-124">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4d01e-125">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="4d01e-125">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="4d01e-126">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="4d01e-126">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="4d01e-127">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="4d01e-127">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




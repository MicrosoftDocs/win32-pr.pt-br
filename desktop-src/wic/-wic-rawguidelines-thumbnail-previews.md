---
description: Miniaturas e visualizações
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniaturas e visualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751017"
---
# <a name="thumbnails-and-previews"></a><span data-ttu-id="ab9e0-103">Miniaturas e visualizações</span><span class="sxs-lookup"><span data-stu-id="ab9e0-103">Thumbnails and Previews</span></span>

<span data-ttu-id="ab9e0-104">O Windows Vista e a Galeria de fotos do Windows contam com o Windows Imaging Component (WIC) para renderizar miniaturas rápidas e visualizações de imagens.</span><span class="sxs-lookup"><span data-stu-id="ab9e0-104">Windows Vista and the Windows Photo Gallery rely on Windows Imaging Component (WIC) to render fast thumbnails and previews of images.</span></span> <span data-ttu-id="ab9e0-105">Para dar suporte à renderização rápida de miniatura e visualização, os codecs BRUTOs devem implementar as interfaces WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) e [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="ab9e0-105">To support fast thumbnail and preview rendering, RAW codecs must implement the WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) and [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) interfaces.</span></span> <span data-ttu-id="ab9e0-106">Para dar suporte a uma experiência de usuário responsiva, é altamente desejável que essas interfaces retornem um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) para o chamador em 200 milissegundos ou menos.</span><span class="sxs-lookup"><span data-stu-id="ab9e0-106">To support a responsive user experience, it is highly desirable that these interfaces return an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to the caller in 200 milliseconds or less.</span></span>

<span data-ttu-id="ab9e0-107">A Microsoft recomenda enfaticamente que os proprietários de formato de arquivo bruto gerem uma visualização renderizada e armazenem em cache o arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="ab9e0-107">Microsoft strongly recommends that RAW file format owners generate a prerendered preview and cache this in the image file.</span></span> <span data-ttu-id="ab9e0-108">Para um formato no dispositivo, isso geralmente é feito no momento da captura.</span><span class="sxs-lookup"><span data-stu-id="ab9e0-108">For an in-device format, this is usually done at capture time.</span></span> <span data-ttu-id="ab9e0-109">No entanto, as visualizações também podem ser geradas novamente e armazenadas no arquivo de imagem sempre que as propriedades da interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) forem alteradas – se não for necessário muito trabalho para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="ab9e0-109">However, previews could also be regenerated and stored in the image file whenever [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface properties are changed-if it does not take too much work to do so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab9e0-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab9e0-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ab9e0-111">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ab9e0-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ab9e0-112">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="ab9e0-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ab9e0-113">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="ab9e0-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="ab9e0-114">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="ab9e0-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




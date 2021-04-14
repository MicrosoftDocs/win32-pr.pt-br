---
title: Guia de programação do WIC
description: Descreve como usar as APIs do WIC.
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370730"
---
# <a name="wic-programming-guide"></a><span data-ttu-id="f1508-103">Guia de programação do WIC</span><span class="sxs-lookup"><span data-stu-id="f1508-103">WIC programming guide</span></span>

<span data-ttu-id="f1508-104">Esta seção contém tópicos conceituais que descrevem como usar as APIs do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="f1508-104">This section contains conceptual topics that describe how to use the Windows Imaging Component (WIC) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f1508-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f1508-105">In this section</span></span>



| <span data-ttu-id="f1508-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="f1508-106">Topic</span></span>                                                                                 | <span data-ttu-id="f1508-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1508-107">Description</span></span>                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1508-108">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="f1508-108">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)<br/> | <span data-ttu-id="f1508-109">O WIC fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem.</span><span class="sxs-lookup"><span data-stu-id="f1508-109">The WIC provides an extensible framework for working with images and image metadata.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="f1508-110">Visão geral da API do WIC</span><span class="sxs-lookup"><span data-stu-id="f1508-110">WIC API Overview</span></span>](-wic-api.md)<br/>                                           | <span data-ttu-id="f1508-111">O WIC fornece uma API baseada em Component Object Model (COM) para uso em C e C++.</span><span class="sxs-lookup"><span data-stu-id="f1508-111">The WIC provides a Component Object Model (COM) based API for use in C and C++.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="f1508-112">Decodificando imagens digitais</span><span class="sxs-lookup"><span data-stu-id="f1508-112">Decoding Digital Images</span></span>](-wic-decoder-portal.md)<br/>                         | <span data-ttu-id="f1508-113">Esta seção contém tópicos conceituais e de instruções que descrevem os decodificadores de bitmap do WIC que são usados na decodificação de imagens digitais.</span><span class="sxs-lookup"><span data-stu-id="f1508-113">This section contains conceptual and how-to topics that describe WIC bitmap decoders which are used in decoding digital images.</span></span><br/>                                                                            |
| [<span data-ttu-id="f1508-114">Usando dados de imagem</span><span class="sxs-lookup"><span data-stu-id="f1508-114">Using Image Data</span></span>](-wic-bitmapsources-portal.md)<br/>                          | <span data-ttu-id="f1508-115">Esta seção contém tópicos conceituais e de instruções que descrevem as fontes de bitmap do WIC e como manipulá-las.</span><span class="sxs-lookup"><span data-stu-id="f1508-115">This section contains conceptual and how-to topics that describe WIC bitmap sources and how to manipulate them.</span></span><br/>                                                                                            |
| [<span data-ttu-id="f1508-116">Dados da imagem de codificação</span><span class="sxs-lookup"><span data-stu-id="f1508-116">Encoding Image Data</span></span>](encoding-bitmaps-to-digital-images.md)<br/>              | <span data-ttu-id="f1508-117">Esta seção contém tópicos conceituais e de instruções que descrevem codificadores de bitmaps do WIC que são usados para codificar imagens digitais.</span><span class="sxs-lookup"><span data-stu-id="f1508-117">This section contains conceptual and how-to topics that describe WIC bitmap encoders which are used to encode digital images.</span></span><br/>                                                                              |
| [<span data-ttu-id="f1508-118">Codecs nativos do WIC</span><span class="sxs-lookup"><span data-stu-id="f1508-118">Native WIC Codecs</span></span>](native-wic-codecs.md)<br/>                                 | <span data-ttu-id="f1508-119">Esta seção contém informações sobre os codecs de imagens nativas disponíveis no WIC.</span><span class="sxs-lookup"><span data-stu-id="f1508-119">This section contains information about the native imaging codecs available in WIC.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="f1508-120">Processando metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="f1508-120">Processing Image Metadata</span></span>](-wic-metadata-portal.md)<br/>                      | <span data-ttu-id="f1508-121">Esta seção contém tópicos conceituais que descrevem o sistema de metadados do WIC.</span><span class="sxs-lookup"><span data-stu-id="f1508-121">This section contains conceptual topics that describe the WIC metadata system.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="f1508-122">Suporte a JPEG YCbCr</span><span class="sxs-lookup"><span data-stu-id="f1508-122">JPEG YCbCr Support</span></span>](jpeg-ycbcr-support.md)<br/>                               | <span data-ttu-id="f1508-123">A partir do Windows 8.1, o codec JPEG do [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) dá suporte à leitura e gravação de dados de imagem em seu formulário YC<sub>b</sub>C<sub>r</sub> nativo.</span><span class="sxs-lookup"><span data-stu-id="f1508-123">Starting with Windows 8.1, the [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG codec supports reading and writing image data in its native YC<sub>b</sub>C<sub>r</sub> form.</span></span> <br/> |
| [<span data-ttu-id="f1508-124">Gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="f1508-124">Color Management</span></span>](-wic-colormanagement.md)<br/>                               | <span data-ttu-id="f1508-125">O WIC simplifica o gerenciamento de cores, fornecendo a interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) e a interface [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) .</span><span class="sxs-lookup"><span data-stu-id="f1508-125">WIC simplifies color management by providing the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) interface and the [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) interface.</span></span><br/>          |
| [<span data-ttu-id="f1508-126">Desenvolvimento de componentes</span><span class="sxs-lookup"><span data-stu-id="f1508-126">Component Development</span></span>](-wic-component-development.md)<br/>                    | <span data-ttu-id="f1508-127">O WIC é uma plataforma extensível que fornece uma API de nível baixo para imagens digitais.</span><span class="sxs-lookup"><span data-stu-id="f1508-127">The WIC is an extensible platform that provides low-level API for digital images.</span></span><br/>                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="f1508-128">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f1508-128">See Also</span></span>

[<span data-ttu-id="f1508-129">Referência do WIC</span><span class="sxs-lookup"><span data-stu-id="f1508-129">WIC Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="f1508-130">Exemplos de WIC</span><span class="sxs-lookup"><span data-stu-id="f1508-130">WIC Samples</span></span>](-wic-samples.md)


 

 





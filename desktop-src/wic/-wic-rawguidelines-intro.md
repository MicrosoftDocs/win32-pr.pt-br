---
description: Introdução (diretrizes do WIC para formatos de imagem bruta de câmera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introdução (diretrizes do WIC para formatos de imagem bruta de câmera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170860"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a><span data-ttu-id="f9fad-103">Introdução (diretrizes do WIC para formatos de imagem bruta de câmera)</span><span class="sxs-lookup"><span data-stu-id="f9fad-103">Introduction (WIC Guidelines for Camera RAW Image Formats)</span></span>

<span data-ttu-id="f9fad-104">O Windows Imaging Component (WIC) fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem.</span><span class="sxs-lookup"><span data-stu-id="f9fad-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="f9fad-105">O WIC possibilita que os fornecedores de software e hardware desenvolvam codecs para que seus próprios formatos de imagem possam obter o mesmo suporte de plataforma que os formatos de imagem nativa, como TIFF (Tagged Image File Format), JPEG (conjunto de especialistas fotográfico) ou foto de HD.</span><span class="sxs-lookup"><span data-stu-id="f9fad-105">WIC makes it possible for software and hardware vendors to develop codecs so that their own image formats can obtain the same platform support as native image formats such as tagged image file format (TIFF), Joint Photographic Experts Group (JPEG), or HD Photo.</span></span>

<span data-ttu-id="f9fad-106">O WIC fornece um único conjunto consistente de interfaces para todo o processamento de imagens, independentemente do formato da imagem.</span><span class="sxs-lookup"><span data-stu-id="f9fad-106">WIC provides a single, consistent set of interfaces for all image processing, regardless of image format.</span></span> <span data-ttu-id="f9fad-107">Portanto, qualquer aplicativo que usa o WIC recebe o suporte automático para novos formatos de imagem assim que o codec é instalado.</span><span class="sxs-lookup"><span data-stu-id="f9fad-107">Therefore, any application that uses WIC receives automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="f9fad-108">O WIC também fornece uma estrutura de metadados extensíveis que possibilita que os aplicativos leiam e gravem seus próprios metadados proprietários diretamente nos arquivos de imagem, para que os metadados nunca sejam perdidos ou separados da imagem.</span><span class="sxs-lookup"><span data-stu-id="f9fad-108">WIC also provides an extensible metadata framework that makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata is never lost or separated from the image.</span></span>

<span data-ttu-id="f9fad-109">O WIC está incluído com o Windows Presentation Foundation (WPF) e é incorporado ao Windows Vista e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="f9fad-109">WIC is included with Windows Presentation Foundation (WPF) and is built into Windows Vista and later Windows versions.</span></span> <span data-ttu-id="f9fad-110">Ele também está disponível como um componente redistribuível autônomo para o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f9fad-110">It is also available as a stand-alone redistributable component for Windows XP.</span></span>

<span data-ttu-id="f9fad-111">Essas diretrizes foram projetadas para ajudar os fabricantes de formato bruto em seu desenvolvimento de codecs de WIC.</span><span class="sxs-lookup"><span data-stu-id="f9fad-111">These guidelines are designed to help RAW format manufacturers in their development of WIC codecs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9fad-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9fad-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f9fad-113">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f9fad-113">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f9fad-114">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="f9fad-114">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="f9fad-115">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="f9fad-115">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="f9fad-116">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="f9fad-116">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




---
description: Criar seu codec na plataforma do Windows Imaging Component (WIC) possibilita que todos os aplicativos criados no WIC obtenham o mesmo suporte de plataforma para o formato de imagem que eles obtêm para os formatos de imagem comuns fornecidos com a plataforma.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusão (como escrever um codec de WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793712"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="aba49-103">Conclusão (como escrever um codec de WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="aba49-103">Conclusion (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="aba49-104">Criar seu codec na plataforma do Windows Imaging Component (WIC) possibilita que todos os aplicativos criados no WIC obtenham o mesmo suporte de plataforma para o formato de imagem que eles obtêm para os formatos de imagem comuns fornecidos com a plataforma.</span><span class="sxs-lookup"><span data-stu-id="aba49-104">Building your codec on the Windows Imaging Component (WIC) platform makes it possible for all applications built on WIC to get the same platform support for your image format that they get for the common image formats shipped with the platform.</span></span> <span data-ttu-id="aba49-105">Ele também permite que a Galeria de fotos do Windows Vista, o Windows Explorer e o Visualizador de fotos exibam miniaturas e visualizações de imagens em seu formato usando o decodificador que você fornecer.</span><span class="sxs-lookup"><span data-stu-id="aba49-105">It also enables the Windows Vista Photo Gallery, Windows Explorer, and Photo Viewer to display thumbnails and previews of images in your format using the decoder that you provide.</span></span> <span data-ttu-id="aba49-106">Para formatos brutos, ele permite que aplicativos mais sofisticados de geração de imagens aproveitem os recursos de processamento bruto do decodificador.</span><span class="sxs-lookup"><span data-stu-id="aba49-106">For raw formats, it enables more sophisticated imaging applications to take advantage of your decoder’s raw processing capabilities.</span></span> <span data-ttu-id="aba49-107">Dependendo das opções de codificador que você dá suporte, você também pode expor recursos exclusivos do codificador para permitir que os aplicativos aproveitem ao máximo os recursos avançados do seu formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="aba49-107">Depending on the encoder options you support, you can also expose unique capabilities of your encoder to enable applications to take full advantage of the advanced features of your image format.</span></span>

<span data-ttu-id="aba49-108">O desenvolvimento de um codec habilitado para WIC exige que você implemente algumas interfaces novas.</span><span class="sxs-lookup"><span data-stu-id="aba49-108">Developing a WIC-enabled codec requires you to implement some new interfaces.</span></span> <span data-ttu-id="aba49-109">Em muitos casos, você pode escrever um wrapper para o codec existente que implementa essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="aba49-109">In many cases, you can write a wrapper for your existing codec that implements these interfaces.</span></span> <span data-ttu-id="aba49-110">Ao instalar o codec, você deve fazer algumas entradas do registro para tornar o codec detectável pela plataforma do WIC e associá-lo aos manipuladores de metadados apropriados.</span><span class="sxs-lookup"><span data-stu-id="aba49-110">When you install your codec, you must make some registry entries to make your codec discoverable by the WIC platform and associate it with the appropriate metadata handlers.</span></span> <span data-ttu-id="aba49-111">Você também precisa invocar uma API para limpar o cache de miniatura de qualquer miniatura padrão (vazia) que possa ter sido associada anteriormente às imagens no seu formato.</span><span class="sxs-lookup"><span data-stu-id="aba49-111">You also need to invoke an API to clear the thumbnail cache of any default (empty) thumbnails that may have previously associated with images in your format.</span></span> <span data-ttu-id="aba49-112">Se desejar, você pode habilitar a Galeria de fotos do Windows Vista para fornecer aos usuários um link para baixar seu codec quando a Galeria de fotos encontrar uma imagem com a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="aba49-112">If you want, you can enable the Windows Vista Photo Gallery to provide users with a link to download your codec when the Photo Gallery encounters an image with your file name extension.</span></span> <span data-ttu-id="aba49-113">Para fazer isso, você deve fornecer à Microsoft informações sobre a extensão de nome de arquivo do codec e a URL para seu site de download.</span><span class="sxs-lookup"><span data-stu-id="aba49-113">To do this, you must provide Microsoft with information about your codec’s file name extension and the URL for your download site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aba49-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aba49-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aba49-115">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="aba49-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aba49-116">Instalação e registro de CODEC</span><span class="sxs-lookup"><span data-stu-id="aba49-116">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="aba49-117">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="aba49-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="aba49-118">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="aba49-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




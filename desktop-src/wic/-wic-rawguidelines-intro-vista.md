---
description: Formatos de imagem BRUTOs no Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formatos de imagem BRUTOs no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170861"
---
# <a name="raw-image-formats-in-windows-vista"></a><span data-ttu-id="1ed7d-103">Formatos de imagem BRUTOs no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ed7d-103">RAW Image Formats in Windows Vista</span></span>

<span data-ttu-id="1ed7d-104">O Windows Vista Explorer, a Galeria de fotos do Windows Vista, a Galeria de fotos do Windows Live e o Visualizador de fotos do Azure 7 usam o Windows Imaging Component (WIC) e, portanto, oferecem suporte a formatos de imagem BRUTOs quando os codecs apropriados são instalados no computador.</span><span class="sxs-lookup"><span data-stu-id="1ed7d-104">Windows Vista Explorer , Windows Vista Photo Gallery, Window Live Photo Gallery, and the Windows 7 Photo Viewer all use Windows Imaging Component (WIC) and therefore support RAW image formats when appropriate codecs are installed on the computer.</span></span>

<span data-ttu-id="1ed7d-105">Como o WIC é uma arquitetura de geração de imagens extensível, qualquer aplicativo de WIC pode consumir novos formatos de imagem assim que novos codecs são instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="1ed7d-105">Because WIC is an extensible imaging architecture, any WIC application can consume new image formats as soon as new codecs are installed on the system.</span></span> <span data-ttu-id="1ed7d-106">Isso torna o WIC ideal como uma solução Plug and Play para os formatos de imagem BRUTOs que as câmeras digitais produzem.</span><span class="sxs-lookup"><span data-stu-id="1ed7d-106">This makes WIC ideal as a Plug and Play solution for the RAW image formats that digital cameras produce.</span></span> <span data-ttu-id="1ed7d-107">Por meio do WIC, os aplicativos do Windows podem obter suporte para novos modelos de câmera sempre que os codecs atualizados são disponibilizados (idealmente na caixa com novas câmeras).</span><span class="sxs-lookup"><span data-stu-id="1ed7d-107">Through WIC, Windows applications can gain support for new camera models whenever updated codecs are made available (ideally in-box with new cameras).</span></span> <span data-ttu-id="1ed7d-108">Os autores de codecs podem dar suporte a esses cenários implementando interfaces WIC comuns a todos os tipos de imagem, conforme descrito em mais detalhes neste documento.</span><span class="sxs-lookup"><span data-stu-id="1ed7d-108">Codec authors can support these scenarios by implementing WIC interfaces that are common to all image types, as described in more detail in this document.</span></span>

<span data-ttu-id="1ed7d-109">Hoje, a maioria dos aplicativos de consumidor básicos não tem conhecimento especial sobre formatos de imagem BRUTOs e não expõe uma interface do usuário para ajustar as configurações de processamento bruto.</span><span class="sxs-lookup"><span data-stu-id="1ed7d-109">Today, most mainstream consumer applications have no special knowledge of RAW image formats and do not expose a user interface for adjusting RAW processing settings.</span></span>

<span data-ttu-id="1ed7d-110">No entanto, para dar suporte a aplicativos de geração de imagens especializados, os autores de codec BRUTOs também devem implementar a interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="1ed7d-110">However, to support specialized imaging applications, RAW codec authors must also implement the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="1ed7d-111">Essa interface expõe recursos especiais para imagens BRUTAs, como a capacidade de fazer ajustes de imagem comuns e processar (desenvolver) imagens BRUTAs em espaços de cores RGB (vermelho-verde-azul) especificados.</span><span class="sxs-lookup"><span data-stu-id="1ed7d-111">This interface exposes special features for RAW images, such as the ability to make common image adjustments and to process (develop) RAW images into specified red-green-blue (RGB) color spaces.</span></span>

<span data-ttu-id="1ed7d-112">Várias outras interfaces de WIC são importantes para que os autores de codecs BRUTOs implementem.</span><span class="sxs-lookup"><span data-stu-id="1ed7d-112">Several other WIC interfaces are important for RAW codec authors to implement.</span></span> <span data-ttu-id="1ed7d-113">Eles são discutidos mais detalhadamente nesta série de tópicos.</span><span class="sxs-lookup"><span data-stu-id="1ed7d-113">These are discussed in more detail in this series of topics.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ed7d-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ed7d-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1ed7d-115">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1ed7d-116">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="1ed7d-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="1ed7d-117">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="1ed7d-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="1ed7d-118">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1ed7d-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




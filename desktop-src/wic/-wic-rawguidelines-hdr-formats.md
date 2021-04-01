---
description: Formatos de pixel de intervalo dinâmico alto
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Formatos de pixel de intervalo dinâmico alto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829491"
---
# <a name="high-dynamic-range-pixel-formats"></a><span data-ttu-id="6612b-103">Formatos de pixel de intervalo dinâmico alto</span><span class="sxs-lookup"><span data-stu-id="6612b-103">High Dynamic Range Pixel Formats</span></span>

<span data-ttu-id="6612b-104">Os codecs devem usar formatos de pixel do Windows Imaging Component (WIC) que preservam todo o intervalo dinâmico dos dados de sensor subjacentes.</span><span class="sxs-lookup"><span data-stu-id="6612b-104">Codecs should use Windows Imaging Component (WIC) pixel formats that preserve all of the dynamic range of the underlying sensor data.</span></span> <span data-ttu-id="6612b-105">\_O GUID WICPixelFormat48bppRGB é um formato típico de 16 bits por canal de ponto fixo que pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="6612b-105">GUID\_WICPixelFormat48bppRGB is a typical fixed-point 16-bit-per-channel format that can be used.</span></span> <span data-ttu-id="6612b-106">Outros formatos de precisão mais altos também podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="6612b-106">Other higher precision formats can be used also.</span></span> <span data-ttu-id="6612b-107">Para habilitar o suporte completo para o pipeline de renderização acelerado da GPU (unidade de processamento gráfico) do Windows Presentation Foundation, a Microsoft incentiva fortemente o suporte a um formato de pixel flutuante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6612b-107">To enable full support for the Windows Presentation Foundation graphics processing unit (GPU)-accelerated rendering pipeline, Microsoft strongly encourages support for a 32-bit floating point pixel format.</span></span>

<span data-ttu-id="6612b-108">Formatos de pixel de alta cor: com o Windows 7, dois novos formatos de pixel WIC foram adicionados para dar suporte aos novos formatos de exibição de alta cor.</span><span class="sxs-lookup"><span data-stu-id="6612b-108">High Color Pixel Formats: With Windows 7, two new WIC pixel formats have been added to support the new High Color display formats.</span></span> <span data-ttu-id="6612b-109">São eles: GUID \_ WICPixelFormat32bppRGBA1010102 e GUID \_ WICPixelFormat32bppRGBA1010102XR.</span><span class="sxs-lookup"><span data-stu-id="6612b-109">These are: GUID\_WICPixelFormat32bppRGBA1010102 and GUID\_WICPixelFormat32bppRGBA1010102XR.</span></span>

<span data-ttu-id="6612b-110">O formato de alta cor flutuante de 16 bits por canal (BPC) é suportado pelo \_ formato de pixel WICPIXELFORMAT64BPPRGBAHALF GUID existente.</span><span class="sxs-lookup"><span data-stu-id="6612b-110">The 16 bit per channel (bpc) float High Color format is supported by the existing GUID\_WICPixelFormat64bppRGBAHalf pixel format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6612b-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6612b-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6612b-112">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6612b-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6612b-113">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="6612b-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="6612b-114">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="6612b-114">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="6612b-115">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="6612b-115">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




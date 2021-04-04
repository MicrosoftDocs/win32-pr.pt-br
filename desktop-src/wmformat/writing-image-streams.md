---
title: Gravando fluxos de imagem
description: Gravando fluxos de imagem
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- ASF (Advanced Systems Format), gravando fluxos de imagem
- ASF (formato de sistemas avançados), gravando fluxos de imagem
- ASF (Advanced Systems Format), fluxos de imagem
- ASF (formato de sistemas avançados), fluxos de imagem
- fluxos de imagem, gravando
- fluxos, gravando fluxos de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916994"
---
# <a name="writing-image-streams"></a><span data-ttu-id="48a5d-109">Gravando fluxos de imagem</span><span class="sxs-lookup"><span data-stu-id="48a5d-109">Writing Image Streams</span></span>

<span data-ttu-id="48a5d-110">As entradas para um fluxo de imagem devem ser imagens de bitmap formatadas em RGB.</span><span class="sxs-lookup"><span data-stu-id="48a5d-110">The inputs for an image stream must be RGB-formatted bitmap images.</span></span> <span data-ttu-id="48a5d-111">O gravador coordena a compactação de exemplos de imagem de entrada usando o formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="48a5d-111">The writer coordinates the compression of input image samples using the JPEG format.</span></span> <span data-ttu-id="48a5d-112">Antes de começar a gravar um arquivo que contém um fluxo de imagem, você deve definir uma qualidade de imagem para a entrada, usando a \_ configuração g wszJPEGCompressionQuality.</span><span class="sxs-lookup"><span data-stu-id="48a5d-112">Before you begin writing a file containing an image stream, you must set an image quality for the input, using the g\_wszJPEGCompressionQuality setting.</span></span> <span data-ttu-id="48a5d-113">Use [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para definir a qualidade para um valor **DWORD** que varia de 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="48a5d-113">Use [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) to set the quality to a **DWORD** value ranging from 1 to 100.</span></span> <span data-ttu-id="48a5d-114">Valores baixos representam uma alta taxa de compactação às custas da qualidade, enquanto valores altos produzem imagens de alta qualidade que exigem mais espaço.</span><span class="sxs-lookup"><span data-stu-id="48a5d-114">Low values represent a high compression ratio at the expense of quality, while high values produce high quality images that require more space.</span></span>

<span data-ttu-id="48a5d-115">Os fluxos de imagem geralmente exigem janelas de buffer maiores do que fluxos de vídeo comuns.</span><span class="sxs-lookup"><span data-stu-id="48a5d-115">Image streams often require larger buffer windows than ordinary video streams.</span></span> <span data-ttu-id="48a5d-116">O tamanho exato necessário depende do tipo de imagem e da qualidade da imagem, entre outros fatores.</span><span class="sxs-lookup"><span data-stu-id="48a5d-116">The exact size required depends on the type of image and the image quality, among other factors.</span></span> <span data-ttu-id="48a5d-117">Use a avaliação e o erro para determinar o tamanho apropriado para as imagens que você pretende processar.</span><span class="sxs-lookup"><span data-stu-id="48a5d-117">Use trial and error to determine the appropriate size for the images you intend to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48a5d-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48a5d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48a5d-119">**Fluxos de imagem**</span><span class="sxs-lookup"><span data-stu-id="48a5d-119">**Image Streams**</span></span>](image-streams.md)
</dt> <dt>

[<span data-ttu-id="48a5d-120">**Para definir as configurações de entrada**</span><span class="sxs-lookup"><span data-stu-id="48a5d-120">**To Set Input Settings**</span></span>](to-set-input-settings.md)
</dt> <dt>

[<span data-ttu-id="48a5d-121">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="48a5d-121">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 





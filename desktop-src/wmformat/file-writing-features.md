---
title: Recursos de gravação de arquivo
description: Recursos de gravação de arquivo
ms.assetid: 4514f463-26cf-48a4-aa0c-c25fc5a1979f
keywords:
- SDK do Windows Media Format, recursos de gravação de arquivos
- SDK do Windows Media Format, recursos
- ASF (Advanced Systems Format), recursos de gravação de arquivos
- ASF (formato de sistemas avançados), recursos de gravação de arquivos
- ASF (Advanced Systems Format), recursos
- ASF (formato de sistemas avançados), recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a4764a318ac7cd420296b15bb4a5818ded06384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005488"
---
# <a name="file-writing-features"></a><span data-ttu-id="0e4ad-109">Recursos de gravação de arquivo</span><span class="sxs-lookup"><span data-stu-id="0e4ad-109">File Writing Features</span></span>

<span data-ttu-id="0e4ad-110">Um dos principais recursos do Windows Media Format SDK é a capacidade de gravar arquivos no ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-110">One of the primary features of the Windows Media Format SDK is the ability to write files in the Advanced Systems Format (ASF).</span></span> <span data-ttu-id="0e4ad-111">O objeto Writer é usado para gravar arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-111">The writer object is used to write ASF files.</span></span> <span data-ttu-id="0e4ad-112">Para obter mais informações, consulte o [objeto Writer](writer-object.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-112">For more information see, [Writer Object](writer-object.md).</span></span>

<span data-ttu-id="0e4ad-113">No cenário de gravação de arquivo mais básico, você atribui um perfil a ser usado e um nome do arquivo a ser criado.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-113">In the most basic file writing scenario, you assign a profile to use and a name of the file to create.</span></span> <span data-ttu-id="0e4ad-114">Você passa amostras para o gravador, um de cada vez.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-114">You pass samples to the writer one at a time.</span></span> <span data-ttu-id="0e4ad-115">Quando você terminar de passar amostras para o gravador, ele concluirá suas operações e preencherá o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-115">When you have finished passing samples to the writer, it finishes its operations and completes the ASF file.</span></span> <span data-ttu-id="0e4ad-116">Para obter mais informações sobre a gravação básica de arquivos, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-116">For more information about basic file writing, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="0e4ad-117">O gravador dá suporte a vários recursos avançados, que são discutidos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-117">The writer supports several advanced features, which are discussed in the following sections.</span></span>

-   [<span data-ttu-id="0e4ad-118">Redimensionamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="0e4ad-118">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="0e4ad-119">Conversão de espaço de cor</span><span class="sxs-lookup"><span data-stu-id="0e4ad-119">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="0e4ad-120">Reamostragem de áudio</span><span class="sxs-lookup"><span data-stu-id="0e4ad-120">Audio Resampling</span></span>](audio-resampling.md)
-   [<span data-ttu-id="0e4ad-121">Coletores</span><span class="sxs-lookup"><span data-stu-id="0e4ad-121">Sinks</span></span>](sinks.md)
-   [<span data-ttu-id="0e4ad-122">Suporte à marca d' água</span><span class="sxs-lookup"><span data-stu-id="0e4ad-122">Watermarking Support</span></span>](watermarking-support.md)
-   [<span data-ttu-id="0e4ad-123">Formatos de entrada, configurações de entrada e extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="0e4ad-123">Input Formats, Input Settings, and Data Unit Extensions</span></span>](input-formats-input-settings-and-data-unit-extensions.md)
-   [<span data-ttu-id="0e4ad-124">Enumeração de formato de entrada</span><span class="sxs-lookup"><span data-stu-id="0e4ad-124">Input Format Enumeration</span></span>](input-format-enumeration.md)

## <a name="related-topics"></a><span data-ttu-id="0e4ad-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e4ad-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e4ad-126">**Recursos**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-126">**Features**</span></span>](features.md)
</dt> </dl>

 

 





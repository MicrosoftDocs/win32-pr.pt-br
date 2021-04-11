---
title: Reamostragem de áudio
description: Reamostragem de áudio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- SDK do Windows Media Format, reamostragem de áudio
- Windows Media Format SDK, reamostrando áudio
- Formato de sistema avançado (ASF), reamostragem de áudio
- ASF (formato de sistemas avançados), reamostragem de áudio
- ASF (Advanced Systems Format), resolução de áudio de reamostragem
- ASF (formato de sistemas avançados), áudio de reamostragem
- reamostragem de áudio
- reamostrando áudio, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292162"
---
# <a name="audio-resampling"></a><span data-ttu-id="6aba3-111">Reamostragem de áudio</span><span class="sxs-lookup"><span data-stu-id="6aba3-111">Audio Resampling</span></span>

<span data-ttu-id="6aba3-112">Cada formato compactado de um codec de áudio tem uma taxa de amostragem e tamanho de amostra específicos.</span><span class="sxs-lookup"><span data-stu-id="6aba3-112">Every compressed format of an audio codec has a specific sample rate and sample size.</span></span> <span data-ttu-id="6aba3-113">Eles não precisam corresponder às configurações do formato de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="6aba3-113">These do not need to match the settings of the input format or output format.</span></span> <span data-ttu-id="6aba3-114">Se um formato de entrada tiver configurações diferentes do formato compactado descrito no perfil, o gravador recriará a amostra do áudio, durante o processo de codificação, para corresponder ao formato compactado.</span><span class="sxs-lookup"><span data-stu-id="6aba3-114">If an input format has different settings than the compressed format described in the profile, the writer will resample the audio, during the encoding process, to match the compressed format.</span></span> <span data-ttu-id="6aba3-115">Somente determinados formatos são aceitos pelo gravador como entrada.</span><span class="sxs-lookup"><span data-stu-id="6aba3-115">Only certain formats are accepted by the writer as input.</span></span> <span data-ttu-id="6aba3-116">Quando você enumera os formatos de entrada para um fluxo de áudio compactado, todos os formatos recuperados podem ser reamostrados para corresponder ao formato no perfil.</span><span class="sxs-lookup"><span data-stu-id="6aba3-116">When you enumerate the input formats for a compressed audio stream, all of the formats retrieved can be resampled to match the format in the profile.</span></span>

<span data-ttu-id="6aba3-117">Ao ler áudio compactado, o leitor irá reamostrar o conteúdo para corresponder ao formato de saída.</span><span class="sxs-lookup"><span data-stu-id="6aba3-117">When reading compressed audio, the reader will resample the content to match the output format.</span></span> <span data-ttu-id="6aba3-118">Você deve usar um dos formatos de saída enumerados pelo leitor, portanto, você tem a garantia de que o áudio pode ser reamostrado para as configurações de formato de saída.</span><span class="sxs-lookup"><span data-stu-id="6aba3-118">You must use one of the output formats enumerated by the reader, so you are guaranteed that the audio can be resampled to the output format settings.</span></span>

<span data-ttu-id="6aba3-119">Cada reamostrabilidade potencialmente afeta a qualidade do áudio.</span><span class="sxs-lookup"><span data-stu-id="6aba3-119">Each resampling potentially affects the quality of the audio.</span></span> <span data-ttu-id="6aba3-120">Quando possível, você deve usar formatos de entrada e saída com configurações que correspondam ao formato compactado.</span><span class="sxs-lookup"><span data-stu-id="6aba3-120">When possible, you should use input and output formats with settings that match the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6aba3-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6aba3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aba3-122">**Recursos de gravação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="6aba3-122">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="6aba3-123">**Trabalhando com entradas**</span><span class="sxs-lookup"><span data-stu-id="6aba3-123">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="6aba3-124">**Trabalhando com saídas**</span><span class="sxs-lookup"><span data-stu-id="6aba3-124">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 





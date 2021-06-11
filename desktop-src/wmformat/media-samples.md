---
title: Exemplos de mídia (Windows Media Format SDK 11)
description: Saiba mais sobre exemplos de mídia no SDK Windows Media Format 11. Um exemplo de mídia é um objeto que contém uma lista ordenada de zero ou mais buffers.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- SDK do Windows Media Format, exemplos de mídia
- Windows Media Format SDK,exemplos
- FORMATO DE SISTEMAS Avançados (ASF), exemplos de mídia
- ASF (Formato de Sistemas Avançados), exemplos de mídia
- ASF (Advanced Systems Format), samples
- ASF (Formato de Sistemas Avançados), exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8d264aa23e80f1e692f28789c2f2e631ef3ed8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989062"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="7b26c-110">Exemplos de mídia (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="7b26c-110">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="7b26c-111">Um exemplo de mídia, ou exemplo, é um bloco de dados de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="7b26c-111">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="7b26c-112">Um exemplo é a unidade básica que é manipulada pela leitura e pela escrita de objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="7b26c-112">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="7b26c-113">O conteúdo de um exemplo individual é ditado pelo tipo de mídia associado ao exemplo.</span><span class="sxs-lookup"><span data-stu-id="7b26c-113">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="7b26c-114">Para vídeo, cada exemplo representa um único quadro.</span><span class="sxs-lookup"><span data-stu-id="7b26c-114">For video, each sample represents a single frame.</span></span> <span data-ttu-id="7b26c-115">Para áudio, a quantidade de dados em um exemplo individual é definida no perfil usado para criar o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="7b26c-115">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="7b26c-116">Os exemplos podem conter dados descompactados ou podem conter dados compactados; nesse caso, eles são chamados de *amostras de fluxo.*</span><span class="sxs-lookup"><span data-stu-id="7b26c-116">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="7b26c-117">Ao criar um arquivo ASF, você passa amostras para o autor.</span><span class="sxs-lookup"><span data-stu-id="7b26c-117">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="7b26c-118">O autor coordena a compactação dos exemplos com o codec apropriado e organiza os dados compactados na seção de dados do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="7b26c-118">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="7b26c-119">Na reprodução, o leitor lê os dados compactados, os descompacta e fornece os dados descompactados reconstruídos como exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="7b26c-119">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="7b26c-120">Todos os exemplos usados pelo SDK Windows Media Format são encapsulados no objeto de buffer cuja memória é alocada automaticamente pelos componentes de tempo de run time do SDK.</span><span class="sxs-lookup"><span data-stu-id="7b26c-120">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="7b26c-121">Você também pode alocar seus próprios buffers se precisar, usando recursos avançados do leitor e do autor.</span><span class="sxs-lookup"><span data-stu-id="7b26c-121">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="7b26c-122">**Observação** O termo exemplo é usado neste SDK para se referir a um exemplo de mídia, não a um exemplo de áudio.</span><span class="sxs-lookup"><span data-stu-id="7b26c-122">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="7b26c-123">Na codificação de áudio, um exemplo refere-se a um único valor de áudio codificado.</span><span class="sxs-lookup"><span data-stu-id="7b26c-123">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="7b26c-124">Normalmente, a qualidade do áudio codificado é especificada por um número de amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="7b26c-124">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="7b26c-125">Por exemplo, o som de qualidade de CD é registrado em 44.100 amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="7b26c-125">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="7b26c-126">Esse valor geralmente é abreviado com a notação de Hz, portanto, 44.100 amostras por segundo seriam 44.100 Hz ou 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="7b26c-126">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b26c-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b26c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b26c-128">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="7b26c-128">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="7b26c-129">**INSSBuffer Interface**</span><span class="sxs-lookup"><span data-stu-id="7b26c-129">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="7b26c-130">**Entradas, fluxos e saídas**</span><span class="sxs-lookup"><span data-stu-id="7b26c-130">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 





---
title: Amostras de mídia (SDK do Windows Media Format 11)
description: Amostras de mídia
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- SDK do Windows Media Format, amostras de mídia
- SDK do Windows Media Format, exemplos
- ASF (Advanced Systems Format), amostras de mídia
- ASF (formato de sistemas avançados), amostras de mídia
- ASF (Advanced Systems Format), amostras
- ASF (formato de sistemas avançados), amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103917931"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="a2750-109">Amostras de mídia (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="a2750-109">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a2750-110">Um exemplo de mídia, ou exemplo, é um bloco de dados de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="a2750-110">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="a2750-111">Um exemplo é a unidade básica que é manipulada pelos objetos de leitura e gravação do SDK do formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="a2750-111">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="a2750-112">O conteúdo de um exemplo individual é ditado pelo tipo de mídia associado ao exemplo.</span><span class="sxs-lookup"><span data-stu-id="a2750-112">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="a2750-113">Para vídeo, cada amostra representa um único quadro.</span><span class="sxs-lookup"><span data-stu-id="a2750-113">For video, each sample represents a single frame.</span></span> <span data-ttu-id="a2750-114">Para áudio, a quantidade de dados em um exemplo individual é definida no perfil usado para criar o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="a2750-114">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="a2750-115">Os exemplos podem conter dados descompactados ou podem conter dados compactados; nesse caso, eles são chamados de *amostras de fluxo*.</span><span class="sxs-lookup"><span data-stu-id="a2750-115">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="a2750-116">Ao criar um arquivo ASF, você passa amostras para o gravador.</span><span class="sxs-lookup"><span data-stu-id="a2750-116">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="a2750-117">O gravador coordena a compactação dos exemplos com o codec apropriado e organiza os dados compactados na seção de dados do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="a2750-117">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="a2750-118">Na reprodução, o leitor lê os dados compactados, descompacta-os e fornece os dados não compactados reconstruídos como exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="a2750-118">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="a2750-119">Todos os exemplos usados pelo Windows Media Format SDK são encapsulados no objeto de buffer cuja memória é alocada automaticamente pelos componentes de tempo de execução do SDK.</span><span class="sxs-lookup"><span data-stu-id="a2750-119">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="a2750-120">Você também pode alocar seus próprios buffers se precisar, usando recursos avançados do gravador e do leitor.</span><span class="sxs-lookup"><span data-stu-id="a2750-120">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="a2750-121">**Observação** O termo exemplo é usado neste SDK para se referir a um exemplo de mídia, não a um exemplo de áudio.</span><span class="sxs-lookup"><span data-stu-id="a2750-121">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="a2750-122">Em codificação de áudio, um exemplo refere-se a um único valor de áudio codificado.</span><span class="sxs-lookup"><span data-stu-id="a2750-122">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="a2750-123">Normalmente, a qualidade do áudio codificado é especificada por um número de amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="a2750-123">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="a2750-124">Por exemplo, o som de qualidade do CD é registrado em 44.100 amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="a2750-124">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="a2750-125">Esse valor é geralmente abreviado com a notação Hz, de modo que 44.100 amostras por segundo seriam 44.100 Hz ou 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="a2750-125">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2750-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2750-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2750-127">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="a2750-127">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="a2750-128">**Interface INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="a2750-128">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="a2750-129">**Entradas, fluxos e saídas**</span><span class="sxs-lookup"><span data-stu-id="a2750-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 





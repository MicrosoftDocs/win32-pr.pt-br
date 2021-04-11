---
title: Redimensionamento de vídeo
description: Redimensionamento de vídeo
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- SDK do Windows Media Format, redimensionamento de vídeo
- SDK do Windows Media Format, redimensionando vídeo
- ASF (Advanced Systems Format), redimensionamento de vídeo
- ASF (formato de sistemas avançados), redimensionamento de vídeo
- ASF (Advanced Systems Format), redimensionando vídeo
- ASF (formato de sistemas avançados), redimensionando vídeo
- redimensionamento de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159591"
---
# <a name="video-resizing"></a><span data-ttu-id="fe136-110">Redimensionamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="fe136-110">Video Resizing</span></span>

<span data-ttu-id="fe136-111">Ao definir as configurações para um fluxo de vídeo, você deve especificar uma largura e uma altura para os quadros de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fe136-111">When you define the settings for a video stream, you must specify a width and height for the video frames.</span></span> <span data-ttu-id="fe136-112">Esse tamanho de vídeo determina o tamanho dos quadros de vídeo codificados na seção de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="fe136-112">This video size determines the size of the video frames encoded in the data section of the file.</span></span> <span data-ttu-id="fe136-113">No entanto, o tamanho do vídeo em um perfil não determina ou limita o tamanho da mídia de entrada que você entrega ao gravador ou o tamanho da mídia de saída que você recebe do leitor.</span><span class="sxs-lookup"><span data-stu-id="fe136-113">However, the video size in a profile does not determine, or limit, the size of the input media that you deliver to the writer, or the size of the output media you receive from the reader.</span></span> <span data-ttu-id="fe136-114">O gravador pode redimensionar os quadros de vídeo para atender às necessidades do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fe136-114">The writer can resize the video frames to suit the needs of your application.</span></span>

<span data-ttu-id="fe136-115">O tamanho da imagem de vídeo pode ser pensado como passar por três estágios: tamanho do vídeo de entrada, tamanho do vídeo de fluxo e tamanho do vídeo de saída.</span><span class="sxs-lookup"><span data-stu-id="fe136-115">Video image size can be thought of as going through three stages: input video size, stream video size, and output video size.</span></span>

<span data-ttu-id="fe136-116">O tamanho do vídeo de entrada é o tamanho dos quadros que você passa como amostras para o objeto do gravador.</span><span class="sxs-lookup"><span data-stu-id="fe136-116">Input video size is the size of the frames that you pass as samples to the writer object.</span></span> <span data-ttu-id="fe136-117">Você define esse tamanho como uma das propriedades de entrada de vídeo necessárias.</span><span class="sxs-lookup"><span data-stu-id="fe136-117">You define this size as one of the required video input properties.</span></span> <span data-ttu-id="fe136-118">Para obter mais informações sobre propriedades de entrada, consulte [para enumerar formatos de entrada](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="fe136-118">For more information about input properties, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

<span data-ttu-id="fe136-119">O tamanho do vídeo do fluxo é o tamanho dos quadros na seção de dados do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="fe136-119">Stream video size is the size of the frames in the data section of the ASF file.</span></span> <span data-ttu-id="fe136-120">Você define esse tamanho como uma das definições de configuração de fluxo necessárias no perfil.</span><span class="sxs-lookup"><span data-stu-id="fe136-120">You define this size as one of the required stream configuration settings in the profile.</span></span> <span data-ttu-id="fe136-121">Se você estiver gravando um arquivo e o tamanho do vídeo de entrada for diferente do tamanho do vídeo do fluxo, o gravador redimensionará os quadros durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="fe136-121">If you are writing a file and the input video size is different from the stream video size, the writer resizes the frames while encoding.</span></span> <span data-ttu-id="fe136-122">Para obter mais informações sobre as propriedades de fluxo de vídeo, consulte [Configuring Video Streams](configuring-video-streams.md).</span><span class="sxs-lookup"><span data-stu-id="fe136-122">For more information about video stream properties, see [Configuring Video Streams](configuring-video-streams.md).</span></span>

<span data-ttu-id="fe136-123">Tamanho do vídeo de saída é o tamanho dos quadros entregues pelo leitor ou leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="fe136-123">Output video size is the size of the frames delivered by the reader or synchronous reader.</span></span> <span data-ttu-id="fe136-124">Você define esse tamanho como uma das propriedades de saída de vídeo necessárias.</span><span class="sxs-lookup"><span data-stu-id="fe136-124">You define this size as one of the required video output properties.</span></span> <span data-ttu-id="fe136-125">Se você estiver lendo um arquivo e o tamanho do vídeo de saída for diferente do tamanho do vídeo do fluxo, o leitor redimensionará os quadros durante a decodificação.</span><span class="sxs-lookup"><span data-stu-id="fe136-125">If you are reading a file and the output video size is different from the stream video size, the reader resizes the frames while decoding.</span></span>

<span data-ttu-id="fe136-126">Não é possível definir um tamanho de vídeo de fluxo para um número ímpar de pixels de largura.</span><span class="sxs-lookup"><span data-stu-id="fe136-126">You cannot set a stream video size to an odd number of pixels wide.</span></span> <span data-ttu-id="fe136-127">Se você definir a largura de um fluxo de vídeo com um valor ímpar, o perfil não será aceito pelo gravador ou o vídeo resultante será codificado com uma linha preta de um lado para fazer a diferença.</span><span class="sxs-lookup"><span data-stu-id="fe136-127">If you set the width of a video stream to an odd value, either the profile will not be accepted by the writer, or the resulting video will be encoded with a black line down one side to make up the difference.</span></span>

<span data-ttu-id="fe136-128">Você deve tomar cuidado ao redimensionar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="fe136-128">You should take care when resizing video.</span></span> <span data-ttu-id="fe136-129">As imagens tendem a ter a melhor aparência em sua resolução original.</span><span class="sxs-lookup"><span data-stu-id="fe136-129">Images tend to look their best at their original resolution.</span></span> <span data-ttu-id="fe136-130">O redimensionamento de imagens pode muitas vezes causar distorção e tornar o texto ilegível.</span><span class="sxs-lookup"><span data-stu-id="fe136-130">Resizing images can often cause distortion and make text illegible.</span></span> <span data-ttu-id="fe136-131">Se você estiver compactando o vídeo em uma taxa de bits baixa, também verá que o redimensionamento de distorções pode levar a artefatos de compactação graves.</span><span class="sxs-lookup"><span data-stu-id="fe136-131">If you are compressing video to a low bit rate, you will also find that resizing distortions can lead to severe compression artifacts.</span></span>

<span data-ttu-id="fe136-132">O codec de tela do Windows Media Video 9 não dá suporte ao redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="fe136-132">The Windows Media Video 9 Screen codec does not support resizing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe136-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe136-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe136-134">**Recursos de gravação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="fe136-134">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="fe136-135">**Trabalhando com entradas**</span><span class="sxs-lookup"><span data-stu-id="fe136-135">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="fe136-136">**Trabalhando com saídas**</span><span class="sxs-lookup"><span data-stu-id="fe136-136">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 





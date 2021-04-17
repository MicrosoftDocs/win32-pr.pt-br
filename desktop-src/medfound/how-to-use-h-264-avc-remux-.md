---
description: Este tópico descreve quando e como usar uma MFT e um coletor MP4 de H. 264/AVC remux.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Quando e como usar o remux do H. 264/AVC e o coletor MP4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762346"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="b00e5-103">Quando e como usar o remux do H. 264/AVC e o coletor MP4</span><span class="sxs-lookup"><span data-stu-id="b00e5-103">When and How to Use H.264/AVC Remux MFT and MP4 Sink</span></span>

<span data-ttu-id="b00e5-104">Este tópico descreve quando e como usar uma MFT e um coletor MP4 de H. 264/AVC remux.</span><span class="sxs-lookup"><span data-stu-id="b00e5-104">This topic describes when and how to use a H.264/AVC Remux MFT and MP4 Sink.</span></span>

## <a name="when-to-use-h264avc-remux-mft"></a><span data-ttu-id="b00e5-105">Quando usar o H. 264/AVC remux MFT</span><span class="sxs-lookup"><span data-stu-id="b00e5-105">When to use H.264/AVC Remux MFT</span></span>

<span data-ttu-id="b00e5-106">O formato de arquivo MPEG-4 requer que cada amostra compactada contenha uma imagem primária com unidades NAL na ordem correta.</span><span class="sxs-lookup"><span data-stu-id="b00e5-106">MPEG-4 file format requires that each compressed sample contains one primary picture with NAL units in the correct order.</span></span> <span data-ttu-id="b00e5-107">(Consulte a definição da imagem primária e a ordem obrigatória das unidades de NAL na seção 7.4.1.2.3, **ordem das unidades de nal e imagens codificadas e associação às unidades de acesso**, da especificação da H. 264 AVC.) Ele também requer que cada amostra compactada esteja associada a um carimbo de data/hora de apresentação, decodificação de carimbo de data/hora e duração da amostra.</span><span class="sxs-lookup"><span data-stu-id="b00e5-107">(Please refer to the definition of primary picture and mandatory NAL units order in section 7.4.1.2.3, **Order of NAL units and coded pictures and association to access units**, of the H.264 AVC specification.) It also requires each compressed sample is associated with a presentation time stamp, decoding time stamp, and sample duration.</span></span>

<span data-ttu-id="b00e5-108">Em muitos cenários, quando os aplicativos precisam gravar vídeo H. 264/AVC em um contêiner de arquivos MPEG-4, o exemplo compactado pode não atender aos requisitos acima.</span><span class="sxs-lookup"><span data-stu-id="b00e5-108">In many scenarios when applications need to record H.264/AVC video in a MPEG-4 file container, the compressed sample may not satisfy the above requirements.</span></span> <span data-ttu-id="b00e5-109">Por exemplo, um exemplo compactado pode não conter uma imagem primária completa ou pode não ter um carimbo de data/hora de apresentação correto associado a ela.</span><span class="sxs-lookup"><span data-stu-id="b00e5-109">For example, one compressed sample might not contain a complete primary picture or might not have a correct presentation time stamp associated with it.</span></span> <span data-ttu-id="b00e5-110">Alguns exemplos de aplicativos são:</span><span class="sxs-lookup"><span data-stu-id="b00e5-110">A few application examples are:</span></span>

-   <span data-ttu-id="b00e5-111">Escreva o vídeo elementares de streaming H. 264/AVC no contêiner de arquivos MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="b00e5-111">Write H.264/AVC streaming elementary video into MPEG-4 file container.</span></span>
-   <span data-ttu-id="b00e5-112">Gravar vídeo da câmera capturada H. 264/AVC no contêiner de arquivos MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="b00e5-112">Record camera captured H.264/AVC elementary video in MPEG-4 file container.</span></span>
-   <span data-ttu-id="b00e5-113">Registre a conferência de vídeo H. 264/AVC no contêiner de arquivos MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="b00e5-113">Record H.264/AVC video conference in MPEG-4 file container.</span></span>
-   <span data-ttu-id="b00e5-114">Concatenar dois vídeos H. 264/AVC em MPEG-2 TS ou MP4 e gravar no contêiner de arquivos MPEG-4 com carimbos de data/hora corretos.</span><span class="sxs-lookup"><span data-stu-id="b00e5-114">Concatenate two H.264/AVC video in MPEG-2 TS or MP4 and write into MPEG-4 file container with correct time stamps.</span></span>
-   <span data-ttu-id="b00e5-115">Vídeo remux H. 264/AVC de AVCHD, MPEG-2 formato de arquivo TS/PS para formato de arquivo MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="b00e5-115">Remux H.264/AVC video from AVCHD, MPEG-2 TS/PS file format to MPEG-4 file format.</span></span>
-   <span data-ttu-id="b00e5-116">Corte o arquivo de vídeo H. 264/AVC sem transcodificação.</span><span class="sxs-lookup"><span data-stu-id="b00e5-116">Trim H.264/AVC video file without transcoding.</span></span>

<span data-ttu-id="b00e5-117">Nessa situação, o aplicativo precisa usar um MFT remux de H. 264/AVC para converter as amostras compactadas que não contêm uma imagem primária completa antes de serem gravadas no contêiner de arquivos MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="b00e5-117">In this situation, the application needs to use a H.264/AVC remux MFT to convert the compressed samples not containing a complete primary picture before they are written into the MPEG-4 file container.</span></span>

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="b00e5-118">Como usar a MFT e o coletor MP4 do H. 264/AVC remux</span><span class="sxs-lookup"><span data-stu-id="b00e5-118">How to use H.264/AVC Remux MFT and MP4 sink</span></span>

<span data-ttu-id="b00e5-119">Defina o tipo de mídia de saída de origem como **MFVideoFormat \_ H264 \_ es**, que indica que cada exemplo pode não conter uma imagem primária completa.</span><span class="sxs-lookup"><span data-stu-id="b00e5-119">Set the source output media type to **MFVideoFormat\_H264\_ES**, which indicates each sample might not contain a complete primary picture.</span></span> <span data-ttu-id="b00e5-120">Defina o tipo de mídia de entrada do coletor MP4 como **MFVideoFormat \_ H264**.</span><span class="sxs-lookup"><span data-stu-id="b00e5-120">Set the input media type of MP4 sink to **MFVideoFormat\_H264**.</span></span> <span data-ttu-id="b00e5-121">Portanto, o tipo de mídia de entrada do MFT H. 264/AVC remux é **MFVideoFormat \_ H264 \_ es** e o tipo de mídia de saída do MFT h. 264/AVC remux é **MFVideoFormat \_ H264**, que será inserido automaticamente no resolvedor de topologia.</span><span class="sxs-lookup"><span data-stu-id="b00e5-121">So, the input media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264\_ES** and the output media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264**, which will be automatically inserted into the topology resolver.</span></span>

<span data-ttu-id="b00e5-122">A duração da amostra é ignorada pelo remux H. 264/AVC, pois a duração da amostra de um exemplo que não contém uma imagem primária completa não tem significado claro.</span><span class="sxs-lookup"><span data-stu-id="b00e5-122">Sample duration is ignored by the H.264/AVC remux, because the sample duration for a sample not containing a complete primary picture does not have clear meaning.</span></span> <span data-ttu-id="b00e5-123">Em vez disso, a duração da amostra é calculada a partir da taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="b00e5-123">Instead, the sample duration is calculated from the frame rate.</span></span> <span data-ttu-id="b00e5-124">A taxa de quadros é calculada a partir do parâmetro Sequence.</span><span class="sxs-lookup"><span data-stu-id="b00e5-124">The frame rate is calculated from the sequence parameter.</span></span> <span data-ttu-id="b00e5-125">Se as informações não existirem no parâmetro Sequence, a taxa de quadros será calculada a partir dos parâmetros no tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="b00e5-125">If the information does not exist in the sequence parameter, the frame rate is calculated from the parameters in the input media type.</span></span> <span data-ttu-id="b00e5-126">Se as informações de taxa de quadros não estiverem disponíveis, a taxa de quadros padrão de 29,97 fps será usada.</span><span class="sxs-lookup"><span data-stu-id="b00e5-126">If frame rate information is not available, the default frame rate of 29.97 fps is used.</span></span>

<span data-ttu-id="b00e5-127">H. 264/AVC remux MFT interpola linearmente os carimbos de data/hora de decodificação (DTS) para cada imagem compactada de acordo com a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="b00e5-127">H.264/AVC remux MFT linearly interpolates the decoding time stamps (DTS) for each compressed picture according to the frame rate.</span></span> <span data-ttu-id="b00e5-128">O MFT H. 264/AVC remux honra os carimbos de data/hora de apresentação de entrada (PTS) nos exemplos de entrada e os transmite para a saída, se existirem.</span><span class="sxs-lookup"><span data-stu-id="b00e5-128">H.264/AVC remux MFT honors the input presentation time stamps (PTS) in input samples and passes them to the output if they exist.</span></span> <span data-ttu-id="b00e5-129">Ele executa a interpolação de PTS de acordo com a taxa de quadros, a PTS anterior e a ordem de saída da imagem por meio do processo de relevo do DBP (buffer de imagem decodificado), conforme especificado no **processo de relevo do anexo C. 4.5.3** da especificação do H. 264 AVC.</span><span class="sxs-lookup"><span data-stu-id="b00e5-129">It performs PTS interpolation according to frame rate, the previous PTS, and the picture output order through Decoded Picture Buffering (DBP) bumping process as specified in **Annex C.4.5.3 Bumping process** of the H.264 AVC specification.</span></span> <span data-ttu-id="b00e5-130">Cada exemplo de saída do MFT da H. 264/AVC remux deve ter PTS, DTS e duração de amostra.</span><span class="sxs-lookup"><span data-stu-id="b00e5-130">Each output sample from the H.264/AVC remux MFT shall have PTS, DTS, and sample duration.</span></span> <span data-ttu-id="b00e5-131">O MFT H. 264/AVC remux também identifica as imagens de IDR no fragmentado e as define como um ponto de limpeza com o atributo MF de [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="b00e5-131">H.264/AVC remux MFT also identifies the IDR pictures in the bitstream and sets them as clean point with the MF attribute of [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span></span>

<span data-ttu-id="b00e5-132">Atualmente, o MFT da H. 264/AVC remux pode lidar com um máximo de 64 quadro reordenado.</span><span class="sxs-lookup"><span data-stu-id="b00e5-132">Currently the H.264/AVC remux MFT can handle a maximum of 64 reordered frame.</span></span> <span data-ttu-id="b00e5-133">Se o número de quadros reordenados exceder 64 com um quadro de referência de longo prazo presente, o MFT H. 264/AVC remux interpolará um PTS incorreto para esse quadro e produzirá esse quadro em um horário incorreto.</span><span class="sxs-lookup"><span data-stu-id="b00e5-133">If the number of reordered frame exceeds 64 with a long term reference frame present, the H.264/AVC remux MFT will interpolate a wrong PTS for that frame and output that frame at a wrong time.</span></span>

<span data-ttu-id="b00e5-134">Para instanciar um MFT do H. 264/AVC remux, defina os tipos de mídia de entrada e saída corretos no MFT do H. 264/AVC remux, defina o tipo de mídia de entrada para o coletor MP4 e resolva a topologia.</span><span class="sxs-lookup"><span data-stu-id="b00e5-134">To instantiate a H.264/AVC remux MFT, set the correct input and output media types on the H.264/AVC remux MFT, set the input media type for the MP4 sink, and resolve the topology.</span></span>

<span data-ttu-id="b00e5-135">O código de exemplo a seguir mostra como inicializar a MFT e o coletor MP4 do H. 264/AVC remux.</span><span class="sxs-lookup"><span data-stu-id="b00e5-135">The following sample code show how to initialize the H.264/AVC remux MFT and MP4 sink.</span></span>

<span data-ttu-id="b00e5-136">Para o MFT de H. 264/AVC remux,</span><span class="sxs-lookup"><span data-stu-id="b00e5-136">For H.264/AVC remux MFT,</span></span>


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



<span data-ttu-id="b00e5-137">Nenhuma outra configuração é necessária.</span><span class="sxs-lookup"><span data-stu-id="b00e5-137">No further configuration is necessary.</span></span>

<span data-ttu-id="b00e5-138">Para o coletor MP4,</span><span class="sxs-lookup"><span data-stu-id="b00e5-138">For MP4 sink,</span></span>


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a><span data-ttu-id="b00e5-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b00e5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b00e5-140">Formatos de mídia compatíveis com o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b00e5-140">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




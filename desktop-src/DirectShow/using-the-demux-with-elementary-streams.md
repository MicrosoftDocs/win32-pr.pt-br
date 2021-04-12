---
description: Usando o demux com fluxos elementares
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Usando o demux com fluxos elementares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b9004d6c99db96405797016b0d9854c96dae92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296928"
---
# <a name="using-the-demux-with-elementary-streams"></a><span data-ttu-id="1205c-103">Usando o demux com fluxos elementares</span><span class="sxs-lookup"><span data-stu-id="1205c-103">Using the Demux with Elementary Streams</span></span>

<span data-ttu-id="1205c-104">Quando o MPEG-2 Demux entrega cargas de PES, ele envia o fluxo de s bytes em lotes de amostras de mídia.</span><span class="sxs-lookup"><span data-stu-id="1205c-104">When the MPEG-2 demux delivers PES payloads, it sends the ES byte stream in batches of media samples.</span></span> <span data-ttu-id="1205c-105">O tamanho de amostra padrão é 8K.</span><span class="sxs-lookup"><span data-stu-id="1205c-105">The default sample size is 8K.</span></span> <span data-ttu-id="1205c-106">O Demux inicia um novo exemplo de mídia em cada limite de PES, mas pode quebrar uma única carga PES em vários exemplos.</span><span class="sxs-lookup"><span data-stu-id="1205c-106">The demux starts a new media sample on each PES boundary, but may break a single PES payload into several samples.</span></span> <span data-ttu-id="1205c-107">Por exemplo, se uma carga PES for 20 mil, ela será entregue em dois exemplos de 8K seguidos de um exemplo de 4K.</span><span class="sxs-lookup"><span data-stu-id="1205c-107">For example, if a PES payload is 20K, it will be delivered in two 8K samples followed by one 4K sample.</span></span> <span data-ttu-id="1205c-108">O Demux não examina o conteúdo do fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="1205c-108">The demux does not examine the contents of the byte stream.</span></span> <span data-ttu-id="1205c-109">Cabe ao decodificador analisar os cabeçalhos de sequência e procurar alterações de formato.</span><span class="sxs-lookup"><span data-stu-id="1205c-109">It is up to the decoder to parse the sequence headers and look for format changes.</span></span>

<span data-ttu-id="1205c-110">Quando o pino de saída do Filtro Demux se conecta ao decodificador, ele oferece o tipo de mídia que foi especificado quando o PIN foi criado.</span><span class="sxs-lookup"><span data-stu-id="1205c-110">When the demux filter's output pin connects to the decoder, it offers the media type that was specified when the pin was created.</span></span> <span data-ttu-id="1205c-111">Como o Demux não examina o fluxo de ES bytes, ele não valida o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="1205c-111">Because the demux does not examine the ES byte stream, it does not validate the media type.</span></span> <span data-ttu-id="1205c-112">Teoricamente, um decodificador MPEG-2 deve ser capaz de se conectar apenas ao tipo principal e ao subtipo preenchido, para indicar o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1205c-112">In theory, an MPEG-2 decoder should be able to connect with just the major type and subtype filled in, to indicate the type of data.</span></span> <span data-ttu-id="1205c-113">O decodificador deve examinar os cabeçalhos de sequência que chegam nos exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="1205c-113">The decoder should then examine the sequence headers that arrive in the media samples.</span></span> <span data-ttu-id="1205c-114">No entanto, na prática, muitos decodificadores não serão conectados, a menos que o tipo de mídia inclua um bloco de formato completo.</span><span class="sxs-lookup"><span data-stu-id="1205c-114">However, in practice, many decoders will not connect unless the media type includes a complete format block.</span></span>

<span data-ttu-id="1205c-115">Por exemplo, suponha que o PID 0x31 contenha o vídeo de perfil principal MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="1205c-115">For example, suppose that PID 0x31 contains MPEG-2 main profile video.</span></span> <span data-ttu-id="1205c-116">No mínimo, você precisaria executar as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="1205c-116">At a minimum, you would need to do the following steps.</span></span>

<span data-ttu-id="1205c-117">Primeiro, crie um tipo de mídia para vídeo MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="1205c-117">First, create a media type for MPEG-2 video.</span></span> <span data-ttu-id="1205c-118">Deixando de lado o bloco de formato por enquanto:</span><span class="sxs-lookup"><span data-stu-id="1205c-118">Leaving aside the format block for now:</span></span>


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



<span data-ttu-id="1205c-119">Em seguida, crie um PIN de saída no Demux:</span><span class="sxs-lookup"><span data-stu-id="1205c-119">Next, create an output pin on the demux:</span></span>


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Create a new output pin.
    IPin *pPin0;
    hr = pDemux->CreateOutputPin(&mt, L"Video Pin", &pPin0);
    if (SUCCEEDED(hr))
    {
        ....
    }
}
```



<span data-ttu-id="1205c-120">Em seguida, consulte o novo PIN para a interface **IMPEG2PIDMap** e chame **MapPID**.</span><span class="sxs-lookup"><span data-stu-id="1205c-120">Then, query the new pin for the **IMPEG2PIDMap** interface and call **MapPID**.</span></span> <span data-ttu-id="1205c-121">Especifique o número PID 0x30 e o \_ fluxo elementar mídia \_ para cargas PES.</span><span class="sxs-lookup"><span data-stu-id="1205c-121">Specify PID number 0x30, and MEDIA\_ELEMENTARY\_STREAM for PES payloads.</span></span>


```C++
// Query the pin for IMPEG2PIDMap. This implicitly configures the
// demux to carry a transport stream. 
IMPEG2PIDMap *pPidMap;
hr = pPin0->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
if (SUCCEEDED(hr))
{
    // Assign PID 0x31 to pin 0. Set the type to "PES payload."
    ULONG Pid = 0x031;
    hr = pPidMap->MapPID(1, &Pid, MEDIA_ELEMENTARY_STREAM);
    pPidMap->Release();
}
```



<span data-ttu-id="1205c-122">Por fim, libere todas as interfaces quando terminar:</span><span class="sxs-lookup"><span data-stu-id="1205c-122">Finally, release all interfaces when you are done:</span></span>


```C++
pPin0->Release();
pDemux->Release();
```



<span data-ttu-id="1205c-123">Veja um exemplo mais completo de como definir o tipo de mídia, incluindo o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="1205c-123">Here is a more complete example of setting the media type, including the format block.</span></span> <span data-ttu-id="1205c-124">Este exemplo ainda assume um vídeo de perfil principal MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="1205c-124">This example still assumes an MPEG-2 main profile video.</span></span> <span data-ttu-id="1205c-125">Os detalhes irão variar dependendo do conteúdo do fluxo:</span><span class="sxs-lookup"><span data-stu-id="1205c-125">The details will vary depending on stream contents:</span></span>


```C++
// Set up a byte array to hold the first sequence header. 
// This may or may not be required, depending on the decoder.
BYTE SeqHdr[] = { ... };  // Contains the sequence header (not shown).

AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
mt.formattype = FORMAT_MPEG2Video;

// Allocate the format block, including space for the sequence header. 
mt.cbFormat = sizeof(MPEG2VIDEOINFO) + sizeof(SeqHdr);
mt.pbFormat = (BYTE*)CoTaskMemAlloc(mt.cbFormat);
if (mt.pbFormat == NULL)
{
    // Out of memory; return an error code.
}
ZeroMemory(mt.pbFormat, mt.cbFormat);

// Cast the buffer pointer to an MPEG2VIDEOINFO struct.
MPEG2VIDEOINFO *pMVIH = (MPEG2VIDEOINFO*)mt.pbFormat;

RECT rcSrc = {0, 480, 0, 720};        // Source rectangle.
pMVIH->hdr.rcSource = rcSrc;
pMVIH->hdr.dwBitRate = 4000000;       // Bit rate.
pMVIH->hdr.AvgTimePerFrame = 333667;  // 29.97 fps.
pMVIH->hdr.dwPictAspectRatioX = 4;    // 4:3 aspect ratio.
pMVIH->hdr.dwPictAspectRatioY = 3;

// BITMAPINFOHEADER information.
pMVIH->hdr.bmiHeader.biSize = 40;
pMVIH->hdr.bmiHeader.biWidth = 720;
pMVIH->hdr.bmiHeader.biHeight = 480;

pMVIH->dwLevel = AM_MPEG2Profile_Main;  // MPEG-2 profile. 
pMVIH->dwProfile = AM_MPEG2Level_Main;  // MPEG-2 level.

// Copy the sequence header into the format block.
pMVIH->cbSequenceHeader = sizeof(SeqHdr); // Size of sequence header.
memcpy(pMVIH->dwSequenceHeader, SeqHdr, sizeof(SeqHdr));
```



## <a name="related-topics"></a><span data-ttu-id="1205c-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1205c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1205c-127">Usando o demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="1205c-127">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




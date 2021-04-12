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
# <a name="using-the-demux-with-elementary-streams"></a>Usando o demux com fluxos elementares

Quando o MPEG-2 Demux entrega cargas de PES, ele envia o fluxo de s bytes em lotes de amostras de mídia. O tamanho de amostra padrão é 8K. O Demux inicia um novo exemplo de mídia em cada limite de PES, mas pode quebrar uma única carga PES em vários exemplos. Por exemplo, se uma carga PES for 20 mil, ela será entregue em dois exemplos de 8K seguidos de um exemplo de 4K. O Demux não examina o conteúdo do fluxo de bytes. Cabe ao decodificador analisar os cabeçalhos de sequência e procurar alterações de formato.

Quando o pino de saída do Filtro Demux se conecta ao decodificador, ele oferece o tipo de mídia que foi especificado quando o PIN foi criado. Como o Demux não examina o fluxo de ES bytes, ele não valida o tipo de mídia. Teoricamente, um decodificador MPEG-2 deve ser capaz de se conectar apenas ao tipo principal e ao subtipo preenchido, para indicar o tipo de dados. O decodificador deve examinar os cabeçalhos de sequência que chegam nos exemplos de mídia. No entanto, na prática, muitos decodificadores não serão conectados, a menos que o tipo de mídia inclua um bloco de formato completo.

Por exemplo, suponha que o PID 0x31 contenha o vídeo de perfil principal MPEG-2. No mínimo, você precisaria executar as etapas a seguir.

Primeiro, crie um tipo de mídia para vídeo MPEG-2. Deixando de lado o bloco de formato por enquanto:


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



Em seguida, crie um PIN de saída no Demux:


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



Em seguida, consulte o novo PIN para a interface **IMPEG2PIDMap** e chame **MapPID**. Especifique o número PID 0x30 e o \_ fluxo elementar mídia \_ para cargas PES.


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



Por fim, libere todas as interfaces quando terminar:


```C++
pPin0->Release();
pDemux->Release();
```



Veja um exemplo mais completo de como definir o tipo de mídia, incluindo o bloco de formato. Este exemplo ainda assume um vídeo de perfil principal MPEG-2. Os detalhes irão variar dependendo do conteúdo do fluxo:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




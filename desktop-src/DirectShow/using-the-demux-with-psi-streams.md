---
description: usando o Demux com PSI Fluxos
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: usando o Demux com PSI Fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3935e188b6e06d1037f08d4ca7bab98918f87d2c652b8506650a6cf3a280dc04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633136"
---
# <a name="using-the-demux-with-psi-streams"></a>usando o Demux com PSI Fluxos

Para obter informações de PSI de um fluxo de transporte MPEG-2 usando o Filtro Demux MPEG-2, crie um PIN de saída no demux com o seguinte tipo de mídia:

-   Tipo principal: KSDATAFORMAT \_ tipo \_ de \_ seções MPEG2
-   Subtipo: MEDIASUBTYPE \_ None
-   Tipo de formato: GUID \_ NULL

Em seguida, chame o método [**IMPEG2PIDMap:: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) do pino de saída com o PID desejado e o sinalizador de mídia \_ MPEG2 \_ psi.


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux = NULL;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Define the media type.
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
    mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;
    mt.subtype = MEDIASUBTYPE_None;

    // Create a new output pin.
    IPin *pPin;
    hr = pDemux->CreateOutputPin(&mt, L"PSI Pin", &pPin);
    if (SUCCEEDED(hr))
    {
        // Map the PID.
        IMPEG2PIDMap *pPidMap = NULL;
        hr = pPin->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
        if (SUCCEEDED(hr))
        {
            ULONG Pid[] = { 0x00 }; // Map any desired PIDs. 
            ULONG cPid = 1;
            hr = pPidMap->MapPID(cPid, Pid, MEDIA_MPEG2_PSI);
            pPidMap->Release();
        }
        pPin->Release();
    }
    pDemux->Release();
}
```



Cada seção PSI completa é entregue em um exemplo de mídia. Para recuperar o número de PID associado a uma seção de tabela, chame [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) no exemplo de mídia. O PID é fornecido nos baixos 13 bits do sinalizador **dwTypeSpecificFlags** na estrutura de **Propriedades am \_ SAMPLE2 \_** . Isso será útil se você mapear vários PIDs do PSI para o mesmo pino de saída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




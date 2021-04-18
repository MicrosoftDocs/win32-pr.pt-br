---
description: Trabalhando com Crossbars
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Trabalhando com Crossbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792541"
---
# <a name="working-with-crossbars"></a>Trabalhando com Crossbars

Se um cartão de captura de vídeo tiver mais de uma entrada física ou der suporte a mais de um caminho de hardware para os dados, o grafo de filtro poderá conter o [filtro Crossbar de vídeo analógico](analog-video-crossbar-filter.md). O construtor do grafo de captura adiciona automaticamente esse filtro quando necessário; Ele será upstream do filtro de captura. Dependendo do hardware, o grafo de filtro pode conter mais de uma instância do filtro Crossbar.

O filtro Crossbar expõe a interface [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , que você pode usar para rotear uma entrada específica para uma saída específica. Por exemplo, uma placa de vídeo pode ter um conector coaxial e uma entrada de S-Video. Eles seriam representados como Pins de entrada no filtro Crossbar. Para selecionar uma entrada, encaminhe o pino de entrada correspondente para o pino de saída do crossbar, usando o método [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

Para localizar filtros Crossbar no grafo, você pode usar o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para procurar filtros que dão suporte a **IAMCrossbar**. Por exemplo, o código a seguir procura dois Crossbars:


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



Para obter uma abordagem mais generalizada, consulte a classe CCrossbar no [exemplo AMCAP](amcap-sample.md).

Depois de ter um ponteiro para a interface **IAMCrossbar** , você pode obter informações sobre o filtro crossbar, incluindo o tipo físico de cada PIN e a matriz da qual os Pins de entrada podem ser roteados para os Pins de saída.

-   Para determinar o tipo de conector físico ao qual um PIN corresponde, chame o método [**IAMCrossbar:: get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) . O método retorna um membro da enumeração [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) . Por exemplo, um PIN de S-Video retorna o valor PhysConn \_ vídeo \_ SVIDEO.

    O método **Get \_ CrossbarInfo** também indica se dois Pins estão relacionados entre si. Por exemplo, um pino de sintonizador de vídeo pode estar relacionado a um pino de sintonizador de áudio. Os Pins relacionados têm a mesma direção do PIN e, normalmente, fazem parte da mesma tomada ou conector físico no cartão.

-   Para determinar se você pode rotear um PIN de entrada para um PIN de saída específico, chame o método [**IAMCrossbar:: canroute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .
-   Para determinar o roteamento atual entre os Pins, chame o método [**IAMCrossbar:: get \_ isrouteto**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .

Todos os métodos anteriores especificam Pins por número de índice, com Pins de saída e Pins de entrada, ambos indexados de zero. Chame o método **IAMCrossbar:: get \_ PinCounts** para localizar o número de Pins no filtro.

Por exemplo, o código a seguir exibe informações sobre um filtro Crossbar na janela do console:


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



Para um cartão hipotético, essa função pode produzir a seguinte saída:


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



No lado da saída, o S-Video e o sintonizador de vídeo estão relacionados ao decodificador de áudio. No lado da entrada, o sintonizador de vídeo está relacionado ao sintonizador de áudio e o S-Video está relacionado à linha de áudio no. A entrada S-Video é roteada para a saída S-Video; e a entrada do sintonizador de vídeo é roteada para a saída do sintonizador de vídeo. No momento, nada é roteado para o decodificador de áudio, mas a linha de áudio no ou o sintonizador de áudio pode ser roteado para ele.

Você pode alterar o roteamento existente chamando o método [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

 

 




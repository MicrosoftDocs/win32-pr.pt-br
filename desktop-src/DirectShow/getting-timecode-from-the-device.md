---
description: Obtendo o código de code do dispositivo
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Obtendo o código de code do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105747361"
---
# <a name="getting-timecode-from-the-device"></a>Obtendo o código de code do dispositivo

Enquanto uma fita de vídeo digital está sendo reproduzida ou está no modo de pausa de registro, você pode recuperar o código de tempo SMPTE ou o número de faixa absoluto. Para fazer isso, chame o método [**IAMTimecodeReader:: GetCode-código**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) . Esse método usa um ponteiro para uma estrutura de [**\_ exemplo de código**](/windows/win32/api/strmif/ns-strmif-timecode_sample) de ponto, que descreve o código de ponto. Antes de chamar o método, inicialize o membro **dwFlags** da estrutura. Use o valor ED \_ DEVCAP de código de tempo \_ \_ lido para recuperar o código de tempo ou o valor Ed \_ DEVCAP \_ ATN \_ Read para recuperar o número de faixa absoluto.

O membro de **código** de Code da estrutura de **\_ exemplo do código** de code é uma estrutura de código de um Quando o método retorna, o membro **dwFrames** da estrutura de código de tempo contém o código de tempo ou o número de faixa. Para o código de tempo, as horas, os minutos, os segundos e os quadros são incluídos em um DWORD como valores de BCD (decimal codificado binário), com o formato *hhmmssff*. Use bitmasks para extrair os valores individuais.

O exemplo a seguir recupera o código de tempo e o número de faixa.


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 

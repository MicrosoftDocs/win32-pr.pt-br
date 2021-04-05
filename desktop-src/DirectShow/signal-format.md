---
description: Formato de sinal
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato de sinal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825828"
---
# <a name="signal-format"></a>Formato de sinal

O formato de sinal de camcorder DV pode ser NTSC ou PAL, Standard ou de execução longa.

**Driver MSDV**

Para obter o formato de sinal de entrada do driver MSDV, chame o método [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) e passe o sinalizador de sinal de entrada do Ed \_ transbasic \_ \_ . O método retorna uma constante definida, indicando o formato.

O código a seguir verifica o formato de sinal e usa esse valor para calcular o tempo médio por quadro. O modo de variável recebe a constante de formato de sinal.


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



Para obter o formato de sinal de saída, chame o mesmo método com o \_ sinalizador de sinal de saída Ed transbasic \_ \_ .

**Driver UVC**

Para obter o formato de sinal de entrada ou saída do driver UVC, chame [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) no PIN e examine o bloco de formato de vídeo. (Para dispositivos UVC, o código mostrado no exemplo anterior geralmente retorna ED \_ \_Sinal transbasic \_ desconhecido, portanto, não é confiável.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




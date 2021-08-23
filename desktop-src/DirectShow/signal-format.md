---
description: Formato de sinal
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato de sinal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66add7467f2f497985094c603aaea83b55967f6b2c07eba4cacde080503ef2e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583176"
---
# <a name="signal-format"></a>Formato de sinal

O formato de sinal de uma gravação dv pode ser NTSC ou PAL, padrão ou reprodução longa.

**MSDV Driver**

Para obter o formato de sinal de entrada do driver MSDV, chame o método [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) e passe o sinalizador ED \_ TRANSBASIC \_ INPUT \_ SIGNAL. O método retorna uma constante definida, indicando o formato.

O código a seguir verifica o formato de sinal e usa esse valor para calcular o tempo médio por quadro. A variável Modo recebe a constante de formato de sinal.


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



Para obter o formato de sinal de saída, chame o mesmo método com o sinalizador ED \_ TRANSBASIC \_ OUTPUT \_ SIGNAL.

**UVC Driver**

Para obter o formato de sinal de entrada ou saída do driver UVC, chame [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) no pino e examine o bloco de formato de vídeo. (Para dispositivos UVC, o código mostrado no exemplo anterior geralmente retorna ED \_ TRANSBASIC \_ SIGNAL \_ UNKNOWN, portanto, ele não é confiável.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma dvcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




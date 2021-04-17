---
description: Interfaces de renderização e captura de áudio
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfaces de renderização e captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812856"
---
# <a name="audio-capture-and-rendering-interfaces"></a>Interfaces de renderização e captura de áudio

Essas interfaces dão suporte à captura e renderização de áudio no DirectShow



| Interface                                              | Descrição                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | Acesse as entradas analógicas na placa de som do sistema e ajuste as características, como mono ou estéreo, nível de mixagem, nível panorâmico, intensidade, agudo e baixo. |
| [**IAMAudioRendererStats**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | Obtenha informações estatísticas de desempenho sobre o processamento de áudio.                                                                                          |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | Controle como o filtro de captura de áudio aloca buffers.                                                                                                   |
| [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | Controle a tolerância de um processador de áudio quando ele corresponde a taxas com outro relógio.                                                                      |
| [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | Permite que um aplicativo especifique qual janela tem o foco para controlar a reprodução de áudio DirectSound.                                                      |
| [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | Mantenha um recurso de dispositivo de áudio antes que ele seja necessário.                                                                                                        |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | Consulte e defina o formato de saída do filtro de captura.                                                                                                         |
| [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | Defina o volume e o saldo de saída de áudio.                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 




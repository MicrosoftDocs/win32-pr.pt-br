---
description: A classe de dispositivo wave/in consiste em dispositivos de áudio para entrada de áudio de onda de baixo nível.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24cc80d41f402abf1886e063563f272abf7992768dd62f03e64b327a7e199360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002524"
---
# <a name="wavein"></a>wave/in

A classe de dispositivo wave/in consiste em dispositivos de áudio para entrada de áudio de onda de baixo nível. Você acessa esses dispositivos usando as funções wave, que são descritas no SDK (Kit de Desenvolvimento de Software de Plataforma). Os dispositivos nessa classe são associados a dispositivos de linha que suportam o tipo de mídia LINEMEDIAMODE AUTOMATEDVOICE, que é especificado no membro \_ **dwMediaModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o dispositivo de linha.

As [**funções lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) definindo o membro **dwStringFormat** como o valor BINARY STRINGFORMAT e adicionando este \_ membro adicional:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

O **membro DeviceId** é o identificador de um dispositivo de áudio fechado. Use esse identificador em uma chamada para a [**função waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir o dispositivo para entrada. Você pode usar o alça do dispositivo resultante para registrar dados de áudio digitalizados da linha ou do dispositivo de telefone.

Embora uma classe de dispositivo "wave" também exista para dispositivos de áudio de onda de baixo nível, você sempre deve usar a classe de dispositivo wave/in para entrada de onda de baixo nível.

Para obter mais informações sobre as funções de onda, consulte [**Funções multimídia**](../multimedia/multimedia-functions.md).

 

 

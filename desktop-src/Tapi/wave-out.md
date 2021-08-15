---
description: A classe de dispositivo wave/out consiste em dispositivos de áudio para saída de áudio de onda de baixo nível.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: wave/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3e8a82b8345e8f50e1ad18f527c82f4ece241e03c0ea7cd083dd2d2ae79282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760171"
---
# <a name="waveout"></a>wave/out

A classe de dispositivo wave/out consiste em dispositivos de áudio para saída de áudio de onda de baixo nível. Você acessa esses dispositivos usando as funções wave, que são descritas no SDK (Kit de Desenvolvimento de Software de Plataforma). Os dispositivos nessa classe são associados a dispositivos de linha que suportam o tipo de mídia LINEMEDIAMODE AUTOMATEDVOICE, que é especificado no membro \_ **dwMediaModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o dispositivo de linha.

As [**funções lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) definindo o membro **dwStringFormat** como o valor BINARY STRINGFORMAT e adicionando este \_ membro adicional:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

O **membro DeviceId** é o identificador de um dispositivo de áudio fechado. Use esse identificador em uma chamada para a [**função waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir o dispositivo para saída. Você pode usar o alça do dispositivo resultante para reproduzir dados de áudio digitalizados na linha ou no dispositivo de telefone.

Embora uma classe de dispositivo "wave" também exista para dispositivos de áudio de onda de baixo nível, você sempre deve usar a classe de dispositivo wave/out para saída de onda de baixo nível.

Para obter mais informações sobre as funções de onda, consulte [**Funções multimídia**](../multimedia/multimedia-functions.md).

 

 

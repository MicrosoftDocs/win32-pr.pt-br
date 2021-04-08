---
description: A classe de dispositivo de Wave/saída consiste em dispositivos de áudio para saída de áudio de ondas de baixo nível.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: Wave/saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975a3308b6f0b29e130ad07534494e1cb1d991a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837473"
---
# <a name="waveout"></a>Wave/saída

A classe de dispositivo de Wave/saída consiste em dispositivos de áudio para saída de áudio de ondas de baixo nível. Você acessa esses dispositivos usando as funções de onda, que são descritas no SDK (Software Development Kit) da plataforma. Os dispositivos nessa classe estão associados a dispositivos de linha que dão suporte ao \_ tipo de mídia LINEMEDIAMODE AUTOMATEDVOICE, que é especificado no membro **dwMediaModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o dispositivo de linha.

As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando esse membro adicional:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

O membro **DeviceID** é o identificador de um dispositivo de áudio fechado. Você usa esse identificador em uma chamada para a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir o dispositivo para saída. Você pode usar o identificador de dispositivo resultante para reproduzir dados de áudio digitalizados no dispositivo de linha ou telefone.

Embora uma classe de dispositivo "Wave" também exista para dispositivos de áudio de ondas de baixo nível, você sempre deve usar a classe de dispositivo de Wave/saída para saída de ondas de baixo nível.

Para obter mais informações sobre as funções de onda, consulte [**funções de multimídia**](../multimedia/multimedia-functions.md).

 

 

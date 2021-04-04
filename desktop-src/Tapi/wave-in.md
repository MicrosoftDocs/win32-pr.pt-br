---
description: A classe de dispositivo Wave/in consiste em dispositivos de áudio para entrada de áudio de ondas de baixo nível.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: onda/entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171238"
---
# <a name="wavein"></a>onda/entrada

A classe de dispositivo Wave/in consiste em dispositivos de áudio para entrada de áudio de ondas de baixo nível. Você acessa esses dispositivos usando as funções de onda, que são descritas no SDK (Software Development Kit) da plataforma. Os dispositivos nessa classe estão associados a dispositivos de linha que dão suporte ao \_ tipo de mídia LINEMEDIAMODE AUTOMATEDVOICE, que é especificado no membro **dwMediaModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o dispositivo de linha.

As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando esse membro adicional:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

O membro **DeviceID** é o identificador de um dispositivo de áudio fechado. Você usa esse identificador em uma chamada para a função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir o dispositivo para entrada. Você pode usar o identificador de dispositivo resultante para registrar dados de áudio digitalizados do dispositivo de linha ou telefone.

Embora uma classe de dispositivo "Wave" também exista para dispositivos de áudio wave de baixo nível, você sempre deve usar a classe Wave/in Device para a entrada de ondas de baixo nível.

Para obter mais informações sobre as funções de onda, consulte [**funções de multimídia**](../multimedia/multimedia-functions.md).

 

 

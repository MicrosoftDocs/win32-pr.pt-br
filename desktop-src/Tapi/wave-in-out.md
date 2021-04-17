---
description: A classe de dispositivo Wave/in/out consiste em dispositivos de áudio full duplex.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: Wave/entrada/saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756981"
---
# <a name="waveinout"></a>Wave/entrada/saída

A classe de dispositivo Wave/in/out consiste em dispositivos de áudio full duplex. Você acessa esses dispositivos usando as funções de onda, que são descritas no SDK (Software Development Kit) da plataforma. Os dispositivos nessa classe estão associados a dispositivos de linha que dão suporte ao \_ tipo de mídia LINEMEDIAMODE AUTOMATEDVOICE, que é especificado no membro **dwMediaModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o dispositivo de linha.

As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando dois membros adicionais:

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

Os membros **DeviceInId** e **DeviceOutId** são identificadores de um dispositivo de áudio fechado. Você usa esses identificadores em uma chamada para a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir o dispositivo para saída. Você pode usar o identificador de dispositivo resultante para reproduzir dados de áudio digitalizados no dispositivo de linha ou telefone.

Para obter mais informações sobre as funções de onda, consulte [**funções de multimídia**](../multimedia/multimedia-functions.md).

 

 

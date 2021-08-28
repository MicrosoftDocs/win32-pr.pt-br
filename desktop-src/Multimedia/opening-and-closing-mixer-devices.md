---
title: abrindo e fechando dispositivos Mixer
description: abrindo e fechando dispositivos Mixer
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- áudio de multimídia, abrindo dispositivos de mixer
- áudio, abrindo dispositivos do mixer
- mixers de áudio, abrindo
- mixers, abrindo
- áudio multimídia, dispositivos do mixer de fechamento
- áudio, fechando dispositivos do mixer
- mixers de áudio, fechando
- mixers, fechando
- abrindo dispositivos do mixer
- fechando dispositivos do mixer
- identificadores de dispositivo vs. identificadores de dispositivo
- mixers de áudio, identificadores de dispositivo versus identificadores de dispositivo
- mixers, identificadores de dispositivo versus identificadores de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc3b1cb524dc8a48eb8a7c2cc805f958429ba65413961d8e677bb62ba3102b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893046"
---
# <a name="opening-and-closing-mixer-devices"></a>abrindo e fechando dispositivos Mixer

Quando você quiser usar um dispositivo de mixer, você pode simplesmente começar a usá-lo ou pode abrir o dispositivo explicitamente antes de usá-lo. A abertura explícita de um dispositivo de mixer oferece dois benefícios principais:

-   Ele garante a existência contínua desse dispositivo de mixer.
-   Ele permite que você receba notificação de alterações de linha de áudio e controle.

Você pode usar a função [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) para abrir explicitamente um dispositivo de mixer. Essa função usa como parâmetros um identificador de dispositivo, um ponteiro para um local de memória e outros valores exclusivos para cada tipo de dispositivo. O local da memória é preenchido com um identificador de dispositivo. Use este identificador de dispositivo para identificar o dispositivo do mixer aberto ao chamar outras funções do mixer de áudio. Desde que exista um identificador de um dispositivo de mixer, o dispositivo continua existindo no sistema. Se uma alteração de configuração ocorrer no dispositivo do mixer e ele não tiver sido aberto explicitamente, seu aplicativo poderá não conseguir acessá-lo repentinamente.

> [!Note]  
> A diferença entre identificadores de dispositivo e identificadores de dispositivo é importante. Os identificadores de dispositivo são retornados quando você abre um driver de dispositivo usando **mixerOpen**. Os identificadores de dispositivo são determinados implicitamente do número de dispositivos presentes em um sistema; Esse número é obtido usando a função [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) .

 

Você pode usar a função [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) para fechar um dispositivo de mixer. Você deve fechar o dispositivo depois de terminar de usá-lo.

 

 
---
title: Recuperando a posição de reprodução atual
description: Recuperando a posição de reprodução atual
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- áudio de onda, posição de reprodução atual
- Wave-interface de áudio, posição de reprodução atual
- executando a onda-arquivos de áudio, posição de reprodução atual
- função waveOutGetPosition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293906"
---
# <a name="retrieving-the-current-playback-position"></a>Recuperando a posição de reprodução atual

Você pode monitorar a posição de reprodução atual dentro do arquivo enquanto o áudio de formato de onda é reproduzido usando a função [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) .

Para dispositivos de forma de onda-áudio, exemplos são o formato de hora preferencial no qual representar a posição atual. Assim, a posição atual de um dispositivo de wave-áudio é especificada como o número de amostras de um canal desde o início do arquivo de áudio de forma de onda. Para consultar a posição atual de um dispositivo de wave-áudio, defina o membro **wType** da estrutura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) para amostras de tempo \_ e passe essa estrutura para **waveOutGetPosition**.

A estrutura **MMTIME** pode representar o tempo em um ou mais formatos diferentes, incluindo milissegundos, exemplos, SMPTE (sociedade de imagem de movimento e engenheiros de televisão) e formatos de ponteiro de música MIDI. O membro **wType** especifica o formato usado para representar o tempo. Antes de chamar uma função que usa a estrutura **MMTIME** , você deve definir **wType** para indicar o formato de hora solicitado. Certifique-se de verificar **wType** após a chamada para ver se há suporte para o formato de hora solicitado. Se não houver suporte para o formato de hora solicitado, o driver de dispositivo especificará a hora em um formato de hora alternativo e alterará o membro **wType** para o formato de hora selecionado.

Para obter mais informações sobre a estrutura **MMTIME** , consulte [timers de multimídia](multimedia-timers.md).

 

 
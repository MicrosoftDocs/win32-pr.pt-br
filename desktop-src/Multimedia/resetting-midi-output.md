---
title: Redefinindo a saída de MIDI
description: Redefinindo a saída de MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- MIDI (interface digital de instrumento musical), redefinindo dispositivos de saída
- MIDI (interface digital de instrumentos musicais), redefinindo dispositivos de saída
- executando arquivos MIDI, redefinindo dispositivos de saída
- Redefinindo dispositivos de saída
- MIDI (interface digital de instrumento musical), dispositivos de saída
- MIDI (interface digital de instrumentos musicais), dispositivos de saída
- executando arquivos MIDI, dispositivos de saída
- Dispositivos de saída MIDI
- EOX (fim de exclusivo)
- fim de exclusivo (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c0073d9fc016e21e401e4cb2e7c28b4fd1aa5e3180801975df4e334243b953
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689256"
---
# <a name="resetting-midi-output"></a>Redefinindo a saída de MIDI

A função [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) desativa todas as notas em todos os canais MIDI para um dispositivo MIDI especificado. Em seguida, a função marca quaisquer buffers exclusivos do sistema pendentes como concluído e os retorna para o aplicativo. Essa função pode ser útil em um aplicativo que usa a saída de MIDI para fornecer ao usuário a capacidade de redefinir a saída de MIDI.

> [!Note]  
> Encerrar uma mensagem exclusiva do sistema sem enviar um byte EOX (fim de exclusivo) pode causar problemas para o dispositivo receptor. A função **midiOutReset** não envia um byte EOX quando ele termina uma mensagem exclusiva do sistema, porque os aplicativos são responsáveis por fazer isso.

 

 

 
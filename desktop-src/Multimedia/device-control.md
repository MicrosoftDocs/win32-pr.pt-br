---
title: Controle de dispositivo (Windows Multimídia)
description: Controle de dispositivo
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6878e5e759f3eddb5e98d241d9a8d081005e3545dc2f0054b46630619eaa06fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497236"
---
# <a name="device-control-windows-multimedia"></a>Controle de dispositivo (Windows Multimídia)

Para controlar um dispositivo MCI, abra o dispositivo, envie os comandos necessários para ele e feche o dispositivo. Os comandos podem ser muito semelhantes, mesmo para dispositivos MCI completamente diferentes. Por exemplo, a seguinte série de comandos MCI reproduz a sexta faixa de um CD de áudio usando a [**função mciSendString:**](/previous-versions//dd757161(v=vs.85))


```C++
mciSendString("open cdaudio", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("set cdaudio time format tmsf", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play cdaudio from 6 to 7", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close cdaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



O exemplo a seguir mostra uma série semelhante de comandos MCI que reproduz as primeiras 10.000 amostras de um arquivo waveform-audio:


```C++
mciSendString(
    "open c:\mmdata\purplefi.wav type waveaudio alias finch", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
mciSendString("set finch time format samples", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play finch from 1 to 10000", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close finch", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Estes exemplos ilustram alguns fatos interessantes sobre comandos MCI:

-   Os mesmos comandos básicos ([**abrir**](open.md), [**definir**](set.md) [**,**](play.md)reproduzir e [**fechar**](close.md)) são usados com dispositivos de áudio de CD e waveform-audio. Os mesmos comandos MCI são usados com todos os dispositivos MCI.
-   O comando open para o dispositivo waveform-audio inclui uma especificação de nome de arquivo. O dispositivo waveform-audio é um dispositivo composto *(um* associado *a* um arquivo de dados), enquanto o dispositivo de áudio cd é um dispositivo simples (um sem um arquivo de dados associado).
-   O comando set especifica formatos de tempo em cada caso, mas o sinalizador de formato de tempo para o dispositivo de áudio CD especifica o formato TMSF (faixas/minutos/segundos/quadros), enquanto o formato de tempo usado com o dispositivo waveform-audio especifica "amostras".
-   As variáveis usadas com os sinalizadores "from" e "to" são apropriadas para o respectivo formato de hora. Por exemplo, para o dispositivo de áudio CD, as variáveis especificam um intervalo de faixas, mas para o dispositivo waveform-audio, as variáveis especificam um intervalo de amostras.

 

 

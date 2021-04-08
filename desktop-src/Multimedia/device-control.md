---
title: Controle de dispositivo (multimídia do Windows)
description: Controle de dispositivo
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008745"
---
# <a name="device-control-windows-multimedia"></a>Controle de dispositivo (multimídia do Windows)

Para controlar um dispositivo MCI, abra o dispositivo, envie os comandos necessários para ele e, em seguida, feche o dispositivo. Os comandos podem ser muito semelhantes, mesmo para dispositivos MCI completamente diferentes. Por exemplo, a série de comandos MCI a seguir desempenha o sexto controle de um CD de áudio usando a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


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



O exemplo a seguir mostra uma série semelhante de comandos MCI que reproduzem os primeiros 10.000 exemplos de um arquivo de wave-áudio:


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

-   Os mesmos comandos básicos ([**abrir**](open.md), [**definir**](set.md), [**reproduzir**](play.md)e [**fechar**](close.md)) são usados com áudio de CD e dispositivos de onda de áudio. Os mesmos comandos MCI são usados com todos os dispositivos MCI.
-   O comando abrir para o dispositivo wave-Audio inclui uma especificação de nome de arquivo. O dispositivo de wave-áudio é um *dispositivo composto* (um associado a um arquivo de dados), enquanto o dispositivo de áudio de CD é um *dispositivo simples* (um sem um arquivo de dados associado).
-   O comando Set especifica formatos de hora em cada caso, mas o sinalizador de formato de tempo para o dispositivo de áudio de CD especifica o formato Tracks/minutes/segundos/frames (TMSF), enquanto o formato de hora usado com o dispositivo wave-Audio especifica "exemplos".
-   As variáveis usadas com os sinalizadores "from" e "to" são apropriadas para o respectivo formato de hora. Por exemplo, para o dispositivo de áudio CD, as variáveis especificam um intervalo de faixas, mas para o dispositivo wave-Audio, as variáveis especificam um intervalo de amostras.

 

 

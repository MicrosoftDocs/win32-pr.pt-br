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
# <a name="device-control-windows-multimedia"></a><span data-ttu-id="8661d-103">Controle de dispositivo (multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="8661d-103">Device Control (Windows Multimedia)</span></span>

<span data-ttu-id="8661d-104">Para controlar um dispositivo MCI, abra o dispositivo, envie os comandos necessários para ele e, em seguida, feche o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8661d-104">To control an MCI device, you open the device, send the necessary commands to it, and then close the device.</span></span> <span data-ttu-id="8661d-105">Os comandos podem ser muito semelhantes, mesmo para dispositivos MCI completamente diferentes.</span><span class="sxs-lookup"><span data-stu-id="8661d-105">The commands can be very similar, even for completely different MCI devices.</span></span> <span data-ttu-id="8661d-106">Por exemplo, a série de comandos MCI a seguir desempenha o sexto controle de um CD de áudio usando a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="8661d-106">For example, the following series of MCI commands plays the sixth track of an audio CD by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


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



<span data-ttu-id="8661d-107">O exemplo a seguir mostra uma série semelhante de comandos MCI que reproduzem os primeiros 10.000 exemplos de um arquivo de wave-áudio:</span><span class="sxs-lookup"><span data-stu-id="8661d-107">The next example shows a similar series of MCI commands that plays the first 10,000 samples of a waveform-audio file:</span></span>


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



<span data-ttu-id="8661d-108">Estes exemplos ilustram alguns fatos interessantes sobre comandos MCI:</span><span class="sxs-lookup"><span data-stu-id="8661d-108">These examples illustrate some interesting facts about MCI commands:</span></span>

-   <span data-ttu-id="8661d-109">Os mesmos comandos básicos ([**abrir**](open.md), [**definir**](set.md), [**reproduzir**](play.md)e [**fechar**](close.md)) são usados com áudio de CD e dispositivos de onda de áudio.</span><span class="sxs-lookup"><span data-stu-id="8661d-109">The same basic commands ([**open**](open.md), [**set**](set.md), [**play**](play.md), and [**close**](close.md)) are used with CD audio and waveform-audio devices.</span></span> <span data-ttu-id="8661d-110">Os mesmos comandos MCI são usados com todos os dispositivos MCI.</span><span class="sxs-lookup"><span data-stu-id="8661d-110">The same MCI commands are used with all MCI devices.</span></span>
-   <span data-ttu-id="8661d-111">O comando abrir para o dispositivo wave-Audio inclui uma especificação de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8661d-111">The open command for the waveform-audio device includes a filename specification.</span></span> <span data-ttu-id="8661d-112">O dispositivo de wave-áudio é um *dispositivo composto* (um associado a um arquivo de dados), enquanto o dispositivo de áudio de CD é um *dispositivo simples* (um sem um arquivo de dados associado).</span><span class="sxs-lookup"><span data-stu-id="8661d-112">The waveform-audio device is a *compound device* (one associated with a data file), while the CD audio device is a *simple device* (one without an associated data file).</span></span>
-   <span data-ttu-id="8661d-113">O comando Set especifica formatos de hora em cada caso, mas o sinalizador de formato de tempo para o dispositivo de áudio de CD especifica o formato Tracks/minutes/segundos/frames (TMSF), enquanto o formato de hora usado com o dispositivo wave-Audio especifica "exemplos".</span><span class="sxs-lookup"><span data-stu-id="8661d-113">The set command specifies time formats in each case, but the time-format flag for the CD audio device specifies tracks/minutes/seconds/frames (TMSF) format, while the time format used with the waveform-audio device specifies "samples".</span></span>
-   <span data-ttu-id="8661d-114">As variáveis usadas com os sinalizadores "from" e "to" são apropriadas para o respectivo formato de hora.</span><span class="sxs-lookup"><span data-stu-id="8661d-114">The variables used with the "from" and "to" flags are appropriate to the respective time format.</span></span> <span data-ttu-id="8661d-115">Por exemplo, para o dispositivo de áudio CD, as variáveis especificam um intervalo de faixas, mas para o dispositivo wave-Audio, as variáveis especificam um intervalo de amostras.</span><span class="sxs-lookup"><span data-stu-id="8661d-115">For example, for the CD audio device, the variables specify a range of tracks, but for the waveform-audio device, the variables specify a range of samples.</span></span>

 

 

---
title: Comportamento padrão de drivers
description: Comportamento padrão de drivers
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640915"
---
# <a name="default-behavior-of-drivers"></a><span data-ttu-id="86100-103">Comportamento padrão de drivers</span><span class="sxs-lookup"><span data-stu-id="86100-103">Default Behavior of Drivers</span></span>

<span data-ttu-id="86100-104">Em muitas situações, as especificações do comando MCI definem os valores padrão e o comportamento dos drivers de um determinado tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86100-104">In many situations, the MCI command specifications define the default values and behavior for drivers of a particular device type.</span></span> <span data-ttu-id="86100-105">Como os dispositivos de multimídia podem ter uma ampla gama de recursos (e limitações), pode haver áreas indefinidas de comportamento.</span><span class="sxs-lookup"><span data-stu-id="86100-105">Since multimedia devices can have a wide range of features (and limitations), there can be undefined areas of behavior.</span></span> <span data-ttu-id="86100-106">Além disso, os drivers podem tratar exceções de forma diferente, com base nos recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86100-106">Also, drivers might handle exceptions differently, based on the capabilities of the device.</span></span>

<span data-ttu-id="86100-107">Por exemplo, considere os comandos a seguir enviados para um driver de áudio de onda usando a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="86100-107">For example, consider the following commands sent to a waveform-audio driver using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="86100-108">O comando [**Record**](record.md) retorna um valor de "parâmetro fora do intervalo" e interrompe a reprodução iniciada pelo comando [**Play**](play.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="86100-108">The [**record**](record.md) command returns a "Parameter out of range" value and stops the playback started by the previous [**play**](play.md) command.</span></span> <span data-ttu-id="86100-109">Uma delas pode esperar que o driver valide o comando de registro antes de parar a reprodução, mas o driver interrompe a reprodução primeiro.</span><span class="sxs-lookup"><span data-stu-id="86100-109">One might expect the driver to validate the record command before stopping playback, but the driver stops the playback first.</span></span>

 

 
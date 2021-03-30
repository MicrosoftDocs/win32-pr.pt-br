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
# <a name="default-behavior-of-drivers"></a>Comportamento padrão de drivers

Em muitas situações, as especificações do comando MCI definem os valores padrão e o comportamento dos drivers de um determinado tipo de dispositivo. Como os dispositivos de multimídia podem ter uma ampla gama de recursos (e limitações), pode haver áreas indefinidas de comportamento. Além disso, os drivers podem tratar exceções de forma diferente, com base nos recursos do dispositivo.

Por exemplo, considere os comandos a seguir enviados para um driver de áudio de onda usando a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



O comando [**Record**](record.md) retorna um valor de "parâmetro fora do intervalo" e interrompe a reprodução iniciada pelo comando [**Play**](play.md) anterior. Uma delas pode esperar que o driver valide o comando de registro antes de parar a reprodução, mas o driver interrompe a reprodução primeiro.

 

 
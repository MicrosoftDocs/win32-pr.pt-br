---
title: Usando o PlaySound para repetir sons
description: Usando o PlaySound para repetir sons
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- áudio de onda, função PlaySound
- áudio de onda, sons de loop
- áudio de onda, parâmetro fdwSound
- Função PlaySound, som de loop
- Função PlaySound, parâmetro fdwSound
- executar loop de Wave-sons de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf97321a72ab566bf622e725700dbf336ddba6d92b9b8e6df9150357492656f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136114"
---
# <a name="using-playsound-to-loop-sounds"></a>Usando o PlaySound para repetir sons

Se você especificar o \_ loop SND e o SND \_ Async flags para o parâmetro *FdwSound* da função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) , o som continuará a ser reproduzido repetidamente, conforme mostrado no exemplo a seguir:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



Se você quiser executar um loop em um som, deverá reproduzi-lo de forma assíncrona; Você não pode usar o \_ sinalizador de sincronização SND com o \_ sinalizador de loop snd. Um som em loop continuará a ser tocado até que você chame o **PlaySound** para tocar outro som. Para interromper a reprodução de um som (em loop ou assíncrono) sem reproduzir outro som, use a seguinte instrução:


```C++
PlaySound(NULL, NULL, 0); 
```



 

 
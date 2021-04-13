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
ms.openlocfilehash: 5373e703c7a02068094e312dee18690a797b330e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365841"
---
# <a name="using-playsound-to-loop-sounds"></a><span data-ttu-id="6e036-109">Usando o PlaySound para repetir sons</span><span class="sxs-lookup"><span data-stu-id="6e036-109">Using PlaySound to Loop Sounds</span></span>

<span data-ttu-id="6e036-110">Se você especificar o \_ loop SND e o SND \_ Async flags para o parâmetro *FdwSound* da função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) , o som continuará a ser reproduzido repetidamente, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="6e036-110">If you specify the SND\_LOOP and SND\_ASYNC flags for the *fdwSound* parameter of the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function, the sound will continue to play repeatedly as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



<span data-ttu-id="6e036-111">Se você quiser executar um loop em um som, deverá reproduzi-lo de forma assíncrona; Você não pode usar o \_ sinalizador de sincronização SND com o \_ sinalizador de loop snd.</span><span class="sxs-lookup"><span data-stu-id="6e036-111">If you want to loop a sound, you must play it asynchronously; you cannot use the SND\_SYNC flag with the SND\_LOOP flag.</span></span> <span data-ttu-id="6e036-112">Um som em loop continuará a ser tocado até que você chame o **PlaySound** para tocar outro som.</span><span class="sxs-lookup"><span data-stu-id="6e036-112">A looped sound will continue to play until you call **PlaySound** to play another sound.</span></span> <span data-ttu-id="6e036-113">Para interromper a reprodução de um som (em loop ou assíncrono) sem reproduzir outro som, use a seguinte instrução:</span><span class="sxs-lookup"><span data-stu-id="6e036-113">To stop playing a sound (looped or asynchronous) without playing another sound, use the following statement:</span></span>


```C++
PlaySound(NULL, NULL, 0); 
```



 

 
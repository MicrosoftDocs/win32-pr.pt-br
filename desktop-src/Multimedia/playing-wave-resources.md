---
title: Reprodução de recursos WAVE
description: Reprodução de recursos WAVE
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- waveform audio, reprodução de recursos WAVE
- áudio auxiliar, reprodução de recursos WAVE
- reprodução de recursos WAVE
- Função PlaySound, reproduzindo recursos WAVE
- Função sndPlaySound
- Função PlaySound, em comparação com a função sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd256d3c4cf07d6d2f57ba9c4d85c54b9d0e599f9382a5b8d9d1f3a0ef4705ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136755"
---
# <a name="playing-wave-resources"></a>Reprodução de recursos WAVE

Você pode usar a [**função PlaySound**](/previous-versions//dd743680(v=vs.85)) para reproduzir um som armazenado como um recurso. Embora isso também seja possível usando a [**função sndPlaySound,**](/previous-versions//dd798676(v=vs.85)) **sndPlaySound** requer que você encontre, carregue, bloqueie, desbloqueie e libere o recurso; **O PlaySound** alcança tudo isso com uma única linha de código.

## <a name="playsound-example"></a>Exemplo de PlaySound


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>Exemplo de sndPlaySound

O sinalizador SND MEMORY indica que o \_ *parâmetro lpszSoundName* é um ponteiro para uma imagem na memória do arquivo WAVE. Para incluir um arquivo WAVE como um recurso em um aplicativo, adicione a seguinte entrada ao script de recurso do aplicativo (. RC) arquivo.


```C++
soundName WAVE c:\sounds\bells.wav 
```



O nome *soundName* é um espaço reservado para um nome que você fornece para se referir a esse recurso WAVE. Os recursos WAVE são carregados e acessados assim como outros recursos definidos pelo Windows aplicativo. A função PlayResource no exemplo a seguir reproduz um recurso WAVE especificado.


```C++
BOOL PlayResource(LPSTR lpName) 
{ 
    BOOL bRtn; 
    LPSTR lpRes; 
    HANDLE hResInfo, hRes; 
 
    // Find the WAVE resource. 
 
    hResInfo = FindResource(hInst, lpName, "WAVE"); 
    if (hResInfo == NULL) 
        return FALSE; 
 
    // Load the WAVE resource. 
 
    hRes = LoadResource(hInst, hResInfo); 
    if (hRes == NULL) 
        return FALSE; 
 
    // Lock the WAVE resource and play it. 
 
    lpRes = LockResource(hRes); 
    if (lpRes != NULL) { 
        bRtn = sndPlaySound(lpRes, SND_MEMORY | SND_SYNC | 
            SND_NODEFAULT); 
        UnlockResource(hRes); 
    } 
    else 
        bRtn = 0; 
 
    // Free the WAVE resource and return success or failure. 
 
    FreeResource(hRes); 
    return bRtn; 
} 
```



Para reproduzir um recurso WAVE usando essa função, passe para a função um ponteiro para uma cadeia de caracteres que contém o nome do recurso, conforme mostrado no exemplo a seguir.


```C++
PlayResource("soundName"); 
```



 

 
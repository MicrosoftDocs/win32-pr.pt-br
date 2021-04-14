---
title: Reproduzindo recursos de onda
description: Reproduzindo recursos de onda
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- áudio de onda, reproduzindo recursos de onda
- áudio auxiliar, reproduzindo recursos de onda
- reproduzindo recursos de onda
- Função PlaySound, reproduzindo recursos de onda
- função sndPlaySound
- Função PlaySound, em comparação com a função sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9678c18e09b12ee1e8d8215d0841cbdaba0ac9c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454052"
---
# <a name="playing-wave-resources"></a>Reproduzindo recursos de onda

Você pode usar a função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) para reproduzir um som que é armazenado como um recurso. Embora isso também seja possível usando a função [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) , o **sndPlaySound** requer que você encontre, carregue, bloqueie, desbloqueie e libere o recurso; O **PlaySound** realiza tudo isso com uma única linha de código.

## <a name="playsound-example"></a>Exemplo de PlaySound


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>Exemplo de sndPlaySound

O sinalizador de memória de SND \_ indica que o parâmetro *lpszSoundName* é um ponteiro para uma imagem na memória do arquivo Wave. Para incluir um arquivo WAVE como um recurso em um aplicativo, adicione a seguinte entrada ao script de recurso do aplicativo (. RC).


```C++
soundName WAVE c:\sounds\bells.wav 
```



O nome *soundName* é um espaço reservado para um nome que você fornece para se referir a esse recurso de onda. Os recursos de onda são carregados e acessados da mesma forma que outros recursos do Windows definidos pelo aplicativo. A função PlayResource no exemplo a seguir reproduz um recurso de onda especificado.


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



Para reproduzir um recurso de onda usando essa função, passe para a função um ponteiro para uma cadeia de caracteres que contém o nome do recurso, conforme mostrado no exemplo a seguir.


```C++
PlayResource("soundName"); 
```



 

 
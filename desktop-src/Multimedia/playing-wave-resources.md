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
# <a name="playing-wave-resources"></a><span data-ttu-id="1db40-109">Reproduzindo recursos de onda</span><span class="sxs-lookup"><span data-stu-id="1db40-109">Playing WAVE Resources</span></span>

<span data-ttu-id="1db40-110">Você pode usar a função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) para reproduzir um som que é armazenado como um recurso.</span><span class="sxs-lookup"><span data-stu-id="1db40-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play a sound that is stored as a resource.</span></span> <span data-ttu-id="1db40-111">Embora isso também seja possível usando a função [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) , o **sndPlaySound** requer que você encontre, carregue, bloqueie, desbloqueie e libere o recurso; O **PlaySound** realiza tudo isso com uma única linha de código.</span><span class="sxs-lookup"><span data-stu-id="1db40-111">Although this is also possible using the [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function, **sndPlaySound** requires that you find, load, lock, unlock, and free the resource; **PlaySound** achieves all of this with a single line of code.</span></span>

## <a name="playsound-example"></a><span data-ttu-id="1db40-112">Exemplo de PlaySound</span><span class="sxs-lookup"><span data-stu-id="1db40-112">PlaySound Example</span></span>


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a><span data-ttu-id="1db40-113">Exemplo de sndPlaySound</span><span class="sxs-lookup"><span data-stu-id="1db40-113">sndPlaySound Example</span></span>

<span data-ttu-id="1db40-114">O sinalizador de memória de SND \_ indica que o parâmetro *lpszSoundName* é um ponteiro para uma imagem na memória do arquivo Wave.</span><span class="sxs-lookup"><span data-stu-id="1db40-114">The SND\_MEMORY flag indicates that the *lpszSoundName* parameter is a pointer to an in-memory image of the WAVE file.</span></span> <span data-ttu-id="1db40-115">Para incluir um arquivo WAVE como um recurso em um aplicativo, adicione a seguinte entrada ao script de recurso do aplicativo (. RC).</span><span class="sxs-lookup"><span data-stu-id="1db40-115">To include a WAVE file as a resource in an application, add the following entry to the application's resource script (.RC) file.</span></span>


```C++
soundName WAVE c:\sounds\bells.wav 
```



<span data-ttu-id="1db40-116">O nome *soundName* é um espaço reservado para um nome que você fornece para se referir a esse recurso de onda.</span><span class="sxs-lookup"><span data-stu-id="1db40-116">The name *soundName* is a placeholder for a name that you supply to refer to this WAVE resource.</span></span> <span data-ttu-id="1db40-117">Os recursos de onda são carregados e acessados da mesma forma que outros recursos do Windows definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1db40-117">WAVE resources are loaded and accessed just like other application-defined Windows resources.</span></span> <span data-ttu-id="1db40-118">A função PlayResource no exemplo a seguir reproduz um recurso de onda especificado.</span><span class="sxs-lookup"><span data-stu-id="1db40-118">The PlayResource function in the following example plays a specified WAVE resource.</span></span>


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



<span data-ttu-id="1db40-119">Para reproduzir um recurso de onda usando essa função, passe para a função um ponteiro para uma cadeia de caracteres que contém o nome do recurso, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="1db40-119">To play a WAVE resource by using this function, pass to the function a pointer to a string containing the name of the resource, as shown in the following example.</span></span>


```C++
PlayResource("soundName"); 
```



 

 
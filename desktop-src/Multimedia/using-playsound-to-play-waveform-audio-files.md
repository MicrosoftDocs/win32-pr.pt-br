---
title: Usando o PlaySound para reproduzir arquivos de Waveform-Audio
description: Usando o PlaySound para reproduzir arquivos de Waveform-Audio
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- áudio de onda, função PlaySound
- áudio de onda, reproduzindo arquivos
- áudio de onda, extensão de nome de arquivo WAV
- Função PlaySound, tocando em formato de onda-arquivos de áudio
- executando formato de onda-arquivos de áudio, função PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917297"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a><span data-ttu-id="077f3-108">Usando o PlaySound para reproduzir arquivos de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="077f3-108">Using PlaySound to Play Waveform-Audio Files</span></span>

<span data-ttu-id="077f3-109">A maioria dos arquivos de som de onda usa o. Extensão de nome de arquivo WAV.</span><span class="sxs-lookup"><span data-stu-id="077f3-109">Most waveform-audio files use the .WAV filename extension.</span></span>

<span data-ttu-id="077f3-110">A instrução a seguir desempenha os \\ sinos C: Sounds \\ . Arquivo WAV:</span><span class="sxs-lookup"><span data-stu-id="077f3-110">The following statement plays the C:\\SOUNDS\\BELLS.WAV file:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



<span data-ttu-id="077f3-111">Se o arquivo especificado não existir, ou se o arquivo não couber na memória disponível, o [**PlaySound**](/previous-versions//dd743680(v=vs.85)) reproduzirá o som do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="077f3-111">If the specified file does not exist, or if the file does not fit into the available memory, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) plays the default system sound.</span></span> <span data-ttu-id="077f3-112">Se nenhum som do sistema padrão tiver sido definido, o **PlaySound** falhará sem produzir nenhum som.</span><span class="sxs-lookup"><span data-stu-id="077f3-112">If no default system sound has been defined, **PlaySound** fails without producing any sound.</span></span> <span data-ttu-id="077f3-113">Se você não quiser que o som do sistema padrão seja reproduzido, especifique o \_ sinalizador SND nodefault, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="077f3-113">If you do not want the default system sound to play, specify the SND\_NODEFAULT flag, as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 
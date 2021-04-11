---
title: A função PlaySound
description: A função PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- áudio de multimídia, função PlaySound
- áudio, função PlaySound
- áudio de onda, função PlaySound
- Função PlaySound, sobre
- função sndPlaySound
- Função PlaySound, em comparação com a função sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104161920"
---
# <a name="the-playsound-function"></a><span data-ttu-id="5810f-109">A função PlaySound</span><span class="sxs-lookup"><span data-stu-id="5810f-109">The PlaySound Function</span></span>

<span data-ttu-id="5810f-110">Você pode usar a função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) para reproduzir áudio de onda se o som couber na memória disponível.</span><span class="sxs-lookup"><span data-stu-id="5810f-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play waveform audio if the sound fits into available memory.</span></span> <span data-ttu-id="5810f-111">(A função [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) oferece um subconjunto dos recursos do PlaySound.</span><span class="sxs-lookup"><span data-stu-id="5810f-111">(The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function offers a subset of the capabilities of PlaySound.</span></span> <span data-ttu-id="5810f-112">Para maximizar a portabilidade do seu aplicativo baseado em Win32, use o **PlaySound**, não **sndPlaySound**.)</span><span class="sxs-lookup"><span data-stu-id="5810f-112">To maximize the portability of your Win32-based application, use **PlaySound**, not **sndPlaySound**.)</span></span>

<span data-ttu-id="5810f-113">A função **PlaySound** permite que você especifique um som de uma das três maneiras:</span><span class="sxs-lookup"><span data-stu-id="5810f-113">The **PlaySound** function allows you to specify a sound in one of three ways:</span></span>

-   <span data-ttu-id="5810f-114">Como um alerta do sistema, usando o alias armazenado no arquivo de WIN.INI ou no registro</span><span class="sxs-lookup"><span data-stu-id="5810f-114">As a system alert, using the alias stored in the WIN.INI file or the registry</span></span>
-   <span data-ttu-id="5810f-115">Como um nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="5810f-115">As a filename</span></span>
-   <span data-ttu-id="5810f-116">Como um identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="5810f-116">As a resource identifier</span></span>

<span data-ttu-id="5810f-117">A função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) permite reproduzir um som em um loop contínuo, terminando somente quando você chama o **PlaySound** novamente, especificando **NULL** ou o identificador de som de outro som para o parâmetro *pszSound* .</span><span class="sxs-lookup"><span data-stu-id="5810f-117">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function allows you to play a sound in a continuous loop, ending only when you call **PlaySound** again, specifying either **NULL** or the sound identifier of another sound for the *pszSound* parameter.</span></span>

<span data-ttu-id="5810f-118">Você pode usar o **PlaySound** para reproduzir o som de forma síncrona ou assíncrona e controlar o comportamento da função de outras maneiras quando ele deve compartilhar recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="5810f-118">You can use **PlaySound** to play the sound synchronously or asynchronously, and to control the behavior of the function in other ways when it must share system resources.</span></span>

<span data-ttu-id="5810f-119">Para obter mais informações sobre como usar o PlaySound, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="5810f-119">For more information about using PlaySound, see the following topics:</span></span>

-   [<span data-ttu-id="5810f-120">Usando o PlaySound para reproduzir arquivos de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="5810f-120">Using PlaySound to Play Waveform-Audio Files</span></span>](using-playsound-to-play-waveform-audio-files.md)
-   [<span data-ttu-id="5810f-121">Usando o PlaySound para repetir sons</span><span class="sxs-lookup"><span data-stu-id="5810f-121">Using PlaySound to Loop Sounds</span></span>](using-playsound-to-loop-sounds.md)
-   [<span data-ttu-id="5810f-122">Usando o PlaySound para reproduzir sons do sistema</span><span class="sxs-lookup"><span data-stu-id="5810f-122">Using PlaySound to Play System Sounds</span></span>](using-playsound-to-play-system-sounds.md)

<span data-ttu-id="5810f-123">Para obter mais exemplos de como usar o **PlaySound** em seus aplicativos baseados no Win32, consulte [reproduzindo recursos de onda](playing-wave-resources.md).</span><span class="sxs-lookup"><span data-stu-id="5810f-123">For more examples of how to use **PlaySound** in your Win32-based applications, see [Playing WAVE Resources](playing-wave-resources.md).</span></span>

 

 
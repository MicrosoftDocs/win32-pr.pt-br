---
title: Reprodução de áudio simples
description: Reprodução de áudio simples
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- áudio de multimídia, onda
- áudio, onda
- áudio de forma de onda, reprodução simples
- Função MessageBeep
- função sndPlaySound
- Função PlaySound, reprodução simples
- áudio de multimídia, função PlaySound
- áudio, função PlaySound
- áudio de onda, função PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917224"
---
# <a name="simple-audio-playback"></a><span data-ttu-id="db3f1-112">Reprodução de áudio simples</span><span class="sxs-lookup"><span data-stu-id="db3f1-112">Simple Audio Playback</span></span>

<span data-ttu-id="db3f1-113">Você pode usar as seguintes funções para reproduzir áudio de onda em seu aplicativo em uma única chamada de função.</span><span class="sxs-lookup"><span data-stu-id="db3f1-113">You can use the following functions to play waveform audio in your application in a single function call.</span></span>



| <span data-ttu-id="db3f1-114">Função</span><span class="sxs-lookup"><span data-stu-id="db3f1-114">Function</span></span>                                                      | <span data-ttu-id="db3f1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="db3f1-115">Description</span></span>                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db3f1-116">MessageBeep</span><span class="sxs-lookup"><span data-stu-id="db3f1-116">MessageBeep</span></span>](/windows/win32/api/winuser/nf-winuser-messagebeep) | <span data-ttu-id="db3f1-117">Reproduz o som que corresponde a um nível de alerta de sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="db3f1-117">Plays the sound that corresponds to a specified system-alert level.</span></span>                                                 |
| <span data-ttu-id="db3f1-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db3f1-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>                          | <span data-ttu-id="db3f1-119">Reproduz o som que corresponde ao som do sistema inserido no registro ou ao conteúdo do arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="db3f1-119">Plays the sound that corresponds to the system sound entered in the registry or the contents of the specified file.</span></span> |
| <span data-ttu-id="db3f1-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db3f1-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>                                | <span data-ttu-id="db3f1-121">Fornece toda a funcionalidade do [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e pode acessar diretamente os recursos.</span><span class="sxs-lookup"><span data-stu-id="db3f1-121">Provides all the functionality of [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and can directly access resources.</span></span>           |



 

<span data-ttu-id="db3f1-122">A função **MessageBeep** é uma parte padrão da API do Win32; como suas funcionalidades são muito limitadas e estão documentadas em outro lugar, elas não são discutidas aqui.</span><span class="sxs-lookup"><span data-stu-id="db3f1-122">The **MessageBeep** function is a standard part of the Win32 API; because its capabilities are very limited and it is documented elsewhere, it is not discussed here.</span></span>

<span data-ttu-id="db3f1-123">As funções listadas dão suporte às seguintes fontes de áudio de formato de onda:</span><span class="sxs-lookup"><span data-stu-id="db3f1-123">The functions listed support the following sources of waveform audio:</span></span>

-   <span data-ttu-id="db3f1-124">Formato de onda-arquivos de áudio associados ao sistema-níveis de alerta</span><span class="sxs-lookup"><span data-stu-id="db3f1-124">Waveform-audio files associated with system-alert levels</span></span>
-   <span data-ttu-id="db3f1-125">Formato de onda-arquivos de áudio especificados por entradas no registro</span><span class="sxs-lookup"><span data-stu-id="db3f1-125">Waveform-audio files specified by entries in the registry</span></span>
-   <span data-ttu-id="db3f1-126">Recursos de onda na memória</span><span class="sxs-lookup"><span data-stu-id="db3f1-126">In-memory WAVE resources</span></span>
-   <span data-ttu-id="db3f1-127">Formato de onda-arquivos de áudio especificados por nome</span><span class="sxs-lookup"><span data-stu-id="db3f1-127">Waveform-audio files specified by name</span></span>

<span data-ttu-id="db3f1-128">As funções [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e [**PlaySound**](/previous-versions//dd743680(v=vs.85)) carregam um arquivo de wave-áudio inteiro na memória e, em vigor, limitam o tamanho do arquivo que eles podem reproduzir.</span><span class="sxs-lookup"><span data-stu-id="db3f1-128">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and [**PlaySound**](/previous-versions//dd743680(v=vs.85)) functions load an entire waveform-audio file into memory and, in effect, limit the size of the file they can play.</span></span> <span data-ttu-id="db3f1-129">Use **sndPlaySound** e **PlaySound** para reproduzir arquivos de wave-áudio pequenos – até cerca de 100 mil.</span><span class="sxs-lookup"><span data-stu-id="db3f1-129">Use **sndPlaySound** and **PlaySound** to play waveform-audio files that are small — up to about 100K.</span></span> <span data-ttu-id="db3f1-130">Essas duas funções também exigem que os dados de som estejam em um formato que seja reproduzido por um dos drivers de áudio de forma de onda instalados, incluindo o mapeador de ondas.</span><span class="sxs-lookup"><span data-stu-id="db3f1-130">These two functions also require the sound data to be in a format that is playable by one of the installed waveform-audio drivers, including the wave mapper.</span></span>

<span data-ttu-id="db3f1-131">Para arquivos de som maiores, use os serviços de interface de controle de mídia (MCI).</span><span class="sxs-lookup"><span data-stu-id="db3f1-131">For larger sound files, use the Media Control Interface (MCI) services.</span></span> <span data-ttu-id="db3f1-132">Para obter mais informações, consulte [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="db3f1-132">For more information, see [MCI](mci.md).</span></span>

 

 
---
title: Diretrizes de criação para arquivos MIDI
description: Diretrizes de criação para arquivos MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- MIDI (interface digital de instrumento musical), diretrizes de criação de arquivo
- A MIDI (interface digital de instrumentos musicais), diretrizes de criação de arquivo
- Criando arquivos MIDI, diretrizes de criação de arquivo
- atribuições de patch de MIDI padrão
- atribuições de chave MIDI padrão
- MIDI (interface digital de instrumento musical), atribuições de patch padrão
- MIDI (interface digital de instrumentos musicais), atribuições de patch padrão
- MIDI (interface digital de instrumento musical), atribuições de chave padrão
- MIDI (interface digital de instrumentos musicais), atribuições de chave padrão
- Criando arquivos MIDI, atribuições de patch padrão
- Criando arquivos MIDI, atribuições de chave padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006075"
---
# <a name="authoring-guidelines-for-midi-files"></a><span data-ttu-id="38ea5-114">Diretrizes de criação para arquivos MIDI</span><span class="sxs-lookup"><span data-stu-id="38ea5-114">Authoring Guidelines for MIDI Files</span></span>

<span data-ttu-id="38ea5-115">Siga estas diretrizes para criar arquivos MIDI independentes de dispositivo para o Windows:</span><span class="sxs-lookup"><span data-stu-id="38ea5-115">Follow these guidelines to author device-independent MIDI files for Windows:</span></span>

-   <span data-ttu-id="38ea5-116">Use as atribuições de [patch de Midi padrão](standard-midi-patch-assignments.md) e as [atribuições de chave MIDI padrão](standard-midi-key-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="38ea5-116">Use the [Standard MIDI Patch Assignments](standard-midi-patch-assignments.md) and [Standard MIDI Key Assignments](standard-midi-key-assignments.md).</span></span>
-   <span data-ttu-id="38ea5-117">Sempre envie uma mensagem de alteração de programa a um canal para selecionar um patch antes de enviar outras mensagens para esse canal.</span><span class="sxs-lookup"><span data-stu-id="38ea5-117">Always send a program-change message to a channel to select a patch before sending other messages to that channel.</span></span> <span data-ttu-id="38ea5-118">Para os dois canais de percussão (10 e 16), selecione o número do programa 0.</span><span class="sxs-lookup"><span data-stu-id="38ea5-118">For the two percussion channels (10 and 16), select program number 0.</span></span>
-   <span data-ttu-id="38ea5-119">Sempre siga um programa MIDI-alterar mensagem com uma mensagem MIDI principal-controlador de volume (número do controlador 7) para definir o volume relativo do patch.</span><span class="sxs-lookup"><span data-stu-id="38ea5-119">Always follow a MIDI program-change message with a MIDI main-volume controller message (controller number 7) to set the relative volume of the patch.</span></span>
-   <span data-ttu-id="38ea5-120">Use um valor de 80 (0x50) para o controlador de volume principal para os níveis de escuta normais.</span><span class="sxs-lookup"><span data-stu-id="38ea5-120">Use a value of 80 (0x50) for the main-volume controller for normal listening levels.</span></span> <span data-ttu-id="38ea5-121">Para níveis mais silenciosos ou mais altos, você pode usar valores menores ou mais altos.</span><span class="sxs-lookup"><span data-stu-id="38ea5-121">For quieter or louder levels, you can use lower or higher values.</span></span>
-   <span data-ttu-id="38ea5-122">Use apenas as seguintes mensagens de MIDI: observação-em com velocidade, anotação, alteração de programa, curva de densidade, volume principal (controlador 7) e pedal de amortecedor (controlador 64).</span><span class="sxs-lookup"><span data-stu-id="38ea5-122">Use only the following MIDI messages: note-on with velocity, note-off, program change, pitch bend, main volume (controller 7), and damper pedal (controller 64).</span></span> <span data-ttu-id="38ea5-123">Os sintetizadores internos são necessários para responder a essas mensagens e a maioria dos instrumentos musicais MIDI também responde a elas.</span><span class="sxs-lookup"><span data-stu-id="38ea5-123">Internal synthesizers are required to respond to these messages and most MIDI musical instruments respond to them as well.</span></span>

 

 





---
title: MCI (interface de controle de mídia)
description: MCI (interface de controle de mídia)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Multimídia do Windows, MCI (interface de controle de mídia)
- multimídia, MCI (interface de controle de mídia)
- áudio de multimídia, MCI (interface de controle de mídia)
- áudio, interface de controle de mídia (MCI)
- MIDI (interface digital de instrumento musical), MCI (interface de controle de mídia)
- MIDI (interface digital de instrumentos musicais), MCI (interface de controle de mídia)
- MCI (interface de controle de mídia), MIDI (interface digital de instrumento musical)
- MCI (interface de controle de mídia), MIDI (interface digital de instrumento musical)
- MCI (interface de controle de mídia), Sequencer MIDI
- MCI (interface de controle de mídia), Sequencer MIDI
- Sequenciador MIDI MCI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005443"
---
# <a name="media-control-interface-mci"></a><span data-ttu-id="69955-114">MCI (interface de controle de mídia)</span><span class="sxs-lookup"><span data-stu-id="69955-114">Media Control Interface (MCI)</span></span>

<span data-ttu-id="69955-115">O Sequencer MIDI do MCI é o componente do sistema MCI que reproduz arquivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="69955-115">The MCI MIDI sequencer is the MCI system component that plays MIDI files.</span></span> <span data-ttu-id="69955-116">Os aplicativos podem reproduzir arquivos MIDI facilmente usando o MCI, mas o MCI impõe as seguintes restrições em recursos de MIDI:</span><span class="sxs-lookup"><span data-stu-id="69955-116">Applications can play MIDI files easily using MCI, but MCI imposes the following restrictions on MIDI capabilities:</span></span>

-   <span data-ttu-id="69955-117">O MCI dá suporte apenas à saída de MIDI.</span><span class="sxs-lookup"><span data-stu-id="69955-117">MCI supports MIDI output only.</span></span>
-   <span data-ttu-id="69955-118">O MCI não permite a sincronização de fechamento entre eventos de MIDI e outros eventos em tempo real (como vídeo).</span><span class="sxs-lookup"><span data-stu-id="69955-118">MCI does not allow close synchronization between MIDI events and other real-time events (such as video).</span></span>

<span data-ttu-id="69955-119">Se precisar de uma sincronização de MIDI precisa, você deverá usar os buffers de fluxo ou os serviços de MIDI.</span><span class="sxs-lookup"><span data-stu-id="69955-119">If you need accurate MIDI synchronization, you must use the stream buffers or the MIDI services.</span></span> <span data-ttu-id="69955-120">Se precisar de recursos de entrada de MIDI, você deverá usar os serviços de MIDI.</span><span class="sxs-lookup"><span data-stu-id="69955-120">If you need MIDI input capabilities, you must use the MIDI services.</span></span>

<span data-ttu-id="69955-121">O sequenciador MIDI MCI reproduz arquivos MIDI padrão e arquivos MIDI RIFF (formato de arquivo de intercâmbio de recursos), conhecidos como arquivos RMID.</span><span class="sxs-lookup"><span data-stu-id="69955-121">The MCI MIDI sequencer plays standard MIDI files and resource interchange file format (RIFF) MIDI files, known as RMID files.</span></span> <span data-ttu-id="69955-122">Arquivos MIDI padrão estão em conformidade com a especificação [1,0 de arquivos MIDI padrão](creating-midi-files.md) .</span><span class="sxs-lookup"><span data-stu-id="69955-122">Standard MIDI files conform to the [Standard MIDI Files 1.0](creating-midi-files.md) specification.</span></span> <span data-ttu-id="69955-123">Como os arquivos RMID são arquivos MIDI padrão com um cabeçalho RIFF, as informações sobre os arquivos MIDI padrão também se aplicam aos arquivos RMID.</span><span class="sxs-lookup"><span data-stu-id="69955-123">Because RMID files are standard MIDI files with a RIFF header, information about standard MIDI files also applies to RMID files.</span></span> <span data-ttu-id="69955-124">Para obter mais informações sobre arquivos RIFF, consulte [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="69955-124">For more information about RIFF files, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

<span data-ttu-id="69955-125">Embora atualmente existam três tipos de arquivos MIDI padrão, o sequenciador MCI reproduz apenas dois deles: formato 0 e formato 1 arquivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="69955-125">Although there are currently three kinds of standard MIDI files, the MCI sequencer plays only two of them: Format 0 and Format 1 MIDI files.</span></span>

<span data-ttu-id="69955-126">Para obter mais informações sobre como controlar dispositivos multimídia (incluindo sequenciais) usando comandos MCI, consulte [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="69955-126">For more information about controlling multimedia devices (including sequencers) using MCI commands, see [MCI](mci.md).</span></span>

 

 





---
title: Criando arquivos MIDI
description: Criando arquivos MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Multimídia do Windows, criando arquivos MIDI
- multimídia, criando arquivos MIDI
- áudio de multimídia, criando arquivos MIDI
- áudio, criando arquivos MIDI
- MIDI (interface digital de instrumento musical), criando arquivos
- MIDI (interface digital de instrumentos musicais), criando arquivos
- Criando arquivos MIDI, sobre
- Associação de fabricantes de MIDI (MMA)
- MMA (Associação de fabricantes de MIDI)
- Especificação detalhada de MIDI
- Especificação de arquivos MIDI padrão
- Especificação MIDI (GM) geral
- Especificação de GM (MIDI geral)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005238"
---
# <a name="creating-midi-files"></a><span data-ttu-id="30d83-116">Criando arquivos MIDI</span><span class="sxs-lookup"><span data-stu-id="30d83-116">Creating MIDI Files</span></span>

<span data-ttu-id="30d83-117">As especificações de MIDI (interface digital de instrumento musical) são publicadas pelo e são materiais com direitos autorais da MMA (Associação de fabricantes de MIDI).</span><span class="sxs-lookup"><span data-stu-id="30d83-117">The Musical Instrument Digital Interface (MIDI) specifications are published by and are copyrighted material of the MIDI Manufacturers Association (MMA).</span></span> <span data-ttu-id="30d83-118">A lista a seguir descreve as especificações que são do maior interesse geral:</span><span class="sxs-lookup"><span data-stu-id="30d83-118">The following list describes the specifications which are of the greatest general interest:</span></span>

## <a name="midi-detailed-specification"></a><span data-ttu-id="30d83-119">Especificação detalhada de MIDI</span><span class="sxs-lookup"><span data-stu-id="30d83-119">MIDI Detailed Specification</span></span>

<span data-ttu-id="30d83-120">A especificação de MIDI detalhado explica os protocolos de hardware e software MIDI.</span><span class="sxs-lookup"><span data-stu-id="30d83-120">The MIDI Detailed Specification explains the MIDI hardware and software protocols.</span></span> <span data-ttu-id="30d83-121">Isso é útil para o desenvolvimento de aplicativos multimídia que implementam o suporte a MIDI usando funções de MIDI para gravar, editar e/ou reproduzir dados MIDI.</span><span class="sxs-lookup"><span data-stu-id="30d83-121">This is useful to those developing multimedia applications which implement MIDI support by using MIDI functions to record, edit, and/or play MIDI data.</span></span>

## <a name="standard-midi-files-10"></a><span data-ttu-id="30d83-122">Arquivos MIDI padrão 1,0</span><span class="sxs-lookup"><span data-stu-id="30d83-122">Standard MIDI Files 1.0</span></span>

<span data-ttu-id="30d83-123">A especificação de arquivos MIDI padrão define uma maneira de trocar dados de MIDI com carimbo de data/hora entre diferentes aplicativos no mesmo ou em plataformas de hardware diferentes.</span><span class="sxs-lookup"><span data-stu-id="30d83-123">The Standard MIDI Files specification defines a way to interchange time-stamped MIDI data between different applications on the same or different hardware platforms.</span></span> <span data-ttu-id="30d83-124">Isso é útil para desenvolvedores que gravam aplicativos que lêem e analisam arquivos de disco que contêm dados MIDI e/ou gravam arquivos de dados MIDI no disco.</span><span class="sxs-lookup"><span data-stu-id="30d83-124">This is useful to developers writing applications that read and parse disk files containing MIDI data and/or write MIDI data files to disk.</span></span>

## <a name="general-midi-system---level-1"></a><span data-ttu-id="30d83-125">Sistema MIDI geral-nível 1</span><span class="sxs-lookup"><span data-stu-id="30d83-125">General MIDI System - Level 1</span></span>

<span data-ttu-id="30d83-126">A especificação MIDI geral (GM) define uma configuração de MIDI mínima de um "sistema MIDI geral".</span><span class="sxs-lookup"><span data-stu-id="30d83-126">The General MIDI (GM) specification defines a minimum MIDI configuration of a "General MIDI System".</span></span> <span data-ttu-id="30d83-127">Esse sistema consiste em uma classe específica de dispositivos de reprodução de MIDI e é de seu interesse para desenvolvedores de multimídia que criam arquivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="30d83-127">This system consists of a specific class of MIDI playback devices and is of interest to multimedia developers who author MIDI files.</span></span> <span data-ttu-id="30d83-128">A maioria das placas de som do PC e sintetizadores MIDI fabricados atualmente são compatíveis com a especificação GM.</span><span class="sxs-lookup"><span data-stu-id="30d83-128">Most PC sound cards and MIDI synthesizers manufactured today are compatible with the GM specification.</span></span> <span data-ttu-id="30d83-129">Os arquivos MIDI que são criados para a especificação do GM geralmente devem soar como se destinam a soar, não importa em qual dispositivo compatível com GM eles são executados.</span><span class="sxs-lookup"><span data-stu-id="30d83-129">MIDI files which are authored to the GM specification should generally sound as they were intended to sound, no matter which GM-compatible device they are played on.</span></span>

<span data-ttu-id="30d83-130">Para permitir que os arquivos MIDI sejam um formato viável para representar música na computação multimídia, o Windows segue a especificação geral do sistema MIDI 1.</span><span class="sxs-lookup"><span data-stu-id="30d83-130">To enable MIDI files to be a viable format for representing music in multimedia computing, Windows follows the General MIDI System Level 1 specification.</span></span> <span data-ttu-id="30d83-131">Os tópicos a seguir fornecem diretrizes adicionais de criação de MIDI:</span><span class="sxs-lookup"><span data-stu-id="30d83-131">The following topics provide additional MIDI authoring guidelines:</span></span>

-   [<span data-ttu-id="30d83-132">Diretrizes de criação para arquivos MIDI</span><span class="sxs-lookup"><span data-stu-id="30d83-132">Authoring Guidelines for MIDI Files</span></span>](authoring-guidelines-for-midi-files.md)
-   [<span data-ttu-id="30d83-133">Atribuições de patch de MIDI padrão</span><span class="sxs-lookup"><span data-stu-id="30d83-133">Standard MIDI Patch Assignments</span></span>](standard-midi-patch-assignments.md)
-   [<span data-ttu-id="30d83-134">Atribuições de chave MIDI padrão</span><span class="sxs-lookup"><span data-stu-id="30d83-134">Standard MIDI Key Assignments</span></span>](standard-midi-key-assignments.md)

 

 





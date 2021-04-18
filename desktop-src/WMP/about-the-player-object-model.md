---
title: Sobre o modelo de objeto do Player
description: Sobre o modelo de objeto do Player
ms.assetid: 41a9cbce-b982-4377-a0ee-b0ca735954f5
keywords:
- Windows Media Player, modelo de objeto
- Modelo de objeto do Windows Media Player, sobre
- modelo de objeto, sobre
- Controle ActiveX do Windows Media Player, modelo de objeto
- Controle ActiveX, modelo de objeto
- Controle ActiveX móvel do Windows Media Player, modelo de objeto
- Windows Media Player Mobile, modelo de objeto
- Software Development Kit (SDK), modelo de objeto de controle ActiveX do Windows Media Player
- SDK (Software Development Kit), modelo de objeto de controle ActiveX do Windows Media Player
- documentação, modelo de objeto de controle ActiveX do Windows Media Player
- Objeto de jogador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a0ded1f25d8d08bd9e588b5384a171698d2ea2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796450"
---
# <a name="about-the-player-object-model"></a><span data-ttu-id="e0946-114">Sobre o modelo de objeto do Player</span><span class="sxs-lookup"><span data-stu-id="e0946-114">About the Player Object Model</span></span>

<span data-ttu-id="e0946-115">O controle do Microsoft Windows Media Player é um controle ActiveX padrão que usa a tecnologia COM (Microsoft Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="e0946-115">The Microsoft Windows Media Player control is a standard ActiveX control that uses Microsoft Component Object Model (COM) technology.</span></span> <span data-ttu-id="e0946-116">A funcionalidade do Windows Media Player é ditáticas em um conjunto de interfaces de programação que segue as diretrizes COM padrão.</span><span class="sxs-lookup"><span data-stu-id="e0946-116">The Windows Media Player functionality is distilled into a set of programming interfaces that follows standard COM guidelines.</span></span> <span data-ttu-id="e0946-117">Você pode programar essas interfaces em uma página da Web HTML padrão usando o modelo de objeto de controle do Player com o Microsoft JScript ou o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e0946-117">You can program these interfaces on a standard HTML webpage using the Player control object model with Microsoft JScript or Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="e0946-118">Você também pode programá-los em capas usando o Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="e0946-118">You can also program them in skins by using Microsoft JScript.</span></span> <span data-ttu-id="e0946-119">Se desejar criar um programa personalizado que incorpore o controle, você poderá usar uma das várias linguagens, incluindo Visual Basic, C++ e C#.</span><span class="sxs-lookup"><span data-stu-id="e0946-119">If you want to create a custom program that embeds the control, you can use one of several languages, including Visual Basic, C++, and C#.</span></span>

<span data-ttu-id="e0946-120">O controle ActiveX do Windows Media Player é instalado com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e0946-120">The Windows Media Player ActiveX control is installed with Windows Media Player.</span></span> <span data-ttu-id="e0946-121">O controle do Player não é instalado com o SDK do Windows Media Player e não pode ser redistribuído separadamente.</span><span class="sxs-lookup"><span data-stu-id="e0946-121">The Player control is not installed with the Windows Media Player SDK and cannot be redistributed separately.</span></span> <span data-ttu-id="e0946-122">Os recursos específicos disponíveis para seu código dependem da versão do Windows Media Player que o usuário instalou.</span><span class="sxs-lookup"><span data-stu-id="e0946-122">The particular features available to your code depend on which version of Windows Media Player the user has installed.</span></span> <span data-ttu-id="e0946-123">A [referência de modelo de objeto para script](object-model-reference-for-scripting.md) e [referência de modelo de objeto para C++](object-model-reference-for-c.md) incluem informações de requisito de versão para cada propriedade, método e evento.</span><span class="sxs-lookup"><span data-stu-id="e0946-123">The [Object Model Reference for Scripting](object-model-reference-for-scripting.md) and [Object Model Reference for C++](object-model-reference-for-c.md) include version requirement information for each property, method, and event.</span></span>

<span data-ttu-id="e0946-124">As seções a seguir fornecem informações gerais sobre o modelo de objeto do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e0946-124">The following sections provide overview information about the Windows Media Player object model.</span></span>



| <span data-ttu-id="e0946-125">Seção</span><span class="sxs-lookup"><span data-stu-id="e0946-125">Section</span></span>                                                                                        | <span data-ttu-id="e0946-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0946-126">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0946-127">Modelo de objeto do Player para linguagens de script</span><span class="sxs-lookup"><span data-stu-id="e0946-127">Player Object Model for Scripting Languages</span></span>](player-object-model-for-scripting-languages.md) | <span data-ttu-id="e0946-128">Esta seção descreve os objetos disponíveis no modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="e0946-128">This section describes the objects available in the object model.</span></span>                                                                                             |
| [<span data-ttu-id="e0946-129">Sobre as versões do modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="e0946-129">About the Object Model Versions</span></span>](about-the-object-model-versions.md)                         | <span data-ttu-id="e0946-130">Esta seção detalha quais itens de modelo de objeto foram adicionados em cada versão desde a introdução do Windows Media Player 7,0.</span><span class="sxs-lookup"><span data-stu-id="e0946-130">This section details which object model items have been added in each version since the introduction of Windows Media Player 7.0.</span></span>                             |
| [<span data-ttu-id="e0946-131">Propriedades, métodos e eventos</span><span class="sxs-lookup"><span data-stu-id="e0946-131">Properties, Methods, and Events</span></span>](properties--methods-and-events.md)                          | <span data-ttu-id="e0946-132">Esta seção explica as propriedades, os métodos e os eventos.</span><span class="sxs-lookup"><span data-stu-id="e0946-132">This section explains properties, methods, and events.</span></span>                                                                                                        |
| [<span data-ttu-id="e0946-133">Tipos de arquivos e protocolos com suporte</span><span class="sxs-lookup"><span data-stu-id="e0946-133">Supported Protocols and File Types</span></span>](supported-protocols-and-file-types.md)                   | <span data-ttu-id="e0946-134">Esta seção lista os protocolos e tipos de arquivo com suporte no Windows Media Player e o modelo de objeto de controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e0946-134">This section lists the protocols and file types supported by Windows Media Player and the Windows Media Player control object model.</span></span>                          |
| [<span data-ttu-id="e0946-135">Sobre a biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0946-135">About the Library</span></span>](about-the-library.md)                                                     | <span data-ttu-id="e0946-136">Esta seção descreve a biblioteca do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e0946-136">This section describes the Windows Media Player library.</span></span>                                                                                                      |
| [<span data-ttu-id="e0946-137">Usando HTML com o Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="e0946-137">Using HTML with Windows Media Player</span></span>](using-html-with-windows-media-player.md)               | <span data-ttu-id="e0946-138">Esta seção descreve as várias maneiras de fazer com que o Windows Media Player e o HTML funcionem juntos.</span><span class="sxs-lookup"><span data-stu-id="e0946-138">This section describes the various ways to make Windows Media Player and HTML work together.</span></span>                                                                  |
| [<span data-ttu-id="e0946-139">Inserindo o controle do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="e0946-139">Embedding the Windows Media Player Control</span></span>](embedding-the-windows-media-player-control.md)   | <span data-ttu-id="e0946-140">Esta seção descreve as várias maneiras de inserir o controle do Windows Media Player em Microsoft Office documentos e em programas personalizados.</span><span class="sxs-lookup"><span data-stu-id="e0946-140">This section describes the various ways to embed the Windows Media Player control in Microsoft Office documents and in custom programs.</span></span>                       |
| [<span data-ttu-id="e0946-141">Sobre a sincronização do dispositivo</span><span class="sxs-lookup"><span data-stu-id="e0946-141">About Device Synchronization</span></span>](about-device-synchronization.md)                               | <span data-ttu-id="e0946-142">Esta seção descreve a funcionalidade fornecida pelo controle Windows Media Player 10 ou posterior para transferir conteúdo de mídia digital para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="e0946-142">This section describes the functionality provided by the Windows Media Player 10 or later control for transferring digital media content to portable devices.</span></span> |
| [<span data-ttu-id="e0946-143">Sobre a gravação de CD</span><span class="sxs-lookup"><span data-stu-id="e0946-143">About CD Burning</span></span>](about-cd-burning.md)                                                       | <span data-ttu-id="e0946-144">Esta seção descreve a funcionalidade fornecida pelo controle do Windows Media Player para a criação de CDs.</span><span class="sxs-lookup"><span data-stu-id="e0946-144">This section describes the functionality provided by the Windows Media Player control for creating CDs.</span></span>                                                       |
| [<span data-ttu-id="e0946-145">Sobre a cópia de CD</span><span class="sxs-lookup"><span data-stu-id="e0946-145">About CD Ripping</span></span>](about-cd-ripping.md)                                                       | <span data-ttu-id="e0946-146">Esta seção descreve a funcionalidade fornecida pelo controle do Windows Media Player para copiar faixas de CDs de áudio para o computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="e0946-146">This section describes the functionality provided by the Windows Media Player control for copying tracks from audio CDs to the user's computer.</span></span>               |
| [<span data-ttu-id="e0946-147">Sobre o monitoramento de pastas</span><span class="sxs-lookup"><span data-stu-id="e0946-147">About Folder Monitoring</span></span>](about-folder-monitoring.md)                                         | <span data-ttu-id="e0946-148">Esta seção descreve a funcionalidade fornecida pelo controle do Windows Media Player para controlar os processos de monitoramento de pasta do Player.</span><span class="sxs-lookup"><span data-stu-id="e0946-148">This section describes the functionality provided by the Windows Media Player control for controlling the Player's folder monitoring processes.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="e0946-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0946-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0946-150">**Modelo de objeto do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="e0946-150">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 





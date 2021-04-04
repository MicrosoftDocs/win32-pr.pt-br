---
title: Elemento PLAYER
description: Elemento PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Capas do Windows Media Player, elemento PLAYER
- capas, elemento PLAYER
- Elemento PLAYER
- referência para capas, elemento PLAYER
- elementos, PLAYER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084101"
---
# <a name="player-element"></a><span data-ttu-id="14845-108">Elemento PLAYER</span><span class="sxs-lookup"><span data-stu-id="14845-108">PLAYER Element</span></span>

<span data-ttu-id="14845-109">O elemento **Player** permite definir manipuladores de eventos e especificar a propriedade **URL** do objeto **Player** em tempo de design em um arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="14845-109">The **PLAYER** element lets you define event handlers and specify the **URL** property of the **Player** object at design time within a skin definition file.</span></span> <span data-ttu-id="14845-110">No código de script, o objeto **Player** é acessado por meio do atributo global **Player** , em vez de um nome especificado por um atributo de **ID** , que não tem suporte do elemento **Player** .</span><span class="sxs-lookup"><span data-stu-id="14845-110">Within script code, the **Player** object is accessed through the **player** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **PLAYER** element.</span></span>

<span data-ttu-id="14845-111">O elemento **Player** dá suporte ao atributo a seguir.</span><span class="sxs-lookup"><span data-stu-id="14845-111">The **PLAYER** element supports the following attribute.</span></span>



| <span data-ttu-id="14845-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="14845-112">Attribute</span></span>             | <span data-ttu-id="14845-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="14845-113">Description</span></span>                                          |
|-----------------------|------------------------------------------------------|
| [<span data-ttu-id="14845-114">URL</span><span class="sxs-lookup"><span data-stu-id="14845-114">URL</span></span>](player-url.md) | <span data-ttu-id="14845-115">Especifica ou recupera o nome do arquivo a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="14845-115">Specifies or retrieves the name of the file to play.</span></span> |



 

<span data-ttu-id="14845-116">O elemento **Player** pode implementar manipuladores de eventos para os eventos a seguir acionados do objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="14845-116">The **PLAYER** element can implement event handlers for the following events fired from the **Player** object.</span></span>



| <span data-ttu-id="14845-117">Evento</span><span class="sxs-lookup"><span data-stu-id="14845-117">Event</span></span>                                                                                            | <span data-ttu-id="14845-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="14845-118">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="14845-119">AudioLanguageChange</span><span class="sxs-lookup"><span data-stu-id="14845-119">AudioLanguageChange</span></span>](player-player-audiolanguagechange.md)                                     | <span data-ttu-id="14845-120">Ocorre quando o idioma de áudio atual é alterado.</span><span class="sxs-lookup"><span data-stu-id="14845-120">Occurs when the current audio language changes.</span></span>                                  |
| [<span data-ttu-id="14845-121">de resposta</span><span class="sxs-lookup"><span data-stu-id="14845-121">Buffering</span></span>](player-player-buffering.md)                                                         | <span data-ttu-id="14845-122">Ocorre quando o Windows Media Player inicia ou termina o armazenamento em buffer.</span><span class="sxs-lookup"><span data-stu-id="14845-122">Occurs when Windows Media Player begins or ends buffering.</span></span>                       |
| [<span data-ttu-id="14845-123">CdromMediaChange</span><span class="sxs-lookup"><span data-stu-id="14845-123">CdromMediaChange</span></span>](player-player-cdrommediachange.md)                                           | <span data-ttu-id="14845-124">Ocorre quando a mídia do CD é alterada.</span><span class="sxs-lookup"><span data-stu-id="14845-124">Occurs when the CD media changes.</span></span>                                                |
| [<span data-ttu-id="14845-125">CurrentItemChange</span><span class="sxs-lookup"><span data-stu-id="14845-125">CurrentItemChange</span></span>](player-player-currentitemchange.md)                                         | <span data-ttu-id="14845-126">Ocorre quando o item atual é alterado.</span><span class="sxs-lookup"><span data-stu-id="14845-126">Occurs when the current item changes.</span></span>                                            |
| [<span data-ttu-id="14845-127">CurrentMediaItemAvailable</span><span class="sxs-lookup"><span data-stu-id="14845-127">CurrentMediaItemAvailable</span></span>](player-player-currentmediaitemavailable.md)                         | <span data-ttu-id="14845-128">Ocorre quando o item de mídia atual fica disponível.</span><span class="sxs-lookup"><span data-stu-id="14845-128">Occurs when the current media item becomes available.</span></span>                            |
| [<span data-ttu-id="14845-129">CurrentPlaylistChange</span><span class="sxs-lookup"><span data-stu-id="14845-129">CurrentPlaylistChange</span></span>](player-player-currentplaylistchange.md)                                 | <span data-ttu-id="14845-130">Ocorre quando a playlist atual é alterada.</span><span class="sxs-lookup"><span data-stu-id="14845-130">Occurs when the current playlist changes.</span></span>                                        |
| [<span data-ttu-id="14845-131">CurrentPlaylistItemAvailable</span><span class="sxs-lookup"><span data-stu-id="14845-131">CurrentPlaylistItemAvailable</span></span>](player-player-currentplaylistitemavailable.md)                   | <span data-ttu-id="14845-132">Ocorre quando o item da playlist atual se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="14845-132">Occurs when the current playlist item becomes available.</span></span>                         |
| [<span data-ttu-id="14845-133">DomainChange</span><span class="sxs-lookup"><span data-stu-id="14845-133">DomainChange</span></span>](player-player-domainchange.md)                                                   | <span data-ttu-id="14845-134">Ocorre quando o domínio do DVD é alterado.</span><span class="sxs-lookup"><span data-stu-id="14845-134">Occurs when the DVD domain changes.</span></span>                                              |
| [<span data-ttu-id="14845-135">Erro</span><span class="sxs-lookup"><span data-stu-id="14845-135">Error</span></span>](player-player-error.md)                                                                 | <span data-ttu-id="14845-136">Ocorre quando o controle do Windows Media Player tem uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="14845-136">Occurs when the Windows Media Player control has an error condition.</span></span>             |
| [<span data-ttu-id="14845-137">MarkerHit</span><span class="sxs-lookup"><span data-stu-id="14845-137">MarkerHit</span></span>](player-player-markerhit.md)                                                         | <span data-ttu-id="14845-138">Ocorre quando o Windows Media Player encontra um marcador no clipe.</span><span class="sxs-lookup"><span data-stu-id="14845-138">Occurs when Windows Media Player encounters a marker in the clip.</span></span>                |
| [<span data-ttu-id="14845-139">MediaChange</span><span class="sxs-lookup"><span data-stu-id="14845-139">MediaChange</span></span>](player-player-mediachange.md)                                                     | <span data-ttu-id="14845-140">Ocorre quando um item de mídia é alterado.</span><span class="sxs-lookup"><span data-stu-id="14845-140">Occurs when a media item changes.</span></span>                                                |
| [<span data-ttu-id="14845-141">MediaCollectionAttributeStringAdded</span><span class="sxs-lookup"><span data-stu-id="14845-141">MediaCollectionAttributeStringAdded</span></span>](player-player-mediacollectionattributestringadded.md)     | <span data-ttu-id="14845-142">Ocorre quando um valor de atributo é adicionado à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="14845-142">Occurs when an attribute value is added to the library.</span></span>                          |
| [<span data-ttu-id="14845-143">MediaCollectionAttributeStringChanged</span><span class="sxs-lookup"><span data-stu-id="14845-143">MediaCollectionAttributeStringChanged</span></span>](player-player-mediacollectionattributestringchanged.md) | <span data-ttu-id="14845-144">Ocorre quando um valor de atributo na biblioteca é alterado.</span><span class="sxs-lookup"><span data-stu-id="14845-144">Occurs when an attribute value in the library is changed.</span></span>                        |
| [<span data-ttu-id="14845-145">MediaCollectionAttributeStringRemoved</span><span class="sxs-lookup"><span data-stu-id="14845-145">MediaCollectionAttributeStringRemoved</span></span>](player-player-mediacollectionattributestringremoved.md) | <span data-ttu-id="14845-146">Ocorre quando um valor de atributo é removido da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="14845-146">Occurs when an attribute value is removed from the library.</span></span>                      |
| [<span data-ttu-id="14845-147">MediaCollectionChange</span><span class="sxs-lookup"><span data-stu-id="14845-147">MediaCollectionChange</span></span>](player-player-mediacollectionchange.md)                                 | <span data-ttu-id="14845-148">Ocorre quando o objeto **mediacollection** é alterado.</span><span class="sxs-lookup"><span data-stu-id="14845-148">Occurs when the **MediaCollection** object changes.</span></span>                              |
| [<span data-ttu-id="14845-149">MediaError</span><span class="sxs-lookup"><span data-stu-id="14845-149">MediaError</span></span>](player-player-mediaerror.md)                                                       | <span data-ttu-id="14845-150">Ocorre quando o objeto de **mídia** tem uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="14845-150">Occurs when the **Media** object has an error condition.</span></span>                         |
| [<span data-ttu-id="14845-151">ModeChange</span><span class="sxs-lookup"><span data-stu-id="14845-151">ModeChange</span></span>](player-player-modechange.md)                                                       | <span data-ttu-id="14845-152">Ocorre ao alternar entre o modo de ordem aleatória e normal.</span><span class="sxs-lookup"><span data-stu-id="14845-152">Occurs when switching between shuffle and normal mode.</span></span>                           |
| [<span data-ttu-id="14845-153">OpenPlaylistSwitch</span><span class="sxs-lookup"><span data-stu-id="14845-153">OpenPlaylistSwitch</span></span>](player-player-openplaylistswitch.md)                                       | <span data-ttu-id="14845-154">Ocorre quando um título em um DVD começa a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="14845-154">Occurs when a title on a DVD begins playing.</span></span>                                     |
| [<span data-ttu-id="14845-155">OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="14845-155">OpenStateChange</span></span>](player-player-openstatechange.md)                                             | <span data-ttu-id="14845-156">Ocorre quando o *Player*. alterações de **OpenState** .</span><span class="sxs-lookup"><span data-stu-id="14845-156">Occurs when *player*.**openState** changes.</span></span>                                      |
| [<span data-ttu-id="14845-157">PlaylistChange</span><span class="sxs-lookup"><span data-stu-id="14845-157">PlaylistChange</span></span>](player-player-playlistchange.md)                                               | <span data-ttu-id="14845-158">Ocorre quando uma playlist é alterada.</span><span class="sxs-lookup"><span data-stu-id="14845-158">Occurs when a playlist changes.</span></span>                                                  |
| [<span data-ttu-id="14845-159">PlaylistCollectionChange</span><span class="sxs-lookup"><span data-stu-id="14845-159">PlaylistCollectionChange</span></span>](player-player-playlistcollectionchange.md)                           | <span data-ttu-id="14845-160">Ocorre quando algo é alterado na coleção de playlist.</span><span class="sxs-lookup"><span data-stu-id="14845-160">Occurs when something changes in the playlist collection.</span></span>                        |
| [<span data-ttu-id="14845-161">PlaylistCollectionPlaylistAdded</span><span class="sxs-lookup"><span data-stu-id="14845-161">PlaylistCollectionPlaylistAdded</span></span>](player-player-playlistcollectionplaylistadded.md)             | <span data-ttu-id="14845-162">Ocorre quando uma playlist é adicionada à coleção de playlist.</span><span class="sxs-lookup"><span data-stu-id="14845-162">Occurs when a playlist is added to the playlist collection.</span></span>                      |
| [<span data-ttu-id="14845-163">PlaylistCollectionPlaylistRemoved</span><span class="sxs-lookup"><span data-stu-id="14845-163">PlaylistCollectionPlaylistRemoved</span></span>](player-player-playlistcollectionplaylistremoved.md)         | <span data-ttu-id="14845-164">Ocorre quando uma playlist é removida da coleção de playlist.</span><span class="sxs-lookup"><span data-stu-id="14845-164">Occurs when a playlist is removed from the playlist collection.</span></span>                  |
| [<span data-ttu-id="14845-165">PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="14845-165">PlayStateChange</span></span>](player-player-playstatechange.md)                                             | <span data-ttu-id="14845-166">Ocorre quando o *Player*. alterações de **PlayState** .</span><span class="sxs-lookup"><span data-stu-id="14845-166">Occurs when *player*.**playState** changes.</span></span>                                      |
| [<span data-ttu-id="14845-167">PositionChange</span><span class="sxs-lookup"><span data-stu-id="14845-167">PositionChange</span></span>](player-player-positionchange.md)                                               | <span data-ttu-id="14845-168">Ocorre quando o *Player*. de *controle*. **CurrentPosition** alterações.</span><span class="sxs-lookup"><span data-stu-id="14845-168">Occurs when *player*.*controls*.**currentPosition** changes.</span></span>                     |
| [<span data-ttu-id="14845-169">ScriptCommand</span><span class="sxs-lookup"><span data-stu-id="14845-169">ScriptCommand</span></span>](player-player-scriptcommand.md)                                                 | <span data-ttu-id="14845-170">Ocorre quando o Windows Media Player encontra um comando de script inserido em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="14845-170">Occurs when Windows Media Player encounters a script command embedded in a file.</span></span> |
| [<span data-ttu-id="14845-171">StatusChange</span><span class="sxs-lookup"><span data-stu-id="14845-171">StatusChange</span></span>](player-player-statuschange.md)                                                   | <span data-ttu-id="14845-172">Ocorre quando o valor da propriedade **status** é alterado.</span><span class="sxs-lookup"><span data-stu-id="14845-172">Occurs when the **status** property changes value.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="14845-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14845-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14845-174">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="14845-174">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="14845-175">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="14845-175">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 





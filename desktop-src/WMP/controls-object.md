---
title: Objeto Controls
description: O objeto Controls fornece uma maneira de manipular a reprodução de mídia usando as propriedades e os métodos a seguir.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Objeto de controles Windows Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103638718"
---
# <a name="controls-object"></a><span data-ttu-id="4d44c-104">Objeto Controls</span><span class="sxs-lookup"><span data-stu-id="4d44c-104">Controls Object</span></span>

<span data-ttu-id="4d44c-105">O objeto **Controls** fornece uma maneira de manipular a reprodução de mídia usando as propriedades e os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d44c-105">The **Controls** object provides a way to manipulate the playback of media using the following properties and methods.</span></span>

<span data-ttu-id="4d44c-106">O objeto **Controls** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d44c-106">The **Controls** object supports the following properties.</span></span>



| <span data-ttu-id="4d44c-107">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4d44c-107">Property</span></span>                                                            | <span data-ttu-id="4d44c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d44c-108">Description</span></span>                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d44c-109">audioLanguageCount</span><span class="sxs-lookup"><span data-stu-id="4d44c-109">audioLanguageCount</span></span>](controls-audiolanguagecount.md)               | <span data-ttu-id="4d44c-110">Recupera o número de idiomas de áudio com suporte.</span><span class="sxs-lookup"><span data-stu-id="4d44c-110">Retrieves the number of supported audio languages.</span></span>                                                                                                |
| [<span data-ttu-id="4d44c-111">currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="4d44c-111">currentAudioLanguage</span></span>](controls-currentaudiolanguage.md)           | <span data-ttu-id="4d44c-112">Especifica ou recupera o LCID (identificador de localidade) do idioma de áudio para reprodução</span><span class="sxs-lookup"><span data-stu-id="4d44c-112">Specifies or retrieves the locale identifier (LCID) of the audio language for playback</span></span>                                                            |
| [<span data-ttu-id="4d44c-113">currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="4d44c-113">currentAudioLanguageIndex</span></span>](controls-currentaudiolanguageindex.md) | <span data-ttu-id="4d44c-114">Especifica ou recupera o índice com base em um que corresponde ao idioma de áudio para reprodução.</span><span class="sxs-lookup"><span data-stu-id="4d44c-114">Specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>                                                   |
| [<span data-ttu-id="4d44c-115">currentItem</span><span class="sxs-lookup"><span data-stu-id="4d44c-115">currentItem</span></span>](controls-currentitem.md)                             | <span data-ttu-id="4d44c-116">Especifica ou recupera o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="4d44c-116">Specifies or retrieves the current media item.</span></span>                                                                                                    |
| [<span data-ttu-id="4d44c-117">currentMarker</span><span class="sxs-lookup"><span data-stu-id="4d44c-117">currentMarker</span></span>](controls-currentmarker.md)                         | <span data-ttu-id="4d44c-118">Especifica ou recupera o número do marcador atual.</span><span class="sxs-lookup"><span data-stu-id="4d44c-118">Specifies or retrieves the current marker number.</span></span>                                                                                                 |
| [<span data-ttu-id="4d44c-119">currentPosition</span><span class="sxs-lookup"><span data-stu-id="4d44c-119">currentPosition</span></span>](controls-currentposition.md)                     | <span data-ttu-id="4d44c-120">Especifica ou recupera a posição atual no item de mídia em segundos desde o início.</span><span class="sxs-lookup"><span data-stu-id="4d44c-120">Specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>                                                      |
| [<span data-ttu-id="4d44c-121">currentPositionString</span><span class="sxs-lookup"><span data-stu-id="4d44c-121">currentPositionString</span></span>](controls-currentpositionstring.md)         | <span data-ttu-id="4d44c-122">Recupera a posição atual no item de mídia como uma **cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="4d44c-122">Retrieves the current position in the media item as a **String**.</span></span>                                                                                 |
| [<span data-ttu-id="4d44c-123">currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="4d44c-123">currentPositionTimecode</span></span>](controls-currentpositiontimecode.md)     | <span data-ttu-id="4d44c-124">Especifica ou recupera a posição atual no item de mídia atual usando um formato de código de tempo.</span><span class="sxs-lookup"><span data-stu-id="4d44c-124">Specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="4d44c-125">Essa propriedade atualmente dá suporte ao código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="4d44c-125">This property currently supports SMPTE time code.</span></span> |
| [<span data-ttu-id="4d44c-126">isAvailable</span><span class="sxs-lookup"><span data-stu-id="4d44c-126">isAvailable</span></span>](controls-isavailable.md)                             | <span data-ttu-id="4d44c-127">Recupera se um tipo especificado de informação está disponível ou se uma determinada ação pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="4d44c-127">Retrieves whether a specified type of information is available or a given action can be performed.</span></span>                                                |



 

<span data-ttu-id="4d44c-128">O objeto **Controls** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d44c-128">The **Controls** object supports the following methods.</span></span>



| <span data-ttu-id="4d44c-129">Método</span><span class="sxs-lookup"><span data-stu-id="4d44c-129">Method</span></span>                                                                  | <span data-ttu-id="4d44c-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d44c-130">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d44c-131">fastForward</span><span class="sxs-lookup"><span data-stu-id="4d44c-131">fastForward</span></span>](controls-fastforward.md)                                 | <span data-ttu-id="4d44c-132">Inicia a reprodução rápida do item de mídia na direção de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="4d44c-132">Starts fast play of the media item in the forward direction.</span></span>                                     |
| [<span data-ttu-id="4d44c-133">fastReverse</span><span class="sxs-lookup"><span data-stu-id="4d44c-133">fastReverse</span></span>](controls-fastreverse.md)                                 | <span data-ttu-id="4d44c-134">Inicia a reprodução rápida do item de mídia na direção inversa.</span><span class="sxs-lookup"><span data-stu-id="4d44c-134">Starts fast play of the media item in the reverse direction.</span></span>                                     |
| [<span data-ttu-id="4d44c-135">getAudioLanguageDescription</span><span class="sxs-lookup"><span data-stu-id="4d44c-135">getAudioLanguageDescription</span></span>](controls-getaudiolanguagedescription.md) | <span data-ttu-id="4d44c-136">Recupera a descrição do idioma de áudio correspondente ao índice baseado em um especificado.</span><span class="sxs-lookup"><span data-stu-id="4d44c-136">Retrieves the description for the audio language corresponding to the specified one-based index.</span></span> |
| [<span data-ttu-id="4d44c-137">getAudioLanguageID</span><span class="sxs-lookup"><span data-stu-id="4d44c-137">getAudioLanguageID</span></span>](controls-getaudiolanguageid.md)                   | <span data-ttu-id="4d44c-138">Recupera o LCID para um índice de idioma de áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="4d44c-138">Retrieves the LCID for a specified audio language index.</span></span>                                         |
| [<span data-ttu-id="4d44c-139">getLanguageName</span><span class="sxs-lookup"><span data-stu-id="4d44c-139">getLanguageName</span></span>](controls-getlanguagename.md)                         | <span data-ttu-id="4d44c-140">Recupera o nome do idioma de áudio com o LCID especificado.</span><span class="sxs-lookup"><span data-stu-id="4d44c-140">Retrieves the name of the audio language with the specified LCID.</span></span>                                |
| [<span data-ttu-id="4d44c-141">avançar</span><span class="sxs-lookup"><span data-stu-id="4d44c-141">next</span></span>](controls-next.md)                                               | <span data-ttu-id="4d44c-142">Define o item atual para o próximo item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4d44c-142">Sets the current item to the next item in the playlist.</span></span>                                          |
| [<span data-ttu-id="4d44c-143">pause</span><span class="sxs-lookup"><span data-stu-id="4d44c-143">pause</span></span>](controls-pause.md)                                             | <span data-ttu-id="4d44c-144">Pausa a reprodução do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="4d44c-144">Pauses the playing of the media item.</span></span>                                                            |
| [<span data-ttu-id="4d44c-145">reproduzir</span><span class="sxs-lookup"><span data-stu-id="4d44c-145">play</span></span>](controls-play.md)                                               | <span data-ttu-id="4d44c-146">Faz com que o item de mídia inicie a reprodução.</span><span class="sxs-lookup"><span data-stu-id="4d44c-146">Causes the media item to start playing.</span></span>                                                          |
| [<span data-ttu-id="4d44c-147">playItem</span><span class="sxs-lookup"><span data-stu-id="4d44c-147">playItem</span></span>](controls-playitem.md)                                       | <span data-ttu-id="4d44c-148">Faz com que o item de mídia atual inicie a reprodução ou retome a reprodução de um item pausado.</span><span class="sxs-lookup"><span data-stu-id="4d44c-148">Causes the current media item to start playing, or resumes play of a paused item.</span></span>                |
| [<span data-ttu-id="4d44c-149">Anterior</span><span class="sxs-lookup"><span data-stu-id="4d44c-149">previous</span></span>](controls-previous.md)                                       | <span data-ttu-id="4d44c-150">Define o item atual para o item anterior na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4d44c-150">Sets the current item to the previous item in the playlist.</span></span>                                      |
| [<span data-ttu-id="4d44c-151">etapa</span><span class="sxs-lookup"><span data-stu-id="4d44c-151">step</span></span>](controls-step.md)                                               | <span data-ttu-id="4d44c-152">Faz com que o item de mídia de vídeo atual congele a reprodução no próximo quadro.</span><span class="sxs-lookup"><span data-stu-id="4d44c-152">Causes the current video media item to freeze playback on the next frame.</span></span>                        |
| [<span data-ttu-id="4d44c-153">stop</span><span class="sxs-lookup"><span data-stu-id="4d44c-153">stop</span></span>](controls-stop.md)                                               | <span data-ttu-id="4d44c-154">Interrompe a reprodução do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="4d44c-154">Stops the playing of the media item.</span></span>                                                             |



 

<span data-ttu-id="4d44c-155">O objeto **Controls** é acessado por meio da propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d44c-155">The **Controls** object is accessed through the following property.</span></span>



| <span data-ttu-id="4d44c-156">Objeto</span><span class="sxs-lookup"><span data-stu-id="4d44c-156">Object</span></span>                      | <span data-ttu-id="4d44c-157">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4d44c-157">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="4d44c-158">Jogador</span><span class="sxs-lookup"><span data-stu-id="4d44c-158">Player</span></span>](player-object.md) | [<span data-ttu-id="4d44c-159">controles</span><span class="sxs-lookup"><span data-stu-id="4d44c-159">controls</span></span>](player-controls.md) |



 

## <a name="see-also"></a><span data-ttu-id="4d44c-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d44c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d44c-161">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="4d44c-161">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





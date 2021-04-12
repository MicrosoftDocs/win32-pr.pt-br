---
title: Referência de MIDI
description: Referência de MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Multimídia do Windows, MIDI (interface digital de instrumentos musicais)
- multimídia, MIDI (interface digital de instrumentos musicais)
- áudio multimídia, MIDI (interface digital de instrumentos musicais)
- áudio, MIDI (interface digital de instrumento musical)
- Multimídia do Windows, referência de MIDI
- referência de multimídia, MIDI
- áudio de multimídia, referência de MIDI
- áudio, referência de MIDI
- MIDI (interface digital de instrumento musical), referência
- MIDI (interface digital de instrumentos musicais), referência
- referência para MIDI, sobre
- Referência de MIDI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365960"
---
# <a name="midi-reference"></a><span data-ttu-id="b8df6-115">Referência de MIDI</span><span class="sxs-lookup"><span data-stu-id="b8df6-115">MIDI Reference</span></span>

<span data-ttu-id="b8df6-116">Esta seção descreve as funções, macros, mensagens e estruturas associadas à MIDI (interface digital de instrumento musical).</span><span class="sxs-lookup"><span data-stu-id="b8df6-116">This section describes the functions, macros, messages, and structures associated with the Musical Instrument Digital Interface (MIDI).</span></span> <span data-ttu-id="b8df6-117">Esses elementos são agrupados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="b8df6-117">These elements are grouped as follows.</span></span>

## <a name="allocating-and-managing-buffers"></a><span data-ttu-id="b8df6-118">Alocando e gerenciando buffers</span><span class="sxs-lookup"><span data-stu-id="b8df6-118">Allocating and Managing Buffers</span></span>

-   [<span data-ttu-id="b8df6-119">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="b8df6-119">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [<span data-ttu-id="b8df6-120">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="b8df6-120">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [<span data-ttu-id="b8df6-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="b8df6-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [<span data-ttu-id="b8df6-122">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="b8df6-122">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [<span data-ttu-id="b8df6-123">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="b8df6-123">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [<span data-ttu-id="b8df6-124">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="b8df6-124">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a><span data-ttu-id="b8df6-125">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="b8df6-125">Callback Functions</span></span>

-   <span data-ttu-id="b8df6-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8df6-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span></span>
-   <span data-ttu-id="b8df6-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8df6-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="b8df6-128">Funcionalidades do dispositivo</span><span class="sxs-lookup"><span data-stu-id="b8df6-128">Device Capabilities</span></span>

-   [<span data-ttu-id="b8df6-129">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="b8df6-129">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [<span data-ttu-id="b8df6-130">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="b8df6-130">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [<span data-ttu-id="b8df6-131">**midiInGetID**</span><span class="sxs-lookup"><span data-stu-id="b8df6-131">**midiInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [<span data-ttu-id="b8df6-132">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="b8df6-132">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [<span data-ttu-id="b8df6-133">**MIDIOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="b8df6-133">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [<span data-ttu-id="b8df6-134">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="b8df6-134">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [<span data-ttu-id="b8df6-135">**midiOutGetID**</span><span class="sxs-lookup"><span data-stu-id="b8df6-135">**midiOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [<span data-ttu-id="b8df6-136">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="b8df6-136">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [<span data-ttu-id="b8df6-137">**MIDISTRMBUFFVER**</span><span class="sxs-lookup"><span data-stu-id="b8df6-137">**MIDISTRMBUFFVER**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a><span data-ttu-id="b8df6-138">Processamento de erro</span><span class="sxs-lookup"><span data-stu-id="b8df6-138">Error Processing</span></span>

-   [<span data-ttu-id="b8df6-139">**midiInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="b8df6-139">**midiInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [<span data-ttu-id="b8df6-140">**midiOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="b8df6-140">**midiOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [<span data-ttu-id="b8df6-141">**erro do MIM \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-141">**MIM\_ERROR**</span></span>](mim-error.md)
-   [<span data-ttu-id="b8df6-142">**\_LONGERROR mim**</span><span class="sxs-lookup"><span data-stu-id="b8df6-142">**MIM\_LONGERROR**</span></span>](mim-longerror.md)
-   [<span data-ttu-id="b8df6-143">**\_erro do mim mm \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-143">**MM\_MIM\_ERROR**</span></span>](mm-mim-error.md)
-   [<span data-ttu-id="b8df6-144">**\_LONGERROR do mim mm \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-144">**MM\_MIM\_LONGERROR**</span></span>](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a><span data-ttu-id="b8df6-145">Gerenciando fluxos de MIDI</span><span class="sxs-lookup"><span data-stu-id="b8df6-145">Managing MIDI Streams</span></span>

-   [<span data-ttu-id="b8df6-146">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="b8df6-146">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [<span data-ttu-id="b8df6-147">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="b8df6-147">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [<span data-ttu-id="b8df6-148">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="b8df6-148">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="b8df6-149">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="b8df6-149">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="b8df6-150">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="b8df6-150">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [<span data-ttu-id="b8df6-151">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="b8df6-151">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [<span data-ttu-id="b8df6-152">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="b8df6-152">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="b8df6-153">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="b8df6-153">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a><span data-ttu-id="b8df6-154">Abrindo e fechando dispositivos</span><span class="sxs-lookup"><span data-stu-id="b8df6-154">Opening and Closing Devices</span></span>

-   [<span data-ttu-id="b8df6-155">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="b8df6-155">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [<span data-ttu-id="b8df6-156">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="b8df6-156">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [<span data-ttu-id="b8df6-157">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="b8df6-157">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [<span data-ttu-id="b8df6-158">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="b8df6-158">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [<span data-ttu-id="b8df6-159">**próximo a MIM \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-159">**MIM\_CLOSE**</span></span>](mim-close.md)
-   [<span data-ttu-id="b8df6-160">**MIM \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="b8df6-160">**MIM\_OPEN**</span></span>](mim-open.md)
-   [<span data-ttu-id="b8df6-161">**Eu \_ fechar do mim \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-161">**MM\_MIM\_CLOSE**</span></span>](mm-mim-close.md)
-   [<span data-ttu-id="b8df6-162">**MIM de MM \_ \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="b8df6-162">**MM\_MIM\_OPEN**</span></span>](mm-mim-open.md)
-   [<span data-ttu-id="b8df6-163">**\_fechamento do MOM mm \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-163">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md)
-   [<span data-ttu-id="b8df6-164">**\_Mom mm \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="b8df6-164">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)
-   [<span data-ttu-id="b8df6-165">**fechamento do MOM \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-165">**MOM\_CLOSE**</span></span>](mom-close.md)
-   [<span data-ttu-id="b8df6-166">**MOM \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="b8df6-166">**MOM\_OPEN**</span></span>](mom-open.md)

## <a name="output-devices"></a><span data-ttu-id="b8df6-167">Dispositivos de saída</span><span class="sxs-lookup"><span data-stu-id="b8df6-167">Output Devices</span></span>

-   [<span data-ttu-id="b8df6-168">Keyarray</span><span class="sxs-lookup"><span data-stu-id="b8df6-168">KEYARRAY</span></span>](keyarray.md)
-   [<span data-ttu-id="b8df6-169">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="b8df6-169">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [<span data-ttu-id="b8df6-170">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="b8df6-170">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [<span data-ttu-id="b8df6-171">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="b8df6-171">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [<span data-ttu-id="b8df6-172">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="b8df6-172">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [<span data-ttu-id="b8df6-173">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="b8df6-173">PATCHARRAY</span></span>](patcharray.md)

## <a name="playing-a-message-or-messages"></a><span data-ttu-id="b8df6-174">Reproduzir uma mensagem ou mensagens</span><span class="sxs-lookup"><span data-stu-id="b8df6-174">Playing a Message or Messages</span></span>

-   [<span data-ttu-id="b8df6-175">**MEVT \_ EVENTPARM**</span><span class="sxs-lookup"><span data-stu-id="b8df6-175">**MEVT\_EVENTPARM**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [<span data-ttu-id="b8df6-176">**\_EVENTTYPE MEVT**</span><span class="sxs-lookup"><span data-stu-id="b8df6-176">**MEVT\_EVENTTYPE**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [<span data-ttu-id="b8df6-177">**MIDIEVENT**</span><span class="sxs-lookup"><span data-stu-id="b8df6-177">**MIDIEVENT**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [<span data-ttu-id="b8df6-178">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="b8df6-178">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [<span data-ttu-id="b8df6-179">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="b8df6-179">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [<span data-ttu-id="b8df6-180">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="b8df6-180">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [<span data-ttu-id="b8df6-181">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="b8df6-181">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="b8df6-182">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="b8df6-182">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="b8df6-183">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="b8df6-183">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="b8df6-184">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="b8df6-184">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [<span data-ttu-id="b8df6-185">**\_Mom mm \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="b8df6-185">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)
-   [<span data-ttu-id="b8df6-186">**MM \_ Mom \_ POSITIONCB**</span><span class="sxs-lookup"><span data-stu-id="b8df6-186">**MM\_MOM\_POSITIONCB**</span></span>](mm-mom-positioncb.md)
-   [<span data-ttu-id="b8df6-187">**MOM \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="b8df6-187">**MOM\_DONE**</span></span>](mom-done.md)
-   [<span data-ttu-id="b8df6-188">**POSITIONCB do MOM \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-188">**MOM\_POSITIONCB**</span></span>](mom-positioncb.md)

## <a name="recording"></a><span data-ttu-id="b8df6-189">Gravação</span><span class="sxs-lookup"><span data-stu-id="b8df6-189">Recording</span></span>

-   [<span data-ttu-id="b8df6-190">**midiConnect**</span><span class="sxs-lookup"><span data-stu-id="b8df6-190">**midiConnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [<span data-ttu-id="b8df6-191">**midiDisconnect**</span><span class="sxs-lookup"><span data-stu-id="b8df6-191">**midiDisconnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [<span data-ttu-id="b8df6-192">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="b8df6-192">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [<span data-ttu-id="b8df6-193">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="b8df6-193">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [<span data-ttu-id="b8df6-194">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="b8df6-194">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [<span data-ttu-id="b8df6-195">**MIDIPROPTEMPO**</span><span class="sxs-lookup"><span data-stu-id="b8df6-195">**MIDIPROPTEMPO**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [<span data-ttu-id="b8df6-196">**MIDIPROPTIMEDIV**</span><span class="sxs-lookup"><span data-stu-id="b8df6-196">**MIDIPROPTIMEDIV**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [<span data-ttu-id="b8df6-197">**dados do MIM \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-197">**MIM\_DATA**</span></span>](mim-data.md)
-   [<span data-ttu-id="b8df6-198">**\_LONGDATA mim**</span><span class="sxs-lookup"><span data-stu-id="b8df6-198">**MIM\_LONGDATA**</span></span>](mim-longdata.md)
-   [<span data-ttu-id="b8df6-199">**\_MOREDATA mim**</span><span class="sxs-lookup"><span data-stu-id="b8df6-199">**MIM\_MOREDATA**</span></span>](mim-moredata.md)
-   [<span data-ttu-id="b8df6-200">**\_dados do mim mm \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-200">**MM\_MIM\_DATA**</span></span>](mm-mim-data.md)
-   [<span data-ttu-id="b8df6-201">**\_MOREDATA do mim mm \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-201">**MM\_MIM\_MOREDATA**</span></span>](mm-mim-moredata.md)
-   [<span data-ttu-id="b8df6-202">**\_LONGDATA do mim mm \_**</span><span class="sxs-lookup"><span data-stu-id="b8df6-202">**MM\_MIM\_LONGDATA**</span></span>](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a><span data-ttu-id="b8df6-203">Enviando mensagens para dispositivos</span><span class="sxs-lookup"><span data-stu-id="b8df6-203">Sending Messages to Devices</span></span>

-   [<span data-ttu-id="b8df6-204">**midiInMessage**</span><span class="sxs-lookup"><span data-stu-id="b8df6-204">**midiInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [<span data-ttu-id="b8df6-205">**midiOutMessage**</span><span class="sxs-lookup"><span data-stu-id="b8df6-205">**midiOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a><span data-ttu-id="b8df6-206">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8df6-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8df6-207">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="b8df6-207">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 
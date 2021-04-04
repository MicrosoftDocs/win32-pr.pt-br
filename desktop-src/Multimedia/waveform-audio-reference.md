---
title: Referência de áudio de onda
description: Esta seção lista as funções, as estruturas e as mensagens associadas ao áudio de onda, que estão documentados em referência de multimídia. Esses elementos são agrupados da seguinte maneira.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Multimídia do Windows, referência de áudio de onda
- referência de áudio de multimídia, formato de onda
- áudio de multimídia, referência de Wave
- referência de áudio, de onda
- Multimídia do Windows, áudio de onda
- multimídia, áudio de onda
- áudio de multimídia, onda
- áudio, onda
- áudio de onda, referência
- referência de áudio de onda, sobre
- referência para áudio wavefore, sobre
- referência de áudio de onda, dispositivos auxiliares
- referência para áudio wavefore, dispositivos auxiliares
- referência de áudio de onda, reprodução
- referência para áudio wavefore, reprodução
- referência de áudio de onda, erros
- referência para áudio wavefore, erros
- referência de áudio de onda, abrindo
- referência para áudio wavefore, abrindo
- referência de áudio de onda, fechamento
- referência para áudio wavefore, fechamento
- referência de áudio de onda, pitch
- referência para áudio wavefore, pitch
- referência de áudio de onda, volume
- referência para áudio wavefore, volume
- referência de áudio de onda, mensagens
- referência para áudio wavefore, mensagens
- referência de áudio de onda, posição atual
- referência para áudio wavefore, posição atual
- referência de áudio de onda, gravação
- referência para áudio wavefore, gravação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007458"
---
# <a name="waveform-audio-reference"></a><span data-ttu-id="1312e-135">Referência de áudio de onda</span><span class="sxs-lookup"><span data-stu-id="1312e-135">Waveform Audio Reference</span></span>

<span data-ttu-id="1312e-136">Esta seção lista as funções, as estruturas e as mensagens associadas ao áudio de onda, que estão documentados em [referência de multimídia](multimedia-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1312e-136">This section lists the functions, structures, and messages associated with waveform audio, which are documented under [Multimedia Reference](multimedia-reference.md).</span></span> <span data-ttu-id="1312e-137">Esses elementos são agrupados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="1312e-137">These elements are grouped as follows.</span></span>

## <a name="auxiliary-devices"></a><span data-ttu-id="1312e-138">Dispositivos auxiliares</span><span class="sxs-lookup"><span data-stu-id="1312e-138">Auxiliary Devices</span></span>

-   [<span data-ttu-id="1312e-139">**AUXCAPS**</span><span class="sxs-lookup"><span data-stu-id="1312e-139">**AUXCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [<span data-ttu-id="1312e-140">**auxGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="1312e-140">**auxGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [<span data-ttu-id="1312e-141">**auxGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="1312e-141">**auxGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [<span data-ttu-id="1312e-142">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="1312e-142">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [<span data-ttu-id="1312e-143">**auxOutMessage**</span><span class="sxs-lookup"><span data-stu-id="1312e-143">**auxOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [<span data-ttu-id="1312e-144">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="1312e-144">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a><span data-ttu-id="1312e-145">Reprodução fácil</span><span class="sxs-lookup"><span data-stu-id="1312e-145">Easy Playback</span></span>

-   <span data-ttu-id="1312e-146">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1312e-146">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>
-   <span data-ttu-id="1312e-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1312e-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>

## <a name="errors"></a><span data-ttu-id="1312e-148">Errors</span><span class="sxs-lookup"><span data-stu-id="1312e-148">Errors</span></span>

-   [<span data-ttu-id="1312e-149">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="1312e-149">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [<span data-ttu-id="1312e-150">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="1312e-150">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a><span data-ttu-id="1312e-151">Abrindo e fechando</span><span class="sxs-lookup"><span data-stu-id="1312e-151">Opening and Closing</span></span>

-   [<span data-ttu-id="1312e-152">**PCMWAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="1312e-152">**PCMWAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [<span data-ttu-id="1312e-153">**MM \_ de \_ fechamento de Wim**</span><span class="sxs-lookup"><span data-stu-id="1312e-153">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md)
-   [<span data-ttu-id="1312e-154">**Wim de MM \_ \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="1312e-154">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)
-   [<span data-ttu-id="1312e-155">**MM \_ wom \_ fechar**</span><span class="sxs-lookup"><span data-stu-id="1312e-155">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md)
-   [<span data-ttu-id="1312e-156">**MM \_ wom \_ abertos**</span><span class="sxs-lookup"><span data-stu-id="1312e-156">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)
-   [<span data-ttu-id="1312e-157">**WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="1312e-157">**WAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [<span data-ttu-id="1312e-158">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="1312e-158">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [<span data-ttu-id="1312e-159">**waveInClose**</span><span class="sxs-lookup"><span data-stu-id="1312e-159">**waveInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   <span data-ttu-id="1312e-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1312e-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span></span>
-   [<span data-ttu-id="1312e-161">**waveInOpen**</span><span class="sxs-lookup"><span data-stu-id="1312e-161">**waveInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [<span data-ttu-id="1312e-162">**waveOutClose**</span><span class="sxs-lookup"><span data-stu-id="1312e-162">**waveOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   <span data-ttu-id="1312e-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1312e-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span></span>
-   [<span data-ttu-id="1312e-164">**waveOutOpen**</span><span class="sxs-lookup"><span data-stu-id="1312e-164">**waveOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [<span data-ttu-id="1312e-165">**\_fechar wim**</span><span class="sxs-lookup"><span data-stu-id="1312e-165">**WIM\_CLOSE**</span></span>](wim-close.md)
-   [<span data-ttu-id="1312e-166">**WIM \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="1312e-166">**WIM\_OPEN**</span></span>](wim-open.md)
-   [<span data-ttu-id="1312e-167">**WOM \_ fechar**</span><span class="sxs-lookup"><span data-stu-id="1312e-167">**WOM\_CLOSE**</span></span>](wom-close.md)
-   [<span data-ttu-id="1312e-168">**WOM \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="1312e-168">**WOM\_OPEN**</span></span>](wom-open.md)

## <a name="pitch"></a><span data-ttu-id="1312e-169">Densidade</span><span class="sxs-lookup"><span data-stu-id="1312e-169">Pitch</span></span>

-   [<span data-ttu-id="1312e-170">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="1312e-170">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [<span data-ttu-id="1312e-171">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="1312e-171">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a><span data-ttu-id="1312e-172">Taxa de reprodução</span><span class="sxs-lookup"><span data-stu-id="1312e-172">Playback Rate</span></span>

-   [<span data-ttu-id="1312e-173">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="1312e-173">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [<span data-ttu-id="1312e-174">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="1312e-174">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a><span data-ttu-id="1312e-175">Progresso da reprodução</span><span class="sxs-lookup"><span data-stu-id="1312e-175">Playback Progress</span></span>

-   [<span data-ttu-id="1312e-176">**MM \_ wom \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="1312e-176">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="1312e-177">**waveOutBreakLoop**</span><span class="sxs-lookup"><span data-stu-id="1312e-177">**waveOutBreakLoop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [<span data-ttu-id="1312e-178">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="1312e-178">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [<span data-ttu-id="1312e-179">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="1312e-179">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [<span data-ttu-id="1312e-180">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="1312e-180">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [<span data-ttu-id="1312e-181">**WOM \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="1312e-181">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="playing"></a><span data-ttu-id="1312e-182">Reproduzindo</span><span class="sxs-lookup"><span data-stu-id="1312e-182">Playing</span></span>

-   [<span data-ttu-id="1312e-183">**MM \_ wom \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="1312e-183">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="1312e-184">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="1312e-184">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [<span data-ttu-id="1312e-185">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="1312e-185">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [<span data-ttu-id="1312e-186">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="1312e-186">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [<span data-ttu-id="1312e-187">**waveOutWrite**</span><span class="sxs-lookup"><span data-stu-id="1312e-187">**waveOutWrite**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [<span data-ttu-id="1312e-188">**WOM \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="1312e-188">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="querying-a-device"></a><span data-ttu-id="1312e-189">Consultando um dispositivo</span><span class="sxs-lookup"><span data-stu-id="1312e-189">Querying a Device</span></span>

-   [<span data-ttu-id="1312e-190">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="1312e-190">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [<span data-ttu-id="1312e-191">**waveInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="1312e-191">**waveInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [<span data-ttu-id="1312e-192">**waveInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="1312e-192">**waveInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [<span data-ttu-id="1312e-193">**WAVEOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="1312e-193">**WAVEOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [<span data-ttu-id="1312e-194">**waveOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="1312e-194">**waveOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [<span data-ttu-id="1312e-195">**waveOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="1312e-195">**waveOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a><span data-ttu-id="1312e-196">Gravação</span><span class="sxs-lookup"><span data-stu-id="1312e-196">Recording</span></span>

-   [<span data-ttu-id="1312e-197">**\_dados wim \_ mm**</span><span class="sxs-lookup"><span data-stu-id="1312e-197">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)
-   [<span data-ttu-id="1312e-198">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="1312e-198">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [<span data-ttu-id="1312e-199">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="1312e-199">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [<span data-ttu-id="1312e-200">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="1312e-200">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [<span data-ttu-id="1312e-201">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="1312e-201">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [<span data-ttu-id="1312e-202">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="1312e-202">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [<span data-ttu-id="1312e-203">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="1312e-203">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [<span data-ttu-id="1312e-204">**\_dados wim**</span><span class="sxs-lookup"><span data-stu-id="1312e-204">**WIM\_DATA**</span></span>](wim-data.md)

## <a name="retrieving-device-identifiers"></a><span data-ttu-id="1312e-205">Recuperando identificadores de dispositivo</span><span class="sxs-lookup"><span data-stu-id="1312e-205">Retrieving Device Identifiers</span></span>

-   [<span data-ttu-id="1312e-206">**waveInGetID**</span><span class="sxs-lookup"><span data-stu-id="1312e-206">**waveInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [<span data-ttu-id="1312e-207">**waveOutGetID**</span><span class="sxs-lookup"><span data-stu-id="1312e-207">**waveOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a><span data-ttu-id="1312e-208">Recuperando a posição atual</span><span class="sxs-lookup"><span data-stu-id="1312e-208">Retrieving the Current Position</span></span>

-   [<span data-ttu-id="1312e-209">**waveInGetPosition**</span><span class="sxs-lookup"><span data-stu-id="1312e-209">**waveInGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [<span data-ttu-id="1312e-210">**waveOutGetPosition**</span><span class="sxs-lookup"><span data-stu-id="1312e-210">**waveOutGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a><span data-ttu-id="1312e-211">Enviando mensagens personalizadas</span><span class="sxs-lookup"><span data-stu-id="1312e-211">Sending Custom Messages</span></span>

-   [<span data-ttu-id="1312e-212">**waveInMessage**</span><span class="sxs-lookup"><span data-stu-id="1312e-212">**waveInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [<span data-ttu-id="1312e-213">**waveOutMessage**</span><span class="sxs-lookup"><span data-stu-id="1312e-213">**waveOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a><span data-ttu-id="1312e-214">Volume</span><span class="sxs-lookup"><span data-stu-id="1312e-214">Volume</span></span>

-   [<span data-ttu-id="1312e-215">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="1312e-215">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [<span data-ttu-id="1312e-216">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="1312e-216">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a><span data-ttu-id="1312e-217">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1312e-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1312e-218">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="1312e-218">Waveform Audio</span></span>](waveform-audio.md)
</dt> </dl>

 

 
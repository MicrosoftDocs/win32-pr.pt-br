---
title: comando Set
description: O comando Set estabelece configurações de controle para o dispositivo. CD de áudio, Digital-Video, MIDI Sequencer, VCR, VIDEODISC, vídeo-Overlay e Wave-Audio Devices reconhecem esse comando.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- definir o comando multimídia do Windows
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "105770156"
---
# <a name="set-command"></a><span data-ttu-id="6350a-105">comando Set</span><span class="sxs-lookup"><span data-stu-id="6350a-105">set command</span></span>

> [!NOTE]
> <span data-ttu-id="6350a-106">Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.</span><span class="sxs-lookup"><span data-stu-id="6350a-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="6350a-107">Neste documento, há referências à palavra ' escravo '.</span><span class="sxs-lookup"><span data-stu-id="6350a-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="6350a-108">O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.</span><span class="sxs-lookup"><span data-stu-id="6350a-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="6350a-109">Essa palavra-chave é usada, pois é atualmente a palavra usada nos comandos.</span><span class="sxs-lookup"><span data-stu-id="6350a-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="6350a-110">Para fins de consistência, este documento contém esta palavra.</span><span class="sxs-lookup"><span data-stu-id="6350a-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="6350a-111">Quando esta palavra for alterada nos comandos, corrigiremos este documento para estar em alinhamento.</span><span class="sxs-lookup"><span data-stu-id="6350a-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>


<span data-ttu-id="6350a-112">O comando Set estabelece configurações de controle para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6350a-112">The set command establishes control settings for the device.</span></span> <span data-ttu-id="6350a-113">CD de áudio, Digital-Video, MIDI Sequencer, VCR, VIDEODISC, vídeo-Overlay e Wave-Audio Devices reconhecem esse comando.</span><span class="sxs-lookup"><span data-stu-id="6350a-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="6350a-114">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6350a-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="6350a-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6350a-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6350a-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6350a-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6350a-117">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="6350a-117">Identifier of an MCI device.</span></span> <span data-ttu-id="6350a-118">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="6350a-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6350a-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span><span class="sxs-lookup"><span data-stu-id="6350a-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span></span>
</dt> <dd>

<span data-ttu-id="6350a-120">Sinalizador para estabelecer as configurações de controle.</span><span class="sxs-lookup"><span data-stu-id="6350a-120">Flag for establishing control settings.</span></span> <span data-ttu-id="6350a-121">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **set** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="6350a-121">The following table lists device types that recognize the **set** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6350a-122">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6350a-122">Device Type</span></span></th>
<th><span data-ttu-id="6350a-123">Sinalizadores de comando</span><span class="sxs-lookup"><span data-stu-id="6350a-123">Command Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6350a-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="6350a-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="6350a-125">áudio desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-125">audio all off</span></span></li>
<li><span data-ttu-id="6350a-126">áudio tudo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-126">audio all on</span></span></li>
<li><span data-ttu-id="6350a-127">áudio restante</span><span class="sxs-lookup"><span data-stu-id="6350a-127">audio left off</span></span></li>
<li><span data-ttu-id="6350a-128">áudio restante em</span><span class="sxs-lookup"><span data-stu-id="6350a-128">audio left on</span></span></li>
<li><span data-ttu-id="6350a-129">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-129">audio right off</span></span></li>
<li><span data-ttu-id="6350a-130">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-130">audio right on</span></span></li>
<li><span data-ttu-id="6350a-131">porta fechada</span><span class="sxs-lookup"><span data-stu-id="6350a-131">door closed</span></span></li>
<li><span data-ttu-id="6350a-132">porta aberta</span><span class="sxs-lookup"><span data-stu-id="6350a-132">door open</span></span></li>
<li><span data-ttu-id="6350a-133">milissegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-133">time format milliseconds</span></span></li>
<li><span data-ttu-id="6350a-134">meio do formato de hora MSF</span><span class="sxs-lookup"><span data-stu-id="6350a-134">time format msf</span></span></li>
<li><span data-ttu-id="6350a-135">tmsf de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-135">time format tmsf</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-136">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="6350a-136">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="6350a-137">áudio desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-137">audio all off</span></span></li>
<li><span data-ttu-id="6350a-138">áudio tudo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-138">audio all on</span></span></li>
<li><span data-ttu-id="6350a-139">áudio restante</span><span class="sxs-lookup"><span data-stu-id="6350a-139">audio left off</span></span></li>
<li><span data-ttu-id="6350a-140">áudio restante em</span><span class="sxs-lookup"><span data-stu-id="6350a-140">audio left on</span></span></li>
<li><span data-ttu-id="6350a-141">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-141">audio right off</span></span></li>
<li><span data-ttu-id="6350a-142">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-142">audio right on</span></span></li>
<li><span data-ttu-id="6350a-143">porta fechada</span><span class="sxs-lookup"><span data-stu-id="6350a-143">door closed</span></span></li>
<li><span data-ttu-id="6350a-144">porta aberta</span><span class="sxs-lookup"><span data-stu-id="6350a-144">door open</span></span></li>
<li><span data-ttu-id="6350a-145"><em>formato</em> de formato de arquivo</span><span class="sxs-lookup"><span data-stu-id="6350a-145">file format <em>format</em></span></span></li>
<li><span data-ttu-id="6350a-146">buscar exatamente em</span><span class="sxs-lookup"><span data-stu-id="6350a-146">seek exactly on</span></span></li>
<li><span data-ttu-id="6350a-147">busca exata</span><span class="sxs-lookup"><span data-stu-id="6350a-147">seek exactly off</span></span></li>
<li><span data-ttu-id="6350a-148"><em>fator</em> de velocidade</span><span class="sxs-lookup"><span data-stu-id="6350a-148">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="6350a-149"><em>formato</em> de formato de arquivo ainda</span><span class="sxs-lookup"><span data-stu-id="6350a-149">still file format <em>format</em></span></span></li>
<li><span data-ttu-id="6350a-150">quadros de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-150">time format frames</span></span></li>
<li><span data-ttu-id="6350a-151">milissegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-151">time format milliseconds</span></span></li>
<li><span data-ttu-id="6350a-152">vídeo desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-152">video off</span></span></li>
<li><span data-ttu-id="6350a-153">vídeo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-153">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-154">overlay</span><span class="sxs-lookup"><span data-stu-id="6350a-154">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="6350a-155">áudio desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-155">audio all off</span></span></li>
<li><span data-ttu-id="6350a-156">áudio tudo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-156">audio all on</span></span></li>
<li><span data-ttu-id="6350a-157">áudio restante</span><span class="sxs-lookup"><span data-stu-id="6350a-157">audio left off</span></span></li>
<li><span data-ttu-id="6350a-158">áudio restante em</span><span class="sxs-lookup"><span data-stu-id="6350a-158">audio left on</span></span></li>
<li><span data-ttu-id="6350a-159">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-159">audio right off</span></span></li>
<li><span data-ttu-id="6350a-160">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-160">audio right on</span></span></li>
<li><span data-ttu-id="6350a-161">porta fechada</span><span class="sxs-lookup"><span data-stu-id="6350a-161">door closed</span></span></li>
<li><span data-ttu-id="6350a-162">porta aberta</span><span class="sxs-lookup"><span data-stu-id="6350a-162">door open</span></span></li>
<li><span data-ttu-id="6350a-163">vídeo desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-163">video off</span></span></li>
<li><span data-ttu-id="6350a-164">vídeo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-164">video on</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-165">sequenciador</span><span class="sxs-lookup"><span data-stu-id="6350a-165">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="6350a-166">áudio desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-166">audio all off</span></span></li>
<li><span data-ttu-id="6350a-167">áudio tudo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-167">audio all on</span></span></li>
<li><span data-ttu-id="6350a-168">áudio restante</span><span class="sxs-lookup"><span data-stu-id="6350a-168">audio left off</span></span></li>
<li><span data-ttu-id="6350a-169">áudio restante em</span><span class="sxs-lookup"><span data-stu-id="6350a-169">audio left on</span></span></li>
<li><span data-ttu-id="6350a-170">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-170">audio right off</span></span></li>
<li><span data-ttu-id="6350a-171">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-171">audio right on</span></span></li>
<li><span data-ttu-id="6350a-172">porta fechada</span><span class="sxs-lookup"><span data-stu-id="6350a-172">door closed</span></span></li>
<li><span data-ttu-id="6350a-173">porta aberta</span><span class="sxs-lookup"><span data-stu-id="6350a-173">door open</span></span></li>
<li><span data-ttu-id="6350a-174">MIDI mestre</span><span class="sxs-lookup"><span data-stu-id="6350a-174">master MIDI</span></span></li>
<li><span data-ttu-id="6350a-175">Mestre nenhum</span><span class="sxs-lookup"><span data-stu-id="6350a-175">master none</span></span></li>
<li><span data-ttu-id="6350a-176">Mestre SMPTE</span><span class="sxs-lookup"><span data-stu-id="6350a-176">master SMPTE</span></span></li>
<li><span data-ttu-id="6350a-177"><em>tempo</em> de deslocamento</span><span class="sxs-lookup"><span data-stu-id="6350a-177">offset <em>time</em></span></span></li>
<li><span data-ttu-id="6350a-178">mapeador de porta</span><span class="sxs-lookup"><span data-stu-id="6350a-178">port mapper</span></span></li>
<li><span data-ttu-id="6350a-179">porta nenhum</span><span class="sxs-lookup"><span data-stu-id="6350a-179">port none</span></span></li>
<li><span data-ttu-id="6350a-180"><em>port_number</em> de porta</span><span class="sxs-lookup"><span data-stu-id="6350a-180">port <em>port_number</em></span></span></li>
<li><span data-ttu-id="6350a-181">arquivo subordinado</span><span class="sxs-lookup"><span data-stu-id="6350a-181">slave file</span></span></li>
<li><span data-ttu-id="6350a-182">MIDI escravo</span><span class="sxs-lookup"><span data-stu-id="6350a-182">slave MIDI</span></span></li>
<li><span data-ttu-id="6350a-183">nenhum subordinado</span><span class="sxs-lookup"><span data-stu-id="6350a-183">slave none</span></span></li>
<li><span data-ttu-id="6350a-184">SMPTE-escravo</span><span class="sxs-lookup"><span data-stu-id="6350a-184">slave SMPTE</span></span></li>
<li><span data-ttu-id="6350a-185">tempo <em>tempo_value</em></span><span class="sxs-lookup"><span data-stu-id="6350a-185">tempo <em>tempo_value</em></span></span></li>
<li><span data-ttu-id="6350a-186">milissegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-186">time format milliseconds</span></span></li>
<li><span data-ttu-id="6350a-187">formato de hora SMPTE <em>FPS</em></span><span class="sxs-lookup"><span data-stu-id="6350a-187">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="6350a-188">drop de formato de hora SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="6350a-188">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="6350a-189">ponteiro de música de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-189">time format song pointer</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-190"><strong>videocassete</strong></span><span class="sxs-lookup"><span data-stu-id="6350a-190"><strong>vcr</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="6350a-191">montar registro em</span><span class="sxs-lookup"><span data-stu-id="6350a-191">assemble record on</span></span></li>
<li><span data-ttu-id="6350a-192">montar registro</span><span class="sxs-lookup"><span data-stu-id="6350a-192">assemble record off</span></span></li>
<li><span data-ttu-id="6350a-193">áudio desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-193">audio all off</span></span></li>
<li><span data-ttu-id="6350a-194">áudio tudo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-194">audio all on</span></span></li>
<li><span data-ttu-id="6350a-195">áudio restante</span><span class="sxs-lookup"><span data-stu-id="6350a-195">audio left off</span></span></li>
<li><span data-ttu-id="6350a-196">áudio restante em</span><span class="sxs-lookup"><span data-stu-id="6350a-196">audio left on</span></span></li>
<li><span data-ttu-id="6350a-197">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-197">audio right off</span></span></li>
<li><span data-ttu-id="6350a-198">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-198">audio right on</span></span></li>
<li><span data-ttu-id="6350a-199"><em>hora</em> do relógio</span><span class="sxs-lookup"><span data-stu-id="6350a-199">clock <em>time</em></span></span></li>
<li><span data-ttu-id="6350a-200">formato do contador</span><span class="sxs-lookup"><span data-stu-id="6350a-200">counter format</span></span></li>
<li><span data-ttu-id="6350a-201"><em>valor</em> do contador</span><span class="sxs-lookup"><span data-stu-id="6350a-201">counter <em>value</em></span></span></li>
<li><span data-ttu-id="6350a-202">porta fechada</span><span class="sxs-lookup"><span data-stu-id="6350a-202">door closed</span></span></li>
<li><span data-ttu-id="6350a-203">porta aberta</span><span class="sxs-lookup"><span data-stu-id="6350a-203">door open</span></span></li>
<li><span data-ttu-id="6350a-204">contador de índice</span><span class="sxs-lookup"><span data-stu-id="6350a-204">index counter</span></span></li>
<li><span data-ttu-id="6350a-205">data do índice</span><span class="sxs-lookup"><span data-stu-id="6350a-205">index date</span></span></li>
<li><span data-ttu-id="6350a-206">hora do índice</span><span class="sxs-lookup"><span data-stu-id="6350a-206">index time</span></span></li>
<li><span data-ttu-id="6350a-207">hora do índice</span><span class="sxs-lookup"><span data-stu-id="6350a-207">index time</span></span></li>
<li><span data-ttu-id="6350a-208"><em>duração</em> de CodeLength</span><span class="sxs-lookup"><span data-stu-id="6350a-208">codelength <em>duration</em></span></span></li>
<li><span data-ttu-id="6350a-209"><em>tempo limite</em> de pausa</span><span class="sxs-lookup"><span data-stu-id="6350a-209">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="6350a-210">duração do registro-</span><span class="sxs-lookup"><span data-stu-id="6350a-210">postroll duration -</span></span></li>
<li><span data-ttu-id="6350a-211"><em>duration</em></span><span class="sxs-lookup"><span data-stu-id="6350a-211"><em>duration</em></span></span></li>
<li><span data-ttu-id="6350a-212">ligar</span><span class="sxs-lookup"><span data-stu-id="6350a-212">power on</span></span></li>
<li><span data-ttu-id="6350a-213">desligar</span><span class="sxs-lookup"><span data-stu-id="6350a-213">power off</span></span></li>
<li><span data-ttu-id="6350a-214"><em>duração</em> da duração da preversão</span><span class="sxs-lookup"><span data-stu-id="6350a-214">preroll duration <em>duration</em></span></span></li>
<li><span data-ttu-id="6350a-215">formato de registro SP</span><span class="sxs-lookup"><span data-stu-id="6350a-215">record format SP</span></span></li>
<li><span data-ttu-id="6350a-216">formato de registro LP</span><span class="sxs-lookup"><span data-stu-id="6350a-216">record format LP</span></span></li>
<li><span data-ttu-id="6350a-217">formato de registro EP</span><span class="sxs-lookup"><span data-stu-id="6350a-217">record format EP</span></span></li>
<li><span data-ttu-id="6350a-218"><em>fator</em> de velocidade</span><span class="sxs-lookup"><span data-stu-id="6350a-218">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="6350a-219">quadros de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-219">time format frames</span></span></li>
<li><span data-ttu-id="6350a-220">HMS de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-220">time format hms</span></span></li>
<li><span data-ttu-id="6350a-221">milissegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-221">time format milliseconds</span></span></li>
<li><span data-ttu-id="6350a-222">meio do formato de hora MSF</span><span class="sxs-lookup"><span data-stu-id="6350a-222">time format msf</span></span></li>
<li><span data-ttu-id="6350a-223">formato de hora SMPTE <em>FPS</em></span><span class="sxs-lookup"><span data-stu-id="6350a-223">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="6350a-224">drop de formato de hora SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="6350a-224">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="6350a-225">tmsf de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-225">time format tmsf</span></span></li>
<li><span data-ttu-id="6350a-226">contador de modo de tempo</span><span class="sxs-lookup"><span data-stu-id="6350a-226">time mode counter</span></span></li>
<li><span data-ttu-id="6350a-227">detecção de modo de tempo</span><span class="sxs-lookup"><span data-stu-id="6350a-227">time mode detect</span></span></li>
<li><span data-ttu-id="6350a-228">tempo de vida de modo de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-228">time mode timecode</span></span></li>
<li><span data-ttu-id="6350a-229">acompanhamento de mais</span><span class="sxs-lookup"><span data-stu-id="6350a-229">tracking plus</span></span></li>
<li><span data-ttu-id="6350a-230">menos controle</span><span class="sxs-lookup"><span data-stu-id="6350a-230">tracking minus</span></span></li>
<li><span data-ttu-id="6350a-231">redefinição de rastreamento</span><span class="sxs-lookup"><span data-stu-id="6350a-231">tracking reset</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-232">videodisc</span><span class="sxs-lookup"><span data-stu-id="6350a-232">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="6350a-233">áudio desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-233">audio all off</span></span></li>
<li><span data-ttu-id="6350a-234">áudio tudo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-234">audio all on</span></span></li>
<li><span data-ttu-id="6350a-235">áudio restante</span><span class="sxs-lookup"><span data-stu-id="6350a-235">audio left off</span></span></li>
<li><span data-ttu-id="6350a-236">áudio restante em</span><span class="sxs-lookup"><span data-stu-id="6350a-236">audio left on</span></span></li>
<li><span data-ttu-id="6350a-237">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-237">audio right off</span></span></li>
<li><span data-ttu-id="6350a-238">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-238">audio right on</span></span></li>
<li><span data-ttu-id="6350a-239">porta fechada</span><span class="sxs-lookup"><span data-stu-id="6350a-239">door closed</span></span></li>
<li><span data-ttu-id="6350a-240">porta aberta</span><span class="sxs-lookup"><span data-stu-id="6350a-240">door open</span></span></li>
<li><span data-ttu-id="6350a-241">quadros de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-241">time format frames</span></span></li>
<li><span data-ttu-id="6350a-242">HMS de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-242">time format hms</span></span></li>
<li><span data-ttu-id="6350a-243">milissegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-243">time format milliseconds</span></span></li>
<li><span data-ttu-id="6350a-244">faixa de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-244">time format track</span></span></li>
<li><span data-ttu-id="6350a-245">vídeo desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-245">video off</span></span></li>
<li><span data-ttu-id="6350a-246">vídeo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-246">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-247">waveaudio</span><span class="sxs-lookup"><span data-stu-id="6350a-247">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="6350a-248"><em>inteiro</em> de alinhamento</span><span class="sxs-lookup"><span data-stu-id="6350a-248">alignment <em>integer</em></span></span></li>
<li><span data-ttu-id="6350a-249">qualquer entrada</span><span class="sxs-lookup"><span data-stu-id="6350a-249">any input</span></span></li>
<li><span data-ttu-id="6350a-250">qualquer saída</span><span class="sxs-lookup"><span data-stu-id="6350a-250">any output</span></span></li>
<li><span data-ttu-id="6350a-251">áudio desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-251">audio all off</span></span></li>
<li><span data-ttu-id="6350a-252">áudio tudo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-252">audio all on</span></span></li>
<li><span data-ttu-id="6350a-253">áudio restante</span><span class="sxs-lookup"><span data-stu-id="6350a-253">audio left off</span></span></li>
<li><span data-ttu-id="6350a-254">áudio restante em</span><span class="sxs-lookup"><span data-stu-id="6350a-254">audio left on</span></span></li>
<li><span data-ttu-id="6350a-255">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-255">audio right off</span></span></li>
<li><span data-ttu-id="6350a-256">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-256">audio right on</span></span></li>
<li><span data-ttu-id="6350a-257"><em>bit_count</em> BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="6350a-257">bitspersample <em>bit_count</em></span></span></li>
<li><span data-ttu-id="6350a-258"><em>byte_rate</em> bytespersec</span><span class="sxs-lookup"><span data-stu-id="6350a-258">bytespersec <em>byte_rate</em></span></span></li>
<li><span data-ttu-id="6350a-259">canais <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="6350a-259">channels <em>channel_count</em></span></span></li>
<li><span data-ttu-id="6350a-260">porta fechada</span><span class="sxs-lookup"><span data-stu-id="6350a-260">door closed</span></span></li>
<li><span data-ttu-id="6350a-261">porta aberta</span><span class="sxs-lookup"><span data-stu-id="6350a-261">door open</span></span></li>
<li><span data-ttu-id="6350a-262">formato PCM de marca</span><span class="sxs-lookup"><span data-stu-id="6350a-262">format tag pcm</span></span></li>
<li><span data-ttu-id="6350a-263">Formatar <em>marca</em> de marca</span><span class="sxs-lookup"><span data-stu-id="6350a-263">format tag <em>tag</em></span></span></li>
<li><span data-ttu-id="6350a-264"><em>número inteiro</em> de entrada</span><span class="sxs-lookup"><span data-stu-id="6350a-264">input <em>integer</em></span></span></li>
<li><span data-ttu-id="6350a-265"><em>número inteiro</em> de saída</span><span class="sxs-lookup"><span data-stu-id="6350a-265">output <em>integer</em></span></span></li>
<li><span data-ttu-id="6350a-266">samplespersec <em>inteiro</em></span><span class="sxs-lookup"><span data-stu-id="6350a-266">samplespersec <em>integer</em></span></span></li>
<li><span data-ttu-id="6350a-267">bytes de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-267">time format bytes</span></span></li>
<li><span data-ttu-id="6350a-268">milissegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-268">time format milliseconds</span></span></li>
<li><span data-ttu-id="6350a-269">exemplos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-269">time format samples</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6350a-270">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszSetting** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="6350a-270">The following table lists the flags that can be specified in the **lpszSetting** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6350a-271">Valor</span><span class="sxs-lookup"><span data-stu-id="6350a-271">Value</span></span></th>
<th><span data-ttu-id="6350a-272">Significado</span><span class="sxs-lookup"><span data-stu-id="6350a-272">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6350a-273"><em>inteiro</em> de alinhamento</span><span class="sxs-lookup"><span data-stu-id="6350a-273">alignment <em>integer</em></span></span></td>
<td><span data-ttu-id="6350a-274">Define o alinhamento dos blocos de dados em relação ao início dos dados passados para o dispositivo de forma de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="6350a-274">Sets the alignment of data blocks relative to the start of data passed to the waveform-audio device.</span></span> <span data-ttu-id="6350a-275">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="6350a-275">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-276">qualquer entrada</span><span class="sxs-lookup"><span data-stu-id="6350a-276">any input</span></span></td>
<td><span data-ttu-id="6350a-277">Use qualquer entrada que dê suporte ao formato atual durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="6350a-277">Use any input that supports the current format when recording.</span></span> <span data-ttu-id="6350a-278">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="6350a-278">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-279">qualquer saída</span><span class="sxs-lookup"><span data-stu-id="6350a-279">any output</span></span></td>
<td><span data-ttu-id="6350a-280">Use qualquer saída que dê suporte ao formato atual durante a execução.</span><span class="sxs-lookup"><span data-stu-id="6350a-280">Use any output that supports the current format when playing.</span></span> <span data-ttu-id="6350a-281">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="6350a-281">This is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-282">montar registro em</span><span class="sxs-lookup"><span data-stu-id="6350a-282">assemble record on</span></span> <br/> <span data-ttu-id="6350a-283">montar registro</span><span class="sxs-lookup"><span data-stu-id="6350a-283">assemble record off</span></span> <br/></td>
<td><span data-ttu-id="6350a-284">No modo de montagem, todas as faixas são registradas conforme definido pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6350a-284">In assemble mode, all tracks are recorded as defined by the device.</span></span> <span data-ttu-id="6350a-285">A maioria dos VCRs estão no modo de montagem por padrão.</span><span class="sxs-lookup"><span data-stu-id="6350a-285">Most VCRs are in assemble mode by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-286">áudio desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-286">audio all off</span></span> <br/> <span data-ttu-id="6350a-287">áudio tudo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-287">audio all on</span></span> <br/></td>
<td><span data-ttu-id="6350a-288">Desabilita ou habilita a saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="6350a-288">Disables or enables audio output.</span></span> <span data-ttu-id="6350a-289">Dispositivos de sobreposição de vídeo, o sequenciador MCISEQ e o dispositivo MCIWAVE de onda-áudio não dão suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6350a-289">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-290">áudio restante</span><span class="sxs-lookup"><span data-stu-id="6350a-290">audio left off</span></span> <br/> <span data-ttu-id="6350a-291">áudio restante em</span><span class="sxs-lookup"><span data-stu-id="6350a-291">audio left on</span></span> <br/> <span data-ttu-id="6350a-292">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-292">audio right off</span></span> <br/> <span data-ttu-id="6350a-293">áudio à direita</span><span class="sxs-lookup"><span data-stu-id="6350a-293">audio right on</span></span> <br/></td>
<td><span data-ttu-id="6350a-294">Desabilita ou habilita a saída para o canal de áudio à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="6350a-294">Disables or enables output to either the left or the right audio channel.</span></span> <span data-ttu-id="6350a-295">Dispositivos de sobreposição de vídeo, o sequenciador MCISEQ e o dispositivo MCIWAVE de onda-áudio não dão suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6350a-295">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-296"><em>bit_count</em> BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="6350a-296">bitspersample <em>bit_count</em></span></span></td>
<td><span data-ttu-id="6350a-297">Define o número de bits por amostra do PCM (modulação de código de pulso) reproduzido ou registrado.</span><span class="sxs-lookup"><span data-stu-id="6350a-297">Sets the number of bits per PCM (Pulse Code Modulation) sample played or recorded.</span></span> <span data-ttu-id="6350a-298">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="6350a-298">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-299"><em>byte_rate</em> bytespersec</span><span class="sxs-lookup"><span data-stu-id="6350a-299">bytespersec <em>byte_rate</em></span></span></td>
<td><span data-ttu-id="6350a-300">Define o número médio de bytes por segundo reproduzidos ou registrados.</span><span class="sxs-lookup"><span data-stu-id="6350a-300">Sets the average number of bytes per second played or recorded.</span></span> <span data-ttu-id="6350a-301">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="6350a-301">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-302">canais <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="6350a-302">channels <em>channel_count</em></span></span></td>
<td><span data-ttu-id="6350a-303">Define os canais para reprodução e gravação.</span><span class="sxs-lookup"><span data-stu-id="6350a-303">Sets the channels for playing and recording.</span></span> <span data-ttu-id="6350a-304">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="6350a-304">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-305"><em>hora</em> do relógio</span><span class="sxs-lookup"><span data-stu-id="6350a-305">clock <em>time</em></span></span></td>
<td><span data-ttu-id="6350a-306">Define a hora no relógio externo para a <em>hora.</em></span><span class="sxs-lookup"><span data-stu-id="6350a-306">Sets time on the external clock to <em>time.</em></span></span> <span data-ttu-id="6350a-307">O formato é especificado como um inteiro não assinado longo.</span><span class="sxs-lookup"><span data-stu-id="6350a-307">The format is specified as a long unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-308">formato do contador</span><span class="sxs-lookup"><span data-stu-id="6350a-308">counter format</span></span></td>
<td><span data-ttu-id="6350a-309">Defina o formato de hora para o contador, conforme retornado pelo contador de <a href="status.md">status</a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="6350a-309">Set the time format for the counter, as returned by <a href="status.md">status</a> &quot;counter&quot;.</span></span> <span data-ttu-id="6350a-310">Para obter informações sobre os tipos aplicáveis, consulte o comando <strong>set</strong> &quot; Time Format &quot; .</span><span class="sxs-lookup"><span data-stu-id="6350a-310">For information about applicable types, see the <strong>set</strong> &quot;time format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-311"><em>valor</em> do contador</span><span class="sxs-lookup"><span data-stu-id="6350a-311">counter <em>value</em></span></span></td>
<td><span data-ttu-id="6350a-312">Define o contador de VCR para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="6350a-312">Sets the VCR counter to the specified value.</span></span> <span data-ttu-id="6350a-313">O valor deve ser especificado no formato de contador atual.</span><span class="sxs-lookup"><span data-stu-id="6350a-313">The value must be specified in the current counter format.</span></span> <span data-ttu-id="6350a-314">Para obter mais informações, consulte o comando <strong>set</strong> &quot; Counter Format &quot; .</span><span class="sxs-lookup"><span data-stu-id="6350a-314">For more information, see the <strong>set</strong> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-315">porta fechada</span><span class="sxs-lookup"><span data-stu-id="6350a-315">door closed</span></span></td>
<td><span data-ttu-id="6350a-316">Cancela a bandeja e fecha a porta, se possível.</span><span class="sxs-lookup"><span data-stu-id="6350a-316">Retracts the tray and closes the door, if possible.</span></span> <span data-ttu-id="6350a-317">Para VCRs, o carrega a fita automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6350a-317">For VCRs, loads the tape automatically.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-318">porta aberta</span><span class="sxs-lookup"><span data-stu-id="6350a-318">door open</span></span></td>
<td><span data-ttu-id="6350a-319">Abre a porta e ejeta a bandeja ou fita, se possível.</span><span class="sxs-lookup"><span data-stu-id="6350a-319">Opens the door and ejects the tray or tape, if possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-320"><em>formato</em> de formato de arquivo</span><span class="sxs-lookup"><span data-stu-id="6350a-320">file format <em>format</em></span></span></td>
<td><span data-ttu-id="6350a-321">Especifica um formato de arquivo que é usado para <a href="save.md">salvar</a> ou <a href="capture.md">capturar</a> comandos.</span><span class="sxs-lookup"><span data-stu-id="6350a-321">Specifies a file format that is used for <a href="save.md">save</a> or <a href="capture.md">capture</a> commands.</span></span> <span data-ttu-id="6350a-322">Se omitido, isso pode padronizar para um formato definido por driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6350a-322">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="6350a-323">Se o formato de arquivo especificado estiver em conflito com o algoritmo e a qualidade selecionados no momento, eles serão alterados para os padrões para o formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6350a-323">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="6350a-324">Os seguintes formatos de arquivo são definidos:</span><span class="sxs-lookup"><span data-stu-id="6350a-324">The following file formats are defined:</span></span>
<ul>
<li><span data-ttu-id="6350a-325">AVI: especifica o formato AVI.</span><span class="sxs-lookup"><span data-stu-id="6350a-325">avi: Specifies AVI format.</span></span></li>
<li><span data-ttu-id="6350a-326">avss: especifica o formato AVSS.</span><span class="sxs-lookup"><span data-stu-id="6350a-326">avss: Specifies AVSS format.</span></span></li>
<li><span data-ttu-id="6350a-327">DIB: especifica o formato DIB.</span><span class="sxs-lookup"><span data-stu-id="6350a-327">dib: Specifies DIB format.</span></span></li>
<li><span data-ttu-id="6350a-328">JFIF: especifica o formato JFIF.</span><span class="sxs-lookup"><span data-stu-id="6350a-328">jfif: Specifies JFIF format.</span></span></li>
<li><span data-ttu-id="6350a-329">JPEG: especifica o formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="6350a-329">jpeg: Specifies JPEG format.</span></span></li>
<li><span data-ttu-id="6350a-330">MPEG: especifica o formato MPEG.</span><span class="sxs-lookup"><span data-stu-id="6350a-330">mpeg: Specifies MPEG format.</span></span></li>
<li><span data-ttu-id="6350a-331">rdib: especifica o formato de DIB RLE.</span><span class="sxs-lookup"><span data-stu-id="6350a-331">rdib: Specifies RLE DIB format.</span></span></li>
<li><span data-ttu-id="6350a-332">rjpeg: especifica o formato RJPEG.</span><span class="sxs-lookup"><span data-stu-id="6350a-332">rjpeg: Specifies RJPEG format.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-333">formato PCM de marca</span><span class="sxs-lookup"><span data-stu-id="6350a-333">format tag pcm</span></span></td>
<td><span data-ttu-id="6350a-334">Define o tipo de formato como PCM para reprodução e gravação.</span><span class="sxs-lookup"><span data-stu-id="6350a-334">Sets the format type to PCM for playing and recording.</span></span> <span data-ttu-id="6350a-335">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="6350a-335">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-336">Formatar <em>marca</em> de marca</span><span class="sxs-lookup"><span data-stu-id="6350a-336">format tag <em>tag</em></span></span></td>
<td><span data-ttu-id="6350a-337">Define o tipo de formato para reprodução e gravação.</span><span class="sxs-lookup"><span data-stu-id="6350a-337">Sets the format type for playing and recording.</span></span> <span data-ttu-id="6350a-338">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="6350a-338">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-339">índice de código de</span><span class="sxs-lookup"><span data-stu-id="6350a-339">index timecode</span></span> <br/> <span data-ttu-id="6350a-340">contador de índice</span><span class="sxs-lookup"><span data-stu-id="6350a-340">index counter</span></span> <br/> <span data-ttu-id="6350a-341">data do índice</span><span class="sxs-lookup"><span data-stu-id="6350a-341">index date</span></span> <br/> <span data-ttu-id="6350a-342">hora do índice</span><span class="sxs-lookup"><span data-stu-id="6350a-342">index time</span></span> <br/></td>
<td><span data-ttu-id="6350a-343">Define a tela de exibição atual no VCR.</span><span class="sxs-lookup"><span data-stu-id="6350a-343">Sets the current display screen on the VCR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-344"><em>número inteiro</em> de entrada</span><span class="sxs-lookup"><span data-stu-id="6350a-344">input <em>integer</em></span></span></td>
<td><span data-ttu-id="6350a-345">Define o canal de áudio usado como entrada.</span><span class="sxs-lookup"><span data-stu-id="6350a-345">Sets the audio channel used as the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-346"><em>duração</em> do comprimento</span><span class="sxs-lookup"><span data-stu-id="6350a-346">length <em>duration</em></span></span></td>
<td><span data-ttu-id="6350a-347">Define o comprimento especificado pelo usuário da fita no VCR.</span><span class="sxs-lookup"><span data-stu-id="6350a-347">Sets the user-specified length of the tape in the VCR.</span></span> <span data-ttu-id="6350a-348">Esse comprimento é retornado pelo comando <a href="status.md">status</a> &quot; length &quot; e é fornecido para compatibilidade com aplicativos que exigem esse comando para retornar um comprimento válido.</span><span class="sxs-lookup"><span data-stu-id="6350a-348">This length is returned by the <a href="status.md">status</a> &quot;length&quot; command and is provided for compatibility with applications that require this command to return a valid length.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-349">MIDI mestre</span><span class="sxs-lookup"><span data-stu-id="6350a-349">master midi</span></span></td>
<td><span data-ttu-id="6350a-350">Define o sequenciador MIDI como a origem da sincronização.</span><span class="sxs-lookup"><span data-stu-id="6350a-350">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="6350a-351">Os dados de sincronização são enviados no formato MIDI.</span><span class="sxs-lookup"><span data-stu-id="6350a-351">Synchronization data is sent in MIDI format.</span></span> <span data-ttu-id="6350a-352">O sequenciador MCISEQ não dá suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6350a-352">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-353">Mestre nenhum</span><span class="sxs-lookup"><span data-stu-id="6350a-353">master none</span></span></td>
<td><span data-ttu-id="6350a-354">Inibe o sequenciador MIDI de enviar dados de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6350a-354">Inhibits the MIDI sequencer from sending synchronization data.</span></span> <span data-ttu-id="6350a-355">O sequenciador MCISEQ não dá suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6350a-355">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-356">Mestre SMPTE</span><span class="sxs-lookup"><span data-stu-id="6350a-356">master smpte</span></span></td>
<td><span data-ttu-id="6350a-357">Define o sequenciador MIDI como a origem da sincronização.</span><span class="sxs-lookup"><span data-stu-id="6350a-357">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="6350a-358">Os dados de sincronização são enviados em formato SMPTE (sociedade de imagem e engenheiros de televisão).</span><span class="sxs-lookup"><span data-stu-id="6350a-358">Synchronization data is sent in SMPTE (Society of Motion Picture and Television Engineers) format.</span></span> <span data-ttu-id="6350a-359">O sequenciador MCISEQ não dá suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6350a-359">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-360"><em>tempo</em> de deslocamento</span><span class="sxs-lookup"><span data-stu-id="6350a-360">offset <em>time</em></span></span></td>
<td><span data-ttu-id="6350a-361">Define o <em>tempo</em>de deslocamento SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6350a-361">Sets the SMPTE offset <em>time</em>.</span></span> <span data-ttu-id="6350a-362">O deslocamento é a hora de início de uma sequência baseada em SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6350a-362">The offset is the beginning time of a SMPTE based sequence.</span></span> <span data-ttu-id="6350a-363">O <em>tempo</em> é expresso como <em>hh</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>, em que <em>hh</em> é hours, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames.</span><span class="sxs-lookup"><span data-stu-id="6350a-363">The <em>time</em> is expressed as <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-364"><em>número inteiro</em> de saída</span><span class="sxs-lookup"><span data-stu-id="6350a-364">output <em>integer</em></span></span></td>
<td><span data-ttu-id="6350a-365">Define o canal de áudio usado como a saída.</span><span class="sxs-lookup"><span data-stu-id="6350a-365">Sets the audio channel used as the output.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-366"><em>tempo limite</em> de pausa</span><span class="sxs-lookup"><span data-stu-id="6350a-366">pause <em>timeout</em></span></span></td>
<td><span data-ttu-id="6350a-367">Define a duração máxima, em milissegundos, de um comando de <a href="pause.md">pausa</a> .</span><span class="sxs-lookup"><span data-stu-id="6350a-367">Sets the maximum duration, in milliseconds, of a <a href="pause.md">pause</a> command.</span></span> <span data-ttu-id="6350a-368">Um valor de <em>tempo limite</em> igual a zero indica que nenhum tempo limite ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="6350a-368">A <em>timeout</em> value of zero indicates that no time-out will occur.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-369"><em>duração</em> da duração do registro</span><span class="sxs-lookup"><span data-stu-id="6350a-369">postroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="6350a-370">Define o comprimento, no formato de hora atual, necessário para <a href="stop.md">finalizar</a> o transporte de videocassete quando um comando Stop ou <strong>Pause</strong> é emitido.</span><span class="sxs-lookup"><span data-stu-id="6350a-370">Sets the length, in the current time format, needed to brake the VCR transport when a <a href="stop.md">stop</a> or <strong>pause</strong> command is issued.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-371">mapeador de porta</span><span class="sxs-lookup"><span data-stu-id="6350a-371">port mapper</span></span></td>
<td><span data-ttu-id="6350a-372">Define o mapeador de MIDI como a porta que recebe as mensagens de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6350a-372">Sets the MIDI mapper as the port receiving the MIDI messages.</span></span> <span data-ttu-id="6350a-373">Esse comando falhará se o mapeador de MIDI ou uma porta necessária estiver sendo usado por outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6350a-373">This command fails if the MIDI mapper or a port it needs is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-374">porta nenhum</span><span class="sxs-lookup"><span data-stu-id="6350a-374">port none</span></span></td>
<td><span data-ttu-id="6350a-375">Desabilita o envio de mensagens MIDI.</span><span class="sxs-lookup"><span data-stu-id="6350a-375">Disables the sending of MIDI messages.</span></span> <span data-ttu-id="6350a-376">Esse comando também fecha uma porta MIDI.</span><span class="sxs-lookup"><span data-stu-id="6350a-376">This command also closes a MIDI port.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-377"><em>port_number</em> de porta</span><span class="sxs-lookup"><span data-stu-id="6350a-377">port <em>port_number</em></span></span></td>
<td><span data-ttu-id="6350a-378">Define a porta MIDI que recebe as mensagens MIDI.</span><span class="sxs-lookup"><span data-stu-id="6350a-378">Sets the MIDI port receiving the MIDI messages.</span></span> <span data-ttu-id="6350a-379">Esse comando falhará se a porta que você está tentando abrir estiver sendo usada por outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6350a-379">This command fails if the port you are trying to open is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-380">ligar</span><span class="sxs-lookup"><span data-stu-id="6350a-380">power on</span></span> <br/> <span data-ttu-id="6350a-381">desligar</span><span class="sxs-lookup"><span data-stu-id="6350a-381">power off</span></span> <br/></td>
<td><span data-ttu-id="6350a-382">Define a energia do dispositivo como on ou off.</span><span class="sxs-lookup"><span data-stu-id="6350a-382">Sets the device power to on or off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-383"><em>duração</em> da duração da preversão</span><span class="sxs-lookup"><span data-stu-id="6350a-383">preroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="6350a-384">Define o comprimento, no formato de hora atual, necessário para estabilizar a saída de VCR.</span><span class="sxs-lookup"><span data-stu-id="6350a-384">Sets the length, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-385">formato de registro SP</span><span class="sxs-lookup"><span data-stu-id="6350a-385">record format SP</span></span> <br/> <span data-ttu-id="6350a-386">formato de registro LP</span><span class="sxs-lookup"><span data-stu-id="6350a-386">record format LP</span></span> <br/> <span data-ttu-id="6350a-387">formato de registro EP</span><span class="sxs-lookup"><span data-stu-id="6350a-387">record format EP</span></span> <br/></td>
<td><span data-ttu-id="6350a-388">Define o modo de gravação para o VCR para o SP para Play Standard, EP para reprodução estendida ou LP para reprodução longa.</span><span class="sxs-lookup"><span data-stu-id="6350a-388">Sets the recording mode for the VCR to SP for standard play, EP for extended play, or LP for long play.</span></span> <span data-ttu-id="6350a-389">Esses valores não se destinam a ser específicos de VHS.</span><span class="sxs-lookup"><span data-stu-id="6350a-389">These values are not intended to be VHS specific.</span></span> <span data-ttu-id="6350a-390">Eles são mapeados para quaisquer três modos apropriados com outros formatos de fita.</span><span class="sxs-lookup"><span data-stu-id="6350a-390">They map to any three appropriate modes with other tape formats.</span></span> <span data-ttu-id="6350a-391">Por exemplo, o SP é mapeado para a gravação mais rápida e de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="6350a-391">For example, SP maps to the fastest, highest quality recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-392">samplespersec <em>inteiro</em></span><span class="sxs-lookup"><span data-stu-id="6350a-392">samplespersec <em>integer</em></span></span></td>
<td><span data-ttu-id="6350a-393">Define a taxa de amostra para reprodução e gravação.</span><span class="sxs-lookup"><span data-stu-id="6350a-393">Sets the sample rate for playing and recording.</span></span> <span data-ttu-id="6350a-394">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="6350a-394">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-395">buscar exatamente em</span><span class="sxs-lookup"><span data-stu-id="6350a-395">seek exactly on</span></span><br/> <span data-ttu-id="6350a-396">busca exata</span><span class="sxs-lookup"><span data-stu-id="6350a-396">seek exactly off</span></span> <br/></td>
<td><span data-ttu-id="6350a-397">Seleciona um dos dois modos de busca.</span><span class="sxs-lookup"><span data-stu-id="6350a-397">Selects one of two seek modes.</span></span> <span data-ttu-id="6350a-398">Com &quot; o Seek exactly on &quot; , Seek sempre será movido para o quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="6350a-398">With &quot;seek exactly on&quot;, seek will always move to the frame specified.</span></span> <span data-ttu-id="6350a-399">Com &quot; Seek exactly off &quot; , Seek passará para o quadro-chave mais próximo antes do quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="6350a-399">With &quot;seek exactly off&quot;, seek will move to the closest key frame prior to the frame specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-400">arquivo subordinado</span><span class="sxs-lookup"><span data-stu-id="6350a-400">slave file</span></span></td>
<td><span data-ttu-id="6350a-401">Define o sequenciador MIDI para usar dados de arquivo como a origem da sincronização.</span><span class="sxs-lookup"><span data-stu-id="6350a-401">Sets the MIDI sequencer to use file data as the synchronization source.</span></span> <span data-ttu-id="6350a-402">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="6350a-402">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-403">MIDI escravo</span><span class="sxs-lookup"><span data-stu-id="6350a-403">slave midi</span></span></td>
<td><span data-ttu-id="6350a-404">Define o sequenciador MIDI para usar dados MIDI de entrada para a origem de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6350a-404">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="6350a-405">O Sequencer reconhece os dados de sincronização com o formato MIDI.</span><span class="sxs-lookup"><span data-stu-id="6350a-405">The sequencer recognizes synchronization data with the MIDI format.</span></span> <span data-ttu-id="6350a-406">O sequenciador MCISEQ não dá suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6350a-406">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-407">nenhum subordinado</span><span class="sxs-lookup"><span data-stu-id="6350a-407">slave none</span></span></td>
<td><span data-ttu-id="6350a-408">Define o sequenciador MIDI para ignorar a sincronização</span><span class="sxs-lookup"><span data-stu-id="6350a-408">Sets the MIDI sequencer to ignore synchronization</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-409">SMPTE-escravo</span><span class="sxs-lookup"><span data-stu-id="6350a-409">slave smpte</span></span></td>
<td><span data-ttu-id="6350a-410">Define o sequenciador MIDI para usar dados MIDI de entrada para a origem de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6350a-410">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="6350a-411">O Sequencer reconhece os dados de sincronização com o formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6350a-411">The sequencer recognizes synchronization data with the SMPTE format.</span></span> <span data-ttu-id="6350a-412">O sequenciador MCISEQ não dá suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6350a-412">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-413">fator de velocidade</span><span class="sxs-lookup"><span data-stu-id="6350a-413">speed factor</span></span></td>
<td><span data-ttu-id="6350a-414">Define a velocidade relativa de reprodução de áudio e vídeo do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6350a-414">Sets the relative speed of video and audio playback from the workspace.</span></span> <span data-ttu-id="6350a-415">Factor é a proporção entre a taxa de quadros nominal e a taxa de quadros desejada, em que a taxa de quadros nominal é designada como 1000.</span><span class="sxs-lookup"><span data-stu-id="6350a-415">Factor is the ratio between the nominal frame rate and the desired frame rate, where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="6350a-416">(Uma taxa de 500 é metade da velocidade normal, 2000 é duas vezes A velocidade normal e assim por diante.) Definir a velocidade como zero reproduz o vídeo o mais rápido possível sem descartar quadros e sem áudio.</span><span class="sxs-lookup"><span data-stu-id="6350a-416">(A rate of 500 is half normal speed, 2000 is twice normal speed, and so on.) Setting the speed to zero plays the video as fast as possible without dropping frames and without audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-417"><em>formato</em> de formato de arquivo ainda</span><span class="sxs-lookup"><span data-stu-id="6350a-417">still file format <em>format</em></span></span></td>
<td><span data-ttu-id="6350a-418">Especifica o formato de arquivo usado para comandos de captura.</span><span class="sxs-lookup"><span data-stu-id="6350a-418">Specifies the file format used for capture commands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-419">tempo tempo_value</span><span class="sxs-lookup"><span data-stu-id="6350a-419">tempo tempo_value</span></span></td>
<td><span data-ttu-id="6350a-420">Define o tempo da sequência de acordo com o formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="6350a-420">Sets the tempo of the sequence according to the current time format.</span></span> <span data-ttu-id="6350a-421">Para um arquivo baseado em PPQN, o tempo_value é interpretado como batidas por minuto.</span><span class="sxs-lookup"><span data-stu-id="6350a-421">For a PPQN-based file, the tempo_value is interpreted as beats per minute.</span></span> <span data-ttu-id="6350a-422">Para um arquivo baseado em SMPTE, o tempo_value é interpretado como quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="6350a-422">For a SMPTE-based file, the tempo_value is interpreted as frames per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-423">bytes de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-423">time format bytes</span></span></td>
<td><span data-ttu-id="6350a-424">Em um formato de arquivo PCM, define o formato de hora como bytes.</span><span class="sxs-lookup"><span data-stu-id="6350a-424">In a PCM file format, sets the time format to bytes.</span></span> <span data-ttu-id="6350a-425">Todas as informações de posição são especificadas como bytes após este comando.</span><span class="sxs-lookup"><span data-stu-id="6350a-425">All position information is specified as bytes following this command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-426">quadros de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-426">time format frames</span></span></td>
<td><span data-ttu-id="6350a-427">Define o formato de hora como quadros.</span><span class="sxs-lookup"><span data-stu-id="6350a-427">Sets the time format to frames.</span></span> <span data-ttu-id="6350a-428">Todos os comandos que usam valores de posição assumirão quadros.</span><span class="sxs-lookup"><span data-stu-id="6350a-428">All commands that use position values will assume frames.</span></span> <span data-ttu-id="6350a-429">Quando o dispositivo é aberto, quadros é o modo padrão.</span><span class="sxs-lookup"><span data-stu-id="6350a-429">When the device is opened, frames is the default mode.</span></span> <span data-ttu-id="6350a-430">Com suporte pelo videodiscs usando o formato CAV.</span><span class="sxs-lookup"><span data-stu-id="6350a-430">Supported by videodiscs using CAV format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-431">HMS de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-431">time format hms</span></span></td>
<td><span data-ttu-id="6350a-432">Define o formato de hora para horas, minutos e segundos.</span><span class="sxs-lookup"><span data-stu-id="6350a-432">Sets the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="6350a-433">Todos os comandos que usam valores de posição assumirão HMS.</span><span class="sxs-lookup"><span data-stu-id="6350a-433">All commands that use position values will assume HMS.</span></span> <span data-ttu-id="6350a-434">HMS é o formato padrão para CLV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="6350a-434">HMS is the default format for CLV videodiscs.</span></span> <span data-ttu-id="6350a-435">Especifique um valor de HMS como hh: mm: SS, em que HH é horas, mm é minutos e SS é segundos.</span><span class="sxs-lookup"><span data-stu-id="6350a-435">Specify an HMS value as hh:mm:ss, where hh is hours, mm is minutes, and ss is seconds.</span></span> <span data-ttu-id="6350a-436">Você pode omitir um campo se ele e todos os campos a seguir forem zero.</span><span class="sxs-lookup"><span data-stu-id="6350a-436">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="6350a-437">Por exemplo, 3, 3:0 e 3:0:0 são maneiras válidas de expressar 3 horas.</span><span class="sxs-lookup"><span data-stu-id="6350a-437">For example, 3, 3:0, and 3:0:0 are all valid ways to express 3 hours.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-438">milissegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-438">time format milliseconds</span></span></td>
<td><span data-ttu-id="6350a-439">Define o formato de hora como milissegundos.</span><span class="sxs-lookup"><span data-stu-id="6350a-439">Sets the time format to milliseconds.</span></span> <span data-ttu-id="6350a-440">Todos os comandos que usam valores de posição pressupõem milissegundos.</span><span class="sxs-lookup"><span data-stu-id="6350a-440">All commands that use position values will assume milliseconds.</span></span> <span data-ttu-id="6350a-441">Você pode abreviar milissegundos como &quot; MS &quot; .</span><span class="sxs-lookup"><span data-stu-id="6350a-441">You can abbreviate milliseconds as &quot;ms&quot;.</span></span> <span data-ttu-id="6350a-442">Para dispositivos do Sequencer, o arquivo de sequência define o formato padrão como PPQN ou SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6350a-442">For sequencer devices, the sequence file sets the default format to PPQN or SMPTE.</span></span> <span data-ttu-id="6350a-443">Os dispositivos de sobreposição de vídeo não dão suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6350a-443">Video-overlay devices do not support this flag.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-444">meio do formato de hora MSF</span><span class="sxs-lookup"><span data-stu-id="6350a-444">time format msf</span></span></td>
<td><span data-ttu-id="6350a-445">Define o formato de hora como minutos, segundos e quadros.</span><span class="sxs-lookup"><span data-stu-id="6350a-445">Sets the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="6350a-446">Todos os comandos que usam valores de posição assumirão o MSF (o formato padrão para áudio de CD).</span><span class="sxs-lookup"><span data-stu-id="6350a-446">All commands that use position values will assume MSF (the default format for CD audio).</span></span> <span data-ttu-id="6350a-447">Especifique um valor do MSF como mm: SS: FF, em que mm é minutos, SS é segundos e FF são quadros.</span><span class="sxs-lookup"><span data-stu-id="6350a-447">Specify an MSF value as mm:ss:ff, where mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="6350a-448">Você pode omitir um campo se ele e todos os campos a seguir forem zero.</span><span class="sxs-lookup"><span data-stu-id="6350a-448">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="6350a-449">Por exemplo, 3, 3:0 e 3:0:0 são maneiras válidas de expressar 3 minutos.</span><span class="sxs-lookup"><span data-stu-id="6350a-449">For example, 3, 3:0, and 3:0:0 are valid ways to express 3 minutes.</span></span><br/> <span data-ttu-id="6350a-450">Os campos do MSF têm os seguintes valores máximos:</span><span class="sxs-lookup"><span data-stu-id="6350a-450">The MSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="6350a-451">Minutos 99</span><span class="sxs-lookup"><span data-stu-id="6350a-451">Minutes 99</span></span></li>
<li><span data-ttu-id="6350a-452">Segundos de 59</span><span class="sxs-lookup"><span data-stu-id="6350a-452">Seconds 59</span></span></li>
<li><span data-ttu-id="6350a-453">Quadros 74</span><span class="sxs-lookup"><span data-stu-id="6350a-453">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-454">exemplos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-454">time format samples</span></span></td>
<td><span data-ttu-id="6350a-455">Define o formato de hora como exemplos.</span><span class="sxs-lookup"><span data-stu-id="6350a-455">Sets the time format to samples.</span></span> <span data-ttu-id="6350a-456">Todas as informações de posição são especificadas como exemplos após este comando.</span><span class="sxs-lookup"><span data-stu-id="6350a-456">All position information is specified as samples following this command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-457">formato de hora SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="6350a-457">time format smpte 24</span></span><br/> <span data-ttu-id="6350a-458">formato de hora SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="6350a-458">time format smpte 25</span></span><br/> <span data-ttu-id="6350a-459">formato de hora SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="6350a-459">time format smpte 30</span></span><br/></td>
<td><span data-ttu-id="6350a-460">Define o formato de hora como uma taxa de quadros SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6350a-460">Sets the time format to an SMPTE frame rate.</span></span> <span data-ttu-id="6350a-461">Para VCRs, define o formato de hora como hh: mm: SS: FF, em que os valores válidos são de 00:00:00:00 a 23:59:59: XX e XX é um valor menor do que os quadros por segundo, conforme especificado pelo número 24, 25 ou 30, conforme especificado no sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6350a-461">For VCRs, sets the time format to hh:mm:ss:ff, where the legal values are 00:00:00:00 through 23:59:59:xx, and xx is one less than the frames per second as specified by the number 24, 25, or 30 as specified in the flag.</span></span> <span data-ttu-id="6350a-462">Na entrada, dois-pontos (:) são necessários para separar os componentes.</span><span class="sxs-lookup"><span data-stu-id="6350a-462">On input, colons (:) are required to separate the components.</span></span> <span data-ttu-id="6350a-463">As unidades menos significativas podem ser omitidas se forem 00; por exemplo, 02:00 é o mesmo que 02:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="6350a-463">The least significant units can be omitted if they are 00; for example, 02:00 is the same as 02:00:00:00.</span></span> <span data-ttu-id="6350a-464">Todos os comandos que usam valores de posição assumirão o formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6350a-464">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="6350a-465">O arquivo de sequência define o formato padrão como PPQN ou SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6350a-465">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-466">drop de formato de hora SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="6350a-466">time format smpte 30 drop</span></span></td>
<td><span data-ttu-id="6350a-467">Define o formato de hora para a taxa de descarte de quadros SMPTE 30.</span><span class="sxs-lookup"><span data-stu-id="6350a-467">Sets the time format to SMPTE 30 drop frame rate.</span></span> <span data-ttu-id="6350a-468">Para VCRs, igual a SMPTE 30, exceto que determinadas posições de código de tempo são removidas do formato para que as posições de código de tempo registradas para cada quadro (na taxa de quadros NTSC de 29,97 fps) correspondam a tempo real (a 30 fps).</span><span class="sxs-lookup"><span data-stu-id="6350a-468">For VCRs, same as SMPTE 30, except that certain timecode positions are dropped from the format to have the recorded timecode positions for each frame (at the NTSC frame rate of 29.97 fps) correspond to real time (at 30 fps).</span></span> <span data-ttu-id="6350a-469">As posições de código de tempo que são descartadas são as seguintes: duas a cada minuto, no minuto, para os nove primeiros de cada dez minutos de conteúdo registrado.</span><span class="sxs-lookup"><span data-stu-id="6350a-469">Timecode positions that are dropped are as follows: two every minute, on the minute, for the first nine of every ten minutes of recorded content.</span></span> <span data-ttu-id="6350a-470">Por exemplo, às 01:04:59:29, a próxima posição do código de tempo seria 01:05:00:02, e não 01:05:00:00.</span><span class="sxs-lookup"><span data-stu-id="6350a-470">For example, at 01:04:59:29, the next timecode position would be 01:05:00:02, not 01:05:00:00.</span></span> <span data-ttu-id="6350a-471">Todos os comandos que usam valores de posição assumirão o formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6350a-471">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="6350a-472">O arquivo de sequência define o formato padrão como PPQN ou SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6350a-472">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-473">ponteiro de música de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-473">time format song pointer</span></span></td>
<td><span data-ttu-id="6350a-474">Define o formato de hora para o ponteiro de música (dezesseis observações).</span><span class="sxs-lookup"><span data-stu-id="6350a-474">Sets the time format to song pointer (sixteenth notes).</span></span> <span data-ttu-id="6350a-475">Todos os comandos que usam valores de posição assumirão unidades de ponteiro de música.</span><span class="sxs-lookup"><span data-stu-id="6350a-475">All commands that use position values will assume song pointer units.</span></span> <span data-ttu-id="6350a-476">Esse sinalizador só é válido para uma sequência de tipo de divisão PPQN.</span><span class="sxs-lookup"><span data-stu-id="6350a-476">This flag is valid only for a sequence of division type PPQN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-477">tmsf de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-477">time format tmsf</span></span></td>
<td><span data-ttu-id="6350a-478">Define o formato de hora para faixas, minutos, segundos e quadros.</span><span class="sxs-lookup"><span data-stu-id="6350a-478">Sets the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="6350a-479">Todos os comandos que usam valores de posição assumirão TMSF.</span><span class="sxs-lookup"><span data-stu-id="6350a-479">All commands that use position values will assume TMSF.</span></span> <span data-ttu-id="6350a-480">Especifique um valor de TMSF como TT: mm: SS: FF, em que TT é faixas, mm é minutos, SS é segundos e FF é quadros.</span><span class="sxs-lookup"><span data-stu-id="6350a-480">Specify a TMSF value as tt:mm:ss:ff, where tt is tracks, mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="6350a-481">Você pode omitir um campo se ele e todos os campos a seguir forem zero.</span><span class="sxs-lookup"><span data-stu-id="6350a-481">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="6350a-482">Por exemplo, 3, 3:0, 3:0:0 e 3:0:0:0 são maneiras válidas de expressar o Track 3.</span><span class="sxs-lookup"><span data-stu-id="6350a-482">For example, 3, 3:0, 3:0:0, and 3:0:0:0 are all valid ways to express track 3.</span></span> <br/> <span data-ttu-id="6350a-483">Os campos TMSF têm os seguintes valores máximos:</span><span class="sxs-lookup"><span data-stu-id="6350a-483">The TMSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="6350a-484">Faixas 99</span><span class="sxs-lookup"><span data-stu-id="6350a-484">Tracks 99</span></span></li>
<li><span data-ttu-id="6350a-485">Minutos 90</span><span class="sxs-lookup"><span data-stu-id="6350a-485">Minutes 90</span></span></li>
<li><span data-ttu-id="6350a-486">Segundos de 59</span><span class="sxs-lookup"><span data-stu-id="6350a-486">Seconds 59</span></span></li>
<li><span data-ttu-id="6350a-487">Quadros 74</span><span class="sxs-lookup"><span data-stu-id="6350a-487">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-488">faixa de formato de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-488">time format track</span></span></td>
<td><span data-ttu-id="6350a-489">Define o formato de posição como faixas.</span><span class="sxs-lookup"><span data-stu-id="6350a-489">Sets the position format to tracks.</span></span> <span data-ttu-id="6350a-490">Todos os comandos que usam valores de posição assumirão faixas.</span><span class="sxs-lookup"><span data-stu-id="6350a-490">All commands that use position values will assume tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-491">contador de modo de tempo</span><span class="sxs-lookup"><span data-stu-id="6350a-491">time mode counter</span></span></td>
<td><span data-ttu-id="6350a-492">Define o modo de informações de posição para usar os contadores de VCR.</span><span class="sxs-lookup"><span data-stu-id="6350a-492">Sets the position-information mode to use the VCR counters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-493">detecção de modo de tempo</span><span class="sxs-lookup"><span data-stu-id="6350a-493">time mode detect</span></span></td>
<td><span data-ttu-id="6350a-494">Define o modo de informações de posição com base na detecção de informações de código de Code na fita.</span><span class="sxs-lookup"><span data-stu-id="6350a-494">Sets the position information mode based on detection of timecode information on the tape.</span></span> <span data-ttu-id="6350a-495">Se as informações de código de tempo forem detectadas, o tipo de hora será definido como código de tempo &quot; &quot; ; caso contrário, o tipo de hora será definido como &quot; contador &quot; .</span><span class="sxs-lookup"><span data-stu-id="6350a-495">If timecode information is detected, the time type is set to &quot;timecode&quot;; otherwise, the time type is set to &quot;counter&quot;.</span></span> <span data-ttu-id="6350a-496">&quot;Detectar &quot; é um modo especial.</span><span class="sxs-lookup"><span data-stu-id="6350a-496">&quot;Detect&quot; is a special mode.</span></span> <span data-ttu-id="6350a-497">Sempre que o driver é aberto, uma nova fita é inserida ou o &quot; comando de modo de tempo &quot; é emitido, o driver verifica o modo de tempo atual disponível na fita e define o &quot; tipo &quot; de hora como um código de tempo &quot; &quot; ou &quot; contador &quot; .</span><span class="sxs-lookup"><span data-stu-id="6350a-497">Whenever the driver is opened, a new tape is inserted, or the &quot;time mode&quot; command is issued, the driver checks the current time mode available on the tape and sets &quot;time type&quot; to either &quot;timecode&quot; or &quot;counter&quot;.</span></span> <span data-ttu-id="6350a-498">Quando &quot; o tipo &quot; de hora é definido, o driver não o altera até que uma das condições acima ocorra novamente.</span><span class="sxs-lookup"><span data-stu-id="6350a-498">Once &quot;time type&quot; is set, the driver doesn't change it until one of the above conditions occurs again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-499">tempo de vida de modo de hora</span><span class="sxs-lookup"><span data-stu-id="6350a-499">time mode timecode</span></span></td>
<td><span data-ttu-id="6350a-500">Define o modo de informações de posição para usar &quot; informações de código &quot; de Code na fita.</span><span class="sxs-lookup"><span data-stu-id="6350a-500">Sets the position information mode to use &quot;timecode&quot; information on the tape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-501">acompanhamento de mais</span><span class="sxs-lookup"><span data-stu-id="6350a-501">tracking plus</span></span> <br/> <span data-ttu-id="6350a-502">menos controle</span><span class="sxs-lookup"><span data-stu-id="6350a-502">tracking minus</span></span> <br/> <span data-ttu-id="6350a-503">redefinição de rastreamento</span><span class="sxs-lookup"><span data-stu-id="6350a-503">tracking reset</span></span> <br/></td>
<td><span data-ttu-id="6350a-504">Ajusta a velocidade do transporte de fita em incrementos finos.</span><span class="sxs-lookup"><span data-stu-id="6350a-504">Adjusts the speed of the videotape transport in fine increments.</span></span> <span data-ttu-id="6350a-505">Use os &quot; sinalizadores de rastreamento &quot; quando uma imagem ruidosa for Obtida de um videocassete.</span><span class="sxs-lookup"><span data-stu-id="6350a-505">Use the &quot;tracking&quot; flags when a noisy picture is obtained from a VCR.</span></span> <span data-ttu-id="6350a-506">&quot;O acompanhamento &quot; do Plus aumenta a velocidade de transporte.</span><span class="sxs-lookup"><span data-stu-id="6350a-506">&quot;Tracking plus&quot; increases the transport speed.</span></span> <span data-ttu-id="6350a-507">&quot;O rastreamento &quot; de menos diminui a velocidade de transporte.</span><span class="sxs-lookup"><span data-stu-id="6350a-507">&quot;Tracking minus&quot; decreases the transport speed.</span></span> <span data-ttu-id="6350a-508">&quot;A redefinição &quot; de controle retorna o ajuste de controle para zero.</span><span class="sxs-lookup"><span data-stu-id="6350a-508">&quot;Tracking reset&quot; returns the tracking adjustment to zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6350a-509">vídeo desativado</span><span class="sxs-lookup"><span data-stu-id="6350a-509">video off</span></span></td>
<td><span data-ttu-id="6350a-510">Desabilita a saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6350a-510">Disables video output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6350a-511">vídeo ativado</span><span class="sxs-lookup"><span data-stu-id="6350a-511">video on</span></span></td>
<td><span data-ttu-id="6350a-512">Habilita a saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6350a-512">Enables video output.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="6350a-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6350a-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6350a-514">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="6350a-514">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="6350a-515">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="6350a-515">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="6350a-516">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6350a-516">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6350a-517">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6350a-517">Return Value</span></span>

<span data-ttu-id="6350a-518">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="6350a-518">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6350a-519">Comentários</span><span class="sxs-lookup"><span data-stu-id="6350a-519">Remarks</span></span>

<span data-ttu-id="6350a-520">Várias propriedades dos dados de formato de onda-áudio são definidas quando o arquivo para armazenar os dados é criado.</span><span class="sxs-lookup"><span data-stu-id="6350a-520">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="6350a-521">Essas propriedades descrevem como os dados são estruturados dentro do arquivo e não podem ser alterados após o início da gravação.</span><span class="sxs-lookup"><span data-stu-id="6350a-521">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="6350a-522">A lista a seguir identifica essas propriedades:</span><span class="sxs-lookup"><span data-stu-id="6350a-522">The following list identifies these properties:</span></span>

-   <span data-ttu-id="6350a-523">alinhamento</span><span class="sxs-lookup"><span data-stu-id="6350a-523">alignment</span></span>
-   <span data-ttu-id="6350a-524">bitspersample</span><span class="sxs-lookup"><span data-stu-id="6350a-524">bitspersample</span></span>
-   <span data-ttu-id="6350a-525">bytespersec</span><span class="sxs-lookup"><span data-stu-id="6350a-525">bytespersec</span></span>
-   <span data-ttu-id="6350a-526">canais</span><span class="sxs-lookup"><span data-stu-id="6350a-526">channels</span></span>
-   <span data-ttu-id="6350a-527">marca de formato</span><span class="sxs-lookup"><span data-stu-id="6350a-527">format tag</span></span>
-   <span data-ttu-id="6350a-528">samplespersec</span><span class="sxs-lookup"><span data-stu-id="6350a-528">samplespersec</span></span>

## <a name="examples"></a><span data-ttu-id="6350a-529">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6350a-529">Examples</span></span>

<span data-ttu-id="6350a-530">O comando a seguir define o formato de hora como milissegundos e define o formato de wave-áudio para 8 bits, mono, 11 kHz.</span><span class="sxs-lookup"><span data-stu-id="6350a-530">The following command sets the time format to milliseconds and sets the waveform-audio format to 8 bit, mono, 11 kHz.</span></span>

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a><span data-ttu-id="6350a-531">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6350a-531">Requirements</span></span>



| <span data-ttu-id="6350a-532">Requisito</span><span class="sxs-lookup"><span data-stu-id="6350a-532">Requirement</span></span> | <span data-ttu-id="6350a-533">Valor</span><span class="sxs-lookup"><span data-stu-id="6350a-533">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6350a-534">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6350a-534">Minimum supported client</span></span><br/> | <span data-ttu-id="6350a-535">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6350a-535">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6350a-536">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6350a-536">Minimum supported server</span></span><br/> | <span data-ttu-id="6350a-537">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6350a-537">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6350a-538">Confira também</span><span class="sxs-lookup"><span data-stu-id="6350a-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6350a-539">MCI</span><span class="sxs-lookup"><span data-stu-id="6350a-539">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6350a-540">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="6350a-540">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="6350a-541">captura</span><span class="sxs-lookup"><span data-stu-id="6350a-541">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="6350a-542">pause</span><span class="sxs-lookup"><span data-stu-id="6350a-542">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="6350a-543">salvar</span><span class="sxs-lookup"><span data-stu-id="6350a-543">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="6350a-544">stop</span><span class="sxs-lookup"><span data-stu-id="6350a-544">stop</span></span>](stop.md)
</dt> </dl>

 


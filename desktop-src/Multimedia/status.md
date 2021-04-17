---
title: comando de status
description: O comando status solicita informações de status de um dispositivo. Todos os dispositivos reconhecem este comando.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- comando de status multimídia do Windows
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "105759626"
---
# <a name="status-command"></a><span data-ttu-id="f49f1-105">comando de status</span><span class="sxs-lookup"><span data-stu-id="f49f1-105">status command</span></span>

> [!NOTE]
> <span data-ttu-id="f49f1-106">Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.</span><span class="sxs-lookup"><span data-stu-id="f49f1-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="f49f1-107">Neste documento, há referências à palavra ' escravo '.</span><span class="sxs-lookup"><span data-stu-id="f49f1-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="f49f1-108">O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.</span><span class="sxs-lookup"><span data-stu-id="f49f1-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="f49f1-109">Essa palavra-chave é usada, pois é atualmente a palavra usada nos comandos.</span><span class="sxs-lookup"><span data-stu-id="f49f1-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="f49f1-110">Para fins de consistência, este documento contém esta palavra.</span><span class="sxs-lookup"><span data-stu-id="f49f1-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="f49f1-111">Quando esta palavra for alterada nos comandos, corrigiremos este documento para estar em alinhamento.</span><span class="sxs-lookup"><span data-stu-id="f49f1-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="f49f1-112">O comando status solicita informações de status de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-112">The status command requests status information from a device.</span></span> <span data-ttu-id="f49f1-113">Todos os dispositivos reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="f49f1-113">All devices recognize this command.</span></span>

<span data-ttu-id="f49f1-114">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f49f1-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="f49f1-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f49f1-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f49f1-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f49f1-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f49f1-117">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f49f1-117">Identifier of an MCI device.</span></span> <span data-ttu-id="f49f1-118">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="f49f1-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f49f1-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="f49f1-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="f49f1-120">Sinalizador para solicitar informações de status.</span><span class="sxs-lookup"><span data-stu-id="f49f1-120">Flag for requesting status information.</span></span> <span data-ttu-id="f49f1-121">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **status** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-121">The following table lists device types that recognize the **status** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f49f1-122">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f49f1-122">Device Type</span></span></th>
<th><span data-ttu-id="f49f1-123">Sinalizadores de solicitação</span><span class="sxs-lookup"><span data-stu-id="f49f1-123">Request Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f49f1-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="f49f1-125"><em>número</em> de faixa do tipo cdaudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-125">cdaudio type track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-126">faixa atual</span><span class="sxs-lookup"><span data-stu-id="f49f1-126">current track</span></span></li>
<li><span data-ttu-id="f49f1-127">comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-127">length</span></span></li>
<li><span data-ttu-id="f49f1-128"><em>número</em> de faixa de comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-128">length track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-129">mídia presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-129">media present</span></span></li>
<li><span data-ttu-id="f49f1-130">mode</span><span class="sxs-lookup"><span data-stu-id="f49f1-130">mode</span></span></li>
<li><span data-ttu-id="f49f1-131">número de faixas</span><span class="sxs-lookup"><span data-stu-id="f49f1-131">number of tracks</span></span></li>
<li><span data-ttu-id="f49f1-132">position</span><span class="sxs-lookup"><span data-stu-id="f49f1-132">position</span></span></li>
<li><span data-ttu-id="f49f1-133"><em>número</em> da faixa de posição</span><span class="sxs-lookup"><span data-stu-id="f49f1-133">position track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-134">esteja</span><span class="sxs-lookup"><span data-stu-id="f49f1-134">ready</span></span></li>
<li><span data-ttu-id="f49f1-135">posição inicial</span><span class="sxs-lookup"><span data-stu-id="f49f1-135">start position</span></span></li>
<li><span data-ttu-id="f49f1-136">formato de hora</span><span class="sxs-lookup"><span data-stu-id="f49f1-136">time format</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-137">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="f49f1-137">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="f49f1-138">áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-138">audio</span></span></li>
<li><span data-ttu-id="f49f1-139">alinhamento de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-139">audio alignment</span></span></li>
<li><span data-ttu-id="f49f1-140">BitsPerSample de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-140">audio bitspersample</span></span></li>
<li><span data-ttu-id="f49f1-141">quebras de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-141">audio breaks</span></span></li>
<li><span data-ttu-id="f49f1-142">bytespersec de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-142">audio bytespersec</span></span></li>
<li><span data-ttu-id="f49f1-143">entrada de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-143">audio input</span></span></li>
<li><span data-ttu-id="f49f1-144">registro de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-144">audio record</span></span></li>
<li><span data-ttu-id="f49f1-145">fonte de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-145">audio source</span></span></li>
<li><span data-ttu-id="f49f1-146">samplespersec de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-146">audio samplespersec</span></span></li>
<li><span data-ttu-id="f49f1-147">fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-147">audio stream</span></span></li>
<li><span data-ttu-id="f49f1-148">graves</span><span class="sxs-lookup"><span data-stu-id="f49f1-148">bass</span></span></li>
<li><span data-ttu-id="f49f1-149">bitsperpel</span><span class="sxs-lookup"><span data-stu-id="f49f1-149">bitsperpel</span></span></li>
<li><span data-ttu-id="f49f1-150">lo</span><span class="sxs-lookup"><span data-stu-id="f49f1-150">brightness</span></span></li>
<li><span data-ttu-id="f49f1-151">cor</span><span class="sxs-lookup"><span data-stu-id="f49f1-151">color</span></span></li>
<li><span data-ttu-id="f49f1-152">contraste</span><span class="sxs-lookup"><span data-stu-id="f49f1-152">contrast</span></span></li>
<li><span data-ttu-id="f49f1-153">faixa atual</span><span class="sxs-lookup"><span data-stu-id="f49f1-153">current track</span></span></li>
<li><span data-ttu-id="f49f1-154"><em>unidade</em> de espaço em disco</span><span class="sxs-lookup"><span data-stu-id="f49f1-154">disk space <em>drive</em></span></span></li>
<li><span data-ttu-id="f49f1-155">conclusão do arquivo</span><span class="sxs-lookup"><span data-stu-id="f49f1-155">file completion</span></span></li>
<li><span data-ttu-id="f49f1-156">formato de arquivo</span><span class="sxs-lookup"><span data-stu-id="f49f1-156">file format</span></span></li>
<li><span data-ttu-id="f49f1-157">modo de arquivo</span><span class="sxs-lookup"><span data-stu-id="f49f1-157">file mode</span></span></li>
<li><span data-ttu-id="f49f1-158">avançar</span><span class="sxs-lookup"><span data-stu-id="f49f1-158">forward</span></span></li>
<li><span data-ttu-id="f49f1-159">quadros ignorados</span><span class="sxs-lookup"><span data-stu-id="f49f1-159">frames skipped</span></span></li>
<li><span data-ttu-id="f49f1-160">gamma</span><span class="sxs-lookup"><span data-stu-id="f49f1-160">gamma</span></span></li>
<li><span data-ttu-id="f49f1-161">input</span><span class="sxs-lookup"><span data-stu-id="f49f1-161">input</span></span></li>
<li><span data-ttu-id="f49f1-162">volume esquerdo</span><span class="sxs-lookup"><span data-stu-id="f49f1-162">left volume</span></span></li>
<li><span data-ttu-id="f49f1-163">comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-163">length</span></span></li>
<li><span data-ttu-id="f49f1-164"><em>número</em> de faixa de comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-164">length track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-165">mídia presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-165">media present</span></span></li>
<li><span data-ttu-id="f49f1-166">mode</span><span class="sxs-lookup"><span data-stu-id="f49f1-166">mode</span></span></li>
<li><span data-ttu-id="f49f1-167">monitor</span><span class="sxs-lookup"><span data-stu-id="f49f1-167">monitor</span></span></li>
<li><span data-ttu-id="f49f1-168">método de monitor</span><span class="sxs-lookup"><span data-stu-id="f49f1-168">monitor method</span></span></li>
<li><span data-ttu-id="f49f1-169">nominal</span><span class="sxs-lookup"><span data-stu-id="f49f1-169">nominal</span></span></li>
<li><span data-ttu-id="f49f1-170">taxa de quadros nominal</span><span class="sxs-lookup"><span data-stu-id="f49f1-170">nominal frame rate</span></span></li>
<li><span data-ttu-id="f49f1-171">taxa de quadros de registro nominal</span><span class="sxs-lookup"><span data-stu-id="f49f1-171">nominal record frame rate</span></span></li>
<li><span data-ttu-id="f49f1-172">número de faixas</span><span class="sxs-lookup"><span data-stu-id="f49f1-172">number of tracks</span></span></li>
<li><span data-ttu-id="f49f1-173">output</span><span class="sxs-lookup"><span data-stu-id="f49f1-173">output</span></span></li>
<li><span data-ttu-id="f49f1-174">identificador da paleta</span><span class="sxs-lookup"><span data-stu-id="f49f1-174">palette handle</span></span></li>
<li><span data-ttu-id="f49f1-175">modo de pausa</span><span class="sxs-lookup"><span data-stu-id="f49f1-175">pause mode</span></span></li>
<li><span data-ttu-id="f49f1-176">velocidade de reprodução</span><span class="sxs-lookup"><span data-stu-id="f49f1-176">play speed</span></span></li>
<li><span data-ttu-id="f49f1-177">position</span><span class="sxs-lookup"><span data-stu-id="f49f1-177">position</span></span></li>
<li><span data-ttu-id="f49f1-178"><em>número</em> da faixa de posição</span><span class="sxs-lookup"><span data-stu-id="f49f1-178">position track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-179">esteja</span><span class="sxs-lookup"><span data-stu-id="f49f1-179">ready</span></span></li>
<li><span data-ttu-id="f49f1-180">taxa de quadros de registro</span><span class="sxs-lookup"><span data-stu-id="f49f1-180">record frame rate</span></span></li>
<li><span data-ttu-id="f49f1-181"><em>quadro</em> de referência</span><span class="sxs-lookup"><span data-stu-id="f49f1-181">reference <em>frame</em></span></span></li>
<li><span data-ttu-id="f49f1-182">Tamanho reservado</span><span class="sxs-lookup"><span data-stu-id="f49f1-182">reserved size</span></span></li>
<li><span data-ttu-id="f49f1-183">volume correto</span><span class="sxs-lookup"><span data-stu-id="f49f1-183">right volume</span></span></li>
<li><span data-ttu-id="f49f1-184">buscar exatamente</span><span class="sxs-lookup"><span data-stu-id="f49f1-184">seek exactly</span></span></li>
<li><span data-ttu-id="f49f1-185">nitidez</span><span class="sxs-lookup"><span data-stu-id="f49f1-185">sharpness</span></span></li>
<li><span data-ttu-id="f49f1-186">SMPTE</span><span class="sxs-lookup"><span data-stu-id="f49f1-186">smpte</span></span></li>
<li><span data-ttu-id="f49f1-187">velocidade</span><span class="sxs-lookup"><span data-stu-id="f49f1-187">speed</span></span></li>
<li><span data-ttu-id="f49f1-188">posição inicial</span><span class="sxs-lookup"><span data-stu-id="f49f1-188">start position</span></span></li>
<li><span data-ttu-id="f49f1-189">formato de arquivo ainda</span><span class="sxs-lookup"><span data-stu-id="f49f1-189">still file format</span></span></li>
<li><span data-ttu-id="f49f1-190">formato de hora</span><span class="sxs-lookup"><span data-stu-id="f49f1-190">time format</span></span></li>
<li><span data-ttu-id="f49f1-191">Nuance</span><span class="sxs-lookup"><span data-stu-id="f49f1-191">tint</span></span></li>
<li><span data-ttu-id="f49f1-192">agudo</span><span class="sxs-lookup"><span data-stu-id="f49f1-192">treble</span></span></li>
<li><span data-ttu-id="f49f1-193">não salvas</span><span class="sxs-lookup"><span data-stu-id="f49f1-193">unsaved</span></span></li>
<li><span data-ttu-id="f49f1-194">video</span><span class="sxs-lookup"><span data-stu-id="f49f1-194">video</span></span></li>
<li><span data-ttu-id="f49f1-195">índice de chave de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-195">video key index</span></span></li>
<li><span data-ttu-id="f49f1-196">cor da chave do vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-196">video key color</span></span></li>
<li><span data-ttu-id="f49f1-197">registro de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-197">video record</span></span></li>
<li><span data-ttu-id="f49f1-198">fonte de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-198">video source</span></span></li>
<li><span data-ttu-id="f49f1-199">número da fonte do vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-199">video source number</span></span></li>
<li><span data-ttu-id="f49f1-200">fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-200">video stream</span></span></li>
<li><span data-ttu-id="f49f1-201">volume</span><span class="sxs-lookup"><span data-stu-id="f49f1-201">volume</span></span></li>
<li><span data-ttu-id="f49f1-202">identificador de janela</span><span class="sxs-lookup"><span data-stu-id="f49f1-202">window handle</span></span></li>
<li><span data-ttu-id="f49f1-203">janela visível</span><span class="sxs-lookup"><span data-stu-id="f49f1-203">window visible</span></span></li>
<li><span data-ttu-id="f49f1-204">janela minimizada</span><span class="sxs-lookup"><span data-stu-id="f49f1-204">window minimized</span></span></li>
<li><span data-ttu-id="f49f1-205">janela maximizada</span><span class="sxs-lookup"><span data-stu-id="f49f1-205">window maximized</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-206">overlay</span><span class="sxs-lookup"><span data-stu-id="f49f1-206">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="f49f1-207">mídia presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-207">media present</span></span></li>
<li><span data-ttu-id="f49f1-208">mode</span><span class="sxs-lookup"><span data-stu-id="f49f1-208">mode</span></span></li>
<li><span data-ttu-id="f49f1-209">número de faixas</span><span class="sxs-lookup"><span data-stu-id="f49f1-209">number of tracks</span></span></li>
<li><span data-ttu-id="f49f1-210">esteja</span><span class="sxs-lookup"><span data-stu-id="f49f1-210">ready</span></span></li>
<li><span data-ttu-id="f49f1-211">Estendi</span><span class="sxs-lookup"><span data-stu-id="f49f1-211">stretch</span></span></li>
<li><span data-ttu-id="f49f1-212">identificador de janela</span><span class="sxs-lookup"><span data-stu-id="f49f1-212">window handle</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-213">sequenciador</span><span class="sxs-lookup"><span data-stu-id="f49f1-213">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="f49f1-214">faixa atual</span><span class="sxs-lookup"><span data-stu-id="f49f1-214">current track</span></span></li>
<li><span data-ttu-id="f49f1-215">tipo de divisão</span><span class="sxs-lookup"><span data-stu-id="f49f1-215">division type</span></span></li>
<li><span data-ttu-id="f49f1-216">comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-216">length</span></span></li>
<li><span data-ttu-id="f49f1-217">comprimento mestre do <em>número</em> de faixas</span><span class="sxs-lookup"><span data-stu-id="f49f1-217">length track <em>number</em> master</span></span></li>
<li><span data-ttu-id="f49f1-218">mídia presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-218">media present</span></span></li>
<li><span data-ttu-id="f49f1-219">mode</span><span class="sxs-lookup"><span data-stu-id="f49f1-219">mode</span></span></li>
<li><span data-ttu-id="f49f1-220">número de faixas</span><span class="sxs-lookup"><span data-stu-id="f49f1-220">number of tracks</span></span></li>
<li><span data-ttu-id="f49f1-221">deslocamento</span><span class="sxs-lookup"><span data-stu-id="f49f1-221">offset</span></span></li>
<li><span data-ttu-id="f49f1-222">porta</span><span class="sxs-lookup"><span data-stu-id="f49f1-222">port</span></span></li>
<li><span data-ttu-id="f49f1-223">position</span><span class="sxs-lookup"><span data-stu-id="f49f1-223">position</span></span></li>
<li><span data-ttu-id="f49f1-224"><em>número</em> da faixa de posição</span><span class="sxs-lookup"><span data-stu-id="f49f1-224">position track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-225">esteja</span><span class="sxs-lookup"><span data-stu-id="f49f1-225">ready</span></span></li>
<li><span data-ttu-id="f49f1-226">subordinado</span><span class="sxs-lookup"><span data-stu-id="f49f1-226">slave</span></span></li>
<li><span data-ttu-id="f49f1-227">posição inicial</span><span class="sxs-lookup"><span data-stu-id="f49f1-227">start position</span></span></li>
<li><span data-ttu-id="f49f1-228">golpe</span><span class="sxs-lookup"><span data-stu-id="f49f1-228">tempo</span></span></li>
<li><span data-ttu-id="f49f1-229">formato de hora</span><span class="sxs-lookup"><span data-stu-id="f49f1-229">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-230">videocassete</span><span class="sxs-lookup"><span data-stu-id="f49f1-230">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="f49f1-231">montar registro</span><span class="sxs-lookup"><span data-stu-id="f49f1-231">assemble record</span></span></li>
<li><span data-ttu-id="f49f1-232">monitor de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-232">audio monitor</span></span></li>
<li><span data-ttu-id="f49f1-233">número do monitor de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-233">audio monitor number</span></span></li>
<li><span data-ttu-id="f49f1-234">registro de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-234">audio record</span></span></li>
<li><span data-ttu-id="f49f1-235"><em>número</em> de faixa do registro de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-235">audio record track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-236">fonte de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-236">audio source</span></span></li>
<li><span data-ttu-id="f49f1-237">número da fonte de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-237">audio source number</span></span></li>
<li><span data-ttu-id="f49f1-238">channel</span><span class="sxs-lookup"><span data-stu-id="f49f1-238">channel</span></span></li>
<li><span data-ttu-id="f49f1-239"><em>número</em> do sintonizador de canal</span><span class="sxs-lookup"><span data-stu-id="f49f1-239">channel tuner <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-240">clock</span><span class="sxs-lookup"><span data-stu-id="f49f1-240">clock</span></span></li>
<li><span data-ttu-id="f49f1-241">ID do relógio</span><span class="sxs-lookup"><span data-stu-id="f49f1-241">clock id</span></span></li>
<li><span data-ttu-id="f49f1-242">contador</span><span class="sxs-lookup"><span data-stu-id="f49f1-242">counter</span></span></li>
<li><span data-ttu-id="f49f1-243">formato do contador</span><span class="sxs-lookup"><span data-stu-id="f49f1-243">counter format</span></span></li>
<li><span data-ttu-id="f49f1-244">resolução do contador</span><span class="sxs-lookup"><span data-stu-id="f49f1-244">counter resolution</span></span></li>
<li><span data-ttu-id="f49f1-245">faixa atual</span><span class="sxs-lookup"><span data-stu-id="f49f1-245">current track</span></span></li>
<li><span data-ttu-id="f49f1-246">taxa de quadros</span><span class="sxs-lookup"><span data-stu-id="f49f1-246">frame rate</span></span></li>
<li><span data-ttu-id="f49f1-247">índice</span><span class="sxs-lookup"><span data-stu-id="f49f1-247">index</span></span></li>
<li><span data-ttu-id="f49f1-248">índice ativado</span><span class="sxs-lookup"><span data-stu-id="f49f1-248">index on</span></span></li>
<li><span data-ttu-id="f49f1-249">comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-249">length</span></span></li>
<li><span data-ttu-id="f49f1-250"><em>número</em> de faixa de comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-250">length track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-251">mídia presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-251">media present</span></span></li>
<li><span data-ttu-id="f49f1-252">tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="f49f1-252">media type</span></span></li>
<li><span data-ttu-id="f49f1-253">mode</span><span class="sxs-lookup"><span data-stu-id="f49f1-253">mode</span></span></li>
<li><span data-ttu-id="f49f1-254">número de faixas de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-254">number of audio tracks</span></span></li>
<li><span data-ttu-id="f49f1-255">número de faixas</span><span class="sxs-lookup"><span data-stu-id="f49f1-255">number of tracks</span></span></li>
<li><span data-ttu-id="f49f1-256">número de faixas de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-256">number of video tracks</span></span></li>
<li><span data-ttu-id="f49f1-257"><em>tempo limite</em> de pausa</span><span class="sxs-lookup"><span data-stu-id="f49f1-257">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="f49f1-258">formato de reprodução</span><span class="sxs-lookup"><span data-stu-id="f49f1-258">play format</span></span></li>
<li><span data-ttu-id="f49f1-259">position</span><span class="sxs-lookup"><span data-stu-id="f49f1-259">position</span></span></li>
<li><span data-ttu-id="f49f1-260">início da posição</span><span class="sxs-lookup"><span data-stu-id="f49f1-260">position start</span></span></li>
<li><span data-ttu-id="f49f1-261"><em>número</em> da faixa de posição</span><span class="sxs-lookup"><span data-stu-id="f49f1-261">position track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-262"><em>duração</em> do registro</span><span class="sxs-lookup"><span data-stu-id="f49f1-262">postroll <em>duration</em></span></span></li>
<li><span data-ttu-id="f49f1-263">ligar</span><span class="sxs-lookup"><span data-stu-id="f49f1-263">power on</span></span></li>
<li><span data-ttu-id="f49f1-264"><em>duração</em> da preversão</span><span class="sxs-lookup"><span data-stu-id="f49f1-264">preroll <em>duration</em></span></span></li>
<li><span data-ttu-id="f49f1-265">esteja</span><span class="sxs-lookup"><span data-stu-id="f49f1-265">ready</span></span></li>
<li><span data-ttu-id="f49f1-266">formato de registro</span><span class="sxs-lookup"><span data-stu-id="f49f1-266">record format</span></span></li>
<li><span data-ttu-id="f49f1-267">velocidade</span><span class="sxs-lookup"><span data-stu-id="f49f1-267">speed</span></span></li>
<li><span data-ttu-id="f49f1-268">formato de hora</span><span class="sxs-lookup"><span data-stu-id="f49f1-268">time format</span></span></li>
<li><span data-ttu-id="f49f1-269">modo de tempo</span><span class="sxs-lookup"><span data-stu-id="f49f1-269">time mode</span></span></li>
<li><span data-ttu-id="f49f1-270">tipo de hora</span><span class="sxs-lookup"><span data-stu-id="f49f1-270">time type</span></span></li>
<li><span data-ttu-id="f49f1-271">código de paficação presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-271">timecode present</span></span></li>
<li><span data-ttu-id="f49f1-272">registro de código de histórico</span><span class="sxs-lookup"><span data-stu-id="f49f1-272">timecode record</span></span></li>
<li><span data-ttu-id="f49f1-273">tipo de código de Code</span><span class="sxs-lookup"><span data-stu-id="f49f1-273">timecode type</span></span></li>
<li><span data-ttu-id="f49f1-274">número do sintonizador</span><span class="sxs-lookup"><span data-stu-id="f49f1-274">tuner number</span></span></li>
<li><span data-ttu-id="f49f1-275">monitor de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-275">video monitor</span></span></li>
<li><span data-ttu-id="f49f1-276">número do monitor de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-276">video monitor number</span></span></li>
<li><span data-ttu-id="f49f1-277">registro de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-277">video record</span></span></li>
<li><span data-ttu-id="f49f1-278"><em>número</em> de faixa do registro de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-278">video record track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-279">fonte de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-279">video source</span></span></li>
<li><span data-ttu-id="f49f1-280">número da fonte do vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-280">video source number</span></span></li>
<li><span data-ttu-id="f49f1-281">protegido contra gravação</span><span class="sxs-lookup"><span data-stu-id="f49f1-281">write protected</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-282">videodisc</span><span class="sxs-lookup"><span data-stu-id="f49f1-282">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="f49f1-283">faixa atual</span><span class="sxs-lookup"><span data-stu-id="f49f1-283">current track</span></span></li>
<li><span data-ttu-id="f49f1-284">tamanho do disco</span><span class="sxs-lookup"><span data-stu-id="f49f1-284">disc size</span></span></li>
<li><span data-ttu-id="f49f1-285">avançar</span><span class="sxs-lookup"><span data-stu-id="f49f1-285">forward</span></span></li>
<li><span data-ttu-id="f49f1-286">comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-286">length</span></span></li>
<li><span data-ttu-id="f49f1-287"><em>número</em> de faixa de comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-287">length track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-288">mídia presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-288">media present</span></span></li>
<li><span data-ttu-id="f49f1-289">tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="f49f1-289">media type</span></span></li>
<li><span data-ttu-id="f49f1-290">mode</span><span class="sxs-lookup"><span data-stu-id="f49f1-290">mode</span></span></li>
<li><span data-ttu-id="f49f1-291">número de faixas</span><span class="sxs-lookup"><span data-stu-id="f49f1-291">number of tracks</span></span></li>
<li><span data-ttu-id="f49f1-292">position</span><span class="sxs-lookup"><span data-stu-id="f49f1-292">position</span></span></li>
<li><span data-ttu-id="f49f1-293"><em>número</em> da faixa de posição</span><span class="sxs-lookup"><span data-stu-id="f49f1-293">position track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-294">esteja</span><span class="sxs-lookup"><span data-stu-id="f49f1-294">ready</span></span></li>
<li><span data-ttu-id="f49f1-295">residente</span><span class="sxs-lookup"><span data-stu-id="f49f1-295">side</span></span></li>
<li><span data-ttu-id="f49f1-296">velocidade</span><span class="sxs-lookup"><span data-stu-id="f49f1-296">speed</span></span></li>
<li><span data-ttu-id="f49f1-297">posição inicial</span><span class="sxs-lookup"><span data-stu-id="f49f1-297">start position</span></span></li>
<li><span data-ttu-id="f49f1-298">formato de hora</span><span class="sxs-lookup"><span data-stu-id="f49f1-298">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-299">waveaudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-299">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="f49f1-300">alinhamento</span><span class="sxs-lookup"><span data-stu-id="f49f1-300">alignment</span></span></li>
<li><span data-ttu-id="f49f1-301">bitspersample</span><span class="sxs-lookup"><span data-stu-id="f49f1-301">bitspersample</span></span></li>
<li><span data-ttu-id="f49f1-302">bytespersec</span><span class="sxs-lookup"><span data-stu-id="f49f1-302">bytespersec</span></span></li>
<li><span data-ttu-id="f49f1-303">canais</span><span class="sxs-lookup"><span data-stu-id="f49f1-303">channels</span></span></li>
<li><span data-ttu-id="f49f1-304">faixa atual</span><span class="sxs-lookup"><span data-stu-id="f49f1-304">current track</span></span></li>
<li><span data-ttu-id="f49f1-305">marca de formato</span><span class="sxs-lookup"><span data-stu-id="f49f1-305">format tag</span></span></li>
<li><span data-ttu-id="f49f1-306">input</span><span class="sxs-lookup"><span data-stu-id="f49f1-306">input</span></span></li>
<li><span data-ttu-id="f49f1-307">comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-307">length</span></span></li>
<li><span data-ttu-id="f49f1-308"><em>número</em> de faixa de comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-308">length track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-309">nível</span><span class="sxs-lookup"><span data-stu-id="f49f1-309">level</span></span></li>
<li><span data-ttu-id="f49f1-310">mídia presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-310">media present</span></span></li>
<li><span data-ttu-id="f49f1-311">mode</span><span class="sxs-lookup"><span data-stu-id="f49f1-311">mode</span></span></li>
<li><span data-ttu-id="f49f1-312">número de faixas</span><span class="sxs-lookup"><span data-stu-id="f49f1-312">number of tracks</span></span></li>
<li><span data-ttu-id="f49f1-313">output</span><span class="sxs-lookup"><span data-stu-id="f49f1-313">output</span></span></li>
<li><span data-ttu-id="f49f1-314">position</span><span class="sxs-lookup"><span data-stu-id="f49f1-314">position</span></span></li>
<li><span data-ttu-id="f49f1-315"><em>número</em> da faixa de posição</span><span class="sxs-lookup"><span data-stu-id="f49f1-315">position track <em>number</em></span></span></li>
<li><span data-ttu-id="f49f1-316">esteja</span><span class="sxs-lookup"><span data-stu-id="f49f1-316">ready</span></span></li>
<li><span data-ttu-id="f49f1-317">samplespersec</span><span class="sxs-lookup"><span data-stu-id="f49f1-317">samplespersec</span></span></li>
<li><span data-ttu-id="f49f1-318">posição inicial</span><span class="sxs-lookup"><span data-stu-id="f49f1-318">start position</span></span></li>
<li><span data-ttu-id="f49f1-319">formato de hora</span><span class="sxs-lookup"><span data-stu-id="f49f1-319">time format</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f49f1-320">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszRequest** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="f49f1-320">The following table lists the flags that can be specified in the **lpszRequest** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f49f1-321">Valor</span><span class="sxs-lookup"><span data-stu-id="f49f1-321">Value</span></span></th>
<th><span data-ttu-id="f49f1-322">Significado</span><span class="sxs-lookup"><span data-stu-id="f49f1-322">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f49f1-323">alinhamento</span><span class="sxs-lookup"><span data-stu-id="f49f1-323">alignment</span></span></td>
<td><span data-ttu-id="f49f1-324">Retorna o alinhamento de bloco de dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f49f1-324">Returns the block alignment of data, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-325">montar registro</span><span class="sxs-lookup"><span data-stu-id="f49f1-325">assemble record</span></span></td>
<td><span data-ttu-id="f49f1-326">Retornará <strong>true</strong> se o dispositivo for definido para montar o modo de registro.</span><span class="sxs-lookup"><span data-stu-id="f49f1-326">Returns <strong>TRUE</strong> if the device is set to assemble mode recording.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-327">áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-327">audio</span></span></td>
<td><span data-ttu-id="f49f1-328">Retorna &quot; on &quot; ou &quot; off &quot; dependendo do comando mais recente <a href="setaudio.md"></a> &quot; de on &quot; ou off de &quot; áudio &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-328">Returns &quot;on&quot; or &quot;off&quot; depending on the most recent <a href="setaudio.md">setaudio</a> &quot;on&quot; or &quot;off&quot; command.</span></span> <span data-ttu-id="f49f1-329">Ele será &quot; retornado &quot; se um ou ambos os alto-falantes estiverem habilitados e &quot; fora do &quot; contrário.</span><span class="sxs-lookup"><span data-stu-id="f49f1-329">It returns &quot;on&quot; if either or both speakers are enabled, and &quot;off&quot; otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-330">alinhamento de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-330">audio alignment</span></span></td>
<td><span data-ttu-id="f49f1-331">Retorna o alinhamento dos blocos de dados em relação ao início da entrada dados de formato de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="f49f1-331">Returns the alignment of data blocks relative to the start of input waveform-audio data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-332">BitsPerSample de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-332">audio bitspersample</span></span></td>
<td><span data-ttu-id="f49f1-333">Retorna o número de bits por amostra que o dispositivo usa para gravação.</span><span class="sxs-lookup"><span data-stu-id="f49f1-333">Returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="f49f1-334">Esse sinalizador se aplica somente a dispositivos que dão suporte ao &quot; &quot; algoritmo PCM.</span><span class="sxs-lookup"><span data-stu-id="f49f1-334">This flag applies only to devices supporting the &quot;pcm&quot; algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-335">quebras de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-335">audio breaks</span></span></td>
<td><span data-ttu-id="f49f1-336">Retorna o número de vezes que a parte de áudio da última sequência AVI se quebrou.</span><span class="sxs-lookup"><span data-stu-id="f49f1-336">Returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="f49f1-337">O sistema conta uma quebra de áudio sempre que tenta gravar dados de áudio no driver de dispositivo e descobre que o driver já reproduziu todos os dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f49f1-337">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="f49f1-338">Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="f49f1-338">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="f49f1-339">Ele destina-se apenas à avaliação de desempenho; o valor de retorno é difícil de interpretar.</span><span class="sxs-lookup"><span data-stu-id="f49f1-339">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-340">bytespersec de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-340">audio bytespersec</span></span></td>
<td><span data-ttu-id="f49f1-341">Retorna o número médio de bytes por segundo usados para gravação.</span><span class="sxs-lookup"><span data-stu-id="f49f1-341">Returns the average number of bytes per second used for recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-342">entrada de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-342">audio input</span></span></td>
<td><span data-ttu-id="f49f1-343">Retorna o nível de áudio instantâneo aproximado do sinal de áudio de entrada analógica.</span><span class="sxs-lookup"><span data-stu-id="f49f1-343">Returns the approximate instantaneous audio level of the analog input audio signal.</span></span> <span data-ttu-id="f49f1-344">Um valor maior que 1000 implica distorção de recorte.</span><span class="sxs-lookup"><span data-stu-id="f49f1-344">A value greater than 1000 implies clipping distortion.</span></span> <span data-ttu-id="f49f1-345">Alguns dispositivos podem retornar esse valor somente durante a gravação de áudio.</span><span class="sxs-lookup"><span data-stu-id="f49f1-345">Some devices can return this value only while recording audio.</span></span> <span data-ttu-id="f49f1-346">O valor não tem nenhum comando <a href="set.md">set</a> ou <a href="setaudio.md">SetAudio</a> associado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-346">The value has no associated <a href="set.md">set</a> or <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-347">monitor de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-347">audio monitor</span></span></td>
<td><span data-ttu-id="f49f1-348">Retorna &quot; &quot; a saída ou um dos tipos de entrada de origem válidos.</span><span class="sxs-lookup"><span data-stu-id="f49f1-348">Returns &quot;output&quot;, or one of the valid source-input types.</span></span> <span data-ttu-id="f49f1-349">Para obter mais informações, consulte o comando monitor <strong>SetAudio</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-349">For more information, see the <strong>setaudio</strong> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-350">número do monitor de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-350">audio monitor number</span></span></td>
<td><span data-ttu-id="f49f1-351">Retorna o número monitorado de vídeo do tipo especificado pelo monitor de áudio de <strong>status</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-351">Returns the monitored-video number of the type specified by <strong>status</strong> &quot;audio monitor&quot;.</span></span> <span data-ttu-id="f49f1-352">Para obter mais informações, consulte o comando <a href="setaudio.md">SetAudio</a> .</span><span class="sxs-lookup"><span data-stu-id="f49f1-352">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-353">registro de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-353">audio record</span></span></td>
<td><span data-ttu-id="f49f1-354">Retorna &quot; on &quot; ou &quot; off &quot; , refletindo o estado definido pelo registro de conjunto de <strong>áudio</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-354">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by <strong>setaudio</strong> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-355"><em>número</em> de faixa do registro de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-355">audio record track <em>number</em></span></span></td>
<td><span data-ttu-id="f49f1-356">Retornará <strong>true</strong> se o VCR estiver definido para gravar áudio.</span><span class="sxs-lookup"><span data-stu-id="f49f1-356">Returns <strong>TRUE</strong> if the VCR is set to record audio.</span></span> <span data-ttu-id="f49f1-357">Se nenhum número de faixa for fornecido, o valor padrão de 1 será assumido.</span><span class="sxs-lookup"><span data-stu-id="f49f1-357">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-358">samplespersec de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-358">audio samplespersec</span></span></td>
<td><span data-ttu-id="f49f1-359">Retorna o número de amostras por segundo registradas.</span><span class="sxs-lookup"><span data-stu-id="f49f1-359">Returns the number of samples per second recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-360">fonte de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-360">audio source</span></span></td>
<td><span data-ttu-id="f49f1-361">Retorna a fonte do digitalizador de áudio atual: &quot; esquerda &quot; , &quot; direita &quot; , &quot; média &quot; ou &quot; estéreo &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-361">Returns the current audio digitizer source: &quot;left&quot;, &quot;right&quot;, &quot;average&quot;, or &quot;stereo&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-362">número da fonte de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-362">audio source number</span></span></td>
<td><span data-ttu-id="f49f1-363">Retorna o número da fonte de áudio do tipo retornado pela fonte de áudio de <strong>status</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-363">Returns the audio-source number of the type returned by <strong>status</strong> &quot;audio source&quot;.</span></span> <span data-ttu-id="f49f1-364">Para obter mais informações, consulte o comando <a href="setaudio.md">SetAudio</a> .</span><span class="sxs-lookup"><span data-stu-id="f49f1-364">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-365">fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-365">audio stream</span></span></td>
<td><span data-ttu-id="f49f1-366">Retorna o número do fluxo de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-366">Returns the current audio-stream number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-367">graves</span><span class="sxs-lookup"><span data-stu-id="f49f1-367">bass</span></span></td>
<td><span data-ttu-id="f49f1-368">Retorna o nível de áudio-Bass atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-368">Returns the current audio-bass level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-369">bitsperpel</span><span class="sxs-lookup"><span data-stu-id="f49f1-369">bitsperpel</span></span></td>
<td><span data-ttu-id="f49f1-370">Retorna o número de bits por pixel para salvar dados capturados ou gravados.</span><span class="sxs-lookup"><span data-stu-id="f49f1-370">Returns the number of bits per pixel for saving captured or recorded data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-371">bitspersample</span><span class="sxs-lookup"><span data-stu-id="f49f1-371">bitspersample</span></span></td>
<td><span data-ttu-id="f49f1-372">Retorna os bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="f49f1-372">Returns the bits per sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-373">lo</span><span class="sxs-lookup"><span data-stu-id="f49f1-373">brightness</span></span></td>
<td><span data-ttu-id="f49f1-374">Retorna o nível de brilho do vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-374">Returns the current video-brightness level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-375">bytespersec</span><span class="sxs-lookup"><span data-stu-id="f49f1-375">bytespersec</span></span></td>
<td><span data-ttu-id="f49f1-376">Retorna o número médio de bytes por segundo reproduzidos ou gravados.</span><span class="sxs-lookup"><span data-stu-id="f49f1-376">Returns the average number of bytes per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-377"><em>número</em> de faixa do tipo cdaudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-377">cdaudio type track <em>number</em></span></span></td>
<td><span data-ttu-id="f49f1-378">Retorna o tipo do número de faixa especificado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-378">Returns the type of the specified track number.</span></span> <span data-ttu-id="f49f1-379">Pode ser &quot; áudio &quot; ou &quot; outros.&quot;</span><span class="sxs-lookup"><span data-stu-id="f49f1-379">This can be &quot;audio&quot; or &quot;other.&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-380">channel</span><span class="sxs-lookup"><span data-stu-id="f49f1-380">channel</span></span></td>
<td><span data-ttu-id="f49f1-381">Retorna o valor inteiro do conjunto de canais no sintonizador.</span><span class="sxs-lookup"><span data-stu-id="f49f1-381">Returns the integer value of the channel set on the tuner.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-382"><em>número</em> do sintonizador de canal</span><span class="sxs-lookup"><span data-stu-id="f49f1-382">channel tuner <em>number</em></span></span></td>
<td><span data-ttu-id="f49f1-383">Se &quot; o &quot; <em>número</em> do sintonizador for fornecido, o canal selecionado no momento no <em>número</em> do sintonizador lógico será retornado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-383">If &quot;tuner&quot; <em>number</em> is given, then the currently selected channel on the logical tuner <em>number</em> will be returned.</span></span> <span data-ttu-id="f49f1-384">Observe que pode haver vários sintonizadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="f49f1-384">Note that there can be several logical tuners.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-385">canais</span><span class="sxs-lookup"><span data-stu-id="f49f1-385">channels</span></span></td>
<td><span data-ttu-id="f49f1-386">Retorna o número de canais definido (1 para mono, 2 para estéreo).</span><span class="sxs-lookup"><span data-stu-id="f49f1-386">Returns the number of channels set (1 for mono, 2 for stereo).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-387">clock</span><span class="sxs-lookup"><span data-stu-id="f49f1-387">clock</span></span></td>
<td><span data-ttu-id="f49f1-388">Retorna o tempo externo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-388">Returns the external time.</span></span> <span data-ttu-id="f49f1-389">O tempo deve ser um inteiro longo não assinado que expresse incrementos totais.</span><span class="sxs-lookup"><span data-stu-id="f49f1-389">The time must be an unsigned long integer expressing total increments.</span></span> <span data-ttu-id="f49f1-390">Para obter mais informações, consulte o comando de taxa de incremento de relógio de <a href="capability.md">funcionalidade</a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-390">For more information, see the <a href="capability.md">capability</a> &quot;clock increment rate&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-391">ID do relógio</span><span class="sxs-lookup"><span data-stu-id="f49f1-391">clock id</span></span></td>
<td><span data-ttu-id="f49f1-392">Retorna um inteiro exclusivo que identifica o relógio.</span><span class="sxs-lookup"><span data-stu-id="f49f1-392">Returns a unique integer identifying the clock.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-393">cor</span><span class="sxs-lookup"><span data-stu-id="f49f1-393">color</span></span></td>
<td><span data-ttu-id="f49f1-394">Retorna o nível de cor atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-394">Returns the current color level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-395">contraste</span><span class="sxs-lookup"><span data-stu-id="f49f1-395">contrast</span></span></td>
<td><span data-ttu-id="f49f1-396">Retorna o nível de contraste atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-396">Returns the current contrast level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-397">contador</span><span class="sxs-lookup"><span data-stu-id="f49f1-397">counter</span></span></td>
<td><span data-ttu-id="f49f1-398">Retorna a posição do contador, no formato do contador atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-398">Returns the counter position, in the current counter format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-399">formato do contador</span><span class="sxs-lookup"><span data-stu-id="f49f1-399">counter format</span></span></td>
<td><span data-ttu-id="f49f1-400">Retorna o formato do contador atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-400">Returns the current counter format.</span></span> <span data-ttu-id="f49f1-401">Para obter mais informações, consulte o comando <a href="set.md">set</a> &quot; Counter Format &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-401">For more information, see the <a href="set.md">set</a> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-402">resolução do contador</span><span class="sxs-lookup"><span data-stu-id="f49f1-402">counter resolution</span></span></td>
<td><span data-ttu-id="f49f1-403">Retorna &quot; quadros &quot; ou &quot; segundos &quot; , indicando a resolução do contador.</span><span class="sxs-lookup"><span data-stu-id="f49f1-403">Returns &quot;frames&quot; or &quot;seconds&quot;, indicating the counter's resolution.</span></span> <span data-ttu-id="f49f1-404">Isso não é o mesmo que precisão.</span><span class="sxs-lookup"><span data-stu-id="f49f1-404">This is not the same as accuracy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-405">faixa atual</span><span class="sxs-lookup"><span data-stu-id="f49f1-405">current track</span></span></td>
<td><span data-ttu-id="f49f1-406">Retorna a faixa atual. O sequenciador MCISEQ retorna 1.</span><span class="sxs-lookup"><span data-stu-id="f49f1-406">Returns the current track. The MCISEQ sequencer returns 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-407">tamanho do disco</span><span class="sxs-lookup"><span data-stu-id="f49f1-407">disc size</span></span></td>
<td><span data-ttu-id="f49f1-408">Retorna 8 ou 12, indicando o tamanho do disco carregado em polegadas.</span><span class="sxs-lookup"><span data-stu-id="f49f1-408">Returns either 8 or 12, indicating the size of the loaded disc in inches.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-409"><em>unidade</em> de espaço em disco</span><span class="sxs-lookup"><span data-stu-id="f49f1-409">disk space <em>drive</em></span></span></td>
<td><span data-ttu-id="f49f1-410">Retorna o espaço em disco aproximado, no formato de hora atual, que pode ser obtido por um comando de <a href="reserve.md">reserva</a> para a unidade de disco especificada <em>.</em></span><span class="sxs-lookup"><span data-stu-id="f49f1-410">Returns the approximate disk space, in the current time format, that can be obtained by a <a href="reserve.md">reserve</a> command for the specified disk <em>drive.</em></span></span> <span data-ttu-id="f49f1-411">A <em>unidade</em> geralmente é especificada como uma única letra ou uma única letra seguida por dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="f49f1-411">The <em>drive</em> is usually specified as a single letter or a single letter followed by a colon (:).</span></span> <span data-ttu-id="f49f1-412">Alguns dispositivos, no entanto, podem usar um caminho.</span><span class="sxs-lookup"><span data-stu-id="f49f1-412">Some devices, however, might use a path.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-413">tipo de divisão</span><span class="sxs-lookup"><span data-stu-id="f49f1-413">division type</span></span></td>
<td><span data-ttu-id="f49f1-414">Retorna um dos seguintes tipos de divisão de arquivo:</span><span class="sxs-lookup"><span data-stu-id="f49f1-414">Returns one of the following file division types:</span></span>
<ul>
<li><span data-ttu-id="f49f1-415">PPQN</span><span class="sxs-lookup"><span data-stu-id="f49f1-415">PPQN</span></span></li>
<li><span data-ttu-id="f49f1-416">Quadro SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="f49f1-416">SMPTE 24 frame</span></span></li>
<li><span data-ttu-id="f49f1-417">Quadro SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="f49f1-417">SMPTE 25 frame</span></span></li>
<li><span data-ttu-id="f49f1-418">Quadro suspenso SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="f49f1-418">SMPTE 30 drop frame</span></span></li>
<li><span data-ttu-id="f49f1-419">Quadro SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="f49f1-419">SMPTE 30 frame</span></span></li>
</ul>
<br/> <span data-ttu-id="f49f1-420">Use essas informações para determinar o formato do arquivo MIDI e o significado das informações de tempo e de posição.</span><span class="sxs-lookup"><span data-stu-id="f49f1-420">Use this information to determine the format of the MIDI file and the meaning of tempo and position information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-421">conclusão do arquivo</span><span class="sxs-lookup"><span data-stu-id="f49f1-421">file completion</span></span></td>
<td><span data-ttu-id="f49f1-422">Retorna a porcentagem estimada em que uma operação de <a href="load.md">carregamento</a>, <a href="save.md">gravação</a>, <a href="capture.md">captura</a>, <a href="cut.md">recorte</a>, <a href="copy.md">cópia</a>, <a href="delete.md">exclusão</a>, <a href="paste.md">colagem</a>ou <a href="undo.md">desfazer</a> foi progredida.</span><span class="sxs-lookup"><span data-stu-id="f49f1-422">Returns the estimated percentage a <a href="load.md">load</a>, <a href="save.md">save</a>, <a href="capture.md">capture</a>, <a href="cut.md">cut</a>, <a href="copy.md">copy</a>, <a href="delete.md">delete</a>, <a href="paste.md">paste</a>, or <a href="undo.md">undo</a> operation has progressed.</span></span> <span data-ttu-id="f49f1-423">(Os aplicativos podem usar isso para fornecer um indicador visual de progresso.)</span><span class="sxs-lookup"><span data-stu-id="f49f1-423">(Applications can use this to provide a visual indicator of progress.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-424">formato de arquivo</span><span class="sxs-lookup"><span data-stu-id="f49f1-424">file format</span></span></td>
<td><span data-ttu-id="f49f1-425">Retorna o formato de arquivo atual para <a href="record.md">gravar</a> ou <strong>salvar</strong> comandos.</span><span class="sxs-lookup"><span data-stu-id="f49f1-425">Returns the current file format for <a href="record.md">record</a> or <strong>save</strong> commands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-426">modo de arquivo</span><span class="sxs-lookup"><span data-stu-id="f49f1-426">file mode</span></span></td>
<td><span data-ttu-id="f49f1-427">Retorna o &quot; carregamento, a gravação, a &quot; &quot; &quot; &quot; edição ou a &quot; &quot; ociosidade &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-427">Returns &quot;loading&quot;, &quot;saving&quot;, &quot;editing&quot;, or &quot;idle&quot;.</span></span> <span data-ttu-id="f49f1-428">Durante uma operação de <a href="load.md"><strong>carregamento</strong></a> , ele retorna o &quot; carregamento &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-428">During a <a href="load.md"><strong>load</strong></a> operation, it returns &quot;loading&quot;.</span></span> <span data-ttu-id="f49f1-429">Durante as operações de <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>salvar</strong></a> e <a href="capture.md"><strong>capturar</strong></a> , ele retorna &quot; salvando &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-429">During <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>save</strong></a> and <a href="capture.md"><strong>capture</strong></a> operations, it returns &quot;saving&quot;.</span></span> <span data-ttu-id="f49f1-430">Durante as operações <a href="cut.md"><strong>recortar</strong></a>, <a href="copy.md"><strong>copiar</strong></a>, <a href="delete.md"><strong>excluir</strong></a>, <a href="paste.md"><strong>colar</strong></a>ou <a href="undo.md"><strong>desfazer</strong></a> , ela retorna &quot; edição &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-430">During <a href="cut.md"><strong>cut</strong></a>, <a href="copy.md"><strong>copy</strong></a>, <a href="delete.md"><strong>delete</strong></a>, <a href="paste.md"><strong>paste</strong></a>, or <a href="undo.md"><strong>undo</strong></a> operations, it returns &quot;editing&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-431">marca de formato</span><span class="sxs-lookup"><span data-stu-id="f49f1-431">format tag</span></span></td>
<td><span data-ttu-id="f49f1-432">Retorna a marca de formato.</span><span class="sxs-lookup"><span data-stu-id="f49f1-432">Returns the format tag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-433">avançar</span><span class="sxs-lookup"><span data-stu-id="f49f1-433">forward</span></span></td>
<td><span data-ttu-id="f49f1-434">Retornará <strong>true</strong> se a direção de reprodução for encaminhada ou se o dispositivo não estiver sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="f49f1-434">Returns <strong>TRUE</strong> if the play direction is forward or if the device is not playing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-435">taxa de quadros</span><span class="sxs-lookup"><span data-stu-id="f49f1-435">frame rate</span></span></td>
<td><span data-ttu-id="f49f1-436">Retorna o número de quadros por segundo que o dispositivo usará por padrão.</span><span class="sxs-lookup"><span data-stu-id="f49f1-436">Returns the number of frames per second that the device will use by default.</span></span> <span data-ttu-id="f49f1-437">Os dispositivos NTSC retornam 30, PAL 25 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f49f1-437">NTSC devices return 30, PAL 25, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-438">quadros ignorados</span><span class="sxs-lookup"><span data-stu-id="f49f1-438">frames skipped</span></span></td>
<td><span data-ttu-id="f49f1-439">Retorna o número de quadros que não foram desenhados quando a última sequência AVI foi reproduzida.</span><span class="sxs-lookup"><span data-stu-id="f49f1-439">Returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="f49f1-440">Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="f49f1-440">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="f49f1-441">Ele destina-se apenas à avaliação de desempenho; o valor de retorno é difícil de interpretar.</span><span class="sxs-lookup"><span data-stu-id="f49f1-441">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-442">gamma</span><span class="sxs-lookup"><span data-stu-id="f49f1-442">gamma</span></span></td>
<td><span data-ttu-id="f49f1-443">Retorna o valor definido com <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gama para &quot; <em>valor</em>.</span><span class="sxs-lookup"><span data-stu-id="f49f1-443">Returns the value set with <a href="setvideo.md"><strong>setvideo</strong></a> &quot;gamma to&quot; <em>value</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-444">índice</span><span class="sxs-lookup"><span data-stu-id="f49f1-444">index</span></span></td>
<td><span data-ttu-id="f49f1-445">Retorna a exibição do índice atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-445">Returns the current index display.</span></span> <span data-ttu-id="f49f1-446">Para obter mais informações, consulte o comando <a href="set.md"><strong>set</strong></a> &quot; index &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-446">For more information, see the <a href="set.md"><strong>set</strong></a> &quot;index&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-447">índice ativado</span><span class="sxs-lookup"><span data-stu-id="f49f1-447">index on</span></span></td>
<td><span data-ttu-id="f49f1-448">Retornará <strong>true</strong> se o índice estiver ativado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-448">Returns <strong>TRUE</strong> if the index is on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-449">input</span><span class="sxs-lookup"><span data-stu-id="f49f1-449">input</span></span></td>
<td><span data-ttu-id="f49f1-450">Retorna o conjunto de entrada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-450">Returns the input set.</span></span> <span data-ttu-id="f49f1-451">Se um não for definido, o erro retornado indica que qualquer dispositivo pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-451">If one is not set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="f49f1-452">Para dispositivos de vídeo digital, o modifica os &quot; graves &quot; , os &quot; agudos &quot; , o &quot; volume, o &quot; &quot; brilho, a &quot; &quot; cor, o &quot; contraste, o gama, a &quot; &quot; &quot; &quot; &quot; nitidez ou o sinalizador de &quot; &quot; tonalidade &quot; para que ele se aplique somente à entrada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-452">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the input.</span></span> <span data-ttu-id="f49f1-453">Esse é o padrão ao monitorar a entrada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-453">This is the default when monitoring the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-454">volume esquerdo</span><span class="sxs-lookup"><span data-stu-id="f49f1-454">left volume</span></span></td>
<td><span data-ttu-id="f49f1-455">Retorna o conjunto de volumes para o canal de áudio à esquerda.</span><span class="sxs-lookup"><span data-stu-id="f49f1-455">Returns the volume set for the left audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-456">comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-456">length</span></span></td>
<td><span data-ttu-id="f49f1-457">Retorna o comprimento total da mídia, no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-457">Returns the total length of the media, in the current time format.</span></span> <span data-ttu-id="f49f1-458">Para arquivos PPQN, o comprimento é retornado em unidades de ponteiro de música.</span><span class="sxs-lookup"><span data-stu-id="f49f1-458">For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="f49f1-459">Para arquivos SMPTE, ele é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames.</span><span class="sxs-lookup"><span data-stu-id="f49f1-459">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="f49f1-460">Para dispositivos VCR, o comprimento é de 2 horas (a menos que o comprimento tenha sido explicitamente alterado usando o comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> ).</span><span class="sxs-lookup"><span data-stu-id="f49f1-460">For VCR devices, the length is 2 hours (unless the length has been explicitly changed using the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> command).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-461"><em>número</em> de faixa de comprimento</span><span class="sxs-lookup"><span data-stu-id="f49f1-461">length track <em>number</em></span></span></td>
<td><span data-ttu-id="f49f1-462">Retorna o comprimento da faixa, em tempo ou quadros, especificado pelo <em>número</em>. Para arquivos PPQN, o comprimento é retornado em unidades de ponteiro de música.</span><span class="sxs-lookup"><span data-stu-id="f49f1-462">Returns the length of the track, in time or frames, specified by <em>number</em>.For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="f49f1-463">Para arquivos SMPTE, ele é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames.</span><span class="sxs-lookup"><span data-stu-id="f49f1-463">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-464">nível</span><span class="sxs-lookup"><span data-stu-id="f49f1-464">level</span></span></td>
<td><span data-ttu-id="f49f1-465">Retorna o valor de exemplo de áudio PCM atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-465">Returns the current PCM audio sample value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-466">master</span><span class="sxs-lookup"><span data-stu-id="f49f1-466">master</span></span></td>
<td><span data-ttu-id="f49f1-467">Retorna &quot; MIDI &quot; , &quot; None &quot; ou &quot; SMPTE, &quot; dependendo do tipo de sincronização definida.</span><span class="sxs-lookup"><span data-stu-id="f49f1-467">Returns &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-468">mídia presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-468">media present</span></span></td>
<td><span data-ttu-id="f49f1-469">Retornará <strong>true</strong> se a mídia for inserida no dispositivo ou <strong>false</strong> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f49f1-469">Returns <strong>TRUE</strong> if the media is inserted in the device or <strong>FALSE</strong> otherwise.</span></span> <span data-ttu-id="f49f1-470">Os dispositivos Sequencer, vídeo-Overlay, digital-video e Wave-Audio retornam <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="f49f1-470">Sequencer, video-overlay, digital-video, and waveform-audio devices return <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-471">tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="f49f1-471">media type</span></span></td>
<td><span data-ttu-id="f49f1-472">Retorna o tipo da mídia.</span><span class="sxs-lookup"><span data-stu-id="f49f1-472">Returns the type of the media.</span></span> <span data-ttu-id="f49f1-473">Para VCRS, isso é &quot; 8mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; ou &quot; outros &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-473">For VCRS, this is &quot;8mm&quot;, &quot;vhs&quot;, &quot;svhs&quot;, &quot;beta&quot;, &quot;Hi8&quot;, &quot;edbeta&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="f49f1-474">Para videodiscs, isso é &quot; CAV &quot; , &quot; CLV &quot; ou &quot; outro &quot; , dependendo do tipo de VIDEODISC.</span><span class="sxs-lookup"><span data-stu-id="f49f1-474">For videodiscs, this is &quot;CAV&quot;, &quot;CLV&quot;, or &quot;other&quot;, depending on the type of videodisc.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-475">mode</span><span class="sxs-lookup"><span data-stu-id="f49f1-475">mode</span></span></td>
<td><span data-ttu-id="f49f1-476">Retorna o modo atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-476">Returns the current mode of the device.</span></span> <span data-ttu-id="f49f1-477">Todos os dispositivos podem retornar os &quot; valores não prontos &quot; , &quot; &quot; em pausa, &quot; &quot; em execução e &quot; parado &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-477">All devices can return the &quot;not ready&quot;, &quot;paused&quot;, &quot;playing&quot;, and &quot;stopped&quot; values.</span></span> <span data-ttu-id="f49f1-478">Alguns dispositivos podem retornar os &quot; valores adicionais abrir &quot; , &quot; estacionados &quot; , de &quot; gravação e de &quot; &quot; busca &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-478">Some devices can return the additional &quot;open&quot;, &quot;parked&quot;, &quot;recording&quot;, and &quot;seeking&quot; values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-479">monitor</span><span class="sxs-lookup"><span data-stu-id="f49f1-479">monitor</span></span></td>
<td><span data-ttu-id="f49f1-480">Retorna o &quot; arquivo &quot; ou a &quot; entrada &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-480">Returns &quot;file&quot; or &quot;input&quot;.</span></span> <span data-ttu-id="f49f1-481">O valor retornado indica a fonte da apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-481">The returned value indicates the current presentation source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-482">método de monitor</span><span class="sxs-lookup"><span data-stu-id="f49f1-482">monitor method</span></span></td>
<td><span data-ttu-id="f49f1-483">Retorna &quot; pre &quot; , &quot; post &quot; ou &quot; Direct &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-483">Returns &quot;pre&quot;, &quot;post&quot;, or &quot;direct&quot;.</span></span> <span data-ttu-id="f49f1-484">O valor retornado indica o método usado para o monitoramento de entrada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-484">The returned value indicates the method used for input monitoring.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-485">nominal</span><span class="sxs-lookup"><span data-stu-id="f49f1-485">nominal</span></span></td>
<td><span data-ttu-id="f49f1-486">O item modifica os &quot; graves &quot; , &quot; brilho &quot; , &quot; cor &quot; , &quot; contraste &quot; , &quot; gama &quot; , &quot; nitidez &quot; , &quot; tonalidade &quot; , &quot; agudos &quot; e sinalizadores de &quot; volume &quot; para retornar o valor nominal em vez da configuração atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-486">The item modifies the &quot;bass&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, &quot;tint&quot;, &quot;treble,&quot; and &quot;volume&quot; flags to return the nominal value instead of the current setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-487">taxa de quadros nominal</span><span class="sxs-lookup"><span data-stu-id="f49f1-487">nominal frame rate</span></span></td>
<td><span data-ttu-id="f49f1-488">Retorna a taxa de quadros nominal associada ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-488">Returns the nominal frame rate associated with the file.</span></span> <span data-ttu-id="f49f1-489">As unidades estão em quadros por segundo multiplicadas por 1000.</span><span class="sxs-lookup"><span data-stu-id="f49f1-489">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-490">taxa de quadros de registro nominal</span><span class="sxs-lookup"><span data-stu-id="f49f1-490">nominal record frame rate</span></span></td>
<td><span data-ttu-id="f49f1-491">Retorna a taxa de quadros nominal associada ao sinal de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-491">Returns the nominal frame rate associated with the input video signal.</span></span> <span data-ttu-id="f49f1-492">As unidades estão em quadros por segundo multiplicadas por 1000.</span><span class="sxs-lookup"><span data-stu-id="f49f1-492">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-493">número de faixas de áudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-493">number of audio tracks</span></span></td>
<td><span data-ttu-id="f49f1-494">Retorna o número de faixas de áudio na mídia.</span><span class="sxs-lookup"><span data-stu-id="f49f1-494">Returns the number of audio tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-495">número de faixas</span><span class="sxs-lookup"><span data-stu-id="f49f1-495">number of tracks</span></span></td>
<td><span data-ttu-id="f49f1-496">Retorna o número de faixas na mídia.</span><span class="sxs-lookup"><span data-stu-id="f49f1-496">Returns the number of tracks on the media.</span></span> <span data-ttu-id="f49f1-497">Os dispositivos MCISEQ e MCIWAVE retornam 1, assim como a maioria dos dispositivos VCR.</span><span class="sxs-lookup"><span data-stu-id="f49f1-497">The MCISEQ and MCIWAVE devices return 1, as do most VCR devices.</span></span> <span data-ttu-id="f49f1-498">O dispositivo MCIPIONR não dá suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="f49f1-498">The MCIPIONR device does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-499">número de faixas de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-499">number of video tracks</span></span></td>
<td><span data-ttu-id="f49f1-500">Retorna o número de faixas de vídeo na mídia.</span><span class="sxs-lookup"><span data-stu-id="f49f1-500">Returns the number of video tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-501">deslocamento</span><span class="sxs-lookup"><span data-stu-id="f49f1-501">offset</span></span></td>
<td><span data-ttu-id="f49f1-502">Retorna o deslocamento de um arquivo baseado em SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f49f1-502">Returns the offset of a SMPTE-based file.</span></span> <span data-ttu-id="f49f1-503">O deslocamento é a hora de início de uma sequência baseada em SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f49f1-503">The offset is the start time of a SMPTE-based sequence.</span></span> <span data-ttu-id="f49f1-504">O tempo é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames.</span><span class="sxs-lookup"><span data-stu-id="f49f1-504">The time is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-505">output</span><span class="sxs-lookup"><span data-stu-id="f49f1-505">output</span></span></td>
<td><span data-ttu-id="f49f1-506">Retorna a saída definida atualmente.</span><span class="sxs-lookup"><span data-stu-id="f49f1-506">Returns the currently set output.</span></span> <span data-ttu-id="f49f1-507">Se nenhuma saída for definida, o erro retornado indica que qualquer dispositivo pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-507">If no output is set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="f49f1-508">Para dispositivos de vídeo digital, o modifica os &quot; graves &quot; , os &quot; agudos &quot; , o &quot; volume, o &quot; &quot; brilho, a &quot; &quot; cor, o &quot; contraste, o gama, a &quot; &quot; &quot; &quot; &quot; nitidez ou o sinalizador de &quot; &quot; tonalidade &quot; para que ele se aplique somente à saída.</span><span class="sxs-lookup"><span data-stu-id="f49f1-508">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the output.</span></span> <span data-ttu-id="f49f1-509">Esse é o padrão ao monitorar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-509">This is the default when monitoring a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-510">modo de pausa</span><span class="sxs-lookup"><span data-stu-id="f49f1-510">pause mode</span></span></td>
<td><span data-ttu-id="f49f1-511">Retornará &quot; &quot; a gravação se o dispositivo estiver em pausa durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="f49f1-511">Returns &quot;recording&quot; if the device is paused while recording.</span></span> <span data-ttu-id="f49f1-512">Ele retornará a &quot; reprodução &quot; se o dispositivo estiver em pausa durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="f49f1-512">It returns &quot;playing&quot; if the device is paused while playing.</span></span> <span data-ttu-id="f49f1-513">Ele retornará a ação de erro &quot; não aplicável no modo atual &quot; se o dispositivo não estiver em pausa.</span><span class="sxs-lookup"><span data-stu-id="f49f1-513">It returns the error &quot;Action not applicable in current mode&quot; if the device is not paused.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-514">tempo limite de pausa</span><span class="sxs-lookup"><span data-stu-id="f49f1-514">pause timeout</span></span></td>
<td><span data-ttu-id="f49f1-515">Retorna a duração máxima, em milissegundos, de um comando de <a href="pause.md"><strong>pausa</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f49f1-515">Returns the maximum duration, in milliseconds, of a <a href="pause.md"><strong>pause</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-516">formato de reprodução</span><span class="sxs-lookup"><span data-stu-id="f49f1-516">play format</span></span></td>
<td><span data-ttu-id="f49f1-517">Retorna um código que indica o formato em que a fita de vídeo será reproduzida, se detectável: &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; ou &quot; outro &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-517">Returns a code indicating the format that the videotape will be played back in, if detectable: &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="f49f1-518">Para obter mais informações, consulte o &quot; sinalizador de formato de registro &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-518">For more information, see the &quot;record format&quot; flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-519">velocidade de reprodução</span><span class="sxs-lookup"><span data-stu-id="f49f1-519">play speed</span></span></td>
<td><span data-ttu-id="f49f1-520">Retorna um valor que representa a precisão da hora de execução real da última sequência AVI correspondente ao tempo de execução de destino.</span><span class="sxs-lookup"><span data-stu-id="f49f1-520">Returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="f49f1-521">O valor 1000 indica que a hora de destino e a hora real foram as mesmas.</span><span class="sxs-lookup"><span data-stu-id="f49f1-521">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="f49f1-522">Um valor de 2000, por exemplo, indicaria que a sequência AVI levou duas vezes mais tempo que deveria ter.</span><span class="sxs-lookup"><span data-stu-id="f49f1-522">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="f49f1-523">Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="f49f1-523">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="f49f1-524">Ele destina-se apenas à avaliação de desempenho; o valor de retorno é difícil de interpretar.</span><span class="sxs-lookup"><span data-stu-id="f49f1-524">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-525">porta</span><span class="sxs-lookup"><span data-stu-id="f49f1-525">port</span></span></td>
<td><span data-ttu-id="f49f1-526">Retorna o número da porta MIDI atribuído à sequência.</span><span class="sxs-lookup"><span data-stu-id="f49f1-526">Returns the MIDI port number assigned to the sequence.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-527">position</span><span class="sxs-lookup"><span data-stu-id="f49f1-527">position</span></span></td>
<td><span data-ttu-id="f49f1-528">Retorna a posição atual. Para arquivos PPQN, a posição é retornada em unidades de ponteiro de música.</span><span class="sxs-lookup"><span data-stu-id="f49f1-528">Returns the current position.For PPQN files, the position is returned in song pointer units.</span></span> <span data-ttu-id="f49f1-529">Para arquivos SMPTE, ele é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, SS é segundos e <em>FF</em> é frames.</span><span class="sxs-lookup"><span data-stu-id="f49f1-529">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, ss is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-530">início da posição</span><span class="sxs-lookup"><span data-stu-id="f49f1-530">position start</span></span></td>
<td><span data-ttu-id="f49f1-531">Retorna a posição do início da mídia utilizável.</span><span class="sxs-lookup"><span data-stu-id="f49f1-531">Returns the position of the start of the usable media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-532"><em>número</em> da faixa de posição</span><span class="sxs-lookup"><span data-stu-id="f49f1-532">position track <em>number</em></span></span></td>
<td><span data-ttu-id="f49f1-533">Retorna a posição do início da faixa especificada pelo <em>número</em>.</span><span class="sxs-lookup"><span data-stu-id="f49f1-533">Returns the position of the start of the track specified by <em>number</em>.</span></span> <span data-ttu-id="f49f1-534">Para arquivos PPQN, o formato de hora é retornado em unidades de ponteiro de música.</span><span class="sxs-lookup"><span data-stu-id="f49f1-534">For PPQN files, the time format is returned in song pointer units.</span></span> <span data-ttu-id="f49f1-535">Para arquivos SMPTE, ele é retornado como <em>hh: mm: SS: FF</em>, em que <em>hh</em> é horas, <em>mm</em> é minutos, <em>SS</em> é segundos e <em>FF</em> é frames.</span><span class="sxs-lookup"><span data-stu-id="f49f1-535">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="f49f1-536">O sequenciador MCISEQ retorna zero.</span><span class="sxs-lookup"><span data-stu-id="f49f1-536">The MCISEQ sequencer returns zero.</span></span> <span data-ttu-id="f49f1-537">O dispositivo MCIPIONR não dá suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="f49f1-537">The MCIPIONR device does not support this flag.</span></span> <span data-ttu-id="f49f1-538">O dispositivo MCIWAVE retorna zero.</span><span class="sxs-lookup"><span data-stu-id="f49f1-538">The MCIWAVE device returns zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-539">duração do registro</span><span class="sxs-lookup"><span data-stu-id="f49f1-539">postroll duration</span></span></td>
<td><span data-ttu-id="f49f1-540">Retorna o comprimento da fita de vídeo, no formato de hora atual, necessário para <a href="stop.md"><strong>finalizar</strong></a> o transporte de videocassete quando um comando Stop ou <a href="pause.md"><strong>Pause</strong></a> é emitido.</span><span class="sxs-lookup"><span data-stu-id="f49f1-540">Returns the length of videotape, in the current time format, needed to brake the VCR transport when a <a href="stop.md"><strong>stop</strong></a> or <a href="pause.md"><strong>pause</strong></a> command is issued.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-541">ligar</span><span class="sxs-lookup"><span data-stu-id="f49f1-541">power on</span></span></td>
<td><span data-ttu-id="f49f1-542">Retornará <strong>true</strong> se a energia do VCR estiver ativada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-542">Returns <strong>TRUE</strong> if the VCR's power is on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-543">duração da preversão</span><span class="sxs-lookup"><span data-stu-id="f49f1-543">preroll duration</span></span></td>
<td><span data-ttu-id="f49f1-544">Retorna o comprimento da fita de vídeo, no formato de hora atual, necessário para estabilizar a saída de videocassete.</span><span class="sxs-lookup"><span data-stu-id="f49f1-544">Returns the length of videotape, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-545">esteja</span><span class="sxs-lookup"><span data-stu-id="f49f1-545">ready</span></span></td>
<td><span data-ttu-id="f49f1-546">Retornará <strong>true</strong> se o dispositivo estiver pronto para aceitar outro comando.</span><span class="sxs-lookup"><span data-stu-id="f49f1-546">Returns <strong>TRUE</strong> if the device is ready to accept another command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-547">formato de registro</span><span class="sxs-lookup"><span data-stu-id="f49f1-547">record format</span></span></td>
<td><span data-ttu-id="f49f1-548">Retorna um código que indica o formato em que a fita de vídeo será gravada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-548">Returns a code indicating the format that the videotape will be recorded in.</span></span> <span data-ttu-id="f49f1-549">Os tipos de retorno atuais são &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; ou &quot; outros &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-549">The current return types are &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="f49f1-550">Esses formatos não são específicos de VHS e podem ser aplicados a qualquer VCR que tenha vários formatos de gravação selecionáveis.</span><span class="sxs-lookup"><span data-stu-id="f49f1-550">These formats are not VHS specific and can be applied to any VCR that has multiple selectable recording formats.</span></span> <span data-ttu-id="f49f1-551">O &quot; tipo de SP &quot; é o formato de gravação mais rápido e de mais alta qualidade e é usado como padrão em VCRs de formato único.</span><span class="sxs-lookup"><span data-stu-id="f49f1-551">The &quot;sp&quot; type is the fastest, highest quality recording format and is used as default on single format VCRs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-552">taxa de quadros de registro</span><span class="sxs-lookup"><span data-stu-id="f49f1-552">record frame rate</span></span></td>
<td><span data-ttu-id="f49f1-553">Retorna a taxa de quadros, em quadros por segundo, multiplicado por 1000, usado para compactação.</span><span class="sxs-lookup"><span data-stu-id="f49f1-553">Returns the frame rate, in frames per second multiplied by 1000, used for compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-554"><em>quadro</em> de referência</span><span class="sxs-lookup"><span data-stu-id="f49f1-554">reference <em>frame</em></span></span></td>
<td><span data-ttu-id="f49f1-555">Retorna o número do quadro da imagem do quadro de chave mais próxima que precede o <em>quadro</em>especificado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-555">Returns the frame number for the nearest key frame image that precedes the specified <em>frame</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-556">Tamanho reservado</span><span class="sxs-lookup"><span data-stu-id="f49f1-556">reserved size</span></span></td>
<td><span data-ttu-id="f49f1-557">Retorna o tamanho, no formato de hora atual, do espaço de trabalho reservado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-557">Returns the size, in the current time format, of the reserved workspace.</span></span> <span data-ttu-id="f49f1-558">O tamanho corresponde ao tempo aproximado que levaria para reproduzir os dados compactados de um espaço de trabalho completo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-558">The size corresponds to the approximate time it would take to play the compressed data from a full workspace.</span></span> <span data-ttu-id="f49f1-559">Ele retornará zero se não houver espaço reservado em disco.</span><span class="sxs-lookup"><span data-stu-id="f49f1-559">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="f49f1-560">Esse sinalizador retorna o tamanho aproximado porque o espaço em disco preciso para dados compactados não pode, em geral, ser previsto até que os dados sejam compactados.</span><span class="sxs-lookup"><span data-stu-id="f49f1-560">This flag returns the approximate size because the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-561">volume correto</span><span class="sxs-lookup"><span data-stu-id="f49f1-561">right volume</span></span></td>
<td><span data-ttu-id="f49f1-562">Retorna o conjunto de volumes para o canal de áudio correto.</span><span class="sxs-lookup"><span data-stu-id="f49f1-562">Returns the volume set for the right audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-563">samplespersec</span><span class="sxs-lookup"><span data-stu-id="f49f1-563">samplespersec</span></span></td>
<td><span data-ttu-id="f49f1-564">Retorna o número de amostras por segundo reproduzidas ou registradas.</span><span class="sxs-lookup"><span data-stu-id="f49f1-564">Returns the number of samples per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-565">buscar exatamente</span><span class="sxs-lookup"><span data-stu-id="f49f1-565">seek exactly</span></span></td>
<td><span data-ttu-id="f49f1-566">Retorna &quot; on &quot; ou &quot; off &quot; , indicando se o sinalizador de &quot; busca exata &quot; está ou não definido.</span><span class="sxs-lookup"><span data-stu-id="f49f1-566">Returns &quot;on&quot; or &quot;off&quot;, indicating whether or not the &quot;seek exactly&quot; flag is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-567">nitidez</span><span class="sxs-lookup"><span data-stu-id="f49f1-567">sharpness</span></span></td>
<td><span data-ttu-id="f49f1-568">Retorna o nível de nitidez atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-568">Returns the current sharpness level of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-569">residente</span><span class="sxs-lookup"><span data-stu-id="f49f1-569">side</span></span></td>
<td><span data-ttu-id="f49f1-570">Retorna 1 ou 2 para indicar qual lado do VIDEODISC é carregado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-570">Returns 1 or 2 to indicate which side of the videodisc is loaded.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-571">subordinado</span><span class="sxs-lookup"><span data-stu-id="f49f1-571">slave</span></span></td>
<td><span data-ttu-id="f49f1-572">Retorna &quot; arquivo &quot; , &quot; MIDI &quot; , &quot; nenhum &quot; ou &quot; SMPTE, &quot; dependendo do tipo de sincronização definido.</span><span class="sxs-lookup"><span data-stu-id="f49f1-572">Returns &quot;file&quot; , &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-573">SMPTE</span><span class="sxs-lookup"><span data-stu-id="f49f1-573">smpte</span></span></td>
<td><span data-ttu-id="f49f1-574">Retorna o código de tempo SMPTE associado à posição atual no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f49f1-574">Returns the SMPTE timecode associated with the current position in the workspace.</span></span> <span data-ttu-id="f49f1-575">Esta é uma cadeia de caracteres com o formato <em>DD: DD: DD: DD</em>, em que cada <em>d</em> denota um dígito de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="f49f1-575">This is a string with the form <em>dd:dd:dd:dd</em>, where each <em>d</em> denotes a digit from 0 to 9.</span></span> <span data-ttu-id="f49f1-576">Se os dados do espaço de trabalho não incluírem dados de código de data, esse sinalizador retornará 00:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="f49f1-576">If the workspace data does not include timecode data, then this flag returns 00:00:00:00.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-577">velocidade</span><span class="sxs-lookup"><span data-stu-id="f49f1-577">speed</span></span></td>
<td><span data-ttu-id="f49f1-578">Retorna a velocidade atual do dispositivo em quadros por segundo (ou no mesmo formato usado pelo comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot; Speed &quot; ).</span><span class="sxs-lookup"><span data-stu-id="f49f1-578">Returns the current speed of the device in frames per second (or in the same format used by the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot;speed&quot; command).</span></span> <span data-ttu-id="f49f1-579">O MCIPIONR VIDEODISC Player não dá suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="f49f1-579">The MCIPIONR videodisc player does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-580">posição inicial</span><span class="sxs-lookup"><span data-stu-id="f49f1-580">start position</span></span></td>
<td><span data-ttu-id="f49f1-581">Retorna a posição inicial da mídia.</span><span class="sxs-lookup"><span data-stu-id="f49f1-581">Returns the starting position of the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-582">formato de arquivo ainda</span><span class="sxs-lookup"><span data-stu-id="f49f1-582">still file format</span></span></td>
<td><span data-ttu-id="f49f1-583">Retorna o formato de arquivo atual para o comando de <a href="capture.md"><strong>captura</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f49f1-583">Returns the current file format for the <a href="capture.md"><strong>capture</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-584">Estendi</span><span class="sxs-lookup"><span data-stu-id="f49f1-584">stretch</span></span></td>
<td><span data-ttu-id="f49f1-585">Retornará <strong>true</strong> se o alongamento estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-585">Returns <strong>TRUE</strong> if stretching is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-586">golpe</span><span class="sxs-lookup"><span data-stu-id="f49f1-586">tempo</span></span></td>
<td><span data-ttu-id="f49f1-587">Retorna o tempo atual de uma sequência de MIDI no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-587">Returns the current tempo of a MIDI sequence in the current time format.</span></span> <span data-ttu-id="f49f1-588">Para arquivos com o formato PPQN, o tempo é em batidas por minuto.</span><span class="sxs-lookup"><span data-stu-id="f49f1-588">For files with PPQN format, the tempo is in beats per minute.</span></span> <span data-ttu-id="f49f1-589">Para arquivos com formato SMPTE, o tempo é em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-589">For files with SMPTE format, the tempo is in frames per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-590">formato de hora</span><span class="sxs-lookup"><span data-stu-id="f49f1-590">time format</span></span></td>
<td><span data-ttu-id="f49f1-591">Retorna o formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-591">Returns the current time format.</span></span> <span data-ttu-id="f49f1-592">Para obter mais informações, consulte os formatos de hora no comando <a href="set.md"><strong>set</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f49f1-592">For more information, see the time formats in the <a href="set.md"><strong>set</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-593">modo de tempo</span><span class="sxs-lookup"><span data-stu-id="f49f1-593">time mode</span></span></td>
<td><span data-ttu-id="f49f1-594">Retorna o modo de tempo de posição atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-594">Returns the current position time mode.</span></span> <span data-ttu-id="f49f1-595">Ele pode ser &quot; detectado &quot; , &quot; código &quot; de Code ou &quot; contador &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-595">It can be &quot;detect&quot;, &quot;timecode&quot;, or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-596">tipo de hora</span><span class="sxs-lookup"><span data-stu-id="f49f1-596">time type</span></span></td>
<td><span data-ttu-id="f49f1-597">Retorna o tempo de posição atual em uso: &quot; código &quot; de hora ou &quot; contador &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-597">Returns the current position time in use: &quot;timecode&quot; or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-598">código de paficação presente</span><span class="sxs-lookup"><span data-stu-id="f49f1-598">timecode present</span></span></td>
<td><span data-ttu-id="f49f1-599">Retorna <strong>true</strong> se o código de tempo tiver sido registrado na posição atual na fita.</span><span class="sxs-lookup"><span data-stu-id="f49f1-599">Returns <strong>TRUE</strong> if timecode has been recorded at the current position on the tape.</span></span> <span data-ttu-id="f49f1-600">O código de tempo deve avançar da posição atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-600">The timecode must advance from the current position.</span></span> <span data-ttu-id="f49f1-601">Talvez seja necessário reproduzir um videocassete para verificar essa condição.</span><span class="sxs-lookup"><span data-stu-id="f49f1-601">A VCR might need to be played to check this condition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-602">registro de código de histórico</span><span class="sxs-lookup"><span data-stu-id="f49f1-602">timecode record</span></span></td>
<td><span data-ttu-id="f49f1-603">Retornará <strong>true</strong> se o VCR estiver definido para registrar o código de pafica.</span><span class="sxs-lookup"><span data-stu-id="f49f1-603">Returns <strong>TRUE</strong> if the VCR is set to record timecode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-604">tipo de código de Code</span><span class="sxs-lookup"><span data-stu-id="f49f1-604">timecode type</span></span></td>
<td><span data-ttu-id="f49f1-605">Retorna &quot; SMPTE &quot; , &quot; SMPTE Drop &quot; , &quot; outro &quot; ou &quot; nenhum &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-605">Returns &quot;smpte&quot;, &quot;smpte drop&quot;, &quot;other&quot;, or &quot;none&quot;.</span></span> <span data-ttu-id="f49f1-606">Observe que os quadros por segundo podem ser obtidos do comando de taxa de quadros de status &quot; &quot; e a precisão do dispositivo pode ser retornada pelo comando de precisão de busca de <a href="capability.md"><strong>funcionalidade</strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-606">Note the frames per second can be obtained from the status &quot;frame rate&quot; command, and the accuracy of the device can be returned by the <a href="capability.md"><strong>capability</strong></a> &quot;seek accuracy&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-607">Nuance</span><span class="sxs-lookup"><span data-stu-id="f49f1-607">tint</span></span></td>
<td><span data-ttu-id="f49f1-608">Retorna o nível de tonalidade de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-608">Returns the current video-tint level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-609">agudo</span><span class="sxs-lookup"><span data-stu-id="f49f1-609">treble</span></span></td>
<td><span data-ttu-id="f49f1-610">Retorna o nível de áudio-agudo atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-610">Returns the current audio-treble level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-611">número do sintonizador</span><span class="sxs-lookup"><span data-stu-id="f49f1-611">tuner number</span></span></td>
<td><span data-ttu-id="f49f1-612">Retorna o número do sintonizador lógico atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-612">Returns the current logical-tuner number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-613">não salvas</span><span class="sxs-lookup"><span data-stu-id="f49f1-613">unsaved</span></span></td>
<td><span data-ttu-id="f49f1-614">Retorna <strong>true</strong> se houver dados registrados no espaço de trabalho que podem ser perdidos como resultado de um comando <a href="close.md"><strong>Close</strong></a>, <a href="load.md"><strong>Load</strong></a>, <a href="record.md"><strong>Record</strong></a>, <a href="reserve.md"><strong>Reserve</strong></a>, <a href="cut.md"><strong>Cut</strong></a>, <a href="delete.md"><strong>delete</strong></a>ou <a href="paste.md"><strong>Paste</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f49f1-614">Returns <strong>TRUE</strong> if there is recorded data in the workspace that might be lost as a result of a <a href="close.md"><strong>close</strong></a>, <a href="load.md"><strong>load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>reserve</strong></a>, <a href="cut.md"><strong>cut</strong></a>, <a href="delete.md"><strong>delete</strong></a>, or <a href="paste.md"><strong>paste</strong></a> command.</span></span> <span data-ttu-id="f49f1-615">Retorna <strong>false</strong> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f49f1-615">Returns <strong>FALSE</strong> otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-616">video</span><span class="sxs-lookup"><span data-stu-id="f49f1-616">video</span></span></td>
<td><span data-ttu-id="f49f1-617">Retorna &quot; on &quot; ou &quot; off &quot; , refletindo o estado definido pelo comando <a href="setvideo.md"><strong>setvideo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f49f1-617">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-618">cor da chave do vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-618">video key color</span></span></td>
<td><span data-ttu-id="f49f1-619">Retorna o valor da cor da chave.</span><span class="sxs-lookup"><span data-stu-id="f49f1-619">Returns the value for the key color.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-620">índice de chave de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-620">video key index</span></span></td>
<td><span data-ttu-id="f49f1-621">Retorna o valor para o índice de chave.</span><span class="sxs-lookup"><span data-stu-id="f49f1-621">Returns the value for the key index.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-622">monitor de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-622">video monitor</span></span></td>
<td><span data-ttu-id="f49f1-623">Retorna &quot; &quot; a saída ou um dos tipos de entrada de origem válidos.</span><span class="sxs-lookup"><span data-stu-id="f49f1-623">Returns &quot;output&quot; or one of the valid source-input types.</span></span> <span data-ttu-id="f49f1-624">Para obter mais informações, consulte o comando monitor <a href="setvideo.md"><strong>setvideo</strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-624">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-625">número do monitor de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-625">video monitor number</span></span></td>
<td><span data-ttu-id="f49f1-626">Retorna o número monitorado de vídeo do tipo retornado pelo monitor de vídeo de status &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-626">Returns the monitored-video number of the type returned by status &quot;video monitor&quot;.</span></span> <span data-ttu-id="f49f1-627">Para obter mais informações, consulte o comando <a href="setvideo.md">setvideo</a> .</span><span class="sxs-lookup"><span data-stu-id="f49f1-627">For more information, see the <a href="setvideo.md">setvideo</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-628">registro de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-628">video record</span></span></td>
<td><span data-ttu-id="f49f1-629">Retorna &quot; ativado &quot; ou &quot; desativado &quot; , refletindo o estado atual definido pelo registro de conjunto de <a href="setvideo.md"><strong>vídeos</strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f49f1-629">Returns &quot;on&quot; or &quot;off&quot;, reflecting the current state set by <a href="setvideo.md"><strong>setvideo</strong></a> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-630"><em>número</em> de faixa do registro de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-630">video record track <em>number</em></span></span></td>
<td><span data-ttu-id="f49f1-631">Retornará <strong>true</strong> se o VCR estiver definido para gravar vídeo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-631">Return <strong>TRUE</strong> if the VCR is set to record video.</span></span> <span data-ttu-id="f49f1-632">Se nenhum número de faixa for fornecido, o valor padrão de 1 será assumido.</span><span class="sxs-lookup"><span data-stu-id="f49f1-632">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-633">fonte de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-633">video source</span></span></td>
<td><span data-ttu-id="f49f1-634">Retorna o tipo de fonte de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f49f1-634">Returns the video-source type.</span></span> <span data-ttu-id="f49f1-635">Para obter mais informações, consulte o comando <a href="setvideo.md"><strong>setvideo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f49f1-635">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-636">número da fonte do vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-636">video source number</span></span></td>
<td><span data-ttu-id="f49f1-637">Retorna um número correspondente à fonte de vídeo do tipo em uso.</span><span class="sxs-lookup"><span data-stu-id="f49f1-637">Returns a number corresponding to the video source of the type in use.</span></span> <span data-ttu-id="f49f1-638">Por exemplo, ele retornará 2 se a segunda entrada de fonte de vídeo NTSC estiver sendo usada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-638">For example, it returns 2 if the second NTSC video source input is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-639">fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="f49f1-639">video stream</span></span></td>
<td><span data-ttu-id="f49f1-640">Retorna o número do fluxo de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="f49f1-640">Returns the current video-stream number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-641">volume</span><span class="sxs-lookup"><span data-stu-id="f49f1-641">volume</span></span></td>
<td><span data-ttu-id="f49f1-642">Retorna o volume médio para o alto-falante esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="f49f1-642">Returns the average volume to the left and right speaker.</span></span> <span data-ttu-id="f49f1-643">Isso retornará um erro se o dispositivo não tiver sido reproduzido ou se o volume não tiver sido definido.</span><span class="sxs-lookup"><span data-stu-id="f49f1-643">This returns an error if the device has not been played or volume has not been set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-644">identificador de janela</span><span class="sxs-lookup"><span data-stu-id="f49f1-644">window handle</span></span></td>
<td><span data-ttu-id="f49f1-645">Retorna o valor decimal ASCII para o identificador de janela na palavra de ordem inferior do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f49f1-645">Returns the ASCII decimal value for the window handle in the low-order word of the return value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-646">janela maximizada</span><span class="sxs-lookup"><span data-stu-id="f49f1-646">window maximized</span></span></td>
<td><span data-ttu-id="f49f1-647">Retornará <strong>true</strong> se a janela for maximizada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-647">Returns <strong>TRUE</strong> if the window is maximized.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-648">janela minimizada</span><span class="sxs-lookup"><span data-stu-id="f49f1-648">window minimized</span></span></td>
<td><span data-ttu-id="f49f1-649">Retornará <strong>true</strong> se a janela for minimizada.</span><span class="sxs-lookup"><span data-stu-id="f49f1-649">Returns <strong>TRUE</strong> if the window is minimized.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49f1-650">janela visível</span><span class="sxs-lookup"><span data-stu-id="f49f1-650">window visible</span></span></td>
<td><span data-ttu-id="f49f1-651">Retornará <strong>true</strong> se a janela não estiver oculta.</span><span class="sxs-lookup"><span data-stu-id="f49f1-651">Returns <strong>TRUE</strong> if the window is not hidden.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f49f1-652">protegido contra gravação</span><span class="sxs-lookup"><span data-stu-id="f49f1-652">write protected</span></span></td>
<td><span data-ttu-id="f49f1-653">Retornará <strong>true</strong> se o dispositivo detectar que ele não pode gravar (ou seja, se a proteção contra gravação estiver ativada).</span><span class="sxs-lookup"><span data-stu-id="f49f1-653">Returns <strong>TRUE</strong> if the device detects that it cannot record (that is, if the write protect is on).</span></span> <span data-ttu-id="f49f1-654">Se ele puder gravar, ou se não for possível determinar se ele pode ou não gravar (sem realmente escrever), o driver retornará <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="f49f1-654">If it can record, or if it is unable to determine whether or not it can record (without actually writing), the driver returns <strong>FALSE</strong>.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="f49f1-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f49f1-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f49f1-656">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="f49f1-656">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f49f1-657">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="f49f1-657">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="f49f1-658">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f49f1-658">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f49f1-659">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f49f1-659">Return Value</span></span>

<span data-ttu-id="f49f1-660">Retorna informações no parâmetro *lpszReturnString* de [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f49f1-660">Returns information in the *lpszReturnString* parameter of [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span></span> <span data-ttu-id="f49f1-661">As informações dependem do tipo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="f49f1-661">The information is dependent on the request type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f49f1-662">Comentários</span><span class="sxs-lookup"><span data-stu-id="f49f1-662">Remarks</span></span>

<span data-ttu-id="f49f1-663">Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="f49f1-663">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="f49f1-664">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f49f1-664">Examples</span></span>

<span data-ttu-id="f49f1-665">O comando a seguir retorna o modo atual do dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="f49f1-665">The following command returns the current mode of the "mysound" device.</span></span>

``` syntax
status mysound mode
```

## <a name="requirements"></a><span data-ttu-id="f49f1-666">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f49f1-666">Requirements</span></span>



| <span data-ttu-id="f49f1-667">Requisito</span><span class="sxs-lookup"><span data-stu-id="f49f1-667">Requirement</span></span> | <span data-ttu-id="f49f1-668">Valor</span><span class="sxs-lookup"><span data-stu-id="f49f1-668">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f49f1-669">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f49f1-669">Minimum supported client</span></span><br/> | <span data-ttu-id="f49f1-670">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f49f1-670">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f49f1-671">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f49f1-671">Minimum supported server</span></span><br/> | <span data-ttu-id="f49f1-672">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f49f1-672">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f49f1-673">Confira também</span><span class="sxs-lookup"><span data-stu-id="f49f1-673">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f49f1-674">MCI</span><span class="sxs-lookup"><span data-stu-id="f49f1-674">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f49f1-675">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="f49f1-675">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="f49f1-676">capability</span><span class="sxs-lookup"><span data-stu-id="f49f1-676">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="f49f1-677">captura</span><span class="sxs-lookup"><span data-stu-id="f49f1-677">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="f49f1-678">close</span><span class="sxs-lookup"><span data-stu-id="f49f1-678">close</span></span>](close.md)
</dt> <dt>

[<span data-ttu-id="f49f1-679">migração</span><span class="sxs-lookup"><span data-stu-id="f49f1-679">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="f49f1-680">delete</span><span class="sxs-lookup"><span data-stu-id="f49f1-680">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="f49f1-681">carga</span><span class="sxs-lookup"><span data-stu-id="f49f1-681">load</span></span>](load.md)
</dt> <dt>

[<span data-ttu-id="f49f1-682">pause</span><span class="sxs-lookup"><span data-stu-id="f49f1-682">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="f49f1-683">Olar</span><span class="sxs-lookup"><span data-stu-id="f49f1-683">paste</span></span>](paste.md)
</dt> <dt>

[<span data-ttu-id="f49f1-684">gravável</span><span class="sxs-lookup"><span data-stu-id="f49f1-684">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="f49f1-685">reservado</span><span class="sxs-lookup"><span data-stu-id="f49f1-685">reserve</span></span>](reserve.md)
</dt> <dt>

[<span data-ttu-id="f49f1-686">salvar</span><span class="sxs-lookup"><span data-stu-id="f49f1-686">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="f49f1-687">set</span><span class="sxs-lookup"><span data-stu-id="f49f1-687">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="f49f1-688">SetAudio</span><span class="sxs-lookup"><span data-stu-id="f49f1-688">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="f49f1-689">setvideo</span><span class="sxs-lookup"><span data-stu-id="f49f1-689">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="f49f1-690">stop</span><span class="sxs-lookup"><span data-stu-id="f49f1-690">stop</span></span>](stop.md)
</dt> <dt>

[<span data-ttu-id="f49f1-691">desfazer</span><span class="sxs-lookup"><span data-stu-id="f49f1-691">undo</span></span>](undo.md)
</dt> </dl>

 


---
title: comando de funcionalidade
description: O comando Capability solicita informações sobre um recurso específico de um dispositivo. Todos os dispositivos MCI reconhecem este comando.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- Multimídia do Windows de comando de funcionalidade
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454810"
---
# <a name="capability-command"></a><span data-ttu-id="9c484-105">comando de funcionalidade</span><span class="sxs-lookup"><span data-stu-id="9c484-105">capability command</span></span>

<span data-ttu-id="9c484-106">O comando Capability solicita informações sobre um recurso específico de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c484-106">The capability command requests information about a particular capability of a device.</span></span> <span data-ttu-id="9c484-107">Todos os dispositivos MCI reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="9c484-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="9c484-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="9c484-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="9c484-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c484-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c484-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9c484-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9c484-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="9c484-111">Identifier of an MCI device.</span></span> <span data-ttu-id="9c484-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="9c484-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="9c484-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="9c484-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="9c484-114">Sinalizador que identifica uma funcionalidade de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c484-114">Flag that identifies a device capability.</span></span> <span data-ttu-id="9c484-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **capacidade** e os sinalizadores usados por cada tipo:</span><span class="sxs-lookup"><span data-stu-id="9c484-115">The following table lists device types that recognize the **capability** command and the flags used by each type:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c484-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9c484-116">Value</span></span></th>
<th><span data-ttu-id="9c484-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c484-117">Type</span></span></th>
<th><span data-ttu-id="9c484-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c484-118">Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c484-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="9c484-119">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="9c484-120">pode ejetar</span><span class="sxs-lookup"><span data-stu-id="9c484-120">can eject</span></span></li>
<li><span data-ttu-id="9c484-121">pode reproduzir</span><span class="sxs-lookup"><span data-stu-id="9c484-121">can play</span></span></li>
<li><span data-ttu-id="9c484-122">pode registrar</span><span class="sxs-lookup"><span data-stu-id="9c484-122">can record</span></span></li>
<li><span data-ttu-id="9c484-123">pode salvar</span><span class="sxs-lookup"><span data-stu-id="9c484-123">can save</span></span></li>
<li><span data-ttu-id="9c484-124">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="9c484-124">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c484-125">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c484-125">device type</span></span></li>
<li><span data-ttu-id="9c484-126">com áudio</span><span class="sxs-lookup"><span data-stu-id="9c484-126">has audio</span></span></li>
<li><span data-ttu-id="9c484-127">tem vídeo</span><span class="sxs-lookup"><span data-stu-id="9c484-127">has video</span></span></li>
<li><span data-ttu-id="9c484-128">usa arquivos</span><span class="sxs-lookup"><span data-stu-id="9c484-128">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-129">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="9c484-129">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="9c484-130">pode ejetar</span><span class="sxs-lookup"><span data-stu-id="9c484-130">can eject</span></span></li>
<li><span data-ttu-id="9c484-131">pode congelar</span><span class="sxs-lookup"><span data-stu-id="9c484-131">can freeze</span></span></li>
<li><span data-ttu-id="9c484-132">pode bloquear</span><span class="sxs-lookup"><span data-stu-id="9c484-132">can lock</span></span></li>
<li><span data-ttu-id="9c484-133">pode reproduzir</span><span class="sxs-lookup"><span data-stu-id="9c484-133">can play</span></span></li>
<li><span data-ttu-id="9c484-134">pode registrar</span><span class="sxs-lookup"><span data-stu-id="9c484-134">can record</span></span></li>
<li><span data-ttu-id="9c484-135">pode reverter</span><span class="sxs-lookup"><span data-stu-id="9c484-135">can reverse</span></span></li>
<li><span data-ttu-id="9c484-136">pode salvar</span><span class="sxs-lookup"><span data-stu-id="9c484-136">can save</span></span></li>
<li><span data-ttu-id="9c484-137">pode ampliar</span><span class="sxs-lookup"><span data-stu-id="9c484-137">can stretch</span></span></li>
<li><span data-ttu-id="9c484-138">pode ampliar a entrada</span><span class="sxs-lookup"><span data-stu-id="9c484-138">can stretch input</span></span></li>
<li><span data-ttu-id="9c484-139">pode testar</span><span class="sxs-lookup"><span data-stu-id="9c484-139">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c484-140">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="9c484-140">compound device</span></span></li>
<li><span data-ttu-id="9c484-141">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c484-141">device type</span></span></li>
<li><span data-ttu-id="9c484-142">com áudio</span><span class="sxs-lookup"><span data-stu-id="9c484-142">has audio</span></span></li>
<li><span data-ttu-id="9c484-143">ainda</span><span class="sxs-lookup"><span data-stu-id="9c484-143">has still</span></span></li>
<li><span data-ttu-id="9c484-144">tem vídeo</span><span class="sxs-lookup"><span data-stu-id="9c484-144">has video</span></span></li>
<li><span data-ttu-id="9c484-145">taxa de execução máxima</span><span class="sxs-lookup"><span data-stu-id="9c484-145">maximum play rate</span></span></li>
<li><span data-ttu-id="9c484-146">taxa mínima de execução</span><span class="sxs-lookup"><span data-stu-id="9c484-146">minimum play rate</span></span></li>
<li><span data-ttu-id="9c484-147">usa arquivos</span><span class="sxs-lookup"><span data-stu-id="9c484-147">uses files</span></span></li>
<li><span data-ttu-id="9c484-148">usa paletas</span><span class="sxs-lookup"><span data-stu-id="9c484-148">uses palettes</span></span></li>
<li><span data-ttu-id="9c484-149">windows</span><span class="sxs-lookup"><span data-stu-id="9c484-149">windows</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-150">overlay</span><span class="sxs-lookup"><span data-stu-id="9c484-150">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="9c484-151">pode ejetar</span><span class="sxs-lookup"><span data-stu-id="9c484-151">can eject</span></span></li>
<li><span data-ttu-id="9c484-152">pode congelar</span><span class="sxs-lookup"><span data-stu-id="9c484-152">can freeze</span></span></li>
<li><span data-ttu-id="9c484-153">pode reproduzir</span><span class="sxs-lookup"><span data-stu-id="9c484-153">can play</span></span></li>
<li><span data-ttu-id="9c484-154">pode registrar</span><span class="sxs-lookup"><span data-stu-id="9c484-154">can record</span></span></li>
<li><span data-ttu-id="9c484-155">pode salvar</span><span class="sxs-lookup"><span data-stu-id="9c484-155">can save</span></span></li>
<li><span data-ttu-id="9c484-156">pode ampliar</span><span class="sxs-lookup"><span data-stu-id="9c484-156">can stretch</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c484-157">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="9c484-157">compound device</span></span></li>
<li><span data-ttu-id="9c484-158">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c484-158">device type</span></span></li>
<li><span data-ttu-id="9c484-159">com áudio</span><span class="sxs-lookup"><span data-stu-id="9c484-159">has audio</span></span></li>
<li><span data-ttu-id="9c484-160">tem vídeo</span><span class="sxs-lookup"><span data-stu-id="9c484-160">has video</span></span></li>
<li><span data-ttu-id="9c484-161">usa arquivos</span><span class="sxs-lookup"><span data-stu-id="9c484-161">uses files</span></span></li>
<li><span data-ttu-id="9c484-162">windows</span><span class="sxs-lookup"><span data-stu-id="9c484-162">windows</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-163">sequenciador</span><span class="sxs-lookup"><span data-stu-id="9c484-163">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="9c484-164">pode ejetar</span><span class="sxs-lookup"><span data-stu-id="9c484-164">can eject</span></span></li>
<li><span data-ttu-id="9c484-165">pode reproduzir</span><span class="sxs-lookup"><span data-stu-id="9c484-165">can play</span></span></li>
<li><span data-ttu-id="9c484-166">pode registrar</span><span class="sxs-lookup"><span data-stu-id="9c484-166">can record</span></span></li>
<li><span data-ttu-id="9c484-167">pode salvar</span><span class="sxs-lookup"><span data-stu-id="9c484-167">can save</span></span></li>
<li><span data-ttu-id="9c484-168">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="9c484-168">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c484-169">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c484-169">device type</span></span></li>
<li><span data-ttu-id="9c484-170">com áudio</span><span class="sxs-lookup"><span data-stu-id="9c484-170">has audio</span></span></li>
<li><span data-ttu-id="9c484-171">tem vídeo</span><span class="sxs-lookup"><span data-stu-id="9c484-171">has video</span></span></li>
<li><span data-ttu-id="9c484-172">usa arquivos</span><span class="sxs-lookup"><span data-stu-id="9c484-172">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-173">videocassete</span><span class="sxs-lookup"><span data-stu-id="9c484-173">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="9c484-174">pode detectar comprimento</span><span class="sxs-lookup"><span data-stu-id="9c484-174">can detect length</span></span></li>
<li><span data-ttu-id="9c484-175">pode ejetar</span><span class="sxs-lookup"><span data-stu-id="9c484-175">can eject</span></span></li>
<li><span data-ttu-id="9c484-176">pode congelar</span><span class="sxs-lookup"><span data-stu-id="9c484-176">can freeze</span></span></li>
<li><span data-ttu-id="9c484-177">pode monitorar fontes</span><span class="sxs-lookup"><span data-stu-id="9c484-177">can monitor sources</span></span></li>
<li><span data-ttu-id="9c484-178">pode reproduzir</span><span class="sxs-lookup"><span data-stu-id="9c484-178">can play</span></span></li>
<li><span data-ttu-id="9c484-179">pode ser prevertido</span><span class="sxs-lookup"><span data-stu-id="9c484-179">can preroll</span></span></li>
<li><span data-ttu-id="9c484-180">pode Visualizar</span><span class="sxs-lookup"><span data-stu-id="9c484-180">can preview</span></span></li>
<li><span data-ttu-id="9c484-181">pode registrar</span><span class="sxs-lookup"><span data-stu-id="9c484-181">can record</span></span></li>
<li><span data-ttu-id="9c484-182">pode reverter</span><span class="sxs-lookup"><span data-stu-id="9c484-182">can reverse</span></span></li>
<li><span data-ttu-id="9c484-183">pode salvar</span><span class="sxs-lookup"><span data-stu-id="9c484-183">can save</span></span></li>
<li><span data-ttu-id="9c484-184">pode testar</span><span class="sxs-lookup"><span data-stu-id="9c484-184">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c484-185">taxa de incremento de relógio</span><span class="sxs-lookup"><span data-stu-id="9c484-185">clock increment rate</span></span></li>
<li><span data-ttu-id="9c484-186">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="9c484-186">compound device</span></span></li>
<li><span data-ttu-id="9c484-187">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c484-187">device type</span></span></li>
<li><span data-ttu-id="9c484-188">com áudio</span><span class="sxs-lookup"><span data-stu-id="9c484-188">has audio</span></span></li>
<li><span data-ttu-id="9c484-189">tem relógio</span><span class="sxs-lookup"><span data-stu-id="9c484-189">has clock</span></span></li>
<li><span data-ttu-id="9c484-190">tem código de paficação</span><span class="sxs-lookup"><span data-stu-id="9c484-190">has timecode</span></span></li>
<li><span data-ttu-id="9c484-191">tem vídeo</span><span class="sxs-lookup"><span data-stu-id="9c484-191">has video</span></span></li>
<li><span data-ttu-id="9c484-192">número de marcas</span><span class="sxs-lookup"><span data-stu-id="9c484-192">number of marks</span></span></li>
<li><span data-ttu-id="9c484-193">precisão da busca</span><span class="sxs-lookup"><span data-stu-id="9c484-193">seek accuracy</span></span></li>
<li><span data-ttu-id="9c484-194">usa arquivos</span><span class="sxs-lookup"><span data-stu-id="9c484-194">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-195">videodisc</span><span class="sxs-lookup"><span data-stu-id="9c484-195">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="9c484-196">pode ejetar</span><span class="sxs-lookup"><span data-stu-id="9c484-196">can eject</span></span></li>
<li><span data-ttu-id="9c484-197">pode reproduzir</span><span class="sxs-lookup"><span data-stu-id="9c484-197">can play</span></span></li>
<li><span data-ttu-id="9c484-198">pode registrar</span><span class="sxs-lookup"><span data-stu-id="9c484-198">can record</span></span></li>
<li><span data-ttu-id="9c484-199">pode reverter</span><span class="sxs-lookup"><span data-stu-id="9c484-199">can reverse</span></span></li>
<li><span data-ttu-id="9c484-200">pode salvar</span><span class="sxs-lookup"><span data-stu-id="9c484-200">can save</span></span></li>
<li><span data-ttu-id="9c484-201">CAV</span><span class="sxs-lookup"><span data-stu-id="9c484-201">CAV</span></span></li>
<li><span data-ttu-id="9c484-202">CLV</span><span class="sxs-lookup"><span data-stu-id="9c484-202">CLV</span></span></li>
<li><span data-ttu-id="9c484-203">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="9c484-203">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c484-204">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c484-204">device type</span></span></li>
<li><span data-ttu-id="9c484-205">taxa de reprodução rápida</span><span class="sxs-lookup"><span data-stu-id="9c484-205">fast play rate</span></span></li>
<li><span data-ttu-id="9c484-206">com áudio</span><span class="sxs-lookup"><span data-stu-id="9c484-206">has audio</span></span></li>
<li><span data-ttu-id="9c484-207">tem vídeo</span><span class="sxs-lookup"><span data-stu-id="9c484-207">has video</span></span></li>
<li><span data-ttu-id="9c484-208">taxa de reprodução normal</span><span class="sxs-lookup"><span data-stu-id="9c484-208">normal play rate</span></span></li>
<li><span data-ttu-id="9c484-209">taxa de reprodução lenta</span><span class="sxs-lookup"><span data-stu-id="9c484-209">slow play rate</span></span></li>
<li><span data-ttu-id="9c484-210">usa arquivos</span><span class="sxs-lookup"><span data-stu-id="9c484-210">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-211">waveaudio</span><span class="sxs-lookup"><span data-stu-id="9c484-211">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="9c484-212">pode ejetar</span><span class="sxs-lookup"><span data-stu-id="9c484-212">can eject</span></span></li>
<li><span data-ttu-id="9c484-213">pode reproduzir</span><span class="sxs-lookup"><span data-stu-id="9c484-213">can play</span></span></li>
<li><span data-ttu-id="9c484-214">pode registrar</span><span class="sxs-lookup"><span data-stu-id="9c484-214">can record</span></span></li>
<li><span data-ttu-id="9c484-215">pode salvar</span><span class="sxs-lookup"><span data-stu-id="9c484-215">can save</span></span></li>
<li><span data-ttu-id="9c484-216">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="9c484-216">compound device</span></span></li>
<li><span data-ttu-id="9c484-217">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c484-217">device type</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c484-218">com áudio</span><span class="sxs-lookup"><span data-stu-id="9c484-218">has audio</span></span></li>
<li><span data-ttu-id="9c484-219">tem vídeo</span><span class="sxs-lookup"><span data-stu-id="9c484-219">has video</span></span></li>
<li><span data-ttu-id="9c484-220">entradas</span><span class="sxs-lookup"><span data-stu-id="9c484-220">inputs</span></span></li>
<li><span data-ttu-id="9c484-221">outputs</span><span class="sxs-lookup"><span data-stu-id="9c484-221">outputs</span></span></li>
<li><span data-ttu-id="9c484-222">usa arquivos</span><span class="sxs-lookup"><span data-stu-id="9c484-222">uses files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9c484-223">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro *lpszRequest* e seus significados:</span><span class="sxs-lookup"><span data-stu-id="9c484-223">The following table lists the flags that can be specified in the *lpszRequest* parameter and their meanings:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c484-224">Flags</span><span class="sxs-lookup"><span data-stu-id="9c484-224">Flags</span></span></th>
<th><span data-ttu-id="9c484-225">Significado</span><span class="sxs-lookup"><span data-stu-id="9c484-225">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c484-226">pode detectar comprimento</span><span class="sxs-lookup"><span data-stu-id="9c484-226">can detect length</span></span></td>
<td><span data-ttu-id="9c484-227">Retornará <strong>true</strong> se o dispositivo puder detectar o comprimento da mídia.</span><span class="sxs-lookup"><span data-stu-id="9c484-227">Returns <strong>TRUE</strong> if the device can detect the length of the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-228">pode ejetar</span><span class="sxs-lookup"><span data-stu-id="9c484-228">can eject</span></span></td>
<td><span data-ttu-id="9c484-229">Retornará <strong>true</strong> se o dispositivo puder ejetar a mídia.</span><span class="sxs-lookup"><span data-stu-id="9c484-229">Returns <strong>TRUE</strong> if the device can eject the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-230">pode congelar</span><span class="sxs-lookup"><span data-stu-id="9c484-230">can freeze</span></span></td>
<td><span data-ttu-id="9c484-231">Retornará <strong>true</strong> se o dispositivo puder congelar dados no buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="9c484-231">Returns <strong>TRUE</strong> if the device can freeze data in the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-232">pode bloquear</span><span class="sxs-lookup"><span data-stu-id="9c484-232">can lock</span></span></td>
<td><span data-ttu-id="9c484-233">Retornará <strong>true</strong> se o dispositivo puder bloquear dados.</span><span class="sxs-lookup"><span data-stu-id="9c484-233">Returns <strong>TRUE</strong> if the device can lock data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-234">pode monitorar fontes</span><span class="sxs-lookup"><span data-stu-id="9c484-234">can monitor sources</span></span></td>
<td><span data-ttu-id="9c484-235">Retornará <strong>true</strong> se o dispositivo puder passar uma entrada (origem) para a saída monitorada, independentemente da seleção de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="9c484-235">Returns <strong>TRUE</strong> if the device can pass an input (source) to the monitored output, independent of the current input selection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-236">pode reproduzir</span><span class="sxs-lookup"><span data-stu-id="9c484-236">can play</span></span></td>
<td><span data-ttu-id="9c484-237">Retornará <strong>true</strong> se o dispositivo puder ser executado.</span><span class="sxs-lookup"><span data-stu-id="9c484-237">Returns <strong>TRUE</strong> if the device can play.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-238">pode ser prevertido</span><span class="sxs-lookup"><span data-stu-id="9c484-238">can preroll</span></span></td>
<td><span data-ttu-id="9c484-239">Retornará <strong>true</strong> se o dispositivo der suporte ao &quot; sinalizador preroll &quot; com o comando <a href="cue.md">Cue</a> .</span><span class="sxs-lookup"><span data-stu-id="9c484-239">Returns <strong>TRUE</strong> if the device supports the &quot;preroll&quot; flag with the <a href="cue.md">cue</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-240">pode Visualizar</span><span class="sxs-lookup"><span data-stu-id="9c484-240">can preview</span></span></td>
<td><span data-ttu-id="9c484-241">Retornará <strong>true</strong> se o dispositivo oferecer suporte a visualizações.</span><span class="sxs-lookup"><span data-stu-id="9c484-241">Returns <strong>TRUE</strong> if the device supports previews.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-242">pode registrar</span><span class="sxs-lookup"><span data-stu-id="9c484-242">can record</span></span></td>
<td><span data-ttu-id="9c484-243">Retornará <strong>true</strong> se o dispositivo der suporte à gravação.</span><span class="sxs-lookup"><span data-stu-id="9c484-243">Returns <strong>TRUE</strong> if the device supports recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-244">pode reverter</span><span class="sxs-lookup"><span data-stu-id="9c484-244">can reverse</span></span></td>
<td><span data-ttu-id="9c484-245">Retornará <strong>true</strong> se o dispositivo puder reproduzir em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="9c484-245">Returns <strong>TRUE</strong> if the device can play in reverse.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-246">pode salvar</span><span class="sxs-lookup"><span data-stu-id="9c484-246">can save</span></span></td>
<td><span data-ttu-id="9c484-247">Retornará <strong>true</strong> se o dispositivo puder salvar dados.</span><span class="sxs-lookup"><span data-stu-id="9c484-247">Returns <strong>TRUE</strong> if the device can save data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-248">pode ampliar</span><span class="sxs-lookup"><span data-stu-id="9c484-248">can stretch</span></span></td>
<td><span data-ttu-id="9c484-249">Retornará <strong>true</strong> se o dispositivo puder alongar quadros para preencher um determinado retângulo de exibição.</span><span class="sxs-lookup"><span data-stu-id="9c484-249">Returns <strong>TRUE</strong> if the device can stretch frames to fill a given display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-250">pode ampliar a entrada</span><span class="sxs-lookup"><span data-stu-id="9c484-250">can stretch input</span></span></td>
<td><span data-ttu-id="9c484-251">Retornará <strong>true</strong> se o dispositivo puder redimensionar uma imagem no processo de digitalização no buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="9c484-251">Returns <strong>TRUE</strong> if the device can resize an image in the process of digitizing it into the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-252">pode testar</span><span class="sxs-lookup"><span data-stu-id="9c484-252">can test</span></span></td>
<td><span data-ttu-id="9c484-253">Retornará <strong>true</strong> se o dispositivo reconhecer a palavra-chave test.</span><span class="sxs-lookup"><span data-stu-id="9c484-253">Returns <strong>TRUE</strong> if the device recognizes the test keyword.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-254">cav</span><span class="sxs-lookup"><span data-stu-id="9c484-254">cav</span></span></td>
<td><span data-ttu-id="9c484-255">Quando combinado com outros itens, esse sinalizador especifica que as informações de retorno se aplicam ao formato CAV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="9c484-255">When combined with other items, this flag specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="9c484-256">Esse será o padrão se nenhum VIDEODISC for inserido.</span><span class="sxs-lookup"><span data-stu-id="9c484-256">This is the default if no videodisc is inserted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-257">taxa de incremento de relógio</span><span class="sxs-lookup"><span data-stu-id="9c484-257">clock increment rate</span></span></td>
<td><span data-ttu-id="9c484-258">Retorna o número de subdivisãos com suporte do relógio externo por segundo.</span><span class="sxs-lookup"><span data-stu-id="9c484-258">Returns the number of subdivisions the external clock supports per second.</span></span> <span data-ttu-id="9c484-259">Se o relógio externo for um relógio de milissegundo, o valor de retorno será 1000.</span><span class="sxs-lookup"><span data-stu-id="9c484-259">If the external clock is a millisecond clock, the return value is 1000.</span></span> <span data-ttu-id="9c484-260">Se o valor de retorno for 0, não haverá suporte para nenhum relógio.</span><span class="sxs-lookup"><span data-stu-id="9c484-260">If the return value is 0, no clock is supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-261">clv</span><span class="sxs-lookup"><span data-stu-id="9c484-261">clv</span></span></td>
<td><span data-ttu-id="9c484-262">Quando combinado com outros itens, esse sinalizador especifica que as informações de retorno se aplicam ao formato CLV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="9c484-262">When combined with other items, this flag specifies that the return information applies to CLV format videodiscs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-263">dispositivo composto</span><span class="sxs-lookup"><span data-stu-id="9c484-263">compound device</span></span></td>
<td><span data-ttu-id="9c484-264">Retornará <strong>true</strong> se o dispositivo der suporte a um nome de elemento (filename).</span><span class="sxs-lookup"><span data-stu-id="9c484-264">Returns <strong>TRUE</strong> if the device supports an element name (filename).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-265">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c484-265">device type</span></span></td>
<td><span data-ttu-id="9c484-266">Retorna um nome de tipo de dispositivo, que pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="9c484-266">Returns a device type name, which can be one of the following:</span></span>
<ul>
<li><span data-ttu-id="9c484-267">cdaudio</span><span class="sxs-lookup"><span data-stu-id="9c484-267">cdaudio</span></span></li>
<li><span data-ttu-id="9c484-268">DATs</span><span class="sxs-lookup"><span data-stu-id="9c484-268">dat</span></span></li>
<li><span data-ttu-id="9c484-269">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="9c484-269">digitalvideo</span></span></li>
<li><span data-ttu-id="9c484-270">outros</span><span class="sxs-lookup"><span data-stu-id="9c484-270">other</span></span></li>
<li><span data-ttu-id="9c484-271">overlay</span><span class="sxs-lookup"><span data-stu-id="9c484-271">overlay</span></span></li>
<li><span data-ttu-id="9c484-272">verificador</span><span class="sxs-lookup"><span data-stu-id="9c484-272">scanner</span></span></li>
<li><span data-ttu-id="9c484-273">sequenciador</span><span class="sxs-lookup"><span data-stu-id="9c484-273">sequencer</span></span></li>
<li><span data-ttu-id="9c484-274">videocassete</span><span class="sxs-lookup"><span data-stu-id="9c484-274">vcr</span></span></li>
<li><span data-ttu-id="9c484-275">videodisc</span><span class="sxs-lookup"><span data-stu-id="9c484-275">videodisc</span></span></li>
<li><span data-ttu-id="9c484-276">waveaudio</span><span class="sxs-lookup"><span data-stu-id="9c484-276">waveaudio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-277">taxa de reprodução rápida</span><span class="sxs-lookup"><span data-stu-id="9c484-277">fast play rate</span></span></td>
<td><span data-ttu-id="9c484-278">Retorna a taxa de reprodução rápida em quadros por segundo ou zero se o dispositivo não puder ser executado rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9c484-278">Returns the fast play rate in frames per second, or zero if the device cannot play fast.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-279">com áudio</span><span class="sxs-lookup"><span data-stu-id="9c484-279">has audio</span></span></td>
<td><span data-ttu-id="9c484-280">Retornará <strong>true</strong> se o dispositivo der suporte à reprodução de áudio.</span><span class="sxs-lookup"><span data-stu-id="9c484-280">Returns <strong>TRUE</strong> if the device supports audio playback.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-281">tem relógio</span><span class="sxs-lookup"><span data-stu-id="9c484-281">has clock</span></span></td>
<td><span data-ttu-id="9c484-282">Retornará <strong>true</strong> se o dispositivo tiver um relógio.</span><span class="sxs-lookup"><span data-stu-id="9c484-282">Returns <strong>TRUE</strong> if the device has a clock.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-283">ainda</span><span class="sxs-lookup"><span data-stu-id="9c484-283">has still</span></span></td>
<td><span data-ttu-id="9c484-284">Retornará <strong>true</strong> se o dispositivo tratar arquivos com uma única imagem com mais eficiência do que arquivos de vídeo de movimento.</span><span class="sxs-lookup"><span data-stu-id="9c484-284">Returns <strong>TRUE</strong> if the device treats files with a single image more efficiently than motion video files.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-285">tem código de paficação</span><span class="sxs-lookup"><span data-stu-id="9c484-285">has timecode</span></span></td>
<td><span data-ttu-id="9c484-286">Retornará <strong>true</strong> se o dispositivo for capaz de dar suporte ao código de Code ou se for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9c484-286">Returns <strong>TRUE</strong> if the device is capable of supporting timecode, or if it is unknown.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-287">tem vídeo</span><span class="sxs-lookup"><span data-stu-id="9c484-287">has video</span></span></td>
<td><span data-ttu-id="9c484-288">Retornará <strong>true</strong> se o dispositivo der suporte a vídeo.</span><span class="sxs-lookup"><span data-stu-id="9c484-288">Returns <strong>TRUE</strong> if the device supports video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-289">entradas</span><span class="sxs-lookup"><span data-stu-id="9c484-289">inputs</span></span></td>
<td><span data-ttu-id="9c484-290">Retorna o número total de dispositivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="9c484-290">Returns the total number of input devices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-291">taxa de execução máxima</span><span class="sxs-lookup"><span data-stu-id="9c484-291">maximum play rate</span></span></td>
<td><span data-ttu-id="9c484-292">Retorna a taxa de execução máxima, em quadros por segundo, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c484-292">Returns the maximum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-293">taxa mínima de execução</span><span class="sxs-lookup"><span data-stu-id="9c484-293">minimum play rate</span></span></td>
<td><span data-ttu-id="9c484-294">Retorna a taxa mínima de reprodução, em quadros por segundo, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c484-294">Returns the minimum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-295">taxa de reprodução normal</span><span class="sxs-lookup"><span data-stu-id="9c484-295">normal play rate</span></span></td>
<td><span data-ttu-id="9c484-296">Retorna a taxa de reprodução normal, em quadros por segundo, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c484-296">Returns the normal play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-297">número de marcas</span><span class="sxs-lookup"><span data-stu-id="9c484-297">number of marks</span></span></td>
<td><span data-ttu-id="9c484-298">Retorna o número máximo de marcas que podem ser usadas; zero indica que não há suporte para marcas.</span><span class="sxs-lookup"><span data-stu-id="9c484-298">Returns the maximum number of marks that can be used; zero indicates that marks are unsupported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-299">outputs</span><span class="sxs-lookup"><span data-stu-id="9c484-299">outputs</span></span></td>
<td><span data-ttu-id="9c484-300">Retorna o número total de dispositivos de saída.</span><span class="sxs-lookup"><span data-stu-id="9c484-300">Returns the total number of output devices.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-301">precisão da busca</span><span class="sxs-lookup"><span data-stu-id="9c484-301">seek accuracy</span></span></td>
<td><span data-ttu-id="9c484-302">Retorna a precisão esperada de uma pesquisa em quadros; 0 indica que o dispositivo é preciso de quadro, 1 indica que o dispositivo espera estar dentro de um quadro da posição de busca indicada e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9c484-302">Returns the expected accuracy of a search in frames; 0 indicates that the device is frame accurate, 1 indicates that the device expects to be within one frame of the indicated seek position, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-303">taxa de reprodução lenta</span><span class="sxs-lookup"><span data-stu-id="9c484-303">slow play rate</span></span></td>
<td><span data-ttu-id="9c484-304">Retorna a taxa de reprodução lenta em quadros por segundo ou zero se o dispositivo não puder ser executado lentamente.</span><span class="sxs-lookup"><span data-stu-id="9c484-304">Returns the slow play rate in frames per second, or zero if the device cannot play slowly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-305">usa arquivos</span><span class="sxs-lookup"><span data-stu-id="9c484-305">uses files</span></span></td>
<td><span data-ttu-id="9c484-306">Retornará <strong>true</strong> se o armazenamento de dados usado por um dispositivo composto for um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9c484-306">Returns <strong>TRUE</strong> if the data storage used by a compound device is a file.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c484-307">usa paletas</span><span class="sxs-lookup"><span data-stu-id="9c484-307">uses palettes</span></span></td>
<td><span data-ttu-id="9c484-308">Retornará <strong>true</strong> se o dispositivo usar paletas.</span><span class="sxs-lookup"><span data-stu-id="9c484-308">Returns <strong>TRUE</strong> if the device uses palettes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c484-309">windows</span><span class="sxs-lookup"><span data-stu-id="9c484-309">windows</span></span></td>
<td><span data-ttu-id="9c484-310">Retorna o número de janelas de exibição simultâneas às quais o dispositivo pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="9c484-310">Returns the number of simultaneous display windows the device can support.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="9c484-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="9c484-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9c484-312">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="9c484-312">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="9c484-313">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="9c484-313">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="9c484-314">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9c484-314">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c484-315">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9c484-315">Return Value</span></span>

<span data-ttu-id="9c484-316">Retorna informações no parâmetro *lpszReturnString* da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9c484-316">Returns information in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="9c484-317">As informações dependem do tipo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c484-317">The information is dependent on the request type.</span></span>

## <a name="examples"></a><span data-ttu-id="9c484-318">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9c484-318">Examples</span></span>

<span data-ttu-id="9c484-319">O comando a seguir retorna o tipo de dispositivo do dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="9c484-319">The following command returns the device type of the "mysound" device.</span></span>

``` syntax
capability mysound device type
```

## <a name="requirements"></a><span data-ttu-id="9c484-320">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c484-320">Requirements</span></span>



| <span data-ttu-id="9c484-321">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c484-321">Requirement</span></span> | <span data-ttu-id="9c484-322">Valor</span><span class="sxs-lookup"><span data-stu-id="9c484-322">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9c484-323">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c484-323">Minimum supported client</span></span><br/> | <span data-ttu-id="9c484-324">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9c484-324">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9c484-325">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c484-325">Minimum supported server</span></span><br/> | <span data-ttu-id="9c484-326">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9c484-326">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9c484-327">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c484-327">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c484-328">MCI</span><span class="sxs-lookup"><span data-stu-id="9c484-328">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9c484-329">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="9c484-329">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="9c484-330">advertência</span><span class="sxs-lookup"><span data-stu-id="9c484-330">cue</span></span>](cue.md)
</dt> </dl>

 


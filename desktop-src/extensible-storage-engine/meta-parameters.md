---
description: 'Saiba mais sobre: meta Parameters'
title: Parâmetros meta
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748726"
---
# <a name="meta-parameters"></a><span data-ttu-id="58912-103">Parâmetros meta</span><span class="sxs-lookup"><span data-stu-id="58912-103">Meta Parameters</span></span>


<span data-ttu-id="58912-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="58912-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="meta-parameters"></a><span data-ttu-id="58912-105">Parâmetros meta</span><span class="sxs-lookup"><span data-stu-id="58912-105">Meta Parameters</span></span>

<span data-ttu-id="58912-106">Este tópico contém parâmetros que são usados para controlar outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="58912-106">This topic contains parameters that are used to control other parameters.</span></span>

<span data-ttu-id="58912-107">JET_paramConfiguration</span><span class="sxs-lookup"><span data-stu-id="58912-107">JET_paramConfiguration</span></span>  
<span data-ttu-id="58912-108">129</span><span class="sxs-lookup"><span data-stu-id="58912-108">129</span></span>  
<span data-ttu-id="58912-109">Esse parâmetro expõe vários conjuntos de valores padrão para todo o conjunto de parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="58912-109">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="58912-110">Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração.</span><span class="sxs-lookup"><span data-stu-id="58912-110">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="58912-111">Se a configuração for definida para uma instância específica, os parâmetros do sistema global não serão redefinidos para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="58912-111">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span>

<span data-ttu-id="58912-112">Além disso, o próprio parâmetro pode ter outros efeitos sobre o comportamento do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="58912-112">In addition, the parameter itself can have other effects on the behavior of the database engine.</span></span>

<span data-ttu-id="58912-113">Neste momento, há duas configurações com suporte:</span><span class="sxs-lookup"><span data-stu-id="58912-113">At this time, there are two supported configurations:</span></span>

  - <span data-ttu-id="58912-114">Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória.</span><span class="sxs-lookup"><span data-stu-id="58912-114">Small Configuration (0): The database engine is optimized for memory use.</span></span>

  - <span data-ttu-id="58912-115">Configuração herdada (1): o mecanismo de banco de dados tem seus padrões tradicionais.</span><span class="sxs-lookup"><span data-stu-id="58912-115">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="58912-116">A configuração pequena altera os padrões dos seguintes parâmetros do sistema para os valores especificados:</span><span class="sxs-lookup"><span data-stu-id="58912-116">Small Configuration changes the defaults of the following system parameters to the specified values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="58912-117">Parâmetro do sistema</span><span class="sxs-lookup"><span data-stu-id="58912-117">System Parameter</span></span></p></th>
<th><p><span data-ttu-id="58912-118">Novo valor padrão</span><span class="sxs-lookup"><span data-stu-id="58912-118">New Default Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58912-119">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="58912-119">JET_paramMaxSessions</span></span></p></td>
<td><p><span data-ttu-id="58912-120">30000</span><span class="sxs-lookup"><span data-stu-id="58912-120">30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-121">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="58912-121">JET_paramMaxOpenTables</span></span></p></td>
<td><p><span data-ttu-id="58912-122">2147483647</span><span class="sxs-lookup"><span data-stu-id="58912-122">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-123">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="58912-123">JET_paramMaxCursors</span></span></p></td>
<td><p><span data-ttu-id="58912-124">2147483647</span><span class="sxs-lookup"><span data-stu-id="58912-124">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-125">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="58912-125">JET_paramMaxVerPages</span></span></p></td>
<td><p><span data-ttu-id="58912-126">2147483647</span><span class="sxs-lookup"><span data-stu-id="58912-126">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-127">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="58912-127">JET_paramMaxTemporaryTables</span></span></p></td>
<td><p><span data-ttu-id="58912-128">2147483647</span><span class="sxs-lookup"><span data-stu-id="58912-128">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-129">JET_paramLogFileSize</span><span class="sxs-lookup"><span data-stu-id="58912-129">JET_paramLogFileSize</span></span></p></td>
<td><p><span data-ttu-id="58912-130">64</span><span class="sxs-lookup"><span data-stu-id="58912-130">64</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-131">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="58912-131">JET_paramLogBuffers</span></span></p></td>
<td><p><span data-ttu-id="58912-132">1</span><span class="sxs-lookup"><span data-stu-id="58912-132">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-133">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="58912-133">JET_paramDbExtensionSize</span></span></p></td>
<td><p><span data-ttu-id="58912-134">16</span><span class="sxs-lookup"><span data-stu-id="58912-134">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-135">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="58912-135">JET_paramPageTempDBMin</span></span></p></td>
<td><p><span data-ttu-id="58912-136">14</span><span class="sxs-lookup"><span data-stu-id="58912-136">14</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-137">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="58912-137">JET_paramCacheSizeMax</span></span></p></td>
<td><p><span data-ttu-id="58912-138">16</span><span class="sxs-lookup"><span data-stu-id="58912-138">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-139">JET_paramCheckpointDepthMax</span><span class="sxs-lookup"><span data-stu-id="58912-139">JET_paramCheckpointDepthMax</span></span></p></td>
<td><p><span data-ttu-id="58912-140">65536</span><span class="sxs-lookup"><span data-stu-id="58912-140">65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-141">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="58912-141">JET_paramLRUKHistoryMax</span></span></p></td>
<td><p><span data-ttu-id="58912-142">10</span><span class="sxs-lookup"><span data-stu-id="58912-142">10</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-143">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="58912-143">JET_paramOutstandingIOMax</span></span></p></td>
<td><p><span data-ttu-id="58912-144">16</span><span class="sxs-lookup"><span data-stu-id="58912-144">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-145">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="58912-145">JET_paramStartFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="58912-146">1</span><span class="sxs-lookup"><span data-stu-id="58912-146">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-147">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="58912-147">JET_paramStopFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="58912-148">2</span><span class="sxs-lookup"><span data-stu-id="58912-148">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-149">JET_paramNoInformationEvent</span><span class="sxs-lookup"><span data-stu-id="58912-149">JET_paramNoInformationEvent</span></span></p></td>
<td><p><span data-ttu-id="58912-150">1</span><span class="sxs-lookup"><span data-stu-id="58912-150">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-151">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="58912-151">JET_paramCacheSizeMin</span></span></p></td>
<td><p><span data-ttu-id="58912-152">16</span><span class="sxs-lookup"><span data-stu-id="58912-152">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-153">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="58912-153">JET_paramPreferredVerPages</span></span></p></td>
<td><p><span data-ttu-id="58912-154">2147483647</span><span class="sxs-lookup"><span data-stu-id="58912-154">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-155">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="58912-155">JET_paramLogFileCreateAsynch</span></span></p></td>
<td><p><span data-ttu-id="58912-156">0</span><span class="sxs-lookup"><span data-stu-id="58912-156">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-157">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="58912-157">JET_paramGlobalMinVerPages</span></span></p></td>
<td><p><span data-ttu-id="58912-158">1</span><span class="sxs-lookup"><span data-stu-id="58912-158">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-159">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="58912-159">JET_paramPageHintCacheSize</span></span></p></td>
<td><p><span data-ttu-id="58912-160">32</span><span class="sxs-lookup"><span data-stu-id="58912-160">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-161">JET_paramDisablePerfmon</span><span class="sxs-lookup"><span data-stu-id="58912-161">JET_paramDisablePerfmon</span></span></p></td>
<td><p><span data-ttu-id="58912-162">1</span><span class="sxs-lookup"><span data-stu-id="58912-162">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-163">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="58912-163">JET_paramEnableFileCache</span></span></p></td>
<td><p><span data-ttu-id="58912-164">1</span><span class="sxs-lookup"><span data-stu-id="58912-164">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-165">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="58912-165">JET_paramEnableViewCache</span></span></p></td>
<td><p><span data-ttu-id="58912-166">1</span><span class="sxs-lookup"><span data-stu-id="58912-166">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-167">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="58912-167">JET_paramVerPageSize</span></span></p></td>
<td><p><span data-ttu-id="58912-168">1024</span><span class="sxs-lookup"><span data-stu-id="58912-168">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-169">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="58912-169">JET_paramEnableAdvanced</span></span></p></td>
<td><p><span data-ttu-id="58912-170">0</span><span class="sxs-lookup"><span data-stu-id="58912-170">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-171">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="58912-171">JET_paramCheckpointIOMax</span></span></p></td>
<td><p><span data-ttu-id="58912-172">8</span><span class="sxs-lookup"><span data-stu-id="58912-172">8</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="58912-173">A configuração pequena também tem vários outros efeitos no mecanismo de banco de dados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="58912-173">Small Configuration also has several other effects on the database engine, including:</span></span>

  - <span data-ttu-id="58912-174">Todos os recursos gerenciados por parâmetros do sistema são alocados a partir do heap, conforme necessário</span><span class="sxs-lookup"><span data-stu-id="58912-174">All resources managed by system parameters are allocated from the heap as needed</span></span>

  - <span data-ttu-id="58912-175">Outros recursos internos usados pelo mecanismo de banco de dados são reduzidos em tamanho</span><span class="sxs-lookup"><span data-stu-id="58912-175">Other internal resources used by the database engine are scaled down in size</span></span>

  - <span data-ttu-id="58912-176">Várias atividades de manutenção são dimensionadas de volta para evitar a atividade de thread em segundo plano</span><span class="sxs-lookup"><span data-stu-id="58912-176">Various maintenance activities are scaled back to avoid background thread activity</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58912-177">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="58912-177">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="58912-178">1 (Herdado)</span><span class="sxs-lookup"><span data-stu-id="58912-178">1 (Legacy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-179">Tipo:</span><span class="sxs-lookup"><span data-stu-id="58912-179">Type:</span></span></p></td>
<td><p><span data-ttu-id="58912-180">Integer</span><span class="sxs-lookup"><span data-stu-id="58912-180">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-181">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="58912-181">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="58912-182">0 – 1</span><span class="sxs-lookup"><span data-stu-id="58912-182">0 – 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-183">Escopo:</span><span class="sxs-lookup"><span data-stu-id="58912-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="58912-184">Instância</span><span class="sxs-lookup"><span data-stu-id="58912-184">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-185">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="58912-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="58912-186">Sim</span><span class="sxs-lookup"><span data-stu-id="58912-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-187">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="58912-187">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="58912-188">Não</span><span class="sxs-lookup"><span data-stu-id="58912-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-189">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="58912-189">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="58912-190">Não</span><span class="sxs-lookup"><span data-stu-id="58912-190">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-191">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="58912-191">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="58912-192">Não</span><span class="sxs-lookup"><span data-stu-id="58912-192">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-193">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="58912-193">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="58912-194">Sim</span><span class="sxs-lookup"><span data-stu-id="58912-194">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-195">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="58912-195">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="58912-196">Sim</span><span class="sxs-lookup"><span data-stu-id="58912-196">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-197">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="58912-197">Availability:</span></span></p></td>
<td><p><span data-ttu-id="58912-198">Começando com o Windows Server 2008 e o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58912-198">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="58912-199">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="58912-199">JET_paramEnableAdvanced</span></span>  
<span data-ttu-id="58912-200">130</span><span class="sxs-lookup"><span data-stu-id="58912-200">130</span></span>  
<span data-ttu-id="58912-201">Esse parâmetro é usado para controlar quando o mecanismo de banco de dados aceita ou rejeita alterações em um subconjunto dos parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="58912-201">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="58912-202">Esse parâmetro é usado em conjunto com JET_paramConfiguration para impedir que alguns parâmetros do sistema sejam definidos fora dos padrões da configuração selecionada.</span><span class="sxs-lookup"><span data-stu-id="58912-202">This parameter is used in conjunction with JET_paramConfiguration to prevent some system parameters from being set away from the selected configuration's defaults.</span></span>

<span data-ttu-id="58912-203">Os seguintes parâmetros do sistema serão protegidos de serem definidos quando esse parâmetro for definido como false:</span><span class="sxs-lookup"><span data-stu-id="58912-203">The following system parameters will be protected from being set when this parameter is set to False:</span></span>

  - <span data-ttu-id="58912-204">JET_paramMaxSessionsfon</span><span class="sxs-lookup"><span data-stu-id="58912-204">JET_paramMaxSessionsfon</span></span>

  - <span data-ttu-id="58912-205">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="58912-205">JET_paramMaxOpenTables</span></span>

  - <span data-ttu-id="58912-206">JET_paramPreferredMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="58912-206">JET_paramPreferredMaxOpenTables</span></span>

  - <span data-ttu-id="58912-207">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="58912-207">JET_paramMaxCursors</span></span>

  - <span data-ttu-id="58912-208">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="58912-208">JET_paramMaxVerPages</span></span>

  - <span data-ttu-id="58912-209">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="58912-209">JET_paramMaxTemporaryTables</span></span>

  - <span data-ttu-id="58912-210">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="58912-210">JET_paramLogBuffers</span></span>

  - <span data-ttu-id="58912-211">JET_paramWaitLogFlush</span><span class="sxs-lookup"><span data-stu-id="58912-211">JET_paramWaitLogFlush</span></span>

  - <span data-ttu-id="58912-212">JET_paramLogCheckpointPeriod</span><span class="sxs-lookup"><span data-stu-id="58912-212">JET_paramLogCheckpointPeriod</span></span>

  - <span data-ttu-id="58912-213">JET_paramLogWaitingUserMax</span><span class="sxs-lookup"><span data-stu-id="58912-213">JET_paramLogWaitingUserMax</span></span>

  - <span data-ttu-id="58912-214">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="58912-214">JET_paramDbExtensionSize</span></span>

  - <span data-ttu-id="58912-215">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="58912-215">JET_paramPageTempDBMin</span></span>

  - <span data-ttu-id="58912-216">JET_paramPageFragment</span><span class="sxs-lookup"><span data-stu-id="58912-216">JET_paramPageFragment</span></span>

  - <span data-ttu-id="58912-217">JET_paramBatchIOBufferMax</span><span class="sxs-lookup"><span data-stu-id="58912-217">JET_paramBatchIOBufferMax</span></span>

  - <span data-ttu-id="58912-218">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="58912-218">JET_paramCacheSizeMax</span></span>

  - <span data-ttu-id="58912-219">JET_paramLRUKCorrInterval</span><span class="sxs-lookup"><span data-stu-id="58912-219">JET_paramLRUKCorrInterval</span></span>

  - <span data-ttu-id="58912-220">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="58912-220">JET_paramLRUKHistoryMax</span></span>

  - <span data-ttu-id="58912-221">JET_paramLRUKPolicy</span><span class="sxs-lookup"><span data-stu-id="58912-221">JET_paramLRUKPolicy</span></span>

  - <span data-ttu-id="58912-222">JET_paramLRUKTimeout</span><span class="sxs-lookup"><span data-stu-id="58912-222">JET_paramLRUKTimeout</span></span>

  - <span data-ttu-id="58912-223">JET_paramLRUKTrxCorrInterval</span><span class="sxs-lookup"><span data-stu-id="58912-223">JET_paramLRUKTrxCorrInterval</span></span>

  - <span data-ttu-id="58912-224">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="58912-224">JET_paramOutstandingIOMax</span></span>

  - <span data-ttu-id="58912-225">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="58912-225">JET_paramStartFlushThreshold</span></span>

  - <span data-ttu-id="58912-226">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="58912-226">JET_paramStopFlushThreshold</span></span>

  - <span data-ttu-id="58912-227">JET_paramCacheSize</span><span class="sxs-lookup"><span data-stu-id="58912-227">JET_paramCacheSize</span></span>

  - <span data-ttu-id="58912-228">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="58912-228">JET_paramCacheSizeMin</span></span>

  - <span data-ttu-id="58912-229">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="58912-229">JET_paramPreferredVerPages</span></span>

  - <span data-ttu-id="58912-230">JET_paramBackupChunkSize</span><span class="sxs-lookup"><span data-stu-id="58912-230">JET_paramBackupChunkSize</span></span>

  - <span data-ttu-id="58912-231">JET_paramBackupOutstandingReads</span><span class="sxs-lookup"><span data-stu-id="58912-231">JET_paramBackupOutstandingReads</span></span>

  - <span data-ttu-id="58912-232">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="58912-232">JET_paramLogFileCreateAsynch</span></span>

  - <span data-ttu-id="58912-233">JET_paramRecordUpgradeDirtyLevel</span><span class="sxs-lookup"><span data-stu-id="58912-233">JET_paramRecordUpgradeDirtyLevel</span></span>

  - <span data-ttu-id="58912-234">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="58912-234">JET_paramGlobalMinVerPages</span></span>

  - <span data-ttu-id="58912-235">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="58912-235">JET_paramPageHintCacheSize</span></span>

  - <span data-ttu-id="58912-236">JET_paramVersionStoreTaskQueueMax</span><span class="sxs-lookup"><span data-stu-id="58912-236">JET_paramVersionStoreTaskQueueMax</span></span>

  - <span data-ttu-id="58912-237">JET_paramDBAPageAvailMin</span><span class="sxs-lookup"><span data-stu-id="58912-237">JET_paramDBAPageAvailMin</span></span>

  - <span data-ttu-id="58912-238">JET_paramMaxRandomIOSize</span><span class="sxs-lookup"><span data-stu-id="58912-238">JET_paramMaxRandomIOSize</span></span>

  - <span data-ttu-id="58912-239">JET_paramCachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="58912-239">JET_paramCachedClosedTables</span></span>

  - <span data-ttu-id="58912-240">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="58912-240">JET_paramEnableFileCache</span></span>

  - <span data-ttu-id="58912-241">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="58912-241">JET_paramEnableViewCache</span></span>

  - <span data-ttu-id="58912-242">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="58912-242">JET_paramVerPageSize</span></span>

  - <span data-ttu-id="58912-243">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="58912-243">JET_paramCheckpointIOMax</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58912-244">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="58912-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="58912-245">True</span><span class="sxs-lookup"><span data-stu-id="58912-245">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-246">Tipo:</span><span class="sxs-lookup"><span data-stu-id="58912-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="58912-247">Boolean</span><span class="sxs-lookup"><span data-stu-id="58912-247">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-248">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="58912-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="58912-249">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="58912-249">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-250">Escopo:</span><span class="sxs-lookup"><span data-stu-id="58912-250">Scope:</span></span></p></td>
<td><p><span data-ttu-id="58912-251">Instância</span><span class="sxs-lookup"><span data-stu-id="58912-251">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-252">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="58912-252">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="58912-253">Sim</span><span class="sxs-lookup"><span data-stu-id="58912-253">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-254">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="58912-254">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="58912-255">Sim</span><span class="sxs-lookup"><span data-stu-id="58912-255">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-256">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="58912-256">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="58912-257">Não</span><span class="sxs-lookup"><span data-stu-id="58912-257">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-258">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="58912-258">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="58912-259">Não</span><span class="sxs-lookup"><span data-stu-id="58912-259">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-260">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="58912-260">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="58912-261">Não</span><span class="sxs-lookup"><span data-stu-id="58912-261">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-262">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="58912-262">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="58912-263">Não</span><span class="sxs-lookup"><span data-stu-id="58912-263">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-264">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="58912-264">Availability:</span></span></p></td>
<td><p><span data-ttu-id="58912-265">Começando com o Windows Server 2008 e o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58912-265">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="58912-266">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58912-266">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58912-267"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="58912-267"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="58912-268">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="58912-268">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58912-269"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="58912-269"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="58912-270">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="58912-270">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58912-271"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="58912-271"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="58912-272">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="58912-272">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="58912-273">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="58912-273">See Also</span></span>

[<span data-ttu-id="58912-274">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="58912-274">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="58912-275">JetInit</span><span class="sxs-lookup"><span data-stu-id="58912-275">JetInit</span></span>](./jetinit-function.md)

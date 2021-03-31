---
description: 'Saiba mais sobre: parâmetros do log de eventos'
title: Parâmetros do log de eventos
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011203"
---
# <a name="event-log-parameters"></a><span data-ttu-id="ed23a-103">Parâmetros do log de eventos</span><span class="sxs-lookup"><span data-stu-id="ed23a-103">Event Log Parameters</span></span>


<span data-ttu-id="ed23a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ed23a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-log-parameters"></a><span data-ttu-id="ed23a-105">Parâmetros do log de eventos</span><span class="sxs-lookup"><span data-stu-id="ed23a-105">Event Log Parameters</span></span>

<span data-ttu-id="ed23a-106">Este tópico contém parâmetros que são usados para o log de eventos.</span><span class="sxs-lookup"><span data-stu-id="ed23a-106">This topic contains parameters that are used for the event log.</span></span>

<span data-ttu-id="ed23a-107">JET_paramEventLogCache</span><span class="sxs-lookup"><span data-stu-id="ed23a-107">JET_paramEventLogCache</span></span>  
<span data-ttu-id="ed23a-108">Esse parâmetro controla o tamanho (em bytes) de um cache de mensagens do EventLog que manterá as mensagens de EventLog emitidas pelo mecanismo de banco de dados enquanto o serviço EventLog é interrompido.</span><span class="sxs-lookup"><span data-stu-id="ed23a-108">This parameter controls the size (in bytes) of an eventlog message cache that will hold eventlog messages emitted by the database engine while the eventlog service is stopped.</span></span> <span data-ttu-id="ed23a-109">Essas mensagens em cache serão liberadas para o log de eventos quando o serviço se tornar operacional.</span><span class="sxs-lookup"><span data-stu-id="ed23a-109">These cached messages will be flushed to the eventlog when the service becomes operational.</span></span> <span data-ttu-id="ed23a-110">Todas as mensagens que excedem o cache serão descartadas.</span><span class="sxs-lookup"><span data-stu-id="ed23a-110">Any messages that overflow the cache will be dropped.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-111">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="ed23a-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-112">0</span><span class="sxs-lookup"><span data-stu-id="ed23a-112">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-114">Integer</span><span class="sxs-lookup"><span data-stu-id="ed23a-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="ed23a-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-116">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="ed23a-116">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-117">Escopo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-118">Global</span><span class="sxs-lookup"><span data-stu-id="ed23a-118">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-119">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-120">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-121">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-122">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-123">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="ed23a-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-124">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-125">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-126">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-127">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="ed23a-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-128">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-129">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="ed23a-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-130">Sim</span><span class="sxs-lookup"><span data-stu-id="ed23a-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-131">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-132">Todos</span><span class="sxs-lookup"><span data-stu-id="ed23a-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed23a-133">*JET_paramEventLoggingLevel*</span><span class="sxs-lookup"><span data-stu-id="ed23a-133">*JET_paramEventLoggingLevel*</span></span>  
  
<span data-ttu-id="ed23a-134">Esse parâmetro configura o nível de detalhe das mensagens de log de eventos emitidas para o log de eventos pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ed23a-134">This parameter configures the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="ed23a-135">Números mais altos resultarão em mensagens de log de eventos mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="ed23a-135">Higher numbers will result in more detailed eventlog messages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-136">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="ed23a-136">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-137">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="ed23a-137">JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-138">Tipo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-138">Type:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-139">Integer</span><span class="sxs-lookup"><span data-stu-id="ed23a-139">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-140">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="ed23a-140">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="ed23a-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-142">Escopo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-142">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-143">Instância</span><span class="sxs-lookup"><span data-stu-id="ed23a-143">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-144">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-144">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-145">Sim</span><span class="sxs-lookup"><span data-stu-id="ed23a-145">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-146">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-146">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-147">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-147">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-148">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="ed23a-148">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-149">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-150">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-150">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-151">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-151">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-152">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="ed23a-152">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-153">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-154">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="ed23a-154">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-155">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-155">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-156">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-156">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-157">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="ed23a-157">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed23a-158">*JET_paramEventSource*</span><span class="sxs-lookup"><span data-stu-id="ed23a-158">*JET_paramEventSource*</span></span>  
<span data-ttu-id="ed23a-159">4</span><span class="sxs-lookup"><span data-stu-id="ed23a-159">4</span></span>  

<span data-ttu-id="ed23a-160">Esse parâmetro fornece uma cadeia de caracteres específica do aplicativo que será adicionada a qualquer mensagem de log de eventos emitida pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ed23a-160">This parameter supplies an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="ed23a-161">Isso permite uma fácil correlação de mensagens de log de eventos com o aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="ed23a-161">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="ed23a-162">Se uma cadeia de caracteres vazia for especificada (como é o padrão), o nome executável do aplicativo host será usado.</span><span class="sxs-lookup"><span data-stu-id="ed23a-162">If an empty string is specified (as is the default) then the host application executable name will be used.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-163">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="ed23a-163">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-164">Tipo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-164">Type:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-165">String</span><span class="sxs-lookup"><span data-stu-id="ed23a-165">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-166">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="ed23a-166">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-167">0 a 259 caracteres</span><span class="sxs-lookup"><span data-stu-id="ed23a-167">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-168">Escopo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-168">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-169">Instância</span><span class="sxs-lookup"><span data-stu-id="ed23a-169">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-170">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-170">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-171">Sim</span><span class="sxs-lookup"><span data-stu-id="ed23a-171">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-172">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-172">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-173">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-173">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-174">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="ed23a-174">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-175">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-175">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-176">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-176">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-177">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-178">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="ed23a-178">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-179">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-180">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="ed23a-180">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-181">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-182">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-182">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-183">Todos</span><span class="sxs-lookup"><span data-stu-id="ed23a-183">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed23a-184">*JET_paramEventSourceKey*</span><span class="sxs-lookup"><span data-stu-id="ed23a-184">*JET_paramEventSourceKey*</span></span>  
<span data-ttu-id="ed23a-185">49</span><span class="sxs-lookup"><span data-stu-id="ed23a-185">49</span></span>  

<span data-ttu-id="ed23a-186">Esse parâmetro pode ser usado para controlar qual log de eventos o mecanismo de banco de dados usa para suas mensagens de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="ed23a-186">This parameter can be used to control which event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="ed23a-187">Por padrão, todas as mensagens de log de eventos vão para o log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed23a-187">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="ed23a-188">Se o nome da chave do registro para outro log de eventos estiver configurado, as mensagens do log de eventos entrarão em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="ed23a-188">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-189">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="ed23a-189">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-190">Tipo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-190">Type:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-191">String</span><span class="sxs-lookup"><span data-stu-id="ed23a-191">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-192">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="ed23a-192">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-193">0 a 259 caracteres</span><span class="sxs-lookup"><span data-stu-id="ed23a-193">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-194">Escopo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-194">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-195">Instância</span><span class="sxs-lookup"><span data-stu-id="ed23a-195">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-196">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-196">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-197">Sim</span><span class="sxs-lookup"><span data-stu-id="ed23a-197">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-198">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-198">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-199">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-199">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-200">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="ed23a-200">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-201">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-201">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-202">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-202">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-203">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-203">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-204">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="ed23a-204">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-205">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-205">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-206">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="ed23a-206">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-207">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-208">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-208">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-209">Todos</span><span class="sxs-lookup"><span data-stu-id="ed23a-209">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed23a-210">*JET_paramNoInformationEvent*</span><span class="sxs-lookup"><span data-stu-id="ed23a-210">*JET_paramNoInformationEvent*</span></span>  
<span data-ttu-id="ed23a-211">50</span><span class="sxs-lookup"><span data-stu-id="ed23a-211">50</span></span>  

<span data-ttu-id="ed23a-212">Quando esse parâmetro for true, as mensagens de log de eventos informativas que normalmente seriam geradas pelo mecanismo de banco de dados serão suprimidas.</span><span class="sxs-lookup"><span data-stu-id="ed23a-212">When this parameter is true, informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-213">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="ed23a-213">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-214">Falso</span><span class="sxs-lookup"><span data-stu-id="ed23a-214">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-215">Tipo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-215">Type:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="ed23a-216">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-217">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="ed23a-217">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-218">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="ed23a-218">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-219">Escopo:</span><span class="sxs-lookup"><span data-stu-id="ed23a-219">Scope:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-220">Instância</span><span class="sxs-lookup"><span data-stu-id="ed23a-220">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-221">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-221">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-222">Sim</span><span class="sxs-lookup"><span data-stu-id="ed23a-222">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-223">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="ed23a-223">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-224">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-224">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-225">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="ed23a-225">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-226">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-226">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-227">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-227">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-228">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-228">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-229">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="ed23a-229">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-230">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-231">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="ed23a-231">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-232">Não</span><span class="sxs-lookup"><span data-stu-id="ed23a-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-233">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="ed23a-233">Availability:</span></span></p></td>
<td><p><span data-ttu-id="ed23a-234">Todos</span><span class="sxs-lookup"><span data-stu-id="ed23a-234">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="ed23a-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed23a-235">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-236"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ed23a-236"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ed23a-237">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ed23a-237">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed23a-238"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ed23a-238"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ed23a-239">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ed23a-239">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed23a-240"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ed23a-240"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ed23a-241">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ed23a-241">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ed23a-242">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ed23a-242">See Also</span></span>

[<span data-ttu-id="ed23a-243">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="ed23a-243">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="ed23a-244">JetInit</span><span class="sxs-lookup"><span data-stu-id="ed23a-244">JetInit</span></span>](./jetinit-function.md)

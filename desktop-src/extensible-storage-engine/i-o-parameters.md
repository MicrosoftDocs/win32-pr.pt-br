---
description: 'Saiba mais sobre: parâmetros de e/s'
title: Parâmetros de e/s
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 13ba0e89602f7e5d4b9df395e89c73c8dc735692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661503"
---
# <a name="io-parameters"></a><span data-ttu-id="a83c0-103">Parâmetros de e/s</span><span class="sxs-lookup"><span data-stu-id="a83c0-103">I/O Parameters</span></span>


<span data-ttu-id="a83c0-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a83c0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="io-parameters"></a><span data-ttu-id="a83c0-105">Parâmetros de e/s</span><span class="sxs-lookup"><span data-stu-id="a83c0-105">I/O Parameters</span></span>

<span data-ttu-id="a83c0-106">Este tópico contém parâmetros que são usados para entrada e saída (e/s).</span><span class="sxs-lookup"><span data-stu-id="a83c0-106">This topic contains parameters that are used for input and output (I/O).</span></span>

<span data-ttu-id="a83c0-107">*JET_paramAccessDeniedRetryPeriod*</span><span class="sxs-lookup"><span data-stu-id="a83c0-107">*JET_paramAccessDeniedRetryPeriod*</span></span>  
<span data-ttu-id="a83c0-108">53</span><span class="sxs-lookup"><span data-stu-id="a83c0-108">53</span></span>  

<span data-ttu-id="a83c0-109">**Windows XP e posterior:**  Esse parâmetro configura a duração do tempo (em milissegundos) que o mecanismo de banco de dados usará para acessar um arquivo bloqueado antes de falhar com JET_errFileAccessDenied.</span><span class="sxs-lookup"><span data-stu-id="a83c0-109">**Windows XP and later:**  This parameter configures the duration of time (in milliseconds) that the database engine will use to access a file that is locked before failing with JET_errFileAccessDenied.</span></span> <span data-ttu-id="a83c0-110">Esse atraso foi projetado para contornar o software antivírus que pode conter alguns dos arquivos do mecanismo de banco de dados aberto brevemente depois que eles são fechados.</span><span class="sxs-lookup"><span data-stu-id="a83c0-110">This time delay is designed to work around anti-virus software that may hold some of the database engine's files open briefly after they are closed.</span></span>

<span data-ttu-id="a83c0-111">**Observação**  Como resultado da lógica de repetição acima, qualquer tentativa de anexar a um banco de dados ou usar um arquivo de log que já esteja em uso pelo mecanismo de banco de dados resultará em um atraso desse tamanho antes que a chamada à API retorne uma falha (legítima).</span><span class="sxs-lookup"><span data-stu-id="a83c0-111">**Note**  As a result of the above retry logic, any attempt to attach to a database or use a log file that is already in use by the database engine will result in a delay of this size before the API call returns a (legitimate) failure.</span></span> <span data-ttu-id="a83c0-112">Esse parâmetro pode ser usado para desativar esse atraso, caso este seja um cenário comum.</span><span class="sxs-lookup"><span data-stu-id="a83c0-112">This parameter can be used to turn down that delay in case this is a common scenario.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-113">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="a83c0-113">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-114">10000</span><span class="sxs-lookup"><span data-stu-id="a83c0-114">10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-115">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-115">Type:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-116">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a83c0-116">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-117">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="a83c0-117">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-118">0 a 4294967295</span><span class="sxs-lookup"><span data-stu-id="a83c0-118">0 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-119">Escopo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-119">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-120">Global</span><span class="sxs-lookup"><span data-stu-id="a83c0-120">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-121">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-121">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-122">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-123">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-123">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-124">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-124">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-125">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="a83c0-125">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-126">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-126">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-127">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-127">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-128">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-128">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-129">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="a83c0-129">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-130">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-130">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-131">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="a83c0-131">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-132">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-132">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-133">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-133">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-134">Windows XP e posterior</span><span class="sxs-lookup"><span data-stu-id="a83c0-134">Windows XP and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a83c0-135">*JET_paramCreatePathIfNotExist*</span><span class="sxs-lookup"><span data-stu-id="a83c0-135">*JET_paramCreatePathIfNotExist*</span></span>  
<span data-ttu-id="a83c0-136">100</span><span class="sxs-lookup"><span data-stu-id="a83c0-136">100</span></span>  

<span data-ttu-id="a83c0-137">Quando esse parâmetro for definido como true, qualquer pasta que estiver ausente em um caminho do sistema de arquivos em uso pelo mecanismo de banco de dados será criada silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="a83c0-137">When this parameter is set to true then any folder that is missing in a file system path in use by the database engine will be silently created.</span></span> <span data-ttu-id="a83c0-138">Caso contrário, a operação que usa o caminho do sistema de arquivos ausente irá falhar com JET_errInvalidPath.</span><span class="sxs-lookup"><span data-stu-id="a83c0-138">Otherwise, the operation that uses the missing file system path will fail with JET_errInvalidPath.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-139">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="a83c0-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-140">Falso</span><span class="sxs-lookup"><span data-stu-id="a83c0-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-141">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="a83c0-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-143">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="a83c0-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-144">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="a83c0-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-145">Escopo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-146">Instância</span><span class="sxs-lookup"><span data-stu-id="a83c0-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-147">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-148">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-149">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-150">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-151">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="a83c0-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-152">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-153">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-154">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-155">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="a83c0-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-156">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-157">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="a83c0-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-158">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-159">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-160">Tudo</span><span class="sxs-lookup"><span data-stu-id="a83c0-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a83c0-161">*JET_paramEnableFileCache*</span><span class="sxs-lookup"><span data-stu-id="a83c0-161">*JET_paramEnableFileCache*</span></span>  
<span data-ttu-id="a83c0-162">126</span><span class="sxs-lookup"><span data-stu-id="a83c0-162">126</span></span>  

<span data-ttu-id="a83c0-163">Quando esse parâmetro for **true**, o mecanismo de banco de dados usará o cache de arquivos do Windows como um cache de leitura para todos os seus vários arquivos.</span><span class="sxs-lookup"><span data-stu-id="a83c0-163">When this parameter is **True**, the database engine will use the Windows file cache as a read cache for all of its various files.</span></span> <span data-ttu-id="a83c0-164">Ele também o usará como um cache de gravação para o banco de dados temporário ou para bancos que estiverem abertos com a recuperação desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a83c0-164">It will also use it as a write cache for the temporary database or for databases that are opened with recovery disabled.</span></span> <span data-ttu-id="a83c0-165">O mecanismo de banco de dados deve desabilitar o cache de gravação para bancos de dados comuns, arquivos de log de transações e arquivos de ponto de verificação para proteger a integridade transacional dos bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="a83c0-165">The database engine must disable write caching for ordinary databases, transaction log files, and checkpoint files to protect the transactional integrity of the databases.</span></span>

<span data-ttu-id="a83c0-166">É importante observar que o uso do cache de arquivos do Windows adicionará uma segunda camada de armazenamento em cache para arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a83c0-166">It is important to note that the use of the Windows file cache will add a second layering of caching for database files.</span></span> <span data-ttu-id="a83c0-167">O cache de banco de dados ainda usará sua própria memória para armazenar em cache os arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a83c0-167">The database cache will still use its own memory to cache the database files.</span></span> <span data-ttu-id="a83c0-168">A intenção desse modo é permitir que o aplicativo configure o mecanismo de banco de dados com um pequeno cache dedicado e permita que o Windows doar memória sobressalente para melhorar ainda mais o cache dos dados do banco de dado.</span><span class="sxs-lookup"><span data-stu-id="a83c0-168">The intent of this mode is to allow the application to configure the database engine with a small dedicated cache and to allow Windows to donate spare memory to further improve the caching of database data.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-169">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="a83c0-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-170">Falso</span><span class="sxs-lookup"><span data-stu-id="a83c0-170">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-171">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="a83c0-172">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-173">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="a83c0-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-174">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="a83c0-174">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-175">Escopo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-176">Global</span><span class="sxs-lookup"><span data-stu-id="a83c0-176">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-177">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-178">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-178">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-179">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-180">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-181">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="a83c0-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-182">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-183">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-184">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-185">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="a83c0-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-186">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-187">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="a83c0-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-188">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-188">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-189">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-190">Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="a83c0-190">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a83c0-191">*JET_paramIOPriority*</span><span class="sxs-lookup"><span data-stu-id="a83c0-191">*JET_paramIOPriority*</span></span>  
<span data-ttu-id="a83c0-192">152</span><span class="sxs-lookup"><span data-stu-id="a83c0-192">152</span></span>  

<span data-ttu-id="a83c0-193">Esse parâmetro controla como o ESE lida com as operações de e/s.</span><span class="sxs-lookup"><span data-stu-id="a83c0-193">This parameter controls how ESE handles I/O operations.</span></span> <span data-ttu-id="a83c0-194">Os valores podem ser definidos como 0 (JET_IOPriorityNormal) para operação normal, ou 1 (JET_IOPriorityLow) para operação de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="a83c0-194">The values can be set to 0 (JET_IOPriorityNormal) for normal operation, or 1 (JET_IOPriorityLow) for low priority operation.</span></span> <span data-ttu-id="a83c0-195">Quando a prioridade é definida como JET_IOPriorityLow, o ESE usa a nova funcionalidade de prioridade de e/s de thread disponível no Windows Vista para reduzir a prioridade de e/s no thread para que as operações de e/s subsequentes sejam emitidas com a nova prioridade baixa.</span><span class="sxs-lookup"><span data-stu-id="a83c0-195">When the priority is set to JET_IOPriorityLow, ESE uses the new thread I/O priority functionality available in Windows Vista to reduce the I/O priority on the thread so that subsequent I/O operations are issued at the new low priority.</span></span>

<span data-ttu-id="a83c0-196">**Windows Vista:**  O JET_paramIOPriority é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a83c0-196">**Windows Vista:**  JET_paramIOPriority is introduced in Windows Vista.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-197">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="a83c0-197">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-198">0</span><span class="sxs-lookup"><span data-stu-id="a83c0-198">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-199">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-199">Type:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-200">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a83c0-200">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-201">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="a83c0-201">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-202">0 - 1</span><span class="sxs-lookup"><span data-stu-id="a83c0-202">0 - 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-203">Escopo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-203">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-204">Instância</span><span class="sxs-lookup"><span data-stu-id="a83c0-204">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-205">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-205">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-206">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-206">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-207">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-207">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-208">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-208">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-209">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="a83c0-209">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-210">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-210">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-211">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-211">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-212">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-212">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-213">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="a83c0-213">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-214">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-214">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-215">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="a83c0-215">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-216">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-216">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-217">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-217">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a83c0-218">Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a83c0-219">*JET_paramOutstandingIOMax*</span><span class="sxs-lookup"><span data-stu-id="a83c0-219">*JET_paramOutstandingIOMax*</span></span>  
<span data-ttu-id="a83c0-220">30</span><span class="sxs-lookup"><span data-stu-id="a83c0-220">30</span></span> 

<span data-ttu-id="a83c0-221">Esse parâmetro controla quantas e/SS de arquivo de banco de dados podem ser enfileiradas no sistema operacional do host ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a83c0-221">This parameter controls how many database file I/Os can be queued in the host operating system at one time.</span></span>

<span data-ttu-id="a83c0-222">Um valor maior para esse parâmetro pode ajudar significativamente o desempenho de um aplicativo de banco de dados grande.</span><span class="sxs-lookup"><span data-stu-id="a83c0-222">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="a83c0-223">**Windows XP e Windows Server 2003:**  Esse parâmetro é ignorado no Windows XP e no Windows Server 2003 e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a83c0-223">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-224">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="a83c0-224">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-225"><strong>Windows 2000: </strong>  64</span><span class="sxs-lookup"><span data-stu-id="a83c0-225"><strong>Windows 2000: </strong>  64</span></span></p>
<p><span data-ttu-id="a83c0-226"><strong>Windows Vista:</strong>   1024</span><span class="sxs-lookup"><span data-stu-id="a83c0-226"><strong>Windows Vista:</strong>   1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-227">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-227">Type:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-228">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a83c0-228">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-229">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="a83c0-229">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-230"><strong>Windows 2000:</strong>  8 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="a83c0-230"><strong>Windows 2000:</strong>  8 – 2147483647</span></span></p>
<p><span data-ttu-id="a83c0-231"><strong>Windows Vista:</strong>  0 a 65536</span><span class="sxs-lookup"><span data-stu-id="a83c0-231"><strong>Windows Vista:</strong>  0 – 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-232">Escopo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-232">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-233">Global</span><span class="sxs-lookup"><span data-stu-id="a83c0-233">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-234">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-234">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-235">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-235">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-236">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-236">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-237">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-237">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-238">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="a83c0-238">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-239">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-239">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-240">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-240">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-241">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-242">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="a83c0-242">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-243">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-243">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-244">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="a83c0-244">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-245">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-246">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-246">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-247">Tudo</span><span class="sxs-lookup"><span data-stu-id="a83c0-247">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a83c0-248">*JET_paramMaxCoalesceReadSize*</span><span class="sxs-lookup"><span data-stu-id="a83c0-248">*JET_paramMaxCoalesceReadSize*</span></span>  
<span data-ttu-id="a83c0-249">164</span><span class="sxs-lookup"><span data-stu-id="a83c0-249">164</span></span>  

<span data-ttu-id="a83c0-250">Número máximo de bytes que podem ser agrupados para uma operação de leitura agrupada.</span><span class="sxs-lookup"><span data-stu-id="a83c0-250">Maximum number of bytes that can be grouped for a coalesced read operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-251">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="a83c0-251">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-252">262144</span><span class="sxs-lookup"><span data-stu-id="a83c0-252">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-253">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-253">Type:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-254">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a83c0-254">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-255">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="a83c0-255">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-256">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="a83c0-256">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-257">Escopo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-257">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-258">Global</span><span class="sxs-lookup"><span data-stu-id="a83c0-258">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-259">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-259">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-260">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-260">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-261">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-261">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-262">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-262">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-263">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="a83c0-263">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-264">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-264">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-265">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-265">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-266">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-266">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-267">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="a83c0-267">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-268">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-268">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-269">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="a83c0-269">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-270">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-270">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-271">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-271">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a83c0-272">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a83c0-273">*JET_paramMaxCoalesceWriteSize*</span><span class="sxs-lookup"><span data-stu-id="a83c0-273">*JET_paramMaxCoalesceWriteSize*</span></span>  
<span data-ttu-id="a83c0-274">165</span><span class="sxs-lookup"><span data-stu-id="a83c0-274">165</span></span>  

<span data-ttu-id="a83c0-275">Número máximo de bytes que podem ser agrupados para uma operação de gravação agrupada.</span><span class="sxs-lookup"><span data-stu-id="a83c0-275">Maximum number of bytes that can be grouped for a coalesced write operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-276">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="a83c0-276">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-277">393216</span><span class="sxs-lookup"><span data-stu-id="a83c0-277">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-278">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-278">Type:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-279">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a83c0-279">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-280">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="a83c0-280">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-281">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="a83c0-281">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-282">Escopo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-282">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-283">Global</span><span class="sxs-lookup"><span data-stu-id="a83c0-283">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-284">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-284">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-285">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-285">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-286">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-286">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-287">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-288">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="a83c0-288">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-289">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-289">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-290">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-290">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-291">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-292">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="a83c0-292">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-293">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-293">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-294">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="a83c0-294">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-295">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-295">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-296">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-296">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-297">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a83c0-297">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a83c0-298">*JET_paramMaxCoalesceReadGapSize*</span><span class="sxs-lookup"><span data-stu-id="a83c0-298">*JET_paramMaxCoalesceReadGapSize*</span></span>  
<span data-ttu-id="a83c0-299">166</span><span class="sxs-lookup"><span data-stu-id="a83c0-299">166</span></span>  

<span data-ttu-id="a83c0-300">Número máximo de bytes que podem ser gappeddos para uma operação de e/s de gravação agrupada.</span><span class="sxs-lookup"><span data-stu-id="a83c0-300">Maximum number of bytes that can be gapped for a coalesced write I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-301">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="a83c0-301">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-302">262144</span><span class="sxs-lookup"><span data-stu-id="a83c0-302">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-303">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-303">Type:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-304">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a83c0-304">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-305">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="a83c0-305">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-306">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="a83c0-306">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-307">Escopo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-307">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-308">Global</span><span class="sxs-lookup"><span data-stu-id="a83c0-308">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-309">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-309">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-310">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-310">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-311">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-311">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-312">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-312">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-313">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="a83c0-313">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-314">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-314">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-315">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-315">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-316">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-316">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-317">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="a83c0-317">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-318">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-318">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-319">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="a83c0-319">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-320">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-320">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-321">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-321">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a83c0-322">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a83c0-323">*JET_paramMaxCoalesceWriteGapSize*</span><span class="sxs-lookup"><span data-stu-id="a83c0-323">*JET_paramMaxCoalesceWriteGapSize*</span></span>  
<span data-ttu-id="a83c0-324">167</span><span class="sxs-lookup"><span data-stu-id="a83c0-324">167</span></span>  

<span data-ttu-id="a83c0-325">Número máximo de bytes que podem ser gapped para uma operação de e/s de leitura agrupada.</span><span class="sxs-lookup"><span data-stu-id="a83c0-325">Max number of bytes that can be gapped for a coalesced read I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-326">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="a83c0-326">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-327">393216</span><span class="sxs-lookup"><span data-stu-id="a83c0-327">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-328">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-328">Type:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-329">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a83c0-329">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-330">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="a83c0-330">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-331">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="a83c0-331">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-332">Escopo:</span><span class="sxs-lookup"><span data-stu-id="a83c0-332">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-333">Global</span><span class="sxs-lookup"><span data-stu-id="a83c0-333">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-334">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-334">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-335">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-335">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-336">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a83c0-336">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-337">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-337">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-338">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="a83c0-338">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-339">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-339">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-340">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-340">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-341">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-341">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-342">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="a83c0-342">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-343">Sim</span><span class="sxs-lookup"><span data-stu-id="a83c0-343">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-344">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="a83c0-344">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-345">Não</span><span class="sxs-lookup"><span data-stu-id="a83c0-345">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-346">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="a83c0-346">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a83c0-347">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a83c0-347">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="a83c0-348">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a83c0-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-349"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a83c0-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a83c0-350">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a83c0-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a83c0-351"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a83c0-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a83c0-352">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a83c0-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a83c0-353"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a83c0-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a83c0-354">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a83c0-354">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a83c0-355">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a83c0-355">See Also</span></span>

[<span data-ttu-id="a83c0-356">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="a83c0-356">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a83c0-357">JetInit</span><span class="sxs-lookup"><span data-stu-id="a83c0-357">JetInit</span></span>](./jetinit-function.md)

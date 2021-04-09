---
description: 'Saiba mais sobre: parâmetros de banco de dados'
title: Parâmetros de Banco de Dados
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090896"
---
# <a name="database-parameters"></a><span data-ttu-id="2b868-103">Parâmetros de Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="2b868-103">Database Parameters</span></span>


<span data-ttu-id="2b868-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2b868-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-parameters"></a><span data-ttu-id="2b868-105">Parâmetros de Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="2b868-105">Database Parameters</span></span>

<span data-ttu-id="2b868-106">Este tópico contém parâmetros que são usados para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-106">This topic contains parameters that are used for the database.</span></span>

<span data-ttu-id="2b868-107">*JET_paramCheckFormatWhenOpenFail*</span><span class="sxs-lookup"><span data-stu-id="2b868-107">*JET_paramCheckFormatWhenOpenFail*</span></span>  
<span data-ttu-id="2b868-108">44</span><span class="sxs-lookup"><span data-stu-id="2b868-108">44</span></span>  

<span data-ttu-id="2b868-109">Esse parâmetro, quando definido, fará com que o [JetInit](./jetinit-function.md) retorne um erro especial quando um banco de dados ou log de transações de uma versão anterior do mecanismo de banco de dados for aberto.</span><span class="sxs-lookup"><span data-stu-id="2b868-109">This parameter, when set, will cause [JetInit](./jetinit-function.md) to return a special error when a database or transaction log from a previous release of the database engine is opened.</span></span> <span data-ttu-id="2b868-110">Esses erros são:</span><span class="sxs-lookup"><span data-stu-id="2b868-110">These errors are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b868-111">Erro</span><span class="sxs-lookup"><span data-stu-id="2b868-111">Error</span></span></p></th>
<th><p><span data-ttu-id="2b868-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b868-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-113">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="2b868-113">JET_errDatabase200Format</span></span></p></td>
<td><p><span data-ttu-id="2b868-114">O banco de dados e/ou os arquivos de log de transações foram criados com o mecanismo de banco de dados no Windows NT 3,51.</span><span class="sxs-lookup"><span data-stu-id="2b868-114">The database and/or transaction log files were created with the database engine in Windows NT 3.51.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-115">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="2b868-115">JET_errDatabase400Format</span></span></p></td>
<td><p><span data-ttu-id="2b868-116">O banco de dados e/ou os arquivos de log de transações foram criados com o mecanismo de banco de dados em uma versão de teste anterior ao Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="2b868-116">The database and/or transaction log files were created with the database engine in a test release prior to Windows NT Server 4.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-117">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="2b868-117">JET_errDatabase500Format</span></span></p></td>
<td><p><span data-ttu-id="2b868-118">O banco de dados e/ou os arquivos de log de transações foram criados com o mecanismo de banco de dados no Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="2b868-118">The database and/or transaction log files were created with the database engine in Windows NT Server 4.0.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-119">**Windows Vista:**  Para o Windows Vista e posterior, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-119">**Windows Vista:**  For Windows Vista and later, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-120">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-120">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-121">True</span><span class="sxs-lookup"><span data-stu-id="2b868-121">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-122">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-122">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="2b868-123">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-124">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-124">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-125">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="2b868-125">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-126">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-126">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-127">Instância</span><span class="sxs-lookup"><span data-stu-id="2b868-127">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-128">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-128">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-129">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-130">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-130">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-131">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-132">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-132">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-133">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-134">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-134">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-135">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-136">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-136">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-137">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-138">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-138">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-139">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-139">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-140">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-140">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-141">Todos</span><span class="sxs-lookup"><span data-stu-id="2b868-141">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-142">*JET_paramDatabasePageSize*</span><span class="sxs-lookup"><span data-stu-id="2b868-142">*JET_paramDatabasePageSize*</span></span>  
<span data-ttu-id="2b868-143">64</span><span class="sxs-lookup"><span data-stu-id="2b868-143">64</span></span>  

<span data-ttu-id="2b868-144">Esse parâmetro configura o tamanho da página para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-144">This parameter configures the page size for the database.</span></span> <span data-ttu-id="2b868-145">O tamanho da página é a menor unidade de alocação de espaço possível para um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-145">The page size is the smallest unit of space allocation possible for a database file.</span></span> <span data-ttu-id="2b868-146">O tamanho da página do banco de dados também é muito importante porque ele define o limite superior do tamanho de um registro individual no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-146">The database page size is also very important because it sets the upper limit on the size of an individual record in the database.</span></span>

<span data-ttu-id="2b868-147">**Observação** Há suporte para apenas um tamanho de página de banco de dados por processo no momento.</span><span class="sxs-lookup"><span data-stu-id="2b868-147">**Note** Only one database page size is supported per process at this time.</span></span> <span data-ttu-id="2b868-148">Isso significa que, se você estiver em um único processo que contém diferentes aplicativos que usam o mecanismo de banco de dados, todos eles deverão concordar em um tamanho de página de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-148">This means that if you are in a single process that contains different applications that use the database engine then they must all agree on a database page size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-149">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-149">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-150">4096</span><span class="sxs-lookup"><span data-stu-id="2b868-150">4096</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-151">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-151">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-152">Integer</span><span class="sxs-lookup"><span data-stu-id="2b868-152">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-153">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-153">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-154">2048, 4096, 8192</span><span class="sxs-lookup"><span data-stu-id="2b868-154">2048, 4096, 8192</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-155">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-155">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-156">Global</span><span class="sxs-lookup"><span data-stu-id="2b868-156">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-157">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-157">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-158">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-159">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-159">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-160">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-161">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-161">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-162">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-163">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-163">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-164">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-164">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-165">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-165">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-166">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-166">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-167">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-167">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-168">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-168">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-169">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-169">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-170">Todos</span><span class="sxs-lookup"><span data-stu-id="2b868-170">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-171">*JET_paramDbExtensionSize*</span><span class="sxs-lookup"><span data-stu-id="2b868-171">*JET_paramDbExtensionSize*</span></span>  
<span data-ttu-id="2b868-172">18</span><span class="sxs-lookup"><span data-stu-id="2b868-172">18</span></span>  

<span data-ttu-id="2b868-173">Esse parâmetro controla a quantidade de espaço que é adicionada a um arquivo de banco de dados cada vez que ele precisa aumentar para acomodar mais informações.</span><span class="sxs-lookup"><span data-stu-id="2b868-173">This parameter controls the amount of space that is added to a database file each time it needs to grow to accommodate more data.</span></span> <span data-ttu-id="2b868-174">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-174">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-175">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-176">256</span><span class="sxs-lookup"><span data-stu-id="2b868-176">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-177">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-177">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-178">Integer</span><span class="sxs-lookup"><span data-stu-id="2b868-178">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-179">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-179">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-180">1 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="2b868-180">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-181">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-181">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-182">Instância</span><span class="sxs-lookup"><span data-stu-id="2b868-182">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-183">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-183">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-184">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-184">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-185">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-185">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-186">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-186">No</span></span></p>
<p><span data-ttu-id="2b868-187"><strong>Windows Vista:</strong>  Para o Windows Vista e posterior: Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-187"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-188">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-189">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-190">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-191">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-191">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-192">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-193">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-194">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-195">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-195">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-196">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-197">Todos</span><span class="sxs-lookup"><span data-stu-id="2b868-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-198">*JET_paramEnableIndexChecking*</span><span class="sxs-lookup"><span data-stu-id="2b868-198">*JET_paramEnableIndexChecking*</span></span>  
<span data-ttu-id="2b868-199">45</span><span class="sxs-lookup"><span data-stu-id="2b868-199">45</span></span>  

<span data-ttu-id="2b868-200">Quando esse parâmetro for true, todos os bancos de dados serão verificados em [JetAttachDatabase](./jetattachdatabase-function.md) tempo para índices em colunas de chave Unicode que foram criadas usando uma versão mais antiga da biblioteca NLS no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2b868-200">When this parameter is true, every database is checked at [JetAttachDatabase](./jetattachdatabase-function.md) time for indexes over Unicode key columns that were built using an older version of the NLS library in the operating system.</span></span> <span data-ttu-id="2b868-201">Isso deve ser feito porque o mecanismo de banco de dados persiste as chaves de classificação geradas por [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) e o valor dessas chaves de classificação muda de Release para Release.</span><span class="sxs-lookup"><span data-stu-id="2b868-201">This must be done because the database engine persists the sort keys generated by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) and the value of these sort keys change from release to release.</span></span>

<span data-ttu-id="2b868-202">Se for detectado que um índice primário está nesse estado, [JetAttachDatabase](./jetattachdatabase-function.md) sempre falhará com JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="2b868-202">If a primary index is detected to be in this state then [JetAttachDatabase](./jetattachdatabase-function.md) will always fail with JET_errPrimaryIndexCorrupted.</span></span>

<span data-ttu-id="2b868-203">Se algum índice secundário for detectado para estar nesse estado, haverá dois resultados possíveis.</span><span class="sxs-lookup"><span data-stu-id="2b868-203">If any secondary indexes are detected to be in this state then there are two possible outcomes.</span></span> <span data-ttu-id="2b868-204">Se JET_bitDbDeleteCorruptIndexes foi passado para [JetAttachDatabase](./jetattachdatabase-function.md) , esses índices serão excluídos e JET_wrnCorruptIndexDeleted serão retornados de [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="2b868-204">If JET_bitDbDeleteCorruptIndexes was passed to [JetAttachDatabase](./jetattachdatabase-function.md) then these indexes will be deleted and JET_wrnCorruptIndexDeleted will be returned from [JetAttachDatabase](./jetattachdatabase-function.md).</span></span> <span data-ttu-id="2b868-205">Esses índices precisarão ser recriados pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2b868-205">These indexes will need to be recreated by your application.</span></span> <span data-ttu-id="2b868-206">Se JET_bitDbDeleteCorruptIndexes não foi passado para [JetAttachDatabase](./jetattachdatabase-function.md) , a chamada falhará com JET_errSecondaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="2b868-206">If JET_bitDbDeleteCorruptIndexes was not passed to [JetAttachDatabase](./jetattachdatabase-function.md) then the call will fail with JET_errSecondaryIndexCorrupted.</span></span>

<span data-ttu-id="2b868-207">**Observação** É altamente recomendável que esse parâmetro seja definido como true pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2b868-207">**Note** It is strongly recommended that this parameter be set to True by your application.</span></span>

<span data-ttu-id="2b868-208">**Observação** É altamente recomendável que os aplicativos evitem o uso de colunas de chave Unicode em seus índices de chave primária (clusterizados).</span><span class="sxs-lookup"><span data-stu-id="2b868-208">**Note** It is very strongly recommended that applications avoid the use of Unicode key columns in their primary key (clustered) indexes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-209">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-209">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-210">Falso</span><span class="sxs-lookup"><span data-stu-id="2b868-210">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-211">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-212">Boolean</span><span class="sxs-lookup"><span data-stu-id="2b868-212">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-213">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-214">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="2b868-214">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-215">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-215">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-216">Global</span><span class="sxs-lookup"><span data-stu-id="2b868-216">Global</span></span></p>
<p><span data-ttu-id="2b868-217"><strong>Windows Vista:</strong>  Para o Windows Vista e posterior: instância</span><span class="sxs-lookup"><span data-stu-id="2b868-217"><strong>Windows Vista:</strong>  For Windows Vista and later: Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-218">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-219">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-219">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-220">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-220">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-221">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-221">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-222">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-222">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-223">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-223">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-224">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-224">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-225">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-225">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-226">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-226">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-227">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-227">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-228">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-228">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-229">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-229">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-230">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-230">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-231">Todos</span><span class="sxs-lookup"><span data-stu-id="2b868-231">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-232">*JET_paramEnableIndexCleanup*</span><span class="sxs-lookup"><span data-stu-id="2b868-232">*JET_paramEnableIndexCleanup*</span></span>  
<span data-ttu-id="2b868-233">54</span><span class="sxs-lookup"><span data-stu-id="2b868-233">54</span></span>  

<span data-ttu-id="2b868-234">Quando esse parâmetro é definido como true, o mecanismo de banco de dados pode limpar automaticamente os índices em colunas de chave Unicode em [JetInit](./jetinit-function.md) , conforme necessário, para evitar alterações no formato de banco de dados causados por alterações na biblioteca NLS no Windows.</span><span class="sxs-lookup"><span data-stu-id="2b868-234">When this parameter is set to true, then the database engine may automatically clean up indexes over Unicode key columns at [JetInit](./jetinit-function.md) time as necessary to avoid database format changes caused by changes to the NLS library in Windows.</span></span> <span data-ttu-id="2b868-235">Essas alterações são feitas rotineiramente na biblioteca NLS para adicionar suporte a novos idiomas, para adicionar caracteres ausentes a um idioma, para adicionar uma ordem de agrupamento a um idioma ou para corrigir bugs na ordem de agrupamento de um idioma.</span><span class="sxs-lookup"><span data-stu-id="2b868-235">Such changes are made routinely to the NLS library to add support for new languages, to add missing characters to a language, to add a collation order to a language, or to fix bugs in the collation order of a language.</span></span> <span data-ttu-id="2b868-236">Essas alterações afetam as chaves de classificação produzidas por [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) que são mantidas pelo mecanismo de banco de dados como componentes de chaves de índice.</span><span class="sxs-lookup"><span data-stu-id="2b868-236">These changes affect the sort keys produced by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) which are persisted by the database engine as components of index keys.</span></span>

<span data-ttu-id="2b868-237">É importante perceber que é possível que as alterações no índice sejam tão ótimas que uma limpeza incremental não é possível.</span><span class="sxs-lookup"><span data-stu-id="2b868-237">It is important to realize that it is possible for the changes to the index to be so great that an incremental cleanup is not possible.</span></span> <span data-ttu-id="2b868-238">Nesse caso, o índice será manipulado conforme prescrito pelo **JET_paramEnableIndexChecking**.</span><span class="sxs-lookup"><span data-stu-id="2b868-238">In this case, the index will be handled as prescribed by **JET_paramEnableIndexChecking**.</span></span>

<span data-ttu-id="2b868-239">**Observação** É altamente recomendável que esse parâmetro e **JET_paramEnableIndexChecking** sejam definidos como **true** pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2b868-239">**Note** It is strongly recommended that this parameter and **JET_paramEnableIndexChecking** be set to **True** by your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-240">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-240">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-241">True</span><span class="sxs-lookup"><span data-stu-id="2b868-241">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-242">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-242">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-243">Boolean</span><span class="sxs-lookup"><span data-stu-id="2b868-243">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-244">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-244">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-245">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="2b868-245">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-246">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-246">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-247">Instância</span><span class="sxs-lookup"><span data-stu-id="2b868-247">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-248">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-248">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-249">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-249">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-250">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-250">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-251">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-251">No</span></span></p>
<p><span data-ttu-id="2b868-252"><strong>Windows Vista:</strong>  Para o Windows Vista e posterior: Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-252"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-253">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-253">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-254">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-254">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-255">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-255">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-256">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-256">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-257">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-257">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-258">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-258">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-259">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-259">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-260">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-260">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-261">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-261">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-262">Windows Server 2003 e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="2b868-262">Windows Server 2003 and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-263">*JET_paramOneDatabasePerSession*</span><span class="sxs-lookup"><span data-stu-id="2b868-263">*JET_paramOneDatabasePerSession*</span></span>  
<span data-ttu-id="2b868-264">102</span><span class="sxs-lookup"><span data-stu-id="2b868-264">102</span></span>  

<span data-ttu-id="2b868-265">Quando esse parâmetro for true, somente um banco de dados poderá ser aberto usando [JetOpenDatabase](./jetopendatabase-function.md) por uma determinada sessão ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="2b868-265">When this parameter is true then only one database is allowed to be opened using [JetOpenDatabase](./jetopendatabase-function.md) by a given session at one time.</span></span> <span data-ttu-id="2b868-266">O banco de dados temporário é excluído dessa restrição.</span><span class="sxs-lookup"><span data-stu-id="2b868-266">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="2b868-267">**Windows XP e Windows Server 2003:**  Esse parâmetro é somente gravação no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2b868-267">**Windows XP and Windows Server 2003:**  This parameter is write only on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="2b868-268">**Windows Vista:**  Esse parâmetro se comporta normalmente a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2b868-268">**Windows Vista:**  This parameter behaves normally as of Windows Vista.</span></span>

<span data-ttu-id="2b868-269">**Observação**  Esse parâmetro é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="2b868-269">**Note**  This parameter is write only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-270">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-270">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-271">Falso</span><span class="sxs-lookup"><span data-stu-id="2b868-271">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-272">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-272">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="2b868-273">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-274">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-274">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-275">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="2b868-275">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-276">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-276">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-277">Global</span><span class="sxs-lookup"><span data-stu-id="2b868-277">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-278">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-278">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-279">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-279">No</span></span></p>
<p><span data-ttu-id="2b868-280"><strong>Windows Vista:</strong>  Para o Windows Vista e posterior: Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-280"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-281">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-281">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-282">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-282">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-283">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-283">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-284">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-284">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-285">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-285">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-286">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-286">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-287">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-287">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-288">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-288">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-289">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-289">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-290">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-290">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-291">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-291">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-292">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="2b868-292">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-293">*JET_paramEnableOnlineDefrag*</span><span class="sxs-lookup"><span data-stu-id="2b868-293">*JET_paramEnableOnlineDefrag*</span></span>  
<span data-ttu-id="2b868-294">35</span><span class="sxs-lookup"><span data-stu-id="2b868-294">35</span></span>  

<span data-ttu-id="2b868-295">Esse parâmetro controla o comportamento da desfragmentação online quando iniciado usando [JetDefragment](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="2b868-295">This parameter controls the behavior of online defragmentation when initiated using [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="2b868-296">Consulte [JetDefragment](./jetdefragment-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="2b868-296">Please see [JetDefragment](./jetdefragment-function.md) for more information.</span></span>

<span data-ttu-id="2b868-297">Windows 2000: no Windows 2000, esse parâmetro era um booliano simples que faria a desfragmentação online quando iniciado por [JetDefragment](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="2b868-297">Windows 2000:  On Windows 2000, this parameter was a simple Boolean that would gate online defragmentation when initiated by [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="2b868-298">Quando definido como **true**, a desfragmentação online será executada nos registros de cada tabela no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-298">When set to **TRUE**, online defragmentation will be performed on the records of each table in the database.</span></span>

<span data-ttu-id="2b868-299">**Windows XP:**  No Windows XP e versões posteriores, esse parâmetro pode ser definido como uma ou mais das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="2b868-299">**Windows XP:**  On Windows XP and later releases, this parameter can be set to one or more of the following options:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b868-300">Opção</span><span class="sxs-lookup"><span data-stu-id="2b868-300">Option</span></span></p></th>
<th><p><span data-ttu-id="2b868-301">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b868-301">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-302">JET_OnlineDefragDisable</span><span class="sxs-lookup"><span data-stu-id="2b868-302">JET_OnlineDefragDisable</span></span></p></td>
<td><p><span data-ttu-id="2b868-303">Não execute a desfragmentação online.</span><span class="sxs-lookup"><span data-stu-id="2b868-303">Do not perform online defragmentation.</span></span> <span data-ttu-id="2b868-304">Este é o binário equivalente à configuração de false do Windows 2000 para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2b868-304">This is the binary equivalent to the Windows 2000 setting of False for this parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-305">JET_OnlineDefragAllOBSOLETE</span><span class="sxs-lookup"><span data-stu-id="2b868-305">JET_OnlineDefragAllOBSOLETE</span></span></p></td>
<td><p><span data-ttu-id="2b868-306">Execute a desfragmentação online completa.</span><span class="sxs-lookup"><span data-stu-id="2b868-306">Perform full online defragmentation.</span></span> <span data-ttu-id="2b868-307">Esse é o binário equivalente à configuração true do Windows 2000 para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2b868-307">This is the binary equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-308">JET_OnlineDefragDatabases</span><span class="sxs-lookup"><span data-stu-id="2b868-308">JET_OnlineDefragDatabases</span></span></p></td>
<td><p><span data-ttu-id="2b868-309">Execute a desfragmentação online dos registros de cada tabela no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-309">Perform online defragmentation of the records of each table in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-310">JET_OnlineDefragSpaceTrees</span><span class="sxs-lookup"><span data-stu-id="2b868-310">JET_OnlineDefragSpaceTrees</span></span></p></td>
<td><p><span data-ttu-id="2b868-311">Execute a desfragmentação online das árvores de espaço de cada tabela no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-311">Perform online defragmentation of the space trees of each table in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-312">JET_OnlineDefragStreamingFiles</span><span class="sxs-lookup"><span data-stu-id="2b868-312">JET_OnlineDefragStreamingFiles</span></span></p></td>
<td><p><span data-ttu-id="2b868-313">Esse parâmetro é usado para dar suporte à infraestrutura do Microsoft Exchange e não se destina a ser usado em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2b868-313">This parameter is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-314">JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="2b868-314">JET_OnlineDefragAll</span></span></p></td>
<td><p><span data-ttu-id="2b868-315">Execute a desfragmentação online completa.</span><span class="sxs-lookup"><span data-stu-id="2b868-315">Perform full online defragmentation.</span></span> <span data-ttu-id="2b868-316">Esse é o equivalente conceitual da configuração true do Windows 2000 para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2b868-316">This is the conceptual equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-317">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-317">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-318"><strong>Windows 2000:</strong>  True</span><span class="sxs-lookup"><span data-stu-id="2b868-318"><strong>Windows 2000:</strong>  True</span></span></p>
<p><span data-ttu-id="2b868-319"><strong>Windows XP: para Windows XP e posterior:</strong> JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="2b868-319"><strong>Windows XP:  For Windows XP and later:</strong> JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-320">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-320">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-321"><strong>Windows 2000:</strong>  Boolean</span><span class="sxs-lookup"><span data-stu-id="2b868-321"><strong>Windows 2000:</strong>  Boolean</span></span></p>
<p><span data-ttu-id="2b868-322"><strong>Windows XP e posterior:</strong>  JET_GRBIT (inteiro)</span><span class="sxs-lookup"><span data-stu-id="2b868-322"><strong>Windows XP and later:</strong>  JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-323">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-323">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-324"><strong>Windows 2000:</strong>  Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="2b868-324"><strong>Windows 2000:</strong>  False, True</span></span></p>
<p><span data-ttu-id="2b868-325"><strong>Windows XP e posterior:</strong>  0 – JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="2b868-325"><strong>Windows XP and later:</strong>  0 – JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-326">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-327">Instância</span><span class="sxs-lookup"><span data-stu-id="2b868-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-328">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-329">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-330">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-331">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-331">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-332">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-333">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-334">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-335">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-336">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-337">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-338">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-339">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-340">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-341">Todos</span><span class="sxs-lookup"><span data-stu-id="2b868-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-342">*JET_paramPageFragment*</span><span class="sxs-lookup"><span data-stu-id="2b868-342">*JET_paramPageFragment*</span></span>  
<span data-ttu-id="2b868-343">20</span><span class="sxs-lookup"><span data-stu-id="2b868-343">20</span></span>  

<span data-ttu-id="2b868-344">Esse parâmetro é o limite que o mecanismo de banco de dados usa para controlar a fragmentação de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="2b868-344">This parameter is the threshold that the database engine uses to control free space fragmentation.</span></span> <span data-ttu-id="2b868-345">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-345">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-346">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-347">8</span><span class="sxs-lookup"><span data-stu-id="2b868-347">8</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-348">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-349">Integer</span><span class="sxs-lookup"><span data-stu-id="2b868-349">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-350">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-351">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="2b868-351">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-352">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-353">Instância</span><span class="sxs-lookup"><span data-stu-id="2b868-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-354">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-355">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-356">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-357">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-358">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-359">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-359">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-360">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-361">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-362">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-363">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-364">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-365">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-366">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-367">Todos</span><span class="sxs-lookup"><span data-stu-id="2b868-367">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-368">*JET_paramRecordUpgradeDirtyLevel*</span><span class="sxs-lookup"><span data-stu-id="2b868-368">*JET_paramRecordUpgradeDirtyLevel*</span></span>  
<span data-ttu-id="2b868-369">78</span><span class="sxs-lookup"><span data-stu-id="2b868-369">78</span></span>

<span data-ttu-id="2b868-370">Esse parâmetro controla a agressividade com que o Gerenciador de cache de página de banco de dados gravará uma página de banco de dados que passou por uma conversão de formato in-loco.</span><span class="sxs-lookup"><span data-stu-id="2b868-370">This parameter controls how aggressively the database page cache manager will write a database page that has undergone an in place format conversion.</span></span> <span data-ttu-id="2b868-371">Essas conversões de formato ocorrem imediatamente conforme as páginas são carregadas de um banco de dados que foi criado com o mecanismo de banco de dados do Windows 2000, mas usados por uma versão do Windows XP ou posterior do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-371">These format conversions occur on the fly as pages are loaded from a database that was created with the Windows 2000 database engine but used by a Windows XP or later release of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-372">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-372">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-373">1</span><span class="sxs-lookup"><span data-stu-id="2b868-373">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-374">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-374">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-375">Integer</span><span class="sxs-lookup"><span data-stu-id="2b868-375">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-376">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-376">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-377">0-3</span><span class="sxs-lookup"><span data-stu-id="2b868-377">0-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-378">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-378">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-379">Global</span><span class="sxs-lookup"><span data-stu-id="2b868-379">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-380">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-380">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-381">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-382">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-382">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-383">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-384">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-384">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-385">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-385">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-386">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-386">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-387">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-387">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-388">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-388">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-389">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-389">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-390">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-390">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-391">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-391">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-392">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-392">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-393">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="2b868-393">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-394">*JET_paramWaypointLatency*</span><span class="sxs-lookup"><span data-stu-id="2b868-394">*JET_paramWaypointLatency*</span></span>  
<span data-ttu-id="2b868-395">153</span><span class="sxs-lookup"><span data-stu-id="2b868-395">153</span></span>  

<span data-ttu-id="2b868-396">A latência (em logs) por trás da dica/log confirmado mais alto para adiar liberações de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2b868-396">The latency (in logs) behind the tip / highest committed log to defer database page flushes.</span></span> <span data-ttu-id="2b868-397">A habilitação dessa latência pode permitir a recuperação do banco de dados no caso de perda catastrófica do arquivo de log mais recente.</span><span class="sxs-lookup"><span data-stu-id="2b868-397">Enabling this latency can allow database recovery in the case of catastrophic loss of the most recent logfile.</span></span> <span data-ttu-id="2b868-398">Consulte JET_bitReplayIgnoreLostLogs.</span><span class="sxs-lookup"><span data-stu-id="2b868-398">See JET_bitReplayIgnoreLostLogs.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-399">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-399">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-400">0</span><span class="sxs-lookup"><span data-stu-id="2b868-400">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-401">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-401">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-402">Integer</span><span class="sxs-lookup"><span data-stu-id="2b868-402">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-403">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-403">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-404">0-1023</span><span class="sxs-lookup"><span data-stu-id="2b868-404">0-1023</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-405">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-405">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-406">Instância</span><span class="sxs-lookup"><span data-stu-id="2b868-406">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-407">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-407">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-408">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-409">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-409">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-410">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-410">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-411">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-411">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-412">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-412">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-413">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-413">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-414">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-414">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-415">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-415">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-416">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-416">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-417">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-417">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-418">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-418">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-419">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-419">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b868-420">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-421">*JET_paramDefragmentSequentialBTrees*</span><span class="sxs-lookup"><span data-stu-id="2b868-421">*JET_paramDefragmentSequentialBTrees*</span></span>  
<span data-ttu-id="2b868-422">160</span><span class="sxs-lookup"><span data-stu-id="2b868-422">160</span></span>  

<span data-ttu-id="2b868-423">Ativar/desativar a desfragmentação de árvore B sequencial automática.</span><span class="sxs-lookup"><span data-stu-id="2b868-423">Turn on/off automatic sequential B-tree defragmentation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-424">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-424">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-425">1</span><span class="sxs-lookup"><span data-stu-id="2b868-425">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-426">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-426">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-427">Boolean</span><span class="sxs-lookup"><span data-stu-id="2b868-427">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-428">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-428">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-429">0-1</span><span class="sxs-lookup"><span data-stu-id="2b868-429">0-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-430">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-430">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-431">Instância</span><span class="sxs-lookup"><span data-stu-id="2b868-431">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-432">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-432">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-433">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-433">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-434">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-434">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-435">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-435">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-436">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-436">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-437">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-437">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-438">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-438">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-439">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-439">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-440">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-440">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-441">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-442">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-442">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-443">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-443">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-444">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-444">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b868-445">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span><span class="sxs-lookup"><span data-stu-id="2b868-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span></span>  
<span data-ttu-id="2b868-447">161</span><span class="sxs-lookup"><span data-stu-id="2b868-447">161</span></span>  

<span data-ttu-id="2b868-448">Determina com que frequência a densidade da árvore B é verificada.</span><span class="sxs-lookup"><span data-stu-id="2b868-448">Determines how frequently B-tree density is checked.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-449">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-449">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-450">10</span><span class="sxs-lookup"><span data-stu-id="2b868-450">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-451">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-451">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-452">Integer</span><span class="sxs-lookup"><span data-stu-id="2b868-452">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-453">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-453">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-454">0-inteiro máx.</span><span class="sxs-lookup"><span data-stu-id="2b868-454">0-Max Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-455">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-455">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-456">Instância</span><span class="sxs-lookup"><span data-stu-id="2b868-456">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-457">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-457">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-458">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-459">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-459">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-460">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-461">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-461">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-462">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-463">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-463">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-464">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-465">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-465">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-466">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-466">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-467">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-467">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-468">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-468">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-469">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-469">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-470">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b868-470">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b868-471">*JET_paramIOThrottlingTimeQuanta*</span><span class="sxs-lookup"><span data-stu-id="2b868-471">*JET_paramIOThrottlingTimeQuanta*</span></span>  
<span data-ttu-id="2b868-472">162</span><span class="sxs-lookup"><span data-stu-id="2b868-472">162</span></span>  

<span data-ttu-id="2b868-473">Tempo máximo, em milissegundos, que o mecanismo de limitação de e/s fornece uma tarefa a ser executada para que ela seja considerada ' concluída '.</span><span class="sxs-lookup"><span data-stu-id="2b868-473">Max time, in milliseconds, that the I/O throttling mechanism gives a task to run for it to be considered 'completed'.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-474">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="2b868-474">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="2b868-475">125</span><span class="sxs-lookup"><span data-stu-id="2b868-475">125</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-476">Tipo:</span><span class="sxs-lookup"><span data-stu-id="2b868-476">Type:</span></span></p></td>
<td><p><span data-ttu-id="2b868-477">Integer</span><span class="sxs-lookup"><span data-stu-id="2b868-477">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-478">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="2b868-478">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="2b868-479">0-10000</span><span class="sxs-lookup"><span data-stu-id="2b868-479">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-480">Escopo:</span><span class="sxs-lookup"><span data-stu-id="2b868-480">Scope:</span></span></p></td>
<td><p><span data-ttu-id="2b868-481">Global</span><span class="sxs-lookup"><span data-stu-id="2b868-481">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-482">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-482">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-483">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-483">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-484">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="2b868-484">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="2b868-485">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-485">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-486">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="2b868-486">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="2b868-487">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-487">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-488">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-488">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-489">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-489">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-490">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="2b868-490">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="2b868-491">Sim</span><span class="sxs-lookup"><span data-stu-id="2b868-491">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-492">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="2b868-492">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="2b868-493">Não</span><span class="sxs-lookup"><span data-stu-id="2b868-493">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-494">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="2b868-494">Availability:</span></span></p></td>
<td><p><span data-ttu-id="2b868-495">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b868-495">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="2b868-496">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b868-496">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b868-497"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2b868-497"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2b868-498">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2b868-498">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b868-499"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="2b868-499"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2b868-500">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2b868-500">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b868-501"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="2b868-501"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2b868-502">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="2b868-502">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2b868-503">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2b868-503">See Also</span></span>

[<span data-ttu-id="2b868-504">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="2b868-504">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="2b868-505">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="2b868-505">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="2b868-506">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="2b868-506">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="2b868-507">JetInit</span><span class="sxs-lookup"><span data-stu-id="2b868-507">JetInit</span></span>](./jetinit-function.md)

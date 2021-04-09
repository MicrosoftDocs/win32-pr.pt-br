---
description: 'Saiba mais sobre: parâmetros de banco de dados temporários'
title: Parâmetros de banco de dados temporários
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: c137472d03f1088da061c20b52050ae1a1f6629e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171336"
---
# <a name="temporary-database-parameters"></a><span data-ttu-id="d1481-103">Parâmetros de banco de dados temporários</span><span class="sxs-lookup"><span data-stu-id="d1481-103">Temporary Database Parameters</span></span>


<span data-ttu-id="d1481-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d1481-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="temporary-database-parameters"></a><span data-ttu-id="d1481-105">Parâmetros de banco de dados temporários</span><span class="sxs-lookup"><span data-stu-id="d1481-105">Temporary Database Parameters</span></span>

<span data-ttu-id="d1481-106">Este tópico contém parâmetros que são usados para o banco de dados temporário.</span><span class="sxs-lookup"><span data-stu-id="d1481-106">This topic contains parameters that are used for the temporary database.</span></span>

<span data-ttu-id="d1481-107">*JET_paramEnableTempTableVersioning*</span><span class="sxs-lookup"><span data-stu-id="d1481-107">*JET_paramEnableTempTableVersioning*</span></span>  
<span data-ttu-id="d1481-108">46</span><span class="sxs-lookup"><span data-stu-id="d1481-108">46</span></span>  

<span data-ttu-id="d1481-109">Esse parâmetro controla o uso de transações em tabelas temporárias.</span><span class="sxs-lookup"><span data-stu-id="d1481-109">This parameter controls the use of transactions in temporary tables.</span></span> <span data-ttu-id="d1481-110">Quando esse parâmetro for false, as tabelas temporárias serão mais rápidas, mas não será possível reverter as atualizações feitas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="d1481-110">When this parameter is false, temporary tables will be faster but it will not be possible to rollback any updates made in a transaction.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1481-111">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d1481-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d1481-112">True</span><span class="sxs-lookup"><span data-stu-id="d1481-112">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d1481-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="d1481-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="d1481-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d1481-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d1481-116">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="d1481-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-117">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d1481-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d1481-118">Instância</span><span class="sxs-lookup"><span data-stu-id="d1481-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-119">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d1481-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d1481-120">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-121">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d1481-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d1481-122">No</span><span class="sxs-lookup"><span data-stu-id="d1481-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-123">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d1481-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d1481-124">No</span><span class="sxs-lookup"><span data-stu-id="d1481-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-125">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d1481-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d1481-126">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-126">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-127">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d1481-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d1481-128">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-129">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d1481-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d1481-130">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-131">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d1481-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d1481-132">Tudo</span><span class="sxs-lookup"><span data-stu-id="d1481-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1481-133">*JET_paramPageTempDBMin*</span><span class="sxs-lookup"><span data-stu-id="d1481-133">*JET_paramPageTempDBMin*</span></span>  
<span data-ttu-id="d1481-134">19</span><span class="sxs-lookup"><span data-stu-id="d1481-134">19</span></span>  

<span data-ttu-id="d1481-135">Esse parâmetro controla o tamanho inicial do banco de dados temporário.</span><span class="sxs-lookup"><span data-stu-id="d1481-135">This parameter controls the initial size of the temporary database.</span></span> <span data-ttu-id="d1481-136">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d1481-136">The size is in database pages.</span></span> <span data-ttu-id="d1481-137">Um tamanho de zero indica que o tamanho padrão de um banco de dados comum deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="d1481-137">A size of zero indicates that the default size of an ordinary database should be used.</span></span>

<span data-ttu-id="d1481-138">Geralmente, é desejável que aplicativos pequenos configurem o banco de dados temporário para que seja o menor possível.</span><span class="sxs-lookup"><span data-stu-id="d1481-138">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="d1481-139">Definir esse parâmetro como 14 atingirá o menor banco de dados temporário possível.</span><span class="sxs-lookup"><span data-stu-id="d1481-139">Setting this parameter to 14 will achieve the smallest temporary database possible.</span></span> <span data-ttu-id="d1481-140">Observe que também é possível eliminar totalmente o banco de dados temporário definindo **JET_paramMaxTemporaryTables** como zero.</span><span class="sxs-lookup"><span data-stu-id="d1481-140">Note that one can also entirely eliminate the temporary database by setting **JET_paramMaxTemporaryTables** to zero.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1481-141">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d1481-141">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d1481-142">0</span><span class="sxs-lookup"><span data-stu-id="d1481-142">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-143">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d1481-143">Type:</span></span></p></td>
<td><p><span data-ttu-id="d1481-144">Integer</span><span class="sxs-lookup"><span data-stu-id="d1481-144">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-145">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d1481-145">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d1481-146">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="d1481-146">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-147">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d1481-147">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d1481-148">Instância</span><span class="sxs-lookup"><span data-stu-id="d1481-148">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-149">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d1481-149">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d1481-150">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-150">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-151">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d1481-151">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d1481-152">No</span><span class="sxs-lookup"><span data-stu-id="d1481-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-153">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d1481-153">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d1481-154">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-155">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d1481-155">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d1481-156">No</span><span class="sxs-lookup"><span data-stu-id="d1481-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-157">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d1481-157">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d1481-158">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-159">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d1481-159">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d1481-160">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-160">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-161">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d1481-161">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d1481-162">Tudo</span><span class="sxs-lookup"><span data-stu-id="d1481-162">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1481-163">*JET_paramTempPath*</span><span class="sxs-lookup"><span data-stu-id="d1481-163">*JET_paramTempPath*</span></span>  
<span data-ttu-id="d1481-164">1</span><span class="sxs-lookup"><span data-stu-id="d1481-164">1</span></span>  

<span data-ttu-id="d1481-165">Esse parâmetro indica o caminho relativo ou absoluto do sistema de arquivos da pasta ou do arquivo que conterá o banco de dados temporário para a instância.</span><span class="sxs-lookup"><span data-stu-id="d1481-165">This parameter indicates the relative or absolute file system path of the folder or file that will contain the temporary database for the instance.</span></span> <span data-ttu-id="d1481-166">Se o caminho for para uma pasta que conterá o banco de dados temporário, ele deverá ser encerrado com um caractere de barra invertida.</span><span class="sxs-lookup"><span data-stu-id="d1481-166">If the path is to a folder that will contain the temporary database then it must be terminated with a backslash character.</span></span> <span data-ttu-id="d1481-167">O banco de dados temporário é usado para manter dado volátil que é gerado no processo de tratamento de chamadas de informações da API do ESE, criação de índices ou armazenamento do conteúdo de uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d1481-167">The temporary database is used to hold volatile data that is generated in the process of handling ESE API info calls, creating indexes, or storing the contents of a temporary table.</span></span>

<span data-ttu-id="d1481-168">**Observação**  Se um caminho relativo for especificado, ele será relativo ao diretório de trabalho atual do processo que hospeda o aplicativo que está usando o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d1481-168">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1481-169">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d1481-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d1481-170">&quot;tmp. edb&quot;</span><span class="sxs-lookup"><span data-stu-id="d1481-170">&quot;tmp.edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-171">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d1481-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="d1481-172">Caminho (cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="d1481-172">Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-173">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d1481-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d1481-174">0 a 247 caracteres</span><span class="sxs-lookup"><span data-stu-id="d1481-174">0 – 247 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-175">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d1481-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d1481-176">Instância</span><span class="sxs-lookup"><span data-stu-id="d1481-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-177">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d1481-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d1481-178">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-179">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d1481-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d1481-180">No</span><span class="sxs-lookup"><span data-stu-id="d1481-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-181">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d1481-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d1481-182">Yes</span><span class="sxs-lookup"><span data-stu-id="d1481-182">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-183">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d1481-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d1481-184">No</span><span class="sxs-lookup"><span data-stu-id="d1481-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-185">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d1481-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d1481-186">No</span><span class="sxs-lookup"><span data-stu-id="d1481-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-187">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d1481-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d1481-188">No</span><span class="sxs-lookup"><span data-stu-id="d1481-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-189">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d1481-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d1481-190">Tudo</span><span class="sxs-lookup"><span data-stu-id="d1481-190">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="d1481-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1481-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1481-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d1481-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d1481-193">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d1481-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1481-194"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d1481-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d1481-195">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d1481-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1481-196"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d1481-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d1481-197">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d1481-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d1481-198">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d1481-198">See Also</span></span>

[<span data-ttu-id="d1481-199">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="d1481-199">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="d1481-200">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="d1481-200">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="d1481-201">JetInit</span><span class="sxs-lookup"><span data-stu-id="d1481-201">JetInit</span></span>](./jetinit-function.md)

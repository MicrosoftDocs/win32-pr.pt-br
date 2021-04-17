---
description: 'Saiba mais sobre: estrutura de JET_DBINFOMISC4'
title: Estrutura JET_DBINFOMISC4
TOCTitle: JET_DBINFOMISC4 Structure
ms:assetid: 63f446bc-98b7-4a60-9575-d6b4757fb0fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269269(v=EXCHG.10)
ms:contentKeyID: 32765571
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e2242b1e419c4834a2a1843165e1c9a2ad1f2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792578"
---
# <a name="jet_dbinfomisc4-structure"></a><span data-ttu-id="8fa18-103">Estrutura JET_DBINFOMISC4</span><span class="sxs-lookup"><span data-stu-id="8fa18-103">JET_DBINFOMISC4 Structure</span></span>


<span data-ttu-id="8fa18-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8fa18-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc4-structure"></a><span data-ttu-id="8fa18-105">Estrutura JET_DBINFOMISC4</span><span class="sxs-lookup"><span data-stu-id="8fa18-105">JET_DBINFOMISC4 Structure</span></span>

<span data-ttu-id="8fa18-106">A estrutura de **JET_DBINFOMISC4** contém informações diversas sobre um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-106">The **JET_DBINFOMISC4** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="8fa18-107">Essas são as informações contidas no cabeçalho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-107">This is the information that is contained in the database header.</span></span>

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
      JET_BKINFO bkinfoCopyPrev;
      JET_BKINFO bkinfoDiffPrev;
    } JET_DBINFOMISC4;
```

### <a name="members"></a><span data-ttu-id="8fa18-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8fa18-108">Members</span></span>

<span data-ttu-id="8fa18-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="8fa18-109">**ulVersion**</span></span>

<span data-ttu-id="8fa18-110">A versão nativa do mecanismo de banco de dados que criou o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="8fa18-111">Consulte [JetGetVersion](./jetgetversion-function.md) para recuperar a versão nativa para o mecanismo de banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="8fa18-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="8fa18-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="8fa18-112">**ulUpdate**</span></span>

<span data-ttu-id="8fa18-113">Rastreia atualizações de formato de banco de dados incremental que são compatíveis com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="8fa18-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8fa18-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="8fa18-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="8fa18-115">Significado</span><span class="sxs-lookup"><span data-stu-id="8fa18-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="8fa18-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="8fa18-117">Formato beta do sistema operacional original (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="8fa18-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="8fa18-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="8fa18-119">Adicione colunas no catálogo para indexação condicional e antigo (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="8fa18-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="8fa18-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="8fa18-121">Adicione o sinalizador fLocalizedText no IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="8fa18-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="8fa18-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="8fa18-123">Adicione SPLIT_BUFFER às páginas raiz da árvore de espaço (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="8fa18-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="8fa18-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="8fa18-125">Reverta a revisão para que ESE97 permaneça compatível com o encaminhamento (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="8fa18-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="8fa18-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="8fa18-127">Adicione novas colunas marcadas ao catálogo ( &quot; CallbackData &quot; e &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="8fa18-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="8fa18-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="8fa18-129">Suporte a SLV: signSLV, fSLVExists no cabeçalho do BD (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="8fa18-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="8fa18-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="8fa18-131">Nova árvore de espaço do SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="8fa18-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="8fa18-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="8fa18-133">Mapa de espaço do SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="8fa18-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="8fa18-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="8fa18-135">IDXSEG de 4 bytes (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="8fa18-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="8fa18-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="8fa18-137">Novo formato de coluna de modelo (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="8fa18-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="8fa18-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="8fa18-139">Colunas de modelo classificadas (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="8fa18-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-140">0x620, um</span><span class="sxs-lookup"><span data-stu-id="8fa18-140">0x620,A</span></span></p></td>
<td><p><span data-ttu-id="8fa18-141">Base de código mesclado (3/26/2003).</span><span class="sxs-lookup"><span data-stu-id="8fa18-141">Merged code base (3/26/2003).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-142">0x620, B</span><span class="sxs-lookup"><span data-stu-id="8fa18-142">0x620,B</span></span></p></td>
<td><p><span data-ttu-id="8fa18-143">Novo formato de soma de verificação (1/08/2004).</span><span class="sxs-lookup"><span data-stu-id="8fa18-143">New checksum format (1/08/2004).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-144">0x620, C</span><span class="sxs-lookup"><span data-stu-id="8fa18-144">0x620,C</span></span></p></td>
<td><p><span data-ttu-id="8fa18-145">Maior comprimento de chave máximo de 1000/2000 bytes para páginas de 4/8 KB (1/15/2004).</span><span class="sxs-lookup"><span data-stu-id="8fa18-145">Increased max key length to 1000/2000 bytes for 4/8kb pages (1/15/2004).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-146">0x620, D</span><span class="sxs-lookup"><span data-stu-id="8fa18-146">0x620,D</span></span></p></td>
<td><p><span data-ttu-id="8fa18-147">Dicas de espaço de catálogo, space_header. v2 (7/15/2007).</span><span class="sxs-lookup"><span data-stu-id="8fa18-147">Catalog space hints, space_header.v2 (7/15/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-148">0x620, E</span><span class="sxs-lookup"><span data-stu-id="8fa18-148">0x620,E</span></span></p></td>
<td><p><span data-ttu-id="8fa18-149">Adicionar novo formato de nó/extensão ao Gerenciador de espaço, use-o para pools reservados de espaço (8/9/2007).</span><span class="sxs-lookup"><span data-stu-id="8fa18-149">Add new node/extent format to space manager, use it for reserved pools of space (8/9/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-150">0x620, F</span><span class="sxs-lookup"><span data-stu-id="8fa18-150">0x620,F</span></span></p></td>
<td><p><span data-ttu-id="8fa18-151">Compactação para valores longos intrínsecos (10/30/2007).</span><span class="sxs-lookup"><span data-stu-id="8fa18-151">Compression for intrinsic long-values (10/30/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-152">0x620, 10</span><span class="sxs-lookup"><span data-stu-id="8fa18-152">0x620,10</span></span></p></td>
<td><p><span data-ttu-id="8fa18-153">Compactação para valores longos separados (12/05/2007).</span><span class="sxs-lookup"><span data-stu-id="8fa18-153">Compression for separated long-values (12/05/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-154">0x620, 11</span><span class="sxs-lookup"><span data-stu-id="8fa18-154">0x620,11</span></span></p></td>
<td><p><span data-ttu-id="8fa18-155">Novo tamanho de bloco LV para páginas grandes (12/29/2007).</span><span class="sxs-lookup"><span data-stu-id="8fa18-155">New LV chunk size for large pages (12/29/2007).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8fa18-156">**signDb**</span><span class="sxs-lookup"><span data-stu-id="8fa18-156">**signDb**</span></span>

<span data-ttu-id="8fa18-157">Assinatura do banco de dados (incluindo a hora de criação).</span><span class="sxs-lookup"><span data-stu-id="8fa18-157">Signature of the database (including creation time).</span></span> <span data-ttu-id="8fa18-158">Essa estrutura é de 28 bytes.</span><span class="sxs-lookup"><span data-stu-id="8fa18-158">This structure is 28 bytes.</span></span>

<span data-ttu-id="8fa18-159">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="8fa18-159">**dbstate**</span></span>

<span data-ttu-id="8fa18-160">Esse é o estado do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-160">This is the database state.</span></span>

<span data-ttu-id="8fa18-161">As opções a seguir estão disponíveis para este membro.</span><span class="sxs-lookup"><span data-stu-id="8fa18-161">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8fa18-162">Valor</span><span class="sxs-lookup"><span data-stu-id="8fa18-162">Value</span></span></p></th>
<th><p><span data-ttu-id="8fa18-163">Significado</span><span class="sxs-lookup"><span data-stu-id="8fa18-163">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-164">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="8fa18-164">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="8fa18-165">1</span><span class="sxs-lookup"><span data-stu-id="8fa18-165">1</span></span></p></td>
<td><p><span data-ttu-id="8fa18-166">O banco de dados acabou de ser criado.</span><span class="sxs-lookup"><span data-stu-id="8fa18-166">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-167">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="8fa18-167">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="8fa18-168">2</span><span class="sxs-lookup"><span data-stu-id="8fa18-168">2</span></span></p></td>
<td><p><span data-ttu-id="8fa18-169">O banco de dados requer a execução de recuperação rígida ou flexível para tornar-se utilizável ou móvel.</span><span class="sxs-lookup"><span data-stu-id="8fa18-169">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="8fa18-170">Um não deve tentar mover bancos de dados nesse estado.</span><span class="sxs-lookup"><span data-stu-id="8fa18-170">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-171">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="8fa18-171">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="8fa18-172">3</span><span class="sxs-lookup"><span data-stu-id="8fa18-172">3</span></span></p></td>
<td><p><span data-ttu-id="8fa18-173">O banco de dados está em um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="8fa18-173">The database is in a clean state.</span></span> <span data-ttu-id="8fa18-174">O banco de dados pode ser anexado sem nenhum arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="8fa18-174">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-175">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="8fa18-175">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="8fa18-176">4</span><span class="sxs-lookup"><span data-stu-id="8fa18-176">4</span></span></p></td>
<td><p><span data-ttu-id="8fa18-177">O banco de dados está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="8fa18-177">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-178">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="8fa18-178">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="8fa18-179">5</span><span class="sxs-lookup"><span data-stu-id="8fa18-179">5</span></span></p></td>
<td><p><span data-ttu-id="8fa18-180">Interno.</span><span class="sxs-lookup"><span data-stu-id="8fa18-180">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8fa18-181">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="8fa18-181">**lgposConsistent**</span></span>

<span data-ttu-id="8fa18-182">NULL se o banco de dados estiver em um estado sujo.</span><span class="sxs-lookup"><span data-stu-id="8fa18-182">Null if the database is in a dirty state.</span></span> <span data-ttu-id="8fa18-183">Esta é a posição de log que foi usada quando o banco de dados foi trazido pela última vez para um estado de desligamento normal.</span><span class="sxs-lookup"><span data-stu-id="8fa18-183">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="8fa18-184">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="8fa18-184">**logtimeConsistent**</span></span>

<span data-ttu-id="8fa18-185">NULL se o banco de dados estiver em um estado sujo.</span><span class="sxs-lookup"><span data-stu-id="8fa18-185">Null if the database is in a dirty state.</span></span> <span data-ttu-id="8fa18-186">Essa é a hora em que o banco de dados foi trazido pela última vez para um estado de desligamento normal.</span><span class="sxs-lookup"><span data-stu-id="8fa18-186">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="8fa18-187">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="8fa18-187">**logtimeAttach**</span></span>

<span data-ttu-id="8fa18-188">A hora em que o banco de dados foi anexado pela última vez com [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="8fa18-188">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="8fa18-189">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="8fa18-189">**lgposAttach**</span></span>

<span data-ttu-id="8fa18-190">A posição do log que foi usada na última vez em que o banco de dados foi anexado com [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="8fa18-190">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="8fa18-191">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="8fa18-191">**logtimeDetach**</span></span>

<span data-ttu-id="8fa18-192">A hora em que o banco de dados foi desanexado pela última vez com [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="8fa18-192">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="8fa18-193">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="8fa18-193">**lgposDetach**</span></span>

<span data-ttu-id="8fa18-194">A posição do log que foi usada na última vez em que o banco de dados foi desanexado com [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="8fa18-194">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="8fa18-195">**signLog**</span><span class="sxs-lookup"><span data-stu-id="8fa18-195">**signLog**</span></span>

<span data-ttu-id="8fa18-196">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="8fa18-196">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="8fa18-197">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="8fa18-197">**bkinfoFullPrev**</span></span>

<span data-ttu-id="8fa18-198">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="8fa18-198">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="8fa18-199">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="8fa18-199">**bkinfoIncPrev**</span></span>

<span data-ttu-id="8fa18-200">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="8fa18-200">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="8fa18-201">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="8fa18-201">**bkinfoFullCur**</span></span>

<span data-ttu-id="8fa18-202">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="8fa18-202">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="8fa18-203">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="8fa18-203">**fShadowingDisabled**</span></span>

<span data-ttu-id="8fa18-204">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="8fa18-204">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="8fa18-205">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="8fa18-205">**fUpgradeDb**</span></span>

<span data-ttu-id="8fa18-206">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="8fa18-206">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="8fa18-207">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="8fa18-207">**dwMajorVersion**</span></span>

<span data-ttu-id="8fa18-208">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-208">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="8fa18-209">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="8fa18-209">Used for updating indexes.</span></span>

<span data-ttu-id="8fa18-210">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="8fa18-210">**dwMinorVersion**</span></span>

<span data-ttu-id="8fa18-211">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-211">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="8fa18-212">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="8fa18-212">Used for updating indexes.</span></span>

<span data-ttu-id="8fa18-213">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="8fa18-213">**dwBuildNumber**</span></span>

<span data-ttu-id="8fa18-214">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-214">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="8fa18-215">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="8fa18-215">Used for updating indexes.</span></span>

<span data-ttu-id="8fa18-216">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="8fa18-216">**lSPNumber**</span></span>

<span data-ttu-id="8fa18-217">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-217">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="8fa18-218">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="8fa18-218">Used for updating indexes.</span></span>

<span data-ttu-id="8fa18-219">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="8fa18-219">**cbPageSize**</span></span>

<span data-ttu-id="8fa18-220">Tamanho da página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-220">Database page size.</span></span> <span data-ttu-id="8fa18-221">0 significa que o tamanho da página é de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="8fa18-221">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="8fa18-222">Esse valor será recuperado somente se JET_DbInfoMisc foi passado para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="8fa18-222">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

<span data-ttu-id="8fa18-223">**genMinRequired**</span><span class="sxs-lookup"><span data-stu-id="8fa18-223">**genMinRequired**</span></span>

<span data-ttu-id="8fa18-224">Representa a geração de log mínima necessária para repetir os logs.</span><span class="sxs-lookup"><span data-stu-id="8fa18-224">Represents the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="8fa18-225">Normalmente, isso é usado como a geração de ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="8fa18-225">This is typically used as the checkpoint generation.</span></span>

<span data-ttu-id="8fa18-226">**genMaxRequired**</span><span class="sxs-lookup"><span data-stu-id="8fa18-226">**genMaxRequired**</span></span>

<span data-ttu-id="8fa18-227">Representa a geração de log máxima necessária para repetir os logs.</span><span class="sxs-lookup"><span data-stu-id="8fa18-227">Represents the maximum log generation required for replaying the logs.</span></span>

<span data-ttu-id="8fa18-228">**logtimeGenMaxCreate**</span><span class="sxs-lookup"><span data-stu-id="8fa18-228">**logtimeGenMaxCreate**</span></span>

<span data-ttu-id="8fa18-229">Representa a data e a hora de criação do arquivo de log genMax.</span><span class="sxs-lookup"><span data-stu-id="8fa18-229">Represents the creation date and time of the genMax log file.</span></span>

<span data-ttu-id="8fa18-230">**ulRepairCount**</span><span class="sxs-lookup"><span data-stu-id="8fa18-230">**ulRepairCount**</span></span>

<span data-ttu-id="8fa18-231">O número de vezes que um reparo foi chamado neste banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-231">The number of times a repair has been called on this database.</span></span>

<span data-ttu-id="8fa18-232">**logtimeRepair**</span><span class="sxs-lookup"><span data-stu-id="8fa18-232">**logtimeRepair**</span></span>

<span data-ttu-id="8fa18-233">Representa a data e a hora em que o último reparo foi executado.</span><span class="sxs-lookup"><span data-stu-id="8fa18-233">Represents the date and time the last repair was run.</span></span>

<span data-ttu-id="8fa18-234">**ulRepairCountOld**</span><span class="sxs-lookup"><span data-stu-id="8fa18-234">**ulRepairCountOld**</span></span>

<span data-ttu-id="8fa18-235">O número de vezes que o reparo foi executado neste banco de dados antes da última desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="8fa18-235">The number of times the repair had been run on this database before the last defragmentation.</span></span>

<span data-ttu-id="8fa18-236">**ulECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="8fa18-236">**ulECCFixSuccess**</span></span>

<span data-ttu-id="8fa18-237">O número de vezes que um erro de um bit foi corrigido e resultou em uma boa página.</span><span class="sxs-lookup"><span data-stu-id="8fa18-237">The number of times a one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="8fa18-238">**logtimeECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="8fa18-238">**logtimeECCFixSuccess**</span></span>

<span data-ttu-id="8fa18-239">Representa a data e a hora em que o último erro de um bit foi corrigido e resultou em uma boa página.</span><span class="sxs-lookup"><span data-stu-id="8fa18-239">Represents the date and time the last one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="8fa18-240">**ulECCFixSuccessOld**</span><span class="sxs-lookup"><span data-stu-id="8fa18-240">**ulECCFixSuccessOld**</span></span>

<span data-ttu-id="8fa18-241">Representa o número de vezes que um erro de um bit foi corrigido e resultou em uma boa página antes do último reparo.</span><span class="sxs-lookup"><span data-stu-id="8fa18-241">Represents the number of times a one bit error was fixed and resulted in a good page before last repair.</span></span>

<span data-ttu-id="8fa18-242">**ulECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="8fa18-242">**ulECCFixFail**</span></span>

<span data-ttu-id="8fa18-243">O número de vezes que um erro de um bit foi corrigido e resultou em uma página inadequada.</span><span class="sxs-lookup"><span data-stu-id="8fa18-243">The number of times a one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="8fa18-244">**logtimeECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="8fa18-244">**logtimeECCFixFail**</span></span>

<span data-ttu-id="8fa18-245">Representa a data e a hora em que o último erro de um bit foi corrigido e resultou em uma página inadequada.</span><span class="sxs-lookup"><span data-stu-id="8fa18-245">Represents the date and time the last one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="8fa18-246">**ulECCFixFailOld**</span><span class="sxs-lookup"><span data-stu-id="8fa18-246">**ulECCFixFailOld**</span></span>

<span data-ttu-id="8fa18-247">O número de vezes que um erro de um bit foi corrigido e resultou em uma página inapropriada antes do último reparo.</span><span class="sxs-lookup"><span data-stu-id="8fa18-247">The number of times a one bit error was fixed and resulted in a bad page before last repair.</span></span>

<span data-ttu-id="8fa18-248">**ulBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="8fa18-248">**ulBadChecksum**</span></span>

<span data-ttu-id="8fa18-249">O número de vezes que um erro ECC não corrigível/checksum foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="8fa18-249">The number of times a non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="8fa18-250">**logtimeBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="8fa18-250">**logtimeBadChecksum**</span></span>

<span data-ttu-id="8fa18-251">Representa a data e a hora em que o último erro não corrigível de ECC/checksum foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="8fa18-251">Represents the date and time the last non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="8fa18-252">**ulBadChecksumOld**</span><span class="sxs-lookup"><span data-stu-id="8fa18-252">**ulBadChecksumOld**</span></span>

<span data-ttu-id="8fa18-253">O número de vezes que um erro ECC não corrigível/checksum foi encontrado antes do último reparo.</span><span class="sxs-lookup"><span data-stu-id="8fa18-253">The number of times a non-correctable ECC/checksum error was found before last repair.</span></span>

<span data-ttu-id="8fa18-254">**genCommitted**</span><span class="sxs-lookup"><span data-stu-id="8fa18-254">**genCommitted**</span></span>

<span data-ttu-id="8fa18-255">O número máximo de gerações de log confirmadas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8fa18-255">The maximum number of log generations committed to the database.</span></span> <span data-ttu-id="8fa18-256">Normalmente, a geração de log atual.</span><span class="sxs-lookup"><span data-stu-id="8fa18-256">Typically the current log generation.</span></span>

<span data-ttu-id="8fa18-257">**bkinfoCopyPrev**</span><span class="sxs-lookup"><span data-stu-id="8fa18-257">**bkinfoCopyPrev**</span></span>

<span data-ttu-id="8fa18-258">O último backup de cópia com êxito.</span><span class="sxs-lookup"><span data-stu-id="8fa18-258">The last successful Copy backup.</span></span>

<span data-ttu-id="8fa18-259">**bkinfoDiffPrev**</span><span class="sxs-lookup"><span data-stu-id="8fa18-259">**bkinfoDiffPrev**</span></span>

<span data-ttu-id="8fa18-260">O último backup diferencial bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8fa18-260">The last successful Differential backup.</span></span> <span data-ttu-id="8fa18-261">Esse valor é redefinido quando bkinfoFullPrev é definido.</span><span class="sxs-lookup"><span data-stu-id="8fa18-261">This value is reset when bkinfoFullPrev is set.</span></span>

### <a name="requirements"></a><span data-ttu-id="8fa18-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fa18-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-263"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8fa18-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8fa18-264">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8fa18-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fa18-265"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="8fa18-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8fa18-266">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8fa18-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fa18-267"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="8fa18-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8fa18-268">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8fa18-268">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8fa18-269">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8fa18-269">See Also</span></span>

[<span data-ttu-id="8fa18-270">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="8fa18-270">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="8fa18-271">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="8fa18-271">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="8fa18-272">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="8fa18-272">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="8fa18-273">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="8fa18-273">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="8fa18-274">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="8fa18-274">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="8fa18-275">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="8fa18-275">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)

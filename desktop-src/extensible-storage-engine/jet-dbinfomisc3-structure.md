---
description: 'Saiba mais sobre: estrutura de JET_DBINFOMISC3'
title: Estrutura JET_DBINFOMISC3
TOCTitle: JET_DBINFOMISC3 Structure
ms:assetid: ffb23ac1-21ad-4dc6-98f8-aa4e6ef395ac
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294148(v=EXCHG.10)
ms:contentKeyID: 32765762
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
ms.openlocfilehash: 761afe13638d7905b5d4a639b7100108ce6ec977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164455"
---
# <a name="jet_dbinfomisc3-structure"></a><span data-ttu-id="50fb5-103">Estrutura JET_DBINFOMISC3</span><span class="sxs-lookup"><span data-stu-id="50fb5-103">JET_DBINFOMISC3 Structure</span></span>


<span data-ttu-id="50fb5-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="50fb5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc3-structure"></a><span data-ttu-id="50fb5-105">Estrutura JET_DBINFOMISC3</span><span class="sxs-lookup"><span data-stu-id="50fb5-105">JET_DBINFOMISC3 Structure</span></span>

<span data-ttu-id="50fb5-106">A estrutura de **JET_DBINFOMISC3** contém informações diversas sobre um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-106">The **JET_DBINFOMISC3** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="50fb5-107">Essas são as informações contidas no cabeçalho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-107">This is the information that is contained in the database header.</span></span>

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
    } JET_DBINFOMISC3;
```

### <a name="members"></a><span data-ttu-id="50fb5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="50fb5-108">Members</span></span>

<span data-ttu-id="50fb5-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="50fb5-109">**ulVersion**</span></span>

<span data-ttu-id="50fb5-110">A versão nativa do mecanismo de banco de dados que criou o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="50fb5-111">Consulte [JetGetVersion](./jetgetversion-function.md) para recuperar a versão nativa para o mecanismo de banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="50fb5-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="50fb5-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="50fb5-112">**ulUpdate**</span></span>

<span data-ttu-id="50fb5-113">Rastreia atualizações de formato de banco de dados incremental que são compatíveis com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="50fb5-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50fb5-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="50fb5-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="50fb5-115">Significado</span><span class="sxs-lookup"><span data-stu-id="50fb5-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="50fb5-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="50fb5-117">Formato beta do sistema operacional original (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="50fb5-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="50fb5-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="50fb5-119">Adicione colunas no catálogo para indexação condicional e antigo (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="50fb5-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="50fb5-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="50fb5-121">Adicione o sinalizador fLocalizedText no IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="50fb5-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="50fb5-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="50fb5-123">Adicione SPLIT_BUFFER às páginas raiz da árvore de espaço (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="50fb5-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="50fb5-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="50fb5-125">Reverta a revisão para que ESE97 permaneça compatível com o encaminhamento (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="50fb5-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="50fb5-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="50fb5-127">Adicione novas colunas marcadas ao catálogo ( &quot; CallbackData &quot; e &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="50fb5-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="50fb5-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="50fb5-129">Suporte a SLV: signSLV, fSLVExists no cabeçalho do BD (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="50fb5-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="50fb5-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="50fb5-131">Nova árvore de espaço do SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="50fb5-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="50fb5-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="50fb5-133">Mapa de espaço do SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="50fb5-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="50fb5-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="50fb5-135">IDXSEG de 4 bytes (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="50fb5-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="50fb5-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="50fb5-137">Novo formato de coluna de modelo (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="50fb5-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="50fb5-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="50fb5-139">Colunas de modelo classificadas (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="50fb5-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-140">0x620, um</span><span class="sxs-lookup"><span data-stu-id="50fb5-140">0x620,A</span></span></p></td>
<td><p><span data-ttu-id="50fb5-141">Base de código mesclado (3/26/2003).</span><span class="sxs-lookup"><span data-stu-id="50fb5-141">Merged code base (3/26/2003).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-142">0x620, B</span><span class="sxs-lookup"><span data-stu-id="50fb5-142">0x620,B</span></span></p></td>
<td><p><span data-ttu-id="50fb5-143">Novo formato de soma de verificação (1/08/2004).</span><span class="sxs-lookup"><span data-stu-id="50fb5-143">New checksum format (1/08/2004).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-144">0x620, C</span><span class="sxs-lookup"><span data-stu-id="50fb5-144">0x620,C</span></span></p></td>
<td><p><span data-ttu-id="50fb5-145">Maior comprimento de chave máximo de 1000/2000 bytes para páginas de 4/8 KB (1/15/2004).</span><span class="sxs-lookup"><span data-stu-id="50fb5-145">Increased max key length to 1000/2000 bytes for 4/8kb pages (1/15/2004).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-146">0x620, D</span><span class="sxs-lookup"><span data-stu-id="50fb5-146">0x620,D</span></span></p></td>
<td><p><span data-ttu-id="50fb5-147">Dicas de espaço de catálogo, space_header. v2 (7/15/2007).</span><span class="sxs-lookup"><span data-stu-id="50fb5-147">Catalog space hints, space_header.v2 (7/15/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-148">0x620, E</span><span class="sxs-lookup"><span data-stu-id="50fb5-148">0x620,E</span></span></p></td>
<td><p><span data-ttu-id="50fb5-149">Adicionar novo formato de nó/extensão ao Gerenciador de espaço, use-o para pools reservados de espaço (8/9/2007).</span><span class="sxs-lookup"><span data-stu-id="50fb5-149">Add new node/extent format to space manager, use it for reserved pools of space (8/9/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-150">0x620, F</span><span class="sxs-lookup"><span data-stu-id="50fb5-150">0x620,F</span></span></p></td>
<td><p><span data-ttu-id="50fb5-151">Compactação para valores longos intrínsecos (10/30/2007).</span><span class="sxs-lookup"><span data-stu-id="50fb5-151">Compression for intrinsic long-values (10/30/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-152">0x620, 10</span><span class="sxs-lookup"><span data-stu-id="50fb5-152">0x620,10</span></span></p></td>
<td><p><span data-ttu-id="50fb5-153">Compactação para valores longos separados (12/05/2007).</span><span class="sxs-lookup"><span data-stu-id="50fb5-153">Compression for separated long-values (12/05/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-154">0x620, 11</span><span class="sxs-lookup"><span data-stu-id="50fb5-154">0x620,11</span></span></p></td>
<td><p><span data-ttu-id="50fb5-155">Novo tamanho de bloco LV para páginas grandes (12/29/2007).</span><span class="sxs-lookup"><span data-stu-id="50fb5-155">New LV chunk size for large pages (12/29/2007).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50fb5-156">**signDb**</span><span class="sxs-lookup"><span data-stu-id="50fb5-156">**signDb**</span></span>

<span data-ttu-id="50fb5-157">Assinatura do banco de dados (incluindo a hora de criação).</span><span class="sxs-lookup"><span data-stu-id="50fb5-157">Signature of the database (including creation time).</span></span> <span data-ttu-id="50fb5-158">Essa estrutura é de 28 bytes.</span><span class="sxs-lookup"><span data-stu-id="50fb5-158">This structure is 28 bytes.</span></span>

<span data-ttu-id="50fb5-159">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="50fb5-159">**dbstate**</span></span>

<span data-ttu-id="50fb5-160">Esse é o estado do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-160">This is the database state.</span></span>

<span data-ttu-id="50fb5-161">As opções a seguir estão disponíveis para este membro.</span><span class="sxs-lookup"><span data-stu-id="50fb5-161">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50fb5-162">Valor</span><span class="sxs-lookup"><span data-stu-id="50fb5-162">Value</span></span></p></th>
<th><p><span data-ttu-id="50fb5-163">Significado</span><span class="sxs-lookup"><span data-stu-id="50fb5-163">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-164">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="50fb5-164">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="50fb5-165">1</span><span class="sxs-lookup"><span data-stu-id="50fb5-165">1</span></span></p></td>
<td><p><span data-ttu-id="50fb5-166">O banco de dados acabou de ser criado.</span><span class="sxs-lookup"><span data-stu-id="50fb5-166">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-167">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="50fb5-167">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="50fb5-168">2</span><span class="sxs-lookup"><span data-stu-id="50fb5-168">2</span></span></p></td>
<td><p><span data-ttu-id="50fb5-169">O banco de dados requer a execução de recuperação rígida ou flexível para tornar-se utilizável ou móvel.</span><span class="sxs-lookup"><span data-stu-id="50fb5-169">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="50fb5-170">Um não deve tentar mover bancos de dados nesse estado.</span><span class="sxs-lookup"><span data-stu-id="50fb5-170">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-171">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="50fb5-171">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="50fb5-172">3</span><span class="sxs-lookup"><span data-stu-id="50fb5-172">3</span></span></p></td>
<td><p><span data-ttu-id="50fb5-173">O banco de dados está em um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="50fb5-173">The database is in a clean state.</span></span> <span data-ttu-id="50fb5-174">O banco de dados pode ser anexado sem nenhum arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="50fb5-174">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-175">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="50fb5-175">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="50fb5-176">4</span><span class="sxs-lookup"><span data-stu-id="50fb5-176">4</span></span></p></td>
<td><p><span data-ttu-id="50fb5-177">O banco de dados está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="50fb5-177">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-178">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="50fb5-178">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="50fb5-179">5</span><span class="sxs-lookup"><span data-stu-id="50fb5-179">5</span></span></p></td>
<td><p><span data-ttu-id="50fb5-180">Interno.</span><span class="sxs-lookup"><span data-stu-id="50fb5-180">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50fb5-181">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="50fb5-181">**lgposConsistent**</span></span>

<span data-ttu-id="50fb5-182">NULL se o banco de dados estiver em um estado sujo.</span><span class="sxs-lookup"><span data-stu-id="50fb5-182">Null if the database is in a dirty state.</span></span> <span data-ttu-id="50fb5-183">Esta é a posição de log que foi usada quando o banco de dados foi trazido pela última vez para um estado de desligamento normal.</span><span class="sxs-lookup"><span data-stu-id="50fb5-183">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="50fb5-184">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="50fb5-184">**logtimeConsistent**</span></span>

<span data-ttu-id="50fb5-185">NULL se o banco de dados estiver em um estado sujo.</span><span class="sxs-lookup"><span data-stu-id="50fb5-185">Null if the database is in a dirty state.</span></span> <span data-ttu-id="50fb5-186">Essa é a hora em que o banco de dados foi trazido pela última vez para um estado de desligamento normal.</span><span class="sxs-lookup"><span data-stu-id="50fb5-186">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="50fb5-187">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="50fb5-187">**logtimeAttach**</span></span>

<span data-ttu-id="50fb5-188">A hora em que o banco de dados foi anexado pela última vez com [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="50fb5-188">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="50fb5-189">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="50fb5-189">**lgposAttach**</span></span>

<span data-ttu-id="50fb5-190">A posição do log que foi usada na última vez em que o banco de dados foi anexado com [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="50fb5-190">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="50fb5-191">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="50fb5-191">**logtimeDetach**</span></span>

<span data-ttu-id="50fb5-192">A hora em que o banco de dados foi desanexado pela última vez com [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="50fb5-192">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="50fb5-193">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="50fb5-193">**lgposDetach**</span></span>

<span data-ttu-id="50fb5-194">A posição do log que foi usada na última vez em que o banco de dados foi desanexado com [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="50fb5-194">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="50fb5-195">**signLog**</span><span class="sxs-lookup"><span data-stu-id="50fb5-195">**signLog**</span></span>

<span data-ttu-id="50fb5-196">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="50fb5-196">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="50fb5-197">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="50fb5-197">**bkinfoFullPrev**</span></span>

<span data-ttu-id="50fb5-198">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="50fb5-198">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="50fb5-199">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="50fb5-199">**bkinfoIncPrev**</span></span>

<span data-ttu-id="50fb5-200">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="50fb5-200">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="50fb5-201">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="50fb5-201">**bkinfoFullCur**</span></span>

<span data-ttu-id="50fb5-202">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="50fb5-202">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="50fb5-203">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="50fb5-203">**fShadowingDisabled**</span></span>

<span data-ttu-id="50fb5-204">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="50fb5-204">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="50fb5-205">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="50fb5-205">**fUpgradeDb**</span></span>

<span data-ttu-id="50fb5-206">Dá suporte à infraestrutura ESE e não pode ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="50fb5-206">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="50fb5-207">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="50fb5-207">**dwMajorVersion**</span></span>

<span data-ttu-id="50fb5-208">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-208">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="50fb5-209">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="50fb5-209">Used for updating indexes.</span></span>

<span data-ttu-id="50fb5-210">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="50fb5-210">**dwMinorVersion**</span></span>

<span data-ttu-id="50fb5-211">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-211">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="50fb5-212">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="50fb5-212">Used for updating indexes.</span></span>

<span data-ttu-id="50fb5-213">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="50fb5-213">**dwBuildNumber**</span></span>

<span data-ttu-id="50fb5-214">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-214">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="50fb5-215">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="50fb5-215">Used for updating indexes.</span></span>

<span data-ttu-id="50fb5-216">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="50fb5-216">**lSPNumber**</span></span>

<span data-ttu-id="50fb5-217">Representa os números de versão do Windows NT quando os índices dos bancos de dados foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-217">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="50fb5-218">Usado para atualizar índices.</span><span class="sxs-lookup"><span data-stu-id="50fb5-218">Used for updating indexes.</span></span>

<span data-ttu-id="50fb5-219">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="50fb5-219">**cbPageSize**</span></span>

<span data-ttu-id="50fb5-220">Tamanho da página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-220">Database page size.</span></span> <span data-ttu-id="50fb5-221">0 significa que o tamanho da página é de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="50fb5-221">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="50fb5-222">Esse valor será recuperado somente se JET_DbInfoMisc foi passado para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="50fb5-222">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

<span data-ttu-id="50fb5-223">**genMinRequired**</span><span class="sxs-lookup"><span data-stu-id="50fb5-223">**genMinRequired**</span></span>

<span data-ttu-id="50fb5-224">Representa a geração de log mínima necessária para repetir os logs.</span><span class="sxs-lookup"><span data-stu-id="50fb5-224">Represents the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="50fb5-225">Normalmente, isso é o mesmo que a geração de ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="50fb5-225">This is typically the same as the checkpoint generation.</span></span>

<span data-ttu-id="50fb5-226">**genMaxRequired**</span><span class="sxs-lookup"><span data-stu-id="50fb5-226">**genMaxRequired**</span></span>

<span data-ttu-id="50fb5-227">Representa a geração de log máxima necessária para repetir os logs.</span><span class="sxs-lookup"><span data-stu-id="50fb5-227">Represents the maximum log generation required for replaying the logs.</span></span>

<span data-ttu-id="50fb5-228">**logtimeGenMaxCreate**</span><span class="sxs-lookup"><span data-stu-id="50fb5-228">**logtimeGenMaxCreate**</span></span>

<span data-ttu-id="50fb5-229">Representa a data e a hora de criação do arquivo de log genMax.</span><span class="sxs-lookup"><span data-stu-id="50fb5-229">Represents the creation date and time of the genMax log file.</span></span>

<span data-ttu-id="50fb5-230">**ulRepairCount**</span><span class="sxs-lookup"><span data-stu-id="50fb5-230">**ulRepairCount**</span></span>

<span data-ttu-id="50fb5-231">O número de vezes que um reparo foi chamado neste banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50fb5-231">The number of times a repair has been called on this database.</span></span>

<span data-ttu-id="50fb5-232">**logtimeRepair**</span><span class="sxs-lookup"><span data-stu-id="50fb5-232">**logtimeRepair**</span></span>

<span data-ttu-id="50fb5-233">Representa a data e a hora em que o último reparo foi executado.</span><span class="sxs-lookup"><span data-stu-id="50fb5-233">Represents the date and time the last repair was run.</span></span>

<span data-ttu-id="50fb5-234">**ulRepairCountOld**</span><span class="sxs-lookup"><span data-stu-id="50fb5-234">**ulRepairCountOld**</span></span>

<span data-ttu-id="50fb5-235">O número de vezes que o reparo foi executado neste banco de dados antes da última desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="50fb5-235">The number of times the repair had been run on this database before the last defragmentation.</span></span>

<span data-ttu-id="50fb5-236">**ulECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="50fb5-236">**ulECCFixSuccess**</span></span>

<span data-ttu-id="50fb5-237">O número de vezes que um erro de um bit foi corrigido e resultou em uma boa página.</span><span class="sxs-lookup"><span data-stu-id="50fb5-237">The number of times a one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="50fb5-238">**logtimeECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="50fb5-238">**logtimeECCFixSuccess**</span></span>

<span data-ttu-id="50fb5-239">Representa a data e a hora em que o último erro de um bit foi corrigido e resultou em uma boa página.</span><span class="sxs-lookup"><span data-stu-id="50fb5-239">Represents the date and time the last one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="50fb5-240">**ulECCFixSuccessOld**</span><span class="sxs-lookup"><span data-stu-id="50fb5-240">**ulECCFixSuccessOld**</span></span>

<span data-ttu-id="50fb5-241">Representa o número de vezes que um erro de um bit foi corrigido e resultou em uma boa página antes do último reparo.</span><span class="sxs-lookup"><span data-stu-id="50fb5-241">Represents the number of times a one bit error was fixed and resulted in a good page before last repair.</span></span>

<span data-ttu-id="50fb5-242">**ulECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="50fb5-242">**ulECCFixFail**</span></span>

<span data-ttu-id="50fb5-243">O número de vezes que um erro de um bit foi corrigido e resultou em uma página inadequada.</span><span class="sxs-lookup"><span data-stu-id="50fb5-243">The number of times a one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="50fb5-244">**logtimeECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="50fb5-244">**logtimeECCFixFail**</span></span>

<span data-ttu-id="50fb5-245">Representa a data e a hora em que o último erro de um bit foi corrigido e resultou em uma página inadequada.</span><span class="sxs-lookup"><span data-stu-id="50fb5-245">Represents the date and time the last one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="50fb5-246">**ulECCFixFailOld**</span><span class="sxs-lookup"><span data-stu-id="50fb5-246">**ulECCFixFailOld**</span></span>

<span data-ttu-id="50fb5-247">O número de vezes que um erro de um bit foi corrigido e resultou em uma página inapropriada antes do último reparo.</span><span class="sxs-lookup"><span data-stu-id="50fb5-247">The number of times a one bit error was fixed and resulted in a bad page before last repair.</span></span>

<span data-ttu-id="50fb5-248">**ulBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="50fb5-248">**ulBadChecksum**</span></span>

<span data-ttu-id="50fb5-249">O número de vezes que um erro ECC não corrigível/checksum foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="50fb5-249">The number of times a non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="50fb5-250">**logtimeBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="50fb5-250">**logtimeBadChecksum**</span></span>

<span data-ttu-id="50fb5-251">Representa a data e a hora em que o último erro não corrigível de ECC/checksum foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="50fb5-251">Represents the date and time the last non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="50fb5-252">**ulBadChecksumOld**</span><span class="sxs-lookup"><span data-stu-id="50fb5-252">**ulBadChecksumOld**</span></span>

<span data-ttu-id="50fb5-253">O número de vezes que um erro ECC não corrigível/checksum foi encontrado antes do último reparo.</span><span class="sxs-lookup"><span data-stu-id="50fb5-253">The number of times a non-correctable ECC/checksum error was found before last repair.</span></span>

<span data-ttu-id="50fb5-254">**genCommitted**</span><span class="sxs-lookup"><span data-stu-id="50fb5-254">**genCommitted**</span></span>

<span data-ttu-id="50fb5-255">A geração de log atual.</span><span class="sxs-lookup"><span data-stu-id="50fb5-255">The current log generation.</span></span> <span data-ttu-id="50fb5-256">Isso pode ser menor que genMaxRequired se JET_paramWaypointLatency for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="50fb5-256">This can be less than genMaxRequired if JET_paramWaypointLatency is non-zero.</span></span>

### <a name="requirements"></a><span data-ttu-id="50fb5-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50fb5-257">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-258"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="50fb5-258"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="50fb5-259">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="50fb5-259">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50fb5-260"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="50fb5-260"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="50fb5-261">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="50fb5-261">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50fb5-262"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="50fb5-262"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="50fb5-263">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="50fb5-263">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="50fb5-264">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="50fb5-264">See Also</span></span>

[<span data-ttu-id="50fb5-265">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="50fb5-265">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="50fb5-266">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="50fb5-266">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="50fb5-267">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="50fb5-267">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="50fb5-268">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="50fb5-268">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="50fb5-269">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="50fb5-269">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="50fb5-270">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="50fb5-270">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)

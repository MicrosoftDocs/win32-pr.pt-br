---
description: 'Saiba mais sobre: função JetOpenTable'
title: Função JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646701"
---
# <a name="jetopentable-function"></a><span data-ttu-id="e00fe-103">Função JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="e00fe-103">JetOpenTable Function</span></span>


<span data-ttu-id="e00fe-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e00fe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentable-function"></a><span data-ttu-id="e00fe-105">Função JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="e00fe-105">JetOpenTable Function</span></span>

<span data-ttu-id="e00fe-106">A função **JetOpenTable** abre um cursor em uma tabela criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e00fe-106">The **JetOpenTable** function opens a cursor on a previously created table.</span></span>

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="e00fe-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e00fe-107">Parameters</span></span>

<span data-ttu-id="e00fe-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e00fe-108">*sesid*</span></span>

<span data-ttu-id="e00fe-109">O contexto da sessão de banco de dados a ser usado.</span><span class="sxs-lookup"><span data-stu-id="e00fe-109">The database session context to use.</span></span>

<span data-ttu-id="e00fe-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="e00fe-110">*dbid*</span></span>

<span data-ttu-id="e00fe-111">O identificador de banco de dados a ser usado para localizar a tabela.</span><span class="sxs-lookup"><span data-stu-id="e00fe-111">The database identifier to use to find the table.</span></span>

<span data-ttu-id="e00fe-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="e00fe-112">*szTableName*</span></span>

<span data-ttu-id="e00fe-113">O nome da tabela a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="e00fe-113">The name of the table to open.</span></span>

<span data-ttu-id="e00fe-114">*pvParameters*</span><span class="sxs-lookup"><span data-stu-id="e00fe-114">*pvParameters*</span></span>

<span data-ttu-id="e00fe-115">Preterido.</span><span class="sxs-lookup"><span data-stu-id="e00fe-115">Deprecated.</span></span> <span data-ttu-id="e00fe-116">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e00fe-116">Set to **NULL**.</span></span>

<span data-ttu-id="e00fe-117">*cbParameters*</span><span class="sxs-lookup"><span data-stu-id="e00fe-117">*cbParameters*</span></span>

<span data-ttu-id="e00fe-118">Preterido.</span><span class="sxs-lookup"><span data-stu-id="e00fe-118">Deprecated.</span></span> <span data-ttu-id="e00fe-119">Defina como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e00fe-119">Set to 0 (zero).</span></span>

<span data-ttu-id="e00fe-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e00fe-120">*grbit*</span></span>

<span data-ttu-id="e00fe-121">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e00fe-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e00fe-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e00fe-122">Value</span></span></p></th>
<th><p><span data-ttu-id="e00fe-123">Significado</span><span class="sxs-lookup"><span data-stu-id="e00fe-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-124">JET_bitTableDenyRead</span><span class="sxs-lookup"><span data-stu-id="e00fe-124">JET_bitTableDenyRead</span></span></p></td>
<td><p><span data-ttu-id="e00fe-125">A tabela não pode ser aberta para acesso de leitura por outra sessão de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e00fe-125">The table cannot be opened for read-access by another database session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-126">JET_bitTableDenyWrite</span><span class="sxs-lookup"><span data-stu-id="e00fe-126">JET_bitTableDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="e00fe-127">A tabela não pode ser aberta para acesso de gravação por outra sessão de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e00fe-127">The table cannot be opened for write-access by another database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-128">JET_bitTableNoCache</span><span class="sxs-lookup"><span data-stu-id="e00fe-128">JET_bitTableNoCache</span></span></p></td>
<td><p><span data-ttu-id="e00fe-129">Não armazene em cache as páginas desta tabela.</span><span class="sxs-lookup"><span data-stu-id="e00fe-129">Do not cache the pages for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-130">JET_bitTablePermitDDL</span><span class="sxs-lookup"><span data-stu-id="e00fe-130">JET_bitTablePermitDDL</span></span></p></td>
<td><p><span data-ttu-id="e00fe-131">Permite a modificação de DDL em tabelas sinalizadas como FixedDDL.</span><span class="sxs-lookup"><span data-stu-id="e00fe-131">Allows DDL modification on tables flagged as FixedDDL.</span></span> <span data-ttu-id="e00fe-132">Essa opção deve ser usada com a opção JET_bitTableDenyRead.</span><span class="sxs-lookup"><span data-stu-id="e00fe-132">This option must be used with the JET_bitTableDenyRead option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-133">JET_bitTablePreread</span><span class="sxs-lookup"><span data-stu-id="e00fe-133">JET_bitTablePreread</span></span></p></td>
<td><p><span data-ttu-id="e00fe-134">Fornece uma dica de que a tabela provavelmente não está no cache do buffer e que a leitura prévia pode ser benéfica para o desempenho.</span><span class="sxs-lookup"><span data-stu-id="e00fe-134">Provides a hint that the table is probably not in the buffer cache, and that pre-reading may be beneficial to performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-135">JET_bitTableReadOnly</span><span class="sxs-lookup"><span data-stu-id="e00fe-135">JET_bitTableReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e00fe-136">Solicita acesso somente leitura à tabela.</span><span class="sxs-lookup"><span data-stu-id="e00fe-136">Requests read-only access to the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-137">JET_bitTableSequential</span><span class="sxs-lookup"><span data-stu-id="e00fe-137">JET_bitTableSequential</span></span></p></td>
<td><p><span data-ttu-id="e00fe-138">A tabela deve ser probuscada de forma muito agressiva no disco porque o aplicativo irá examiná-lo em sequência.</span><span class="sxs-lookup"><span data-stu-id="e00fe-138">The table should be very aggressively prefetched from disk because the application will be scanning it sequentially.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-139">JET_bitTableUpdatable</span><span class="sxs-lookup"><span data-stu-id="e00fe-139">JET_bitTableUpdatable</span></span></p></td>
<td><p><span data-ttu-id="e00fe-140">Solicita o acesso de gravação à tabela.</span><span class="sxs-lookup"><span data-stu-id="e00fe-140">Requests write-access to the table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e00fe-141">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="e00fe-141">*ptableid*</span></span>

<span data-ttu-id="e00fe-142">Em caso de sucesso, aponta para o identificador da tabela.</span><span class="sxs-lookup"><span data-stu-id="e00fe-142">On success, points to the identifier of the table.</span></span> <span data-ttu-id="e00fe-143">Em caso de falha, o conteúdo de *pTableID* é indefinido.</span><span class="sxs-lookup"><span data-stu-id="e00fe-143">On failure, the contents for *ptableid* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="e00fe-144">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e00fe-144">Return Value</span></span>

<span data-ttu-id="e00fe-145">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="e00fe-145">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e00fe-146">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e00fe-146">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e00fe-147">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e00fe-147">Return code</span></span></p></th>
<th><p><span data-ttu-id="e00fe-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="e00fe-148">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-149">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e00fe-149">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e00fe-150">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e00fe-150">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-151">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="e00fe-151">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="e00fe-152"><em>DBID</em> não é um identificador de banco de dados válido.</span><span class="sxs-lookup"><span data-stu-id="e00fe-152"><em>dbid</em> is not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-153">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="e00fe-153">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="e00fe-154">Uma combinação inadequada de <em>grbit</em> foi passada.</span><span class="sxs-lookup"><span data-stu-id="e00fe-154">A bad combination of <em>grbit</em> was passed in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-155">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="e00fe-155">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="e00fe-156">O nome fornecido em <em>szTableName</em> é inválido.</span><span class="sxs-lookup"><span data-stu-id="e00fe-156">The name given in <em>szTableName</em> is invalid.</span></span></p>
<p><span data-ttu-id="e00fe-157">Para obter mais informações sobre nomes de tabela válidos, consulte o parâmetro <em>szTableName</em> em <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span><span class="sxs-lookup"><span data-stu-id="e00fe-157">For more information about valid table names, see the <em>szTableName</em> parameter in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-158">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="e00fe-158">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="e00fe-159">Foi feita uma tentativa de abrir uma tabela que não existe no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e00fe-159">An attempt was made to open a table that does not exist in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-160">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="e00fe-160">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="e00fe-161">A operação falhou porque o mecanismo não pode alocar os recursos necessários para abrir um novo cursor.</span><span class="sxs-lookup"><span data-stu-id="e00fe-161">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="e00fe-162">Consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="e00fe-162">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-163">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="e00fe-163">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="e00fe-164">A tabela está sendo usada por outra operação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e00fe-164">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-165">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="e00fe-165">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="e00fe-166">Um aviso não fatal que indica que a tabela está sendo usada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="e00fe-166">A nonfatal warning indicating that the table is being used by the system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-167">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="e00fe-167">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="e00fe-168">A tabela está bloqueada por outra operação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e00fe-168">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-169">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="e00fe-169">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="e00fe-170">Foi feita uma tentativa de abrir muitas tabelas exclusivas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e00fe-170">An attempt was made to open too many unique tables at once.</span></span> <span data-ttu-id="e00fe-171">Consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="e00fe-171">See the Remarks section.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e00fe-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="e00fe-172">Remarks</span></span>

<span data-ttu-id="e00fe-173">As tabelas abertas com **JetOpenTable** normalmente devem ser fechadas com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="e00fe-173">Tables opened with **JetOpenTable** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="e00fe-174">A exceção a essa regra ocorre quando **JetOpenTable** é chamado em uma transação e a transação é revertida (com [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="e00fe-174">The exception to this rule happens when **JetOpenTable** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="e00fe-175">Ao reverter uma transação, a tabela é fechada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e00fe-175">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="e00fe-176">Nesse caso, é um erro fechar a tabela com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="e00fe-176">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="e00fe-177">É legal abrir tabelas do sistema com **JetOpenTable** (por exemplo, MSysObjects, MSysUnicodeFixup).</span><span class="sxs-lookup"><span data-stu-id="e00fe-177">It is legal to open system tables with **JetOpenTable** (for example, MSysObjects, MSysUnicodeFixup).</span></span> <span data-ttu-id="e00fe-178">O esquema das tabelas do sistema pode ser alterado, portanto, o acesso a tabelas do sistema não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="e00fe-178">The schema of the system tables may change, so accessing system tables is discouraged.</span></span> <span data-ttu-id="e00fe-179">O número de tabelas exclusivas que podem ser abertas simultaneamente é afetado diretamente pelo *JET_paramMaxOpenTables*.</span><span class="sxs-lookup"><span data-stu-id="e00fe-179">The number of unique tables that can be opened simultaneously is affected directly by *JET_paramMaxOpenTables*.</span></span> <span data-ttu-id="e00fe-180">Se a tabela estiver aberta no momento, um novo cursor será criado na tabela.</span><span class="sxs-lookup"><span data-stu-id="e00fe-180">If the table is currently open then a new cursor will be created on the table.</span></span> <span data-ttu-id="e00fe-181">Os recursos de cursor são configurados usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com *JET_paramMaxCursors*.</span><span class="sxs-lookup"><span data-stu-id="e00fe-181">Cursor resources are configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxCursors*.</span></span> <span data-ttu-id="e00fe-182">Consulte também [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="e00fe-182">Also see [JetDupCursor](./jetdupcursor-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="e00fe-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e00fe-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-184"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e00fe-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e00fe-185">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e00fe-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-186"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e00fe-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e00fe-187">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e00fe-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-188"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e00fe-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e00fe-189">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e00fe-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-190"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="e00fe-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e00fe-191">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e00fe-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e00fe-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e00fe-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e00fe-193">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e00fe-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e00fe-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e00fe-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e00fe-195">Implementado como <strong>JetOpenTableW</strong> (Unicode) e <strong>JetOpenTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e00fe-195">Implemented as <strong>JetOpenTableW</strong> (Unicode) and <strong>JetOpenTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e00fe-196">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e00fe-196">See Also</span></span>

[<span data-ttu-id="e00fe-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e00fe-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e00fe-198">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e00fe-198">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e00fe-199">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e00fe-199">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e00fe-200">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e00fe-200">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e00fe-201">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="e00fe-201">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="e00fe-202">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="e00fe-202">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="e00fe-203">JetRollback</span><span class="sxs-lookup"><span data-stu-id="e00fe-203">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="e00fe-204">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="e00fe-204">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="e00fe-205">Parâmetros do recurso</span><span class="sxs-lookup"><span data-stu-id="e00fe-205">Resource Parameters</span></span>](./resource-parameters.md)

---
description: 'Saiba mais sobre: função JetOpenTemporaryTable'
title: Função JetOpenTemporaryTable
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761004"
---
# <a name="jetopentemporarytable-function"></a><span data-ttu-id="603e1-103">Função JetOpenTemporaryTable</span><span class="sxs-lookup"><span data-stu-id="603e1-103">JetOpenTemporaryTable Function</span></span>


<span data-ttu-id="603e1-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="603e1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemporarytable-function"></a><span data-ttu-id="603e1-105">Função JetOpenTemporaryTable</span><span class="sxs-lookup"><span data-stu-id="603e1-105">JetOpenTemporaryTable Function</span></span>

<span data-ttu-id="603e1-106">A função **JetOpenTemporaryTable** cria uma tabela volátil com um único índice que pode ser usado para armazenar e recuperar registros, assim como uma tabela comum que é criada por meio de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="603e1-106">The **JetOpenTemporaryTable** function creates a volatile table with a single index that can be used to store and retrieve records, just like an ordinary table that is created via [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

<span data-ttu-id="603e1-107">**Windows Vista:** o **JetOpenTemporaryTable** é introduzido no Windows Vista.  </span><span class="sxs-lookup"><span data-stu-id="603e1-107">**Windows Vista:**  **JetOpenTemporaryTable** is introduced in Windows Vista.</span></span>

<span data-ttu-id="603e1-108">As tabelas temporárias são mais rápidas do que as tabelas comuns devido à sua natureza volátil.</span><span class="sxs-lookup"><span data-stu-id="603e1-108">Temporary tables are faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="603e1-109">Eles podem classificar e executar rapidamente a remoção duplicada em conjuntos de registros quando são acessados de forma puramente sequencial.</span><span class="sxs-lookup"><span data-stu-id="603e1-109">They can quickly sort and perform duplicate removal on record sets when they are accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a><span data-ttu-id="603e1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="603e1-110">Parameters</span></span>

<span data-ttu-id="603e1-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="603e1-111">*sesid*</span></span>

<span data-ttu-id="603e1-112">A sessão que será usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="603e1-112">The session that will be used for this call.</span></span>

<span data-ttu-id="603e1-113">*popentemporarytable*</span><span class="sxs-lookup"><span data-stu-id="603e1-113">*popentemporarytable*</span></span>

<span data-ttu-id="603e1-114">Um ponteiro para uma estrutura de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) que contém a descrição da tabela temporária a ser criada na entrada.</span><span class="sxs-lookup"><span data-stu-id="603e1-114">A pointer to a [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) structure that contains the description of the temporary table to create on input.</span></span> <span data-ttu-id="603e1-115">Após uma chamada bem-sucedida, a estrutura contém o identificador para a tabela temporária e as identificações de coluna.</span><span class="sxs-lookup"><span data-stu-id="603e1-115">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span>

### <a name="return-value"></a><span data-ttu-id="603e1-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="603e1-116">Return Value</span></span>

<span data-ttu-id="603e1-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="603e1-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="603e1-118">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="603e1-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="603e1-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="603e1-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="603e1-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="603e1-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="603e1-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="603e1-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="603e1-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="603e1-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-123">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="603e1-123">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="603e1-124">A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</span><span class="sxs-lookup"><span data-stu-id="603e1-124">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="603e1-125"><strong>JetOpenTemporaryTable</strong> pode retornar JET_errOutOfMemory se o espaço de endereço do processo do host se tornar muito fragmentado.</span><span class="sxs-lookup"><span data-stu-id="603e1-125"><strong>JetOpenTemporaryTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="603e1-126">O Gerenciador de tabelas temporárias alocará um bloco de 1 MB de espaço de endereço para cada tabela temporária criada, independentemente da quantidade de dados armazenada.</span><span class="sxs-lookup"><span data-stu-id="603e1-126">The temporary table manager will allocates a 1 MB chunk of address space for every temporary table created regardless of the amount of data is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="603e1-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="603e1-128">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro resultou em um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="603e1-128">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="603e1-129">Esse erro é retornado por <strong>JetOpenTemporaryTable</strong> sob as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="603e1-129">This error is returned by <strong>JetOpenTemporaryTable</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="603e1-130">O membro <strong>cbStruct</strong> da estrutura de <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> não corresponde a uma versão dessa estrutura que é suportada por essa versão do mecanismo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="603e1-130">The <strong>cbStruct</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure does not correspond to a version of this structure that is supported by that version of the database engine</span></span></p></li>
<li><p><span data-ttu-id="603e1-131">O membro <strong>cbKeyMost</strong> da estrutura de <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> é menor que JET_cbKeyMostMin.</span><span class="sxs-lookup"><span data-stu-id="603e1-131">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is less than JET_cbKeyMostMin.</span></span></p></li>
<li><p><span data-ttu-id="603e1-132">O membro <strong>cbKeyMost</strong> da estrutura de <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> é maior do que o maior valor com suporte para o tamanho da página do banco de dados da instância (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="603e1-132">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than the largest supported value for the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="603e1-133">Consulte o parâmetro JET_paramKeyMost na lista de <a href="gg269241(v=exchg.10).md">parâmetros informativos</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="603e1-133">See the JET_paramKeyMost parameter in the list of <a href="gg269241(v=exchg.10).md">Informational Parameters</a> for more information.</span></span></p></li>
<li><p><span data-ttu-id="603e1-134">O membro cbVarSegMac da estrutura de <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> é maior do que o membro <strong>cbKeyMost</strong> .</span><span class="sxs-lookup"><span data-stu-id="603e1-134">The cbVarSegMac member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than The <strong>cbKeyMost</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="603e1-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="603e1-136">A operação não pode ser concluída porque a instância que estava associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="603e1-136">The operation cannot complete because the instance that was associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="603e1-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="603e1-138">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="603e1-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="603e1-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="603e1-140">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="603e1-140">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="603e1-141"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="603e1-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="603e1-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="603e1-143">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="603e1-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="603e1-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="603e1-145">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="603e1-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="603e1-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="603e1-147">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="603e1-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="603e1-148"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="603e1-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-149">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="603e1-149">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="603e1-150">O identificador de sessão é inválido ou se refere a uma sessão fechada.</span><span class="sxs-lookup"><span data-stu-id="603e1-150">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="603e1-151"><strong>Observação</strong>  Esse erro não é retornado em todas as circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="603e1-151"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="603e1-152">Os identificadores são validados apenas com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="603e1-152">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-153">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="603e1-153">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="603e1-154">A operação falhou porque o mecanismo não pode alocar os recursos necessários para abrir um novo cursor.</span><span class="sxs-lookup"><span data-stu-id="603e1-154">The operation failed because the engine cannot allocate the resources that are required to open a new cursor.</span></span> <span data-ttu-id="603e1-155">Os recursos de cursor são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="603e1-155">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-156">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="603e1-156">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="603e1-157">A operação falhou porque o mecanismo não pode alocar os recursos necessários para criar uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="603e1-157">The operation failed because the engine cannot allocate the resources that are required to create a temporary table.</span></span> <span data-ttu-id="603e1-158">Os recursos de tabela temporária são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="603e1-158">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-159">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="603e1-159">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="603e1-160"><strong>JetOpenTemporaryTable</strong> falhou porque JET_bitTTForwardOnly foi especificado e a tabela temporária especificada não pôde ser criada usando a otimização somente de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="603e1-160"><strong>JetOpenTemporaryTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table that was specified could not be created using the forward-only optimization.</span></span></p>
<p><span data-ttu-id="603e1-161"><strong>Windows Server 2003:</strong>  Esse erro só será retornado pelo Windows Server 2003 e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="603e1-161"><strong>Windows Server 2003:</strong>  This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-162">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="603e1-162">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="603e1-163">Foi feita uma tentativa de adicionar muitas colunas à tabela.</span><span class="sxs-lookup"><span data-stu-id="603e1-163">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="603e1-164">Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</span><span class="sxs-lookup"><span data-stu-id="603e1-164">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-165">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="603e1-165">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="603e1-166">A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache o esquema da tabela.</span><span class="sxs-lookup"><span data-stu-id="603e1-166">The operation failed because the engine cannot allocate the resources that are required to cache the schema of the table.</span></span> <span data-ttu-id="603e1-167">Para configurar o número de tabelas que têm esquemas que podem ser armazenados em cache, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="603e1-167">To configure the number of tables that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-168">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="603e1-168">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="603e1-169">O membro <strong>CP</strong> da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como uma página de código válida.</span><span class="sxs-lookup"><span data-stu-id="603e1-169">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="603e1-170">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="603e1-170">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="603e1-171">Um valor de 0 significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="603e1-171">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-172">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="603e1-172">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="603e1-173">O membro <strong>coltyp</strong> da <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como um tipo de coluna válido.</span><span class="sxs-lookup"><span data-stu-id="603e1-173">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-174">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="603e1-174">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="603e1-175">Não foi possível criar o índice porque foi feita uma tentativa de usar uma identificação de localidade inválida.</span><span class="sxs-lookup"><span data-stu-id="603e1-175">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="603e1-176">A ID de localidade pode ser completamente inválida ou o pacote de idiomas associado pode não estar instalado.</span><span class="sxs-lookup"><span data-stu-id="603e1-176">The locale ID might be either completely invalid or the associated language pack might not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-177">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="603e1-177">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="603e1-178">Não foi possível criar o índice porque foi feita uma tentativa de usar um conjunto inválido de sinalizadores de normalização.</span><span class="sxs-lookup"><span data-stu-id="603e1-178">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span></p>
<p><span data-ttu-id="603e1-179"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="603e1-179"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p>
<p><span data-ttu-id="603e1-180"><strong>Windows 2000:</strong>  No Windows 2000, sinalizadores de normalização inválidos resultarão em JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="603e1-180"><strong>Windows 2000:</strong>  On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-181">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="603e1-181">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="603e1-182">Não foi possível criar o índice porque uma definição de índice inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="603e1-182">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="603e1-183"><strong>JetOpenTemporaryTable</strong> retornará esse erro nas seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="603e1-183"><strong>JetOpenTemporaryTable</strong> will return this error under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="603e1-184">A localidade neutra do idioma é especificada.</span><span class="sxs-lookup"><span data-stu-id="603e1-184">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="603e1-185">Um conjunto inválido de sinalizadores de normalização foi especificado.</span><span class="sxs-lookup"><span data-stu-id="603e1-185">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="603e1-186"><strong>Windows 2000:</strong>  Esse erro só será retornado pelo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="603e1-186"><strong>Windows 2000:</strong>  This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-187">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="603e1-187">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="603e1-188">A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache os índices da tabela.</span><span class="sxs-lookup"><span data-stu-id="603e1-188">The operation failed because the engine cannot allocate the resources that are required to cache the indexes of the table.</span></span> <span data-ttu-id="603e1-189">Para configurar o número de índices que têm esquemas que podem ser armazenados em cache, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="603e1-189">To configure the number of indexes that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="603e1-190">Em caso de sucesso, será retornado um cursor aberto na tabela temporária recém-criada.</span><span class="sxs-lookup"><span data-stu-id="603e1-190">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="603e1-191">O estado do banco de dados temporário será preparado para conter a nova tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="603e1-191">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="603e1-192">O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="603e1-192">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="603e1-193">Em caso de falha, a tabela temporária não será criada e um cursor não será retornado.</span><span class="sxs-lookup"><span data-stu-id="603e1-193">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="603e1-194">O estado do banco de dados temporário pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="603e1-194">The state of the temporary database can be changed.</span></span> <span data-ttu-id="603e1-195">O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="603e1-195">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="603e1-196">Comentários</span><span class="sxs-lookup"><span data-stu-id="603e1-196">Remarks</span></span>

<span data-ttu-id="603e1-197">As tabelas temporárias não dão suporte ao complemento completo de opções de definição de coluna que normalmente são compatíveis com o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="603e1-197">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="603e1-198">Na verdade, somente JET_bitColumnFixed e JET_bitColumnTagged têm suporte.</span><span class="sxs-lookup"><span data-stu-id="603e1-198">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="603e1-199">Isso significa que não é possível criar um incremento automático, uma versão ou uma coluna de valores múltiplos em uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="603e1-199">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="603e1-200">Finalmente, não há suporte para colunas de atualização de caução porque elas só podem ser usadas por uma sessão por vez.</span><span class="sxs-lookup"><span data-stu-id="603e1-200">Finally, escrow update columns are not supported because they can only be used by one session at a time.</span></span> <span data-ttu-id="603e1-201">Se qualquer uma dessas opções for solicitada, elas serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="603e1-201">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="603e1-202">As tabelas temporárias não dão suporte a valores padrão.</span><span class="sxs-lookup"><span data-stu-id="603e1-202">Temporary tables do not support default values.</span></span> <span data-ttu-id="603e1-203">Se for fornecida uma definição de coluna que contenha uma especificação de valor padrão, essa especificação será ignorada.</span><span class="sxs-lookup"><span data-stu-id="603e1-203">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="603e1-204">As tabelas temporárias são retornadas ao chamador como resultado de muitas funções diferentes do ESE.</span><span class="sxs-lookup"><span data-stu-id="603e1-204">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="603e1-205">Por exemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md) com a opção JET_IdxInfo definida retornará uma tabela temporária contendo uma lista de todas as colunas de chave em um determinado índice.</span><span class="sxs-lookup"><span data-stu-id="603e1-205">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="603e1-206">As tabelas temporárias seguem as mesmas regras de ciclo de vida que as tabelas temporárias comuns, conforme descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="603e1-206">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="603e1-207">As tabelas temporárias também são usadas internamente pelo mecanismo de banco de dados para muitas tarefas.</span><span class="sxs-lookup"><span data-stu-id="603e1-207">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="603e1-208">A mais importante dessas tarefas é a criação de um índice em uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="603e1-208">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="603e1-209">Uma tabela temporária será usada para classificar as chaves de índice que são usadas para construir esse índice.</span><span class="sxs-lookup"><span data-stu-id="603e1-209">A temporary table will be used to sort the index keys that are used to construct that index.</span></span>

<span data-ttu-id="603e1-210">Todas as tabelas temporárias são armazenadas no banco de dados temporário.</span><span class="sxs-lookup"><span data-stu-id="603e1-210">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="603e1-211">O banco de dados temporário é um arquivo de banco de dados especial que é mantido durante o tempo de vida de uma instância do ESE e é excluído quando essa instância é desligada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="603e1-211">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="603e1-212">O local do banco de dados temporário pode ser configurado usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="603e1-212">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="603e1-213">O posicionamento do banco de dados temporário em disco em relação aos arquivos de log de transações e arquivos de banco de dados poderá ser importante se seu aplicativo fizer uso intensivo de tabelas temporárias ou criar índices com frequência.</span><span class="sxs-lookup"><span data-stu-id="603e1-213">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="603e1-214">O ciclo de vida de uma tabela temporária é vinculado aos cursores que fazem referência a ela.</span><span class="sxs-lookup"><span data-stu-id="603e1-214">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="603e1-215">Se todos os cursores que fazem referência a uma tabela temporária forem fechados, implicitamente ou explicitamente, a tabela temporária será excluída.</span><span class="sxs-lookup"><span data-stu-id="603e1-215">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="603e1-216">Se uma tabela temporária for criada dentro de uma transação e essa transação for revertida posteriormente, a tabela temporária será excluída porque todos os cursores que fazem referência a ela neste momento serão fechados implicitamente.</span><span class="sxs-lookup"><span data-stu-id="603e1-216">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="603e1-217">Novos cursores podem fazer referência a uma tabela temporária somente por meio do uso de [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="603e1-217">New cursors can reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="603e1-218">Nesse caso, os novos cursores serão posicionados na primeira entrada de índice da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="603e1-218">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="603e1-219">[JetDupCursor](./jetdupcursor-function.md) só funcionará durante determinadas fases de uso para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="603e1-219">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="603e1-220">Consulte os comentários sobre os recursos de cursor de tabela temporária para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="603e1-220">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="603e1-221">Não é possível fazer referência a uma tabela temporária de mais de uma sessão por vez.</span><span class="sxs-lookup"><span data-stu-id="603e1-221">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="603e1-222">**Cuidado**  Há um problema importante no [JetDupCursor](./jetdupcursor-function.md) que afeta as tabelas temporárias.</span><span class="sxs-lookup"><span data-stu-id="603e1-222">**Caution**  There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="603e1-223">Se for feita uma tentativa de duplicar uma tabela temporária que está no modo somente de encaminhamento, o cursor resultante não será criado corretamente e não terá funcionamento adequado.</span><span class="sxs-lookup"><span data-stu-id="603e1-223">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="603e1-224">Ainda é seguro duplicar um cursor em uma tabela temporária materializada.</span><span class="sxs-lookup"><span data-stu-id="603e1-224">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="603e1-225">O Gerenciador de tabelas temporárias pode implementar uma tabela temporária de três maneiras.</span><span class="sxs-lookup"><span data-stu-id="603e1-225">The temporary table manager can implement a temporary table in three ways.</span></span> <span data-ttu-id="603e1-226">O primeiro método é manter uma tabela na memória.</span><span class="sxs-lookup"><span data-stu-id="603e1-226">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="603e1-227">Essa estratégia é a mais rápida, mas só pode ser usada para tabelas pequenas, simples e temporárias.</span><span class="sxs-lookup"><span data-stu-id="603e1-227">This strategy is the fastest but can only be used for small, simple, temporary tables.</span></span> <span data-ttu-id="603e1-228">O segundo método é criar uma classificação baseada em disco que possa ser controlada usando um iterador somente de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="603e1-228">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="603e1-229">Essa estratégia só pode ser usada em determinadas circunstâncias e é a maneira mais rápida de classificar e remover duplicatas de um conjunto de dados muito grande.</span><span class="sxs-lookup"><span data-stu-id="603e1-229">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="603e1-230">O terceiro método é criar uma árvore B + no banco de dados temporário para manter a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="603e1-230">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="603e1-231">Essa estratégia é a mais lenta, mas a mais versátil e é conhecida como uma tabela temporária materializada.</span><span class="sxs-lookup"><span data-stu-id="603e1-231">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="603e1-232">Essas estratégias podem ser usadas em combinação para atingir por fim a funcionalidade solicitada pela tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="603e1-232">These strategies can be used in combination to ultimately achieve the functionality that is requested of the temporary table.</span></span>

<span data-ttu-id="603e1-233">Quando a tabela temporária não está materializada, ela é usada principalmente em duas fases principais.</span><span class="sxs-lookup"><span data-stu-id="603e1-233">When the temporary table is not materialized then it is used primarily in two major phases.</span></span> <span data-ttu-id="603e1-234">A primeira fase é a fase de inserção em que a tabela é populada com seu conjunto de dados inicial.</span><span class="sxs-lookup"><span data-stu-id="603e1-234">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="603e1-235">Durante essa fase, apenas a inserção de dados é permitida.</span><span class="sxs-lookup"><span data-stu-id="603e1-235">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="603e1-236">Essa fase termina quando é feita uma tentativa de mover o cursor usando [JetMove](./jetmove-function.md) ou [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="603e1-236">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="603e1-237">A segunda fase é a fase de extração de dados.</span><span class="sxs-lookup"><span data-stu-id="603e1-237">The second phase is the data extraction phase.</span></span> <span data-ttu-id="603e1-238">Durante essa fase, os dados armazenados na tabela temporária podem ser extraídos de acordo com os recursos que foram solicitados quando a tabela temporária foi criada.</span><span class="sxs-lookup"><span data-stu-id="603e1-238">During this phase, the data that is stored in the temporary table can be extracted according to the capabilities that were requested when the temporary table was created.</span></span>

<span data-ttu-id="603e1-239">**Recursos de cursor de tabela temporária**</span><span class="sxs-lookup"><span data-stu-id="603e1-239">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="603e1-240">Quando a tabela temporária é materializada, o cursor tem os seguintes recursos, mas pode ser ainda mais limitado pelas opções que são solicitadas:</span><span class="sxs-lookup"><span data-stu-id="603e1-240">When the temporary table is materialized, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="603e1-241">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="603e1-241">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="603e1-242">JetDelete</span><span class="sxs-lookup"><span data-stu-id="603e1-242">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="603e1-243">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="603e1-243">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="603e1-244">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="603e1-244">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="603e1-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="603e1-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="603e1-246">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="603e1-246">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="603e1-247">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="603e1-247">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="603e1-248">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="603e1-248">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="603e1-249">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="603e1-249">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="603e1-250">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="603e1-250">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="603e1-251">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="603e1-251">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="603e1-252">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="603e1-252">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="603e1-253">JetMove</span><span class="sxs-lookup"><span data-stu-id="603e1-253">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="603e1-254">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="603e1-254">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="603e1-255">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="603e1-255">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="603e1-256">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="603e1-256">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="603e1-257">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="603e1-257">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="603e1-258">JetSeek</span><span class="sxs-lookup"><span data-stu-id="603e1-258">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="603e1-259">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="603e1-259">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="603e1-260">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="603e1-260">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="603e1-261">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="603e1-261">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="603e1-262">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="603e1-262">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="603e1-263">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="603e1-263">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="603e1-264">Quando a tabela temporária não está materializada e está na fase de inserção, o cursor tem os seguintes recursos, mas pode ser ainda mais limitado pelas opções que são solicitadas:</span><span class="sxs-lookup"><span data-stu-id="603e1-264">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="603e1-265">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="603e1-265">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="603e1-266">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="603e1-266">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="603e1-267">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="603e1-267">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="603e1-268">JetMove</span><span class="sxs-lookup"><span data-stu-id="603e1-268">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="603e1-269">**Observação**  Faz a transição para a fase de extração.</span><span class="sxs-lookup"><span data-stu-id="603e1-269">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="603e1-270">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="603e1-270">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="603e1-271">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="603e1-271">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="603e1-272">JetSeek</span><span class="sxs-lookup"><span data-stu-id="603e1-272">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="603e1-273">**Observação**  Faz a transição para a fase de extração.</span><span class="sxs-lookup"><span data-stu-id="603e1-273">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="603e1-274">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="603e1-274">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="603e1-275">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="603e1-275">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="603e1-276">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="603e1-276">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="603e1-277">Quando a tabela temporária não está materializada e está na fase de extração, o cursor tem os seguintes recursos, mas pode ser ainda mais limitado pelas opções que são solicitadas:</span><span class="sxs-lookup"><span data-stu-id="603e1-277">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="603e1-278">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="603e1-278">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="603e1-279">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="603e1-279">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="603e1-280">**Observação**  Se for feita uma tentativa de duplicar uma tabela temporária que está no modo somente de encaminhamento, o cursor resultante não será criado corretamente e não terá funcionamento adequado.</span><span class="sxs-lookup"><span data-stu-id="603e1-280">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="603e1-281">Ainda é seguro duplicar um cursor em uma tabela temporária materializada.</span><span class="sxs-lookup"><span data-stu-id="603e1-281">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="603e1-282">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="603e1-282">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="603e1-283">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="603e1-283">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="603e1-284">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="603e1-284">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="603e1-285">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="603e1-285">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="603e1-286">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="603e1-286">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="603e1-287">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="603e1-287">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="603e1-288">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="603e1-288">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="603e1-289">JetMove</span><span class="sxs-lookup"><span data-stu-id="603e1-289">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="603e1-290">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="603e1-290">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="603e1-291">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="603e1-291">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="603e1-292">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="603e1-292">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="603e1-293">JetSeek</span><span class="sxs-lookup"><span data-stu-id="603e1-293">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="603e1-294">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="603e1-294">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="603e1-295">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="603e1-295">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="603e1-296">Requisitos</span><span class="sxs-lookup"><span data-stu-id="603e1-296">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="603e1-297"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="603e1-297"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="603e1-298">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="603e1-298">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-299"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="603e1-299"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="603e1-300">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="603e1-300">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-301"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="603e1-301"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="603e1-302">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="603e1-302">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="603e1-303"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="603e1-303"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="603e1-304">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="603e1-304">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="603e1-305"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="603e1-305"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="603e1-306">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="603e1-306">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="603e1-307">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="603e1-307">See Also</span></span>

[<span data-ttu-id="603e1-308">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="603e1-308">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="603e1-309">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="603e1-309">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="603e1-310">JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="603e1-310">JET_OPENTEMPORARYTABLE</span></span>](./jet-opentemporarytable-structure.md)  
[<span data-ttu-id="603e1-311">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="603e1-311">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="603e1-312">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="603e1-312">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="603e1-313">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="603e1-313">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="603e1-314">JetMove</span><span class="sxs-lookup"><span data-stu-id="603e1-314">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="603e1-315">JetRollback</span><span class="sxs-lookup"><span data-stu-id="603e1-315">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="603e1-316">JetSeek</span><span class="sxs-lookup"><span data-stu-id="603e1-316">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="603e1-317">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="603e1-317">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="603e1-318">Parâmetros informativos</span><span class="sxs-lookup"><span data-stu-id="603e1-318">Informational Parameters</span></span>](./informational-parameters.md)  
[<span data-ttu-id="603e1-319">Parâmetros de banco de dados temporários</span><span class="sxs-lookup"><span data-stu-id="603e1-319">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)

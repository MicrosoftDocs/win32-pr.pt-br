---
description: 'Saiba mais sobre: função JetSetColumnDefaultValue'
title: Função JetSetColumnDefaultValue
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826928"
---
# <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="e92ba-103">Função JetSetColumnDefaultValue</span><span class="sxs-lookup"><span data-stu-id="e92ba-103">JetSetColumnDefaultValue Function</span></span>


<span data-ttu-id="e92ba-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e92ba-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="e92ba-105">Função JetSetColumnDefaultValue</span><span class="sxs-lookup"><span data-stu-id="e92ba-105">JetSetColumnDefaultValue Function</span></span>

<span data-ttu-id="e92ba-106">A função **JetSetColumnDefaultValue** pode ser usada para alterar o valor padrão de uma coluna existente.</span><span class="sxs-lookup"><span data-stu-id="e92ba-106">The **JetSetColumnDefaultValue** function can be used to change the default value of an existing column.</span></span>

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e92ba-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e92ba-107">Parameters</span></span>

<span data-ttu-id="e92ba-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e92ba-108">*sesid*</span></span>

<span data-ttu-id="e92ba-109">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="e92ba-109">The session to use for this call.</span></span>

<span data-ttu-id="e92ba-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="e92ba-110">*dbid*</span></span>

<span data-ttu-id="e92ba-111">O banco de dados a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="e92ba-111">The database to use for this call.</span></span>

<span data-ttu-id="e92ba-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="e92ba-112">*szTableName*</span></span>

<span data-ttu-id="e92ba-113">O nome da tabela que contém a coluna que será afetada.</span><span class="sxs-lookup"><span data-stu-id="e92ba-113">The name of the table containing the column that will be affected.</span></span>

<span data-ttu-id="e92ba-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="e92ba-114">*szColumnName*</span></span>

<span data-ttu-id="e92ba-115">O nome da coluna cujo valor padrão será alterado.</span><span class="sxs-lookup"><span data-stu-id="e92ba-115">The name of the column whose default value will be changed.</span></span>

<span data-ttu-id="e92ba-116">*pvData*</span><span class="sxs-lookup"><span data-stu-id="e92ba-116">*pvData*</span></span>

<span data-ttu-id="e92ba-117">O buffer de entrada que contém o novo valor padrão.</span><span class="sxs-lookup"><span data-stu-id="e92ba-117">The input buffer containing the new default value.</span></span>

<span data-ttu-id="e92ba-118">*cbData*</span><span class="sxs-lookup"><span data-stu-id="e92ba-118">*cbData*</span></span>

<span data-ttu-id="e92ba-119">O tamanho do buffer de entrada que contém o novo valor padrão.</span><span class="sxs-lookup"><span data-stu-id="e92ba-119">The size of the input buffer containing the new default value.</span></span>

<span data-ttu-id="e92ba-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e92ba-120">*grbit*</span></span>

<span data-ttu-id="e92ba-121">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e92ba-121">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="e92ba-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e92ba-122">Return Value</span></span>

<span data-ttu-id="e92ba-123">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="e92ba-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e92ba-124">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e92ba-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e92ba-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e92ba-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="e92ba-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="e92ba-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e92ba-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e92ba-128">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e92ba-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e92ba-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e92ba-130">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e92ba-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-131">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="e92ba-131">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="e92ba-132">O mesmo que JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="e92ba-132">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-133">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="e92ba-133">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="e92ba-134">Esta coluna especificada está atualmente em uso por um índice.</span><span class="sxs-lookup"><span data-stu-id="e92ba-134">This specified column is currently in use by an index.</span></span></p>
<p><span data-ttu-id="e92ba-135"><strong>JetSetColumnDefaultValue</strong> não pode alterar o valor padrão de uma coluna que é referenciada na definição de um índice.</span><span class="sxs-lookup"><span data-stu-id="e92ba-135"><strong>JetSetColumnDefaultValue</strong> cannot change the default value of a column that is referenced in the definition of an index.</span></span> <span data-ttu-id="e92ba-136">Isso ocorre porque isso pode alterar o conteúdo do índice.</span><span class="sxs-lookup"><span data-stu-id="e92ba-136">This is because doing so could change the contents of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-137">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="e92ba-137">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="e92ba-138">Esta coluna especificada não existe para esta tabela.</span><span class="sxs-lookup"><span data-stu-id="e92ba-138">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e92ba-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e92ba-140">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="e92ba-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e92ba-141">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e92ba-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-142">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="e92ba-142">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="e92ba-143">A ID de banco de dados especificada era inválida.</span><span class="sxs-lookup"><span data-stu-id="e92ba-143">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-144">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="e92ba-144">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="e92ba-145">Um dos nomes de objeto especificados era inválido.</span><span class="sxs-lookup"><span data-stu-id="e92ba-145">One of the specified object names was invalid.</span></span> <span data-ttu-id="e92ba-146">Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="e92ba-146">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="e92ba-147">Essas regras são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="e92ba-147">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="e92ba-148">Os nomes de objeto devem ser compostos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="e92ba-148">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="e92ba-149">Os nomes de objeto devem ter pelo menos um caractere de comprimento.</span><span class="sxs-lookup"><span data-stu-id="e92ba-149">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="e92ba-150">Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="e92ba-150">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="e92ba-151">Os nomes de objeto não podem começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="e92ba-151">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="e92ba-152">Os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="e92ba-152">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="e92ba-153">Os nomes de objeto não podem conter um ponto de exclamação (!), período (.), colchete à esquerda ([) ou caractere de colchete direito (]).</span><span class="sxs-lookup"><span data-stu-id="e92ba-153">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="e92ba-154">Depois de validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usada para o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="e92ba-154">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="e92ba-155">Isso significa que os nomes de objeto também não podem conter um espaço.</span><span class="sxs-lookup"><span data-stu-id="e92ba-155">This means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e92ba-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e92ba-157">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="e92ba-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-158">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="e92ba-158">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="e92ba-159">Não foi possível definir a coluna como nula.</span><span class="sxs-lookup"><span data-stu-id="e92ba-159">The column could not be set to NULL.</span></span> <span data-ttu-id="e92ba-160">Isso acontece para <strong>JetSetColumnDefaultValue</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="e92ba-160">This happens for <strong>JetSetColumnDefaultValue</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="e92ba-161"><em>cbData</em> é zero.</span><span class="sxs-lookup"><span data-stu-id="e92ba-161"><em>cbData</em> is zero.</span></span></p></li>
<li><p><span data-ttu-id="e92ba-162"><strong>pvData</strong> é nulo.</span><span class="sxs-lookup"><span data-stu-id="e92ba-162"><strong>pvData</strong> is NULL.</span></span></p></li>
</ul>
<p><span data-ttu-id="e92ba-163">Portanto, não é possível definir o valor padrão de uma coluna (back) para NULL ou para um valor de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="e92ba-163">Therefore, it is not possible to set the default value of a column (back) to NULL or to a zero length value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-164">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="e92ba-164">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="e92ba-165">Esta tabela especificada não existe para este banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e92ba-165">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e92ba-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e92ba-167">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="e92ba-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-168">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e92ba-168">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e92ba-169">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e92ba-169">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="e92ba-170">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e92ba-170">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-171">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="e92ba-171">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="e92ba-172">Esta tabela especificada está em uso por outra sessão.</span><span class="sxs-lookup"><span data-stu-id="e92ba-172">This specified table is in use by another session.</span></span></p>
<p><span data-ttu-id="e92ba-173"><strong>JetSetColumnDefaultValue</strong> requer acesso exclusivo a uma tabela para alterar o valor padrão da coluna para versões anteriores ao Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e92ba-173"><strong>JetSetColumnDefaultValue</strong> requires exclusive access to a table in order to change the default value of the column for releases prior to Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e92ba-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e92ba-175">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="e92ba-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-176">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="e92ba-176">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e92ba-177">É ilegal tentar uma atualização quando dentro do escopo de uma transação somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e92ba-177">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="e92ba-178">Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="e92ba-178">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="e92ba-179">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e92ba-179">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-180">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e92ba-180">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="e92ba-181">Outra sessão bloqueou anteriormente o registro para atualização.</span><span class="sxs-lookup"><span data-stu-id="e92ba-181">Another session has previously locked the record for update.</span></span> <span data-ttu-id="e92ba-182">A atualização tentada por esta sessão falhará.</span><span class="sxs-lookup"><span data-stu-id="e92ba-182">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e92ba-183">Em caso de sucesso, o valor padrão da coluna especificada na tabela fornecida no banco de dados especificado é permanentemente alterado para o novo valor padrão.</span><span class="sxs-lookup"><span data-stu-id="e92ba-183">On success, the default value of the specified column in the given table in the given database is permanently changed to the new default value.</span></span>

<span data-ttu-id="e92ba-184">Se houver falha, nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="e92ba-184">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e92ba-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="e92ba-185">Remarks</span></span>

<span data-ttu-id="e92ba-186">Não é possível alterar o valor padrão de uma coluna em uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="e92ba-186">It is not possible to change the default value of a column in a template table.</span></span>

<span data-ttu-id="e92ba-187">O mecanismo de banco de dados truncará silenciosamente o valor padrão de uma coluna para 255 bytes para colunas de texto longo e binário longo.</span><span class="sxs-lookup"><span data-stu-id="e92ba-187">The database engine will silently truncate the default value of a column to 255 bytes for long text and long binary columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e92ba-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e92ba-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-189"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e92ba-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e92ba-190">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e92ba-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-191"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e92ba-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e92ba-192">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e92ba-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-193"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e92ba-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e92ba-194">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e92ba-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-195"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="e92ba-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e92ba-196">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e92ba-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e92ba-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e92ba-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e92ba-198">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e92ba-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e92ba-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e92ba-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e92ba-200">Implementado como <strong>JetSetColumnDefaultValueW</strong> (Unicode) e <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e92ba-200">Implemented as <strong>JetSetColumnDefaultValueW</strong> (Unicode) and <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e92ba-201">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e92ba-201">See Also</span></span>

[<span data-ttu-id="e92ba-202">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="e92ba-202">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="e92ba-203">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e92ba-203">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e92ba-204">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e92ba-204">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e92ba-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e92ba-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e92ba-206">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="e92ba-206">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)  
[<span data-ttu-id="e92ba-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e92ba-207">JetStopService</span></span>](./jetstopservice-function.md)

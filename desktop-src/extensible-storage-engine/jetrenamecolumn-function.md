---
description: 'Saiba mais sobre: função JetRenameColumn'
title: Função JetRenameColumn
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784514"
---
# <a name="jetrenamecolumn-function"></a><span data-ttu-id="adb6b-103">Função JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="adb6b-103">JetRenameColumn Function</span></span>


<span data-ttu-id="adb6b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="adb6b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenamecolumn-function"></a><span data-ttu-id="adb6b-105">Função JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="adb6b-105">JetRenameColumn Function</span></span>

<span data-ttu-id="adb6b-106">A função **JetRenameColumn** pode ser usada para alterar o nome de uma coluna existente em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="adb6b-106">The **JetRenameColumn** function can be used to change the name of an existing column on a table.</span></span>

<span data-ttu-id="adb6b-107">**Windows XP:** o **JetRenameColumn** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="adb6b-107">**Windows XP:**  **JetRenameColumn** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="adb6b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adb6b-108">Parameters</span></span>

<span data-ttu-id="adb6b-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="adb6b-109">*sesid*</span></span>

<span data-ttu-id="adb6b-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="adb6b-110">The session to use for this call.</span></span>

<span data-ttu-id="adb6b-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="adb6b-111">*tableid*</span></span>

<span data-ttu-id="adb6b-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="adb6b-112">The cursor to use for this call.</span></span>

<span data-ttu-id="adb6b-113">*szName*</span><span class="sxs-lookup"><span data-stu-id="adb6b-113">*szName*</span></span>

<span data-ttu-id="adb6b-114">O nome atual da coluna que será renomeada.</span><span class="sxs-lookup"><span data-stu-id="adb6b-114">The current name of the column that will be renamed.</span></span>

<span data-ttu-id="adb6b-115">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="adb6b-115">*szNameNew*</span></span>

<span data-ttu-id="adb6b-116">O novo nome da coluna que será renomeada.</span><span class="sxs-lookup"><span data-stu-id="adb6b-116">The new name for the column that will be renamed.</span></span>

<span data-ttu-id="adb6b-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="adb6b-117">*grbit*</span></span>

<span data-ttu-id="adb6b-118">Esse parâmetro deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="adb6b-118">This parameter must be 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="adb6b-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="adb6b-119">Return Value</span></span>

<span data-ttu-id="adb6b-120">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="adb6b-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="adb6b-121">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="adb6b-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adb6b-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="adb6b-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="adb6b-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="adb6b-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adb6b-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="adb6b-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="adb6b-125">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="adb6b-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb6b-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="adb6b-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="adb6b-127">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="adb6b-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb6b-128">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="adb6b-128">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="adb6b-129">Esta coluna especificada não existe para esta tabela.</span><span class="sxs-lookup"><span data-stu-id="adb6b-129">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb6b-130">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="adb6b-130">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="adb6b-131">Um dos nomes de objeto especificados era inválido.</span><span class="sxs-lookup"><span data-stu-id="adb6b-131">One of the specified object names was invalid.</span></span> <span data-ttu-id="adb6b-132">Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="adb6b-132">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="adb6b-133">Essas regras são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="adb6b-133">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="adb6b-134">Os nomes de objeto devem ser compostos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="adb6b-134">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="adb6b-135">Os nomes de objeto devem ter pelo menos um caractere de comprimento.</span><span class="sxs-lookup"><span data-stu-id="adb6b-135">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="adb6b-136">Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="adb6b-136">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="adb6b-137">Os nomes de objeto não podem começar com um espaço-os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="adb6b-137">Object names may not begin with a space - object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="adb6b-138">Os nomes de objeto não podem conter um ponto de exclamação (!), período (.), colchete à esquerda ([) ou caractere de colchete direito (]).</span><span class="sxs-lookup"><span data-stu-id="adb6b-138">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="adb6b-139">Depois de validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usada para o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="adb6b-139">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="adb6b-140">Isso efetivamente significa que os nomes de objeto também não podem conter um espaço.</span><span class="sxs-lookup"><span data-stu-id="adb6b-140">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb6b-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="adb6b-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="adb6b-142">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="adb6b-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="adb6b-143">Isso pode ocorrer para <strong>JetRenameColumn</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="adb6b-143">This can happen for <strong>JetRenameColumn</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="adb6b-144"><em>szName</em> é nulo.</span><span class="sxs-lookup"><span data-stu-id="adb6b-144"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="adb6b-145"><em>szNameNew</em> é nulo.</span><span class="sxs-lookup"><span data-stu-id="adb6b-145"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb6b-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="adb6b-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="adb6b-147">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="adb6b-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="adb6b-148">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="adb6b-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb6b-149">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="adb6b-149">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="adb6b-150">Esta operação só pode ser executada quando a sessão não está dentro de uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="adb6b-150">This operation may only be performed when the session is not currently inside a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb6b-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="adb6b-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="adb6b-152">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="adb6b-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb6b-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="adb6b-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="adb6b-154">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="adb6b-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb6b-155">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="adb6b-155">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="adb6b-156">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="adb6b-156">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="adb6b-157">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="adb6b-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb6b-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="adb6b-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="adb6b-159">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="adb6b-159">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb6b-160">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="adb6b-160">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="adb6b-161">Uma atualização não pode ser feita enquanto estiver dentro do escopo de uma transação somente leitura.</span><span class="sxs-lookup"><span data-stu-id="adb6b-161">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="adb6b-162">Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="adb6b-162">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="adb6b-163">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="adb6b-163">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="adb6b-164">Em caso de sucesso, o nome da coluna especificada na tabela associada ao cursor é permanentemente alterado para o novo nome.</span><span class="sxs-lookup"><span data-stu-id="adb6b-164">On success, the name of the specified column in the table associated with the cursor is permanently changed to the new name.</span></span> <span data-ttu-id="adb6b-165">Todos os índices que fazem referência a essa coluna também serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="adb6b-165">Any indexes that reference that column will also be updated.</span></span>

<span data-ttu-id="adb6b-166">Se houver falha, nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="adb6b-166">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="adb6b-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="adb6b-167">Remarks</span></span>

<span data-ttu-id="adb6b-168">A operação de renomeação de coluna é incomum porque, ao contrário de outras operações de esquema, ela não é executada como uma transação.</span><span class="sxs-lookup"><span data-stu-id="adb6b-168">The column rename operation is unusual because, unlike other schema operations, it is not carried out as a transaction.</span></span> <span data-ttu-id="adb6b-169">Quando uma coluna em uma determinada tabela é renomeada em uma sessão, qualquer outra sessão que usa essa tabela verá a alteração imediatamente, mesmo se elas estiverem em uma transação que impediria que essa sessão verificasse qualquer outra alteração feita pela sessão fazendo a operação de renomeação.</span><span class="sxs-lookup"><span data-stu-id="adb6b-169">When a column in a given table is renamed in one session then any other session using that table will see the change immediately, even if they are in a transaction that would prevent that session from seeing any other change made by the session doing the rename operation.</span></span>

<span data-ttu-id="adb6b-170">A ID de coluna de uma coluna não é afetada pela operação de renomeação.</span><span class="sxs-lookup"><span data-stu-id="adb6b-170">The column ID of a column is not affected by the rename operation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="adb6b-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adb6b-171">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adb6b-172"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="adb6b-172"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="adb6b-173">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="adb6b-173">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb6b-174"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="adb6b-174"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="adb6b-175">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="adb6b-175">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb6b-176"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="adb6b-176"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="adb6b-177">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="adb6b-177">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb6b-178"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="adb6b-178"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="adb6b-179">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="adb6b-179">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb6b-180"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="adb6b-180"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="adb6b-181">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="adb6b-181">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb6b-182"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="adb6b-182"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="adb6b-183">Implementado como <strong>JetRenameColumnW</strong> (Unicode) e <strong>JetRenameColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="adb6b-183">Implemented as <strong>JetRenameColumnW</strong> (Unicode) and <strong>JetRenameColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="adb6b-184">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="adb6b-184">See Also</span></span>

[<span data-ttu-id="adb6b-185">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="adb6b-185">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="adb6b-186">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="adb6b-186">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="adb6b-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="adb6b-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="adb6b-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="adb6b-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="adb6b-189">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="adb6b-189">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)

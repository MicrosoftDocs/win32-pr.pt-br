---
description: 'Saiba mais sobre: função JetRenameTable'
title: Função JetRenameTable
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624b194a1cad836b8927e6e7e4b8490fcad250b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297402"
---
# <a name="jetrenametable-function"></a><span data-ttu-id="ac8d8-103">Função JetRenameTable</span><span class="sxs-lookup"><span data-stu-id="ac8d8-103">JetRenameTable Function</span></span>


<span data-ttu-id="ac8d8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ac8d8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenametable-function"></a><span data-ttu-id="ac8d8-105">Função JetRenameTable</span><span class="sxs-lookup"><span data-stu-id="ac8d8-105">JetRenameTable Function</span></span>

<span data-ttu-id="ac8d8-106">A função **JetRenameTable** pode ser usada para alterar o nome de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-106">The **JetRenameTable** function can be used to change the name of an existing table.</span></span>

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a><span data-ttu-id="ac8d8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac8d8-107">Parameters</span></span>

<span data-ttu-id="ac8d8-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ac8d8-108">*sesid*</span></span>

<span data-ttu-id="ac8d8-109">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-109">The session to use for this call.</span></span>

<span data-ttu-id="ac8d8-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="ac8d8-110">*dbid*</span></span>

<span data-ttu-id="ac8d8-111">O banco de dados a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-111">The database to use for this call.</span></span>

<span data-ttu-id="ac8d8-112">*szName*</span><span class="sxs-lookup"><span data-stu-id="ac8d8-112">*szName*</span></span>

<span data-ttu-id="ac8d8-113">O nome atual da tabela que será renomeada.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-113">The current name of the table that will be renamed.</span></span>

<span data-ttu-id="ac8d8-114">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="ac8d8-114">*szNameNew*</span></span>

<span data-ttu-id="ac8d8-115">O novo nome da tabela que será renomeada.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-115">The new name for the table that will be renamed.</span></span>

### <a name="return-value"></a><span data-ttu-id="ac8d8-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ac8d8-116">Return Value</span></span>

<span data-ttu-id="ac8d8-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ac8d8-118">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ac8d8-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac8d8-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ac8d8-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="ac8d8-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac8d8-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ac8d8-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac8d8-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ac8d8-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-124">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ac8d8-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-126">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ac8d8-127">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac8d8-128">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="ac8d8-128">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-129">O banco de dados especificado era inválido.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-129">The specified database was invalid.</span></span></p>
<p><span data-ttu-id="ac8d8-130">Esse erro só é retornado no Windows 2000 quando uma operação de renomeação de tabela é tentada no banco de dados temporário.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-130">This error is only returned in Windows 2000 when a table rename operation is attempted on the temporary database.</span></span> <span data-ttu-id="ac8d8-131">JET_errInvalidDatabaseId é retornado para esse caso em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-131">JET_errInvalidDatabaseId is returned for this case in later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-132">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="ac8d8-132">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-133">A ID de banco de dados especificada era inválida.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-133">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac8d8-134">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="ac8d8-134">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-135">Um dos nomes de objeto especificados era inválido.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-135">One of the specified object names was invalid.</span></span> <span data-ttu-id="ac8d8-136">Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-136">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="ac8d8-137">Essas regras são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="ac8d8-137">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="ac8d8-138">Os nomes de objeto devem ser compostos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-138">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="ac8d8-139">Os nomes de objeto devem ter pelo menos um caractere de comprimento.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-139">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="ac8d8-140">Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-140">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="ac8d8-141">Os nomes de objeto não podem começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-141">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="ac8d8-142">Os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="ac8d8-142">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="ac8d8-143">Os nomes de objeto não podem conter um ponto de exclamação (!), ponto (.), colchete esquerdo ([) ou colchete direito (]), uma vez validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usado para o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-143">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character - once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="ac8d8-144">Isso efetivamente significa que os nomes de objeto também não podem conter um espaço.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-144">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ac8d8-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-146">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="ac8d8-147">Isso pode ocorrer para <strong>JetRenameTable</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="ac8d8-147">This can happen for <strong>JetRenameTable</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="ac8d8-148"><em>szName</em> é nulo.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-148"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="ac8d8-149"><em>szNameNew</em> é nulo.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-149"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac8d8-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ac8d8-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-151">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-152">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="ac8d8-152">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-153">Esta tabela especificada não existe para este banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-153">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac8d8-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ac8d8-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-155">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-155">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-156">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ac8d8-156">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-157">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-157">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="ac8d8-158">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-158">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac8d8-159">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ac8d8-159">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-160">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-160">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-161">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac8d8-161">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="ac8d8-162">Uma atualização não pode ser feita enquanto estiver dentro do escopo de uma transação somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-162">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="ac8d8-163">Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-163">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="ac8d8-164">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ac8d8-165">Em caso de sucesso, o nome da tabela especificada no banco de dados especificado é permanentemente alterado para o novo nome.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-165">On success, the name of the specified table in the given database is permanently changed to the new name.</span></span>

<span data-ttu-id="ac8d8-166">Se houver falha, nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-166">On failure, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ac8d8-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac8d8-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-168"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ac8d8-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ac8d8-169">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac8d8-170"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ac8d8-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ac8d8-171">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-172"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ac8d8-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ac8d8-173">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac8d8-174"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="ac8d8-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ac8d8-175">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac8d8-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ac8d8-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ac8d8-177">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac8d8-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ac8d8-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ac8d8-179">Implementado como <strong>JetRenameTableW</strong> (Unicode) e <strong>JetRenameTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ac8d8-179">Implemented as <strong>JetRenameTableW</strong> (Unicode) and <strong>JetRenameTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ac8d8-180">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ac8d8-180">See Also</span></span>

[<span data-ttu-id="ac8d8-181">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="ac8d8-181">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="ac8d8-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ac8d8-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ac8d8-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ac8d8-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ac8d8-184">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="ac8d8-184">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)

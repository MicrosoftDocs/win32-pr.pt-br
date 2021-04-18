---
description: 'Saiba mais sobre: função JetDetachDatabase2'
title: Função JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7688df9a18d8e13a85e4a244fc8502a7147e154f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788845"
---
# <a name="jetdetachdatabase2-function"></a><span data-ttu-id="ce18c-103">Função JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="ce18c-103">JetDetachDatabase2 Function</span></span>


<span data-ttu-id="ce18c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ce18c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase2-function"></a><span data-ttu-id="ce18c-105">Função JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="ce18c-105">JetDetachDatabase2 Function</span></span>

<span data-ttu-id="ce18c-106">A função **JetDetachDatabase2** libera um arquivo de banco de dados que foi anexado anteriormente a uma sessão de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ce18c-106">The **JetDetachDatabase2** function releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="ce18c-107">**Windows XP:** o **JetDetachDatabase2** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="ce18c-107">**Windows XP:**  **JetDetachDatabase2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ce18c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce18c-108">Parameters</span></span>

<span data-ttu-id="ce18c-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ce18c-109">*sesid*</span></span>

<span data-ttu-id="ce18c-110">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="ce18c-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="ce18c-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="ce18c-111">*szFilename*</span></span>

<span data-ttu-id="ce18c-112">O nome do banco de dados a ser desanexado.</span><span class="sxs-lookup"><span data-stu-id="ce18c-112">The name of the database to detach.</span></span> <span data-ttu-id="ce18c-113">Se *szFilename* for **nulo** ou uma cadeia de caracteres vazia, todos os bancos de dados anexados a *sesid* serão desanexados.</span><span class="sxs-lookup"><span data-stu-id="ce18c-113">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

<span data-ttu-id="ce18c-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ce18c-114">*grbit*</span></span>

<span data-ttu-id="ce18c-115">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce18c-115">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce18c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ce18c-116">Value</span></span></p></th>
<th><p><span data-ttu-id="ce18c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="ce18c-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce18c-118">JET_bitForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="ce18c-118">JET_bitForceCloseAndDetach</span></span></p></td>
<td><p><span data-ttu-id="ce18c-119">Força o banco de dados a ser fechado e desanexado.</span><span class="sxs-lookup"><span data-stu-id="ce18c-119">Forces the database to be closed and detached.</span></span> <span data-ttu-id="ce18c-120">Se não houver suporte para JET_bitForceCloseAndDetach, JET_errForceDetachNotAllowed será retornado.</span><span class="sxs-lookup"><span data-stu-id="ce18c-120">If JET_bitForceCloseAndDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce18c-121">JET_bitForceDetach</span><span class="sxs-lookup"><span data-stu-id="ce18c-121">JET_bitForceDetach</span></span></p></td>
<td><p><span data-ttu-id="ce18c-122">Força o banco de dados a ser desanexado.</span><span class="sxs-lookup"><span data-stu-id="ce18c-122">Forces the database to be detached.</span></span> <span data-ttu-id="ce18c-123">Se não houver suporte para JET_bitForceDetach, JET_errForceDetachNotAllowed será retornado.</span><span class="sxs-lookup"><span data-stu-id="ce18c-123">If JET_bitForceDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ce18c-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ce18c-124">Return Value</span></span>

<span data-ttu-id="ce18c-125">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce18c-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ce18c-126">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ce18c-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce18c-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ce18c-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="ce18c-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce18c-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce18c-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ce18c-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ce18c-130">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="ce18c-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce18c-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="ce18c-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="ce18c-132">O backup do banco de dados está sendo feito e não pode ser desanexado.</span><span class="sxs-lookup"><span data-stu-id="ce18c-132">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce18c-133">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="ce18c-133">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="ce18c-134">O banco de dados foi aberto pelo <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span><span class="sxs-lookup"><span data-stu-id="ce18c-134">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="ce18c-135">Os bancos de dados devem ser fechados antes da desanexação.</span><span class="sxs-lookup"><span data-stu-id="ce18c-135">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce18c-136">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="ce18c-136">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="ce18c-137">O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="ce18c-137">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce18c-138">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="ce18c-138">JET_errForceDetachNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="ce18c-139">Não há suporte para JET_bitForceDetach.</span><span class="sxs-lookup"><span data-stu-id="ce18c-139">JET_bitForceDetach is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce18c-140">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="ce18c-140">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="ce18c-141">Foi feita uma tentativa de desanexar um banco de dados enquanto estava em uma transação.</span><span class="sxs-lookup"><span data-stu-id="ce18c-141">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ce18c-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce18c-142">Remarks</span></span>

<span data-ttu-id="ce18c-143">Se um banco de dados anexado foi aberto (com [JetAttachDatabase](./jetattachdatabase-function.md)), ele deve ser fechado com [JetCloseDatabase](./jetclosedatabase-function.md) antes de desanexar.</span><span class="sxs-lookup"><span data-stu-id="ce18c-143">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="ce18c-144">Somente Windows 2000: os bancos de dados que não foram desanexados antes de chamar [JetTerm](./jetterm-function.md) serão automaticamente reanexados quando [JetInit](./jetinit-function.md) for próximo chamado.</span><span class="sxs-lookup"><span data-stu-id="ce18c-144">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ce18c-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce18c-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce18c-146"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ce18c-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ce18c-147">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ce18c-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce18c-148"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ce18c-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ce18c-149">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ce18c-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce18c-150"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ce18c-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ce18c-151">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ce18c-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce18c-152"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="ce18c-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ce18c-153">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ce18c-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce18c-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ce18c-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ce18c-155">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ce18c-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce18c-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ce18c-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ce18c-157">Implementado como <strong>JetDetachDatabase2W</strong> (Unicode) e <strong>JetDetachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ce18c-157">Implemented as <strong>JetDetachDatabase2W</strong> (Unicode) and <strong>JetDetachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ce18c-158">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ce18c-158">See Also</span></span>

[<span data-ttu-id="ce18c-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ce18c-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ce18c-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ce18c-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ce18c-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ce18c-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ce18c-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ce18c-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ce18c-163">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="ce18c-163">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="ce18c-164">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="ce18c-164">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="ce18c-165">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="ce18c-165">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="ce18c-166">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="ce18c-166">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="ce18c-167">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="ce18c-167">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="ce18c-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="ce18c-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="ce18c-169">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="ce18c-169">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="ce18c-170">JetTerm</span><span class="sxs-lookup"><span data-stu-id="ce18c-170">JetTerm</span></span>](./jetterm-function.md)

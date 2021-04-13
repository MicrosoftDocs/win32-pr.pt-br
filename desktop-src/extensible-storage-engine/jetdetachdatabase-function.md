---
description: 'Saiba mais sobre: função JetDetachDatabase'
title: Função JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e4437955acc0ed5714f7fbfb9f42fd4abafa58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297634"
---
# <a name="jetdetachdatabase-function"></a><span data-ttu-id="51ba8-103">Função JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="51ba8-103">JetDetachDatabase Function</span></span>


<span data-ttu-id="51ba8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="51ba8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase-function"></a><span data-ttu-id="51ba8-105">Função JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="51ba8-105">JetDetachDatabase Function</span></span>

<span data-ttu-id="51ba8-106">A função **JetDetachDatabase** libera um arquivo de banco de dados que foi anexado anteriormente a uma sessão de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="51ba8-106">The **JetDetachDatabase** function releases a database file that was previously attached to a database session.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a><span data-ttu-id="51ba8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51ba8-107">Parameters</span></span>

<span data-ttu-id="51ba8-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="51ba8-108">*sesid*</span></span>

<span data-ttu-id="51ba8-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="51ba8-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="51ba8-110">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="51ba8-110">*szFilename*</span></span>

<span data-ttu-id="51ba8-111">O nome do banco de dados a ser desanexado.</span><span class="sxs-lookup"><span data-stu-id="51ba8-111">The name of the database to detach.</span></span> <span data-ttu-id="51ba8-112">Se *szFilename* for **nulo** ou uma cadeia de caracteres vazia, todos os bancos de dados anexados a *sesid* serão desanexados.</span><span class="sxs-lookup"><span data-stu-id="51ba8-112">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

### <a name="return-value"></a><span data-ttu-id="51ba8-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="51ba8-113">Return Value</span></span>

<span data-ttu-id="51ba8-114">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="51ba8-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="51ba8-115">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="51ba8-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51ba8-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="51ba8-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="51ba8-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="51ba8-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51ba8-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="51ba8-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="51ba8-119">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="51ba8-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51ba8-120">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="51ba8-120">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="51ba8-121">O backup do banco de dados está sendo feito e não pode ser desanexado.</span><span class="sxs-lookup"><span data-stu-id="51ba8-121">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51ba8-122">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="51ba8-122">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="51ba8-123">O banco de dados foi aberto pelo <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span><span class="sxs-lookup"><span data-stu-id="51ba8-123">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="51ba8-124">Os bancos de dados devem ser fechados antes da desanexação.</span><span class="sxs-lookup"><span data-stu-id="51ba8-124">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51ba8-125">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="51ba8-125">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="51ba8-126">O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="51ba8-126">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51ba8-127">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="51ba8-127">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="51ba8-128">Foi feita uma tentativa de desanexar um banco de dados enquanto estava em uma transação.</span><span class="sxs-lookup"><span data-stu-id="51ba8-128">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="51ba8-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="51ba8-129">Remarks</span></span>

<span data-ttu-id="51ba8-130">Se um banco de dados anexado foi aberto (com [JetAttachDatabase](./jetattachdatabase-function.md)), ele deve ser fechado com [JetCloseDatabase](./jetclosedatabase-function.md) antes de desanexar.</span><span class="sxs-lookup"><span data-stu-id="51ba8-130">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="51ba8-131">Somente Windows 2000: os bancos de dados que não foram desanexados antes de chamar [JetTerm](./jetterm-function.md) serão automaticamente reanexados quando [JetInit](./jetinit-function.md) for próximo chamado.</span><span class="sxs-lookup"><span data-stu-id="51ba8-131">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="51ba8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51ba8-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51ba8-133"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="51ba8-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="51ba8-134">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="51ba8-134">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51ba8-135"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="51ba8-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="51ba8-136">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="51ba8-136">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51ba8-137"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="51ba8-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="51ba8-138">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="51ba8-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51ba8-139"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="51ba8-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="51ba8-140">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="51ba8-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51ba8-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="51ba8-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="51ba8-142">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="51ba8-142">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51ba8-143"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="51ba8-143"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="51ba8-144">Implementado como <strong>JetDetachDatabaseW</strong> (Unicode) e <strong>JetDetachDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="51ba8-144">Implemented as <strong>JetDetachDatabaseW</strong> (Unicode) and <strong>JetDetachDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="51ba8-145">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="51ba8-145">See Also</span></span>

[<span data-ttu-id="51ba8-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="51ba8-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="51ba8-147">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="51ba8-147">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="51ba8-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="51ba8-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="51ba8-149">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="51ba8-149">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="51ba8-150">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="51ba8-150">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="51ba8-151">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="51ba8-151">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="51ba8-152">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="51ba8-152">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="51ba8-153">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="51ba8-153">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="51ba8-154">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="51ba8-154">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="51ba8-155">JetTerm</span><span class="sxs-lookup"><span data-stu-id="51ba8-155">JetTerm</span></span>](./jetterm-function.md)

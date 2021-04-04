---
description: 'Saiba mais sobre: função JetDeleteColumn'
title: Função JetDeleteColumn
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103930769"
---
# <a name="jetdeletecolumn-function"></a><span data-ttu-id="5299f-103">Função JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="5299f-103">JetDeleteColumn Function</span></span>


<span data-ttu-id="5299f-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5299f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn-function"></a><span data-ttu-id="5299f-105">Função JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="5299f-105">JetDeleteColumn Function</span></span>

<span data-ttu-id="5299f-106">A função **JetDeleteColumn** exclui uma coluna de uma tabela de banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="5299f-106">The **JetDeleteColumn** function deletes a column from an ESE database table.</span></span>

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a><span data-ttu-id="5299f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5299f-107">Parameters</span></span>

<span data-ttu-id="5299f-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5299f-108">*sesid*</span></span>

<span data-ttu-id="5299f-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="5299f-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="5299f-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="5299f-110">*tableid*</span></span>

<span data-ttu-id="5299f-111">A tabela da qual excluir a coluna.</span><span class="sxs-lookup"><span data-stu-id="5299f-111">The table from which to delete the column.</span></span>

<span data-ttu-id="5299f-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="5299f-112">*szColumnName*</span></span>

<span data-ttu-id="5299f-113">O nome da coluna a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="5299f-113">The name of the column to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="5299f-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5299f-114">Return Value</span></span>

<span data-ttu-id="5299f-115">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="5299f-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5299f-116">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5299f-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5299f-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5299f-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="5299f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5299f-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5299f-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5299f-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5299f-120">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="5299f-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5299f-121">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="5299f-121">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="5299f-122">A coluna está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="5299f-122">The column is currently in use.</span></span> <span data-ttu-id="5299f-123">Ele pode estar sendo usado por um índice.</span><span class="sxs-lookup"><span data-stu-id="5299f-123">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5299f-124">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="5299f-124">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="5299f-125">Foi feita uma tentativa de modificar o DDL fixo.</span><span class="sxs-lookup"><span data-stu-id="5299f-125">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5299f-126">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="5299f-126">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="5299f-127">A coluna chamada em <em>szColumnName</em> existe na tabela de modelo e o DDL de uma tabela de modelo não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="5299f-127">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5299f-128">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="5299f-128">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="5299f-129">Isso pode ser retornado se um nome inadequado para <em>szColumnName</em> foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="5299f-129">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5299f-130">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="5299f-130">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="5299f-131">A tabela não é gravável.</span><span class="sxs-lookup"><span data-stu-id="5299f-131">The table is not writable.</span></span> <span data-ttu-id="5299f-132">Isso poderá ser retornado se o banco de dados tiver sido aberto no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5299f-132">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5299f-133">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="5299f-133">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="5299f-134">A transação é uma transação somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5299f-134">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="5299f-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="5299f-135">Remarks</span></span>

<span data-ttu-id="5299f-136">Chamar **JetDeleteColumn** é idêntico a chamar [JetDeleteColumn2](./jetdeletecolumn2-function.md) com *grbit* definido como zero (0).</span><span class="sxs-lookup"><span data-stu-id="5299f-136">Calling **JetDeleteColumn** is identical to calling [JetDeleteColumn2](./jetdeletecolumn2-function.md) with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5299f-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5299f-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5299f-138"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5299f-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5299f-139">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5299f-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5299f-140"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="5299f-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5299f-141">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5299f-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5299f-142"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="5299f-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5299f-143">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5299f-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5299f-144"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="5299f-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5299f-145">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5299f-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5299f-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5299f-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5299f-147">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5299f-147">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5299f-148"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5299f-148"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5299f-149">Implementado como <strong>JetDeleteColumnW</strong> (Unicode) e <strong>JetDeleteColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5299f-149">Implemented as <strong>JetDeleteColumnW</strong> (Unicode) and <strong>JetDeleteColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5299f-150">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5299f-150">See Also</span></span>

[<span data-ttu-id="5299f-151">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5299f-151">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5299f-152">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5299f-152">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5299f-153">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5299f-153">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5299f-154">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5299f-154">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5299f-155">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="5299f-155">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)

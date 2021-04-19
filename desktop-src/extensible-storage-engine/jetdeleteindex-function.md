---
description: 'Saiba mais sobre: função JetDeleteIndex'
title: Função JetDeleteIndex
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52a29e619d6643df4984bd7f296dcef4ef0a5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763778"
---
# <a name="jetdeleteindex-function"></a><span data-ttu-id="6ba4e-103">Função JetDeleteIndex</span><span class="sxs-lookup"><span data-stu-id="6ba4e-103">JetDeleteIndex Function</span></span>


<span data-ttu-id="6ba4e-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6ba4e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeleteindex-function"></a><span data-ttu-id="6ba4e-105">Função JetDeleteIndex</span><span class="sxs-lookup"><span data-stu-id="6ba4e-105">JetDeleteIndex Function</span></span>

<span data-ttu-id="6ba4e-106">A função **JetDeleteIndex** exclui um índice de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-106">The **JetDeleteIndex** function deletes an index from a table.</span></span>

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="6ba4e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ba4e-107">Parameters</span></span>

<span data-ttu-id="6ba4e-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6ba4e-108">*sesid*</span></span>

<span data-ttu-id="6ba4e-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="6ba4e-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="6ba4e-110">*tableid*</span></span>

<span data-ttu-id="6ba4e-111">A tabela que contém a coluna a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-111">The table that contains the column that is to be deleted.</span></span>

<span data-ttu-id="6ba4e-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="6ba4e-112">*szIndexName*</span></span>

<span data-ttu-id="6ba4e-113">O nome do índice a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-113">The name of the index to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="6ba4e-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6ba4e-114">Return Value</span></span>

<span data-ttu-id="6ba4e-115">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6ba4e-116">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6ba4e-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ba4e-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6ba4e-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="6ba4e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ba4e-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ba4e-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6ba4e-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6ba4e-120">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba4e-121">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="6ba4e-121">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="6ba4e-122">Foi feita uma tentativa de excluir um índice de uma tabela fixa (por exemplo, um criado com JET_bitTableCreateFixedDDL).</span><span class="sxs-lookup"><span data-stu-id="6ba4e-122">An attempt was made to delete an index from a fixed table (for example, one created with JET_bitTableCreateFixedDDL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ba4e-123">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="6ba4e-123">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="6ba4e-124">Foi feita uma tentativa de excluir um índice de uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-124">An attempt was made to delete an index from a template table.</span></span> <span data-ttu-id="6ba4e-125">Uma tabela de modelo tem um DDL fixo.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-125">A template table has fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba4e-126">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="6ba4e-126">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="6ba4e-127">O índice nomeado em <em>szIndexName</em> não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-127">The index named in <em>szIndexName</em> was not found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ba4e-128">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="6ba4e-128">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="6ba4e-129">Não é possível atualizar a tabela porque ela foi aberta como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-129">The table cannot be updated because it was opened read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba4e-130">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6ba4e-130">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6ba4e-131">Vários threads tentaram usar a mesma sessão de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-131">Multiple threads attempted to use the same database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ba4e-132">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="6ba4e-132">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6ba4e-133">A transação foi aberta como uma transação somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-133">The transaction was opened as a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6ba4e-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ba4e-134">Remarks</span></span>

<span data-ttu-id="6ba4e-135">Quando bem-sucedido, o índice é excluído e, portanto, não pode ser usado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-135">When successful, the index is deleted and therefore cannot be used subsequently.</span></span> <span data-ttu-id="6ba4e-136">Não deve haver nenhuma transação ativa usando o índice.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-136">There must not be any active transaction using the index.</span></span>

<span data-ttu-id="6ba4e-137">Em caso de sucesso, a moeda é definida antes do primeiro registro.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-137">On success, the currency is set before the first record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6ba4e-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ba4e-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ba4e-139"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6ba4e-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba4e-140">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba4e-141"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6ba4e-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba4e-142">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ba4e-143"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6ba4e-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba4e-144">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba4e-145"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="6ba4e-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba4e-146">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ba4e-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6ba4e-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba4e-148">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-148">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba4e-149"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6ba4e-149"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba4e-150">Implementado como <strong>JetDeleteIndexW</strong> (Unicode) e <strong>JetDeleteIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6ba4e-150">Implemented as <strong>JetDeleteIndexW</strong> (Unicode) and <strong>JetDeleteIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6ba4e-151">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6ba4e-151">See Also</span></span>

[<span data-ttu-id="6ba4e-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6ba4e-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6ba4e-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6ba4e-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6ba4e-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6ba4e-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6ba4e-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6ba4e-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="6ba4e-156">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="6ba4e-156">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="6ba4e-157">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="6ba4e-157">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)

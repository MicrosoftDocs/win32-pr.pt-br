---
description: 'Saiba mais sobre: função JetDeleteColumn2'
title: Função JetDeleteColumn2
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793939"
---
# <a name="jetdeletecolumn2-function"></a><span data-ttu-id="e3f59-103">Função JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="e3f59-103">JetDeleteColumn2 Function</span></span>


<span data-ttu-id="e3f59-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e3f59-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn2-function"></a><span data-ttu-id="e3f59-105">Função JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="e3f59-105">JetDeleteColumn2 Function</span></span>

<span data-ttu-id="e3f59-106">A função **JetDeleteColumn2** exclui uma coluna de uma tabela de banco de dados ESE e permite que uma opção *grbit* seja definida.</span><span class="sxs-lookup"><span data-stu-id="e3f59-106">The **JetDeleteColumn2** function deletes a column from an ESE database table and enables a *grbit* option to be set.</span></span>

<span data-ttu-id="e3f59-107">**Windows XP: o JetDeleteColumn2** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e3f59-107">**Windows XP:  JetDeleteColumn2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e3f59-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3f59-108">Parameters</span></span>

<span data-ttu-id="e3f59-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e3f59-109">*sesid*</span></span>

<span data-ttu-id="e3f59-110">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="e3f59-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="e3f59-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="e3f59-111">*tableid*</span></span>

<span data-ttu-id="e3f59-112">A tabela que contém a coluna a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="e3f59-112">The table that contains the column to be deleted.</span></span>

<span data-ttu-id="e3f59-113">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="e3f59-113">*szColumnName*</span></span>

<span data-ttu-id="e3f59-114">O nome da coluna a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="e3f59-114">The name of the column to be deleted.</span></span>

<span data-ttu-id="e3f59-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e3f59-115">*grbit*</span></span>

<span data-ttu-id="e3f59-116">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3f59-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3f59-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e3f59-117">Value</span></span></p></th>
<th><p><span data-ttu-id="e3f59-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e3f59-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3f59-119">JET_bitDeleteColumnIgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="e3f59-119">JET_bitDeleteColumnIgnoreTemplateColumns</span></span></p></td>
<td><p><span data-ttu-id="e3f59-120">A configuração JET_bitDeleteColumIgnoreTemplateColumns fará com que a API Tente apenas excluir colunas na tabela derivada.</span><span class="sxs-lookup"><span data-stu-id="e3f59-120">Setting JET_bitDeleteColumIgnoreTemplateColumns will cause the API to only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="e3f59-121">Se existir uma coluna com esse nome na tabela base, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="e3f59-121">If a column of that name exists in the base table it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e3f59-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e3f59-122">Return Value</span></span>

<span data-ttu-id="e3f59-123">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3f59-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e3f59-124">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e3f59-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3f59-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e3f59-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="e3f59-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3f59-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3f59-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e3f59-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e3f59-128">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e3f59-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f59-129">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="e3f59-129">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="e3f59-130">A coluna está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="e3f59-130">The column is currently in use.</span></span> <span data-ttu-id="e3f59-131">Ele pode estar sendo usado por um índice.</span><span class="sxs-lookup"><span data-stu-id="e3f59-131">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f59-132">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="e3f59-132">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="e3f59-133">Foi feita uma tentativa de modificar o DDL fixo.</span><span class="sxs-lookup"><span data-stu-id="e3f59-133">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f59-134">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="e3f59-134">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="e3f59-135">A coluna chamada em <em>szColumnName</em> existe na tabela de modelo e o DDL de uma tabela de modelo não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="e3f59-135">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f59-136">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="e3f59-136">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="e3f59-137">Isso pode ser retornado se um nome inadequado para <em>szColumnName</em> foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="e3f59-137">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f59-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="e3f59-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="e3f59-139">A tabela não é gravável.</span><span class="sxs-lookup"><span data-stu-id="e3f59-139">The table is not writable.</span></span> <span data-ttu-id="e3f59-140">Isso poderá ser retornado se o banco de dados tiver sido aberto no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e3f59-140">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f59-141">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="e3f59-141">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e3f59-142">A transação é uma transação somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e3f59-142">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e3f59-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3f59-143">Remarks</span></span>

<span data-ttu-id="e3f59-144">Chamar [JetDeleteColumn](./jetdeletecolumn-function.md) é idêntico a chamar **JetDeleteColumn2** com *grbit* definido como zero (0).</span><span class="sxs-lookup"><span data-stu-id="e3f59-144">Calling [JetDeleteColumn](./jetdeletecolumn-function.md) is identical to calling **JetDeleteColumn2** with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="e3f59-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3f59-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3f59-146"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e3f59-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e3f59-147">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e3f59-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f59-148"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e3f59-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e3f59-149">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e3f59-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f59-150"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e3f59-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e3f59-151">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e3f59-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f59-152"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="e3f59-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e3f59-153">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e3f59-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f59-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e3f59-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e3f59-155">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e3f59-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f59-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e3f59-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e3f59-157">Implementado como <strong>JetDeleteColumn2W</strong> (Unicode) e <strong>JetDeleteColumn2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e3f59-157">Implemented as <strong>JetDeleteColumn2W</strong> (Unicode) and <strong>JetDeleteColumn2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e3f59-158">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e3f59-158">See Also</span></span>

[<span data-ttu-id="e3f59-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e3f59-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e3f59-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e3f59-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e3f59-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e3f59-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e3f59-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e3f59-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e3f59-163">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="e3f59-163">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)

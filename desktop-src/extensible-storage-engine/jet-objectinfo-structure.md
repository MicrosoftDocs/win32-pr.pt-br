---
description: 'Saiba mais sobre: estrutura de JET_OBJECTINFO'
title: Estrutura JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011419"
---
# <a name="jet_objectinfo-structure"></a><span data-ttu-id="ce4b9-103">Estrutura JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="ce4b9-103">JET_OBJECTINFO Structure</span></span>


<span data-ttu-id="ce4b9-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ce4b9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectinfo-structure"></a><span data-ttu-id="ce4b9-105">Estrutura JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="ce4b9-105">JET_OBJECTINFO Structure</span></span>

<span data-ttu-id="ce4b9-106">A estrutura de **JET_OBJECTINFO** contém informações sobre um objeto.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-106">The **JET_OBJECTINFO** structure holds information about an object.</span></span> <span data-ttu-id="ce4b9-107">As tabelas são os únicos tipos de objeto com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-107">Tables are the only object types that are currently supported.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a><span data-ttu-id="ce4b9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ce4b9-108">Members</span></span>

<span data-ttu-id="ce4b9-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="ce4b9-109">**cbStruct**</span></span>

<span data-ttu-id="ce4b9-110">O tamanho, em bytes, da estrutura de **JET_OBJECTINFO** .</span><span class="sxs-lookup"><span data-stu-id="ce4b9-110">The size, in bytes, of the **JET_OBJECTINFO** structure.</span></span>

<span data-ttu-id="ce4b9-111">**objtyp**</span><span class="sxs-lookup"><span data-stu-id="ce4b9-111">**objtyp**</span></span>

<span data-ttu-id="ce4b9-112">Mantém a [JET_OBJTYP](./jet-objtyp.md) da estrutura.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-112">Holds the [JET_OBJTYP](./jet-objtyp.md) of the structure.</span></span> <span data-ttu-id="ce4b9-113">No momento, apenas tabelas serão retornadas (ou seja, JET_objtypTable).</span><span class="sxs-lookup"><span data-stu-id="ce4b9-113">Currently only tables will be returned (that is, JET_objtypTable).</span></span>

<span data-ttu-id="ce4b9-114">**dtCreate**</span><span class="sxs-lookup"><span data-stu-id="ce4b9-114">**dtCreate**</span></span>

<span data-ttu-id="ce4b9-115">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-115">Obsolete.</span></span> <span data-ttu-id="ce4b9-116">Não use.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-116">Do not use.</span></span>

<span data-ttu-id="ce4b9-117">**dtUpdate**</span><span class="sxs-lookup"><span data-stu-id="ce4b9-117">**dtUpdate**</span></span>

<span data-ttu-id="ce4b9-118">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-118">Obsolete.</span></span> <span data-ttu-id="ce4b9-119">Não use.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-119">Do not use.</span></span>

<span data-ttu-id="ce4b9-120">**grbit**</span><span class="sxs-lookup"><span data-stu-id="ce4b9-120">**grbit**</span></span>

<span data-ttu-id="ce4b9-121">Um grupo de bits que contém as opções que estão disponíveis para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-121">A group of bits that contain the options that are available for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce4b9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ce4b9-122">Value</span></span></p></th>
<th><p><span data-ttu-id="ce4b9-123">Significado</span><span class="sxs-lookup"><span data-stu-id="ce4b9-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce4b9-124">JET_bitTableInfoBookmark</span><span class="sxs-lookup"><span data-stu-id="ce4b9-124">JET_bitTableInfoBookmark</span></span></p></td>
<td><p><span data-ttu-id="ce4b9-125">A tabela pode ter indicadores.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-125">The table can have bookmarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce4b9-126">JET_bitTableInfoRollback</span><span class="sxs-lookup"><span data-stu-id="ce4b9-126">JET_bitTableInfoRollback</span></span></p></td>
<td><p><span data-ttu-id="ce4b9-127">A tabela pode ser revertida.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-127">The table can be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce4b9-128">JET_bitTableInfoUpdatable</span><span class="sxs-lookup"><span data-stu-id="ce4b9-128">JET_bitTableInfoUpdatable</span></span></p></td>
<td><p><span data-ttu-id="ce4b9-129">A tabela pode ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-129">The table can be updated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ce4b9-130">**sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="ce4b9-130">**flags**</span></span>

<span data-ttu-id="ce4b9-131">Um campo de bits que contém zero ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-131">A bit field that contains zero or more of the following flags.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce4b9-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ce4b9-132">Value</span></span></p></th>
<th><p><span data-ttu-id="ce4b9-133">Significado</span><span class="sxs-lookup"><span data-stu-id="ce4b9-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce4b9-134">JET_bitObjectSystem</span><span class="sxs-lookup"><span data-stu-id="ce4b9-134">JET_bitObjectSystem</span></span></p></td>
<td><p><span data-ttu-id="ce4b9-135">A tabela é uma tabela do sistema e é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-135">The table is a System Table and is for internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce4b9-136">JET_bitObjectTableDerived</span><span class="sxs-lookup"><span data-stu-id="ce4b9-136">JET_bitObjectTableDerived</span></span></p></td>
<td><p><span data-ttu-id="ce4b9-137">A tabela herdada DDL de uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-137">The table inherited DDL from a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce4b9-138">JET_bitObjectTableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="ce4b9-138">JET_bitObjectTableFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="ce4b9-139">Não é possível modificar o DDL da tabela.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-139">The DDL for the table cannot be modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce4b9-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="ce4b9-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="ce4b9-141">Usado em conjunto com JET_bitObjectTableTemplate para não permitir colunas fixas ou variáveis em tabelas derivadas (para que colunas fixas ou variáveis possam ser adicionadas ao modelo no futuro).</span><span class="sxs-lookup"><span data-stu-id="ce4b9-141">Used in conjunction with JET_bitObjectTableTemplate to disallow fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span></p>
<p><span data-ttu-id="ce4b9-142"><strong>Windows XP:  </strong> Esse valor é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-142"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce4b9-143">JET_bitObjectTableTemplate</span><span class="sxs-lookup"><span data-stu-id="ce4b9-143">JET_bitObjectTableTemplate</span></span></p></td>
<td><p><span data-ttu-id="ce4b9-144">A tabela é uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-144">The table is a template table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ce4b9-145">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="ce4b9-145">**cRecord**</span></span>

<span data-ttu-id="ce4b9-146">O número de registros na tabela.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-146">The number of records in the table.</span></span>

<span data-ttu-id="ce4b9-147">Esse valor será recuperado somente se **JET_OBJECTINFO** foi passado para [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="ce4b9-147">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

<span data-ttu-id="ce4b9-148">**cPage**</span><span class="sxs-lookup"><span data-stu-id="ce4b9-148">**cPage**</span></span>

<span data-ttu-id="ce4b9-149">O número de páginas que estão sendo usadas pela tabela.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-149">The number of pages that are being used by the table.</span></span>

<span data-ttu-id="ce4b9-150">Esse valor será recuperado somente se **JET_OBJECTINFO** foi passado para [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="ce4b9-150">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="ce4b9-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce4b9-151">Remarks</span></span>

<span data-ttu-id="ce4b9-152">Uma estrutura de **JET_OBJECTINFO** é preenchida por uma chamada para [JetGetObjectInfo](./jetgetobjectinfo-function.md) ou [JetGetTableInfo](./jetgettableinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="ce4b9-152">A **JET_OBJECTINFO** structure gets populated by a call to [JetGetObjectInfo](./jetgetobjectinfo-function.md) or [JetGetTableInfo](./jetgettableinfo-function.md).</span></span> <span data-ttu-id="ce4b9-153">Se a chamada à API não for concluída com sucesso, o conteúdo da estrutura será indefinido.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-153">If the API call does not succeed, the contents of the structure are undefined.</span></span>

<span data-ttu-id="ce4b9-154">Se aplicável, as estatísticas de tabela incluem o número de registros e o número de páginas que estão no índice clusterizado (ou seja, o índice que contém os dados de registro).</span><span class="sxs-lookup"><span data-stu-id="ce4b9-154">If applicable, the table statistics include the number of records and the number of pages that are in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="ce4b9-155">As estatísticas de índice são acessadas separadamente por nome, usando [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="ce4b9-155">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="ce4b9-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce4b9-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce4b9-157"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ce4b9-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ce4b9-158">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce4b9-159"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ce4b9-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ce4b9-160">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce4b9-161"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ce4b9-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ce4b9-162">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ce4b9-162">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ce4b9-163">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ce4b9-163">See Also</span></span>

[<span data-ttu-id="ce4b9-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ce4b9-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ce4b9-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ce4b9-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ce4b9-166">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="ce4b9-166">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="ce4b9-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ce4b9-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ce4b9-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ce4b9-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ce4b9-169">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="ce4b9-169">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="ce4b9-170">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="ce4b9-170">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="ce4b9-171">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="ce4b9-171">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="ce4b9-172">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="ce4b9-172">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

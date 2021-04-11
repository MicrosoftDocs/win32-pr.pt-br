---
description: 'Saiba mais sobre: estrutura de JET_OBJECTLIST'
title: Estrutura JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297152"
---
# <a name="jet_objectlist-structure"></a><span data-ttu-id="d01bd-103">Estrutura JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="d01bd-103">JET_OBJECTLIST Structure</span></span>


<span data-ttu-id="d01bd-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d01bd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectlist-structure"></a><span data-ttu-id="d01bd-105">Estrutura JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="d01bd-105">JET_OBJECTLIST Structure</span></span>

<span data-ttu-id="d01bd-106">A estrutura de **JET_OBJECTLIST** atravessa uma tabela temporária que foi criada com [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-106">The **JET_OBJECTLIST** structure traverses a temporary table that was created with [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span> <span data-ttu-id="d01bd-107">Cada linha na tabela temporária descreve um objeto no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d01bd-107">Each row in the temporary table describes an object in the database.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a><span data-ttu-id="d01bd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d01bd-108">Members</span></span>

<span data-ttu-id="d01bd-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d01bd-109">**cbStruct**</span></span>

<span data-ttu-id="d01bd-110">O tamanho da estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d01bd-110">The size of the structure, in bytes.</span></span> <span data-ttu-id="d01bd-111">A chamada à API atualizará esse campo, de modo que o chamador deve garantir que esse valor corresponda a sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="d01bd-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="d01bd-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="d01bd-112">**tableid**</span></span>

<span data-ttu-id="d01bd-113">O identificador de tabela da tabela temporária que foi criada.</span><span class="sxs-lookup"><span data-stu-id="d01bd-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="d01bd-114">O chamador deve conter o código que fechará a tabela.</span><span class="sxs-lookup"><span data-stu-id="d01bd-114">The caller must contain code that will close the table.</span></span>

<span data-ttu-id="d01bd-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="d01bd-115">**cRecord**</span></span>

<span data-ttu-id="d01bd-116">O número de registros na tabela temporária que foi criado.</span><span class="sxs-lookup"><span data-stu-id="d01bd-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="d01bd-117">**columnidcontainername**</span><span class="sxs-lookup"><span data-stu-id="d01bd-117">**columnidcontainername**</span></span>

<span data-ttu-id="d01bd-118">O identificador de coluna do nome do tipo de contêiner.</span><span class="sxs-lookup"><span data-stu-id="d01bd-118">The column identifier of the name of the type of container.</span></span>

<span data-ttu-id="d01bd-119">Os únicos contêineres com suporte atualmente são tabelas.</span><span class="sxs-lookup"><span data-stu-id="d01bd-119">The only containers that are currently supported are tables.</span></span> <span data-ttu-id="d01bd-120">Esta coluna é uma [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-120">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="d01bd-121">**columnidobjectname**</span><span class="sxs-lookup"><span data-stu-id="d01bd-121">**columnidobjectname**</span></span>

<span data-ttu-id="d01bd-122">O identificador de coluna do nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="d01bd-122">The column identifier of the name of the object.</span></span>

<span data-ttu-id="d01bd-123">Esta coluna é uma [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-123">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="d01bd-124">**columnidobjtyp**</span><span class="sxs-lookup"><span data-stu-id="d01bd-124">**columnidobjtyp**</span></span>

<span data-ttu-id="d01bd-125">O identificador de coluna do tipo do objeto.</span><span class="sxs-lookup"><span data-stu-id="d01bd-125">The column identifier of the type of the object.</span></span> <span data-ttu-id="d01bd-126">Os únicos contêineres com suporte atualmente são tabelas, portanto, esse campo será JET_objtypTable.</span><span class="sxs-lookup"><span data-stu-id="d01bd-126">The only containers that are currently supported are tables, so this field will be JET_objtypTable.</span></span>

<span data-ttu-id="d01bd-127">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-127">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="d01bd-128">**columniddtCreate**</span><span class="sxs-lookup"><span data-stu-id="d01bd-128">**columniddtCreate**</span></span>

<span data-ttu-id="d01bd-129">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d01bd-129">Obsolete.</span></span> <span data-ttu-id="d01bd-130">Não use.</span><span class="sxs-lookup"><span data-stu-id="d01bd-130">Do not use.</span></span>

<span data-ttu-id="d01bd-131">**columniddtUpdate**</span><span class="sxs-lookup"><span data-stu-id="d01bd-131">**columniddtUpdate**</span></span>

<span data-ttu-id="d01bd-132">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d01bd-132">Obsolete.</span></span> <span data-ttu-id="d01bd-133">Não use.</span><span class="sxs-lookup"><span data-stu-id="d01bd-133">Do not use.</span></span>

<span data-ttu-id="d01bd-134">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="d01bd-134">**columnidgrbit**</span></span>

<span data-ttu-id="d01bd-135">O identificador de coluna do **grbits** que é aplicável ao objeto.</span><span class="sxs-lookup"><span data-stu-id="d01bd-135">The column identifier of the **grbits** that are applicable to the object.</span></span> <span data-ttu-id="d01bd-136">Para obter uma lista de **grbits** aplicáveis, consulte [JET_TABLECREATE](./jet-tablecreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-136">For a list of applicable **grbits**, see [JET_TABLECREATE](./jet-tablecreate-structure.md).</span></span>

<span data-ttu-id="d01bd-137">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-137">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="d01bd-138">**columnidflags**</span><span class="sxs-lookup"><span data-stu-id="d01bd-138">**columnidflags**</span></span>

<span data-ttu-id="d01bd-139">O identificador de coluna dos sinalizadores que são aplicáveis ao objeto.</span><span class="sxs-lookup"><span data-stu-id="d01bd-139">The column identifier of the flags that are applicable to the object.</span></span> <span data-ttu-id="d01bd-140">Para obter uma lista de sinalizadores aplicáveis, consulte [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-140">For a list of applicable flags, see [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span></span>

<span data-ttu-id="d01bd-141">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-141">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="d01bd-142">**columnidcRecord**</span><span class="sxs-lookup"><span data-stu-id="d01bd-142">**columnidcRecord**</span></span>

<span data-ttu-id="d01bd-143">O identificador de coluna do número de registros que estão presentes na tabela nomeada em **columnidobjectname**.</span><span class="sxs-lookup"><span data-stu-id="d01bd-143">The column identifier of the number of records that are present in the table that is named in **columnidobjectname**.</span></span>

<span data-ttu-id="d01bd-144">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-144">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="d01bd-145">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="d01bd-145">**columnidcPage**</span></span>

<span data-ttu-id="d01bd-146">O identificador de coluna do número de páginas usado pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="d01bd-146">The column identifier of the number of pages the object uses.</span></span>

<span data-ttu-id="d01bd-147">Esta coluna é uma [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d01bd-147">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="d01bd-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="d01bd-148">Remarks</span></span>

<span data-ttu-id="d01bd-149">Cada linha na tabela temporária corresponde a um objeto no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d01bd-149">Each row in the temporary table corresponds to an object in the database.</span></span>

<span data-ttu-id="d01bd-150">Quando a tabela temporária é criada com o parâmetro *InfoLevel* na função [JetGetObjectInfo](./jetgetobjectinfo-function.md) definida como JET_ObjInfoListNoStats, as colunas identificadas por **columnidcRecord** e **columnidcPage** não conterá informações significativas.</span><span class="sxs-lookup"><span data-stu-id="d01bd-150">When the temporary table is created with the *InfoLevel* parameter in the [JetGetObjectInfo](./jetgetobjectinfo-function.md) function set to JET_ObjInfoListNoStats, the columns identified by **columnidcRecord** and **columnidcPage** will not contain meaningful information.</span></span>

<span data-ttu-id="d01bd-151">Atualmente, somente as informações sobre tabelas estarão na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="d01bd-151">Currently, only information about tables will be in the temporary table.</span></span>

### <a name="requirements"></a><span data-ttu-id="d01bd-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d01bd-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d01bd-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d01bd-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d01bd-154">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d01bd-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d01bd-155"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d01bd-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d01bd-156">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d01bd-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d01bd-157"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d01bd-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d01bd-158">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d01bd-158">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d01bd-159">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d01bd-159">See Also</span></span>

[<span data-ttu-id="d01bd-160">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="d01bd-160">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="d01bd-161">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d01bd-161">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d01bd-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d01bd-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d01bd-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d01bd-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d01bd-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d01bd-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d01bd-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d01bd-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d01bd-166">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="d01bd-166">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="d01bd-167">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="d01bd-167">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="d01bd-168">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="d01bd-168">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)

---
description: 'Saiba mais sobre: função JetDeleteTable'
title: Função JetDeleteTable
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787760"
---
# <a name="jetdeletetable-function"></a><span data-ttu-id="6fa10-103">Função JetDeleteTable</span><span class="sxs-lookup"><span data-stu-id="6fa10-103">JetDeleteTable Function</span></span>


<span data-ttu-id="6fa10-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6fa10-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletetable-function"></a><span data-ttu-id="6fa10-105">Função JetDeleteTable</span><span class="sxs-lookup"><span data-stu-id="6fa10-105">JetDeleteTable Function</span></span>

<span data-ttu-id="6fa10-106">A função **JetDeleteTable** exclui uma tabela em um banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="6fa10-106">The **JetDeleteTable** function deletes a table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a><span data-ttu-id="6fa10-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fa10-107">Parameters</span></span>

<span data-ttu-id="6fa10-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6fa10-108">*sesid*</span></span>

<span data-ttu-id="6fa10-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="6fa10-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="6fa10-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="6fa10-110">*dbid*</span></span>

<span data-ttu-id="6fa10-111">O identificador de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="6fa10-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="6fa10-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="6fa10-112">*szTableName*</span></span>

<span data-ttu-id="6fa10-113">O nome da tabela a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="6fa10-113">The name of the table to delete.</span></span>

### <a name="return-value"></a><span data-ttu-id="6fa10-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6fa10-114">Return Value</span></span>

<span data-ttu-id="6fa10-115">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="6fa10-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6fa10-116">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6fa10-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fa10-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6fa10-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="6fa10-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fa10-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fa10-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6fa10-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6fa10-120">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6fa10-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fa10-121">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="6fa10-121">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="6fa10-122">Foi feita uma tentativa de excluir uma tabela enquanto outra sessão tem uma ID de tabela aberta (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) com <a href="gg294118(v=exchg.10).md">JetOpenTable</a> ou <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span><span class="sxs-lookup"><span data-stu-id="6fa10-122">An attempt was made to delete a table while another session has an open table ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) with <a href="gg294118(v=exchg.10).md">JetOpenTable</a> or <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fa10-123">Tabela de JET_errCannotDeletetemporary</span><span class="sxs-lookup"><span data-stu-id="6fa10-123">JET_errCannotDeletetemporary table</span></span></p></td>
<td><p><span data-ttu-id="6fa10-124">Foi feita uma tentativa de excluir uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="6fa10-124">An attempt was made to delete a temporary table.</span></span> <span data-ttu-id="6fa10-125">Uma tabela temporária é excluída automaticamente quando fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="6fa10-125">A temporary table is automatically deleted when it is closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fa10-126">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="6fa10-126">JET_errCannotDeleteTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="6fa10-127">Foi feita uma tentativa de excluir uma tabela de modelo, ou seja, uma tabela da qual o DDL pode ser herdado.</span><span class="sxs-lookup"><span data-stu-id="6fa10-127">An attempt was made to delete a template table, that is, a table from which DDL can be inherited.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="6fa10-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fa10-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fa10-129"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6fa10-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6fa10-130">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6fa10-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fa10-131"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6fa10-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6fa10-132">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6fa10-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fa10-133"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6fa10-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6fa10-134">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6fa10-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fa10-135"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="6fa10-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6fa10-136">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6fa10-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fa10-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6fa10-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6fa10-138">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6fa10-138">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fa10-139"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6fa10-139"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6fa10-140">Implementado como <strong>JetDeleteTableW</strong> (Unicode) e <strong>JetDeleteTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6fa10-140">Implemented as <strong>JetDeleteTableW</strong> (Unicode) and <strong>JetDeleteTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6fa10-141">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6fa10-141">See Also</span></span>

[<span data-ttu-id="6fa10-142">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6fa10-142">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="6fa10-143">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6fa10-143">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6fa10-144">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="6fa10-144">JetCloseTable</span></span>](./jetclosetable-function.md)

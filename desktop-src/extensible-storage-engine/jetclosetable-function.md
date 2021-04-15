---
description: 'Saiba mais sobre: função JetCloseTable'
title: Função JetCloseTable
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b38ba9b14c34d20b01b6530f2ed3406e55b3bc3f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104506543"
---
# <a name="jetclosetable-function"></a><span data-ttu-id="7d51c-103">Função JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="7d51c-103">JetCloseTable Function</span></span>


<span data-ttu-id="7d51c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7d51c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosetable-function"></a><span data-ttu-id="7d51c-105">Função JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="7d51c-105">JetCloseTable Function</span></span>

<span data-ttu-id="7d51c-106">A função **JetCloseTable** fecha uma tabela aberta em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7d51c-106">The **JetCloseTable** function closes an open table in a database.</span></span> <span data-ttu-id="7d51c-107">A tabela pode ser uma tabela temporária ou uma tabela normal.</span><span class="sxs-lookup"><span data-stu-id="7d51c-107">The table may be a temporary table or a normal table.</span></span>

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a><span data-ttu-id="7d51c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d51c-108">Parameters</span></span>

<span data-ttu-id="7d51c-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="7d51c-109">*sesid*</span></span>

<span data-ttu-id="7d51c-110">Identifica o contexto de sessão de banco de dados que será usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="7d51c-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="7d51c-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="7d51c-111">*tableid*</span></span>

<span data-ttu-id="7d51c-112">Identifica a tabela a ser fechada.</span><span class="sxs-lookup"><span data-stu-id="7d51c-112">Identifies the table to be closed.</span></span>

<span data-ttu-id="7d51c-113">Defina *TableName* como JET_tableidNil para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="7d51c-113">Set *tableid* to JET_tableidNil to release memory.</span></span>

### <a name="return-value"></a><span data-ttu-id="7d51c-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7d51c-114">Return Value</span></span>

<span data-ttu-id="7d51c-115">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d51c-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7d51c-116">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7d51c-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d51c-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7d51c-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="7d51c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d51c-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d51c-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7d51c-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7d51c-120">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="7d51c-120">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="7d51c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d51c-121">Remarks</span></span>

<span data-ttu-id="7d51c-122">Essa função deve ser chamada em todas as tabelas abertas com [JetOpenTable](./jetopentable-function.md).</span><span class="sxs-lookup"><span data-stu-id="7d51c-122">This function must be called on all tables opened with [JetOpenTable](./jetopentable-function.md).</span></span>

<span data-ttu-id="7d51c-123">A exceção a essa regra ocorre quando [JetOpenTable](./jetopentable-function.md) é chamado em uma transação e a transação é revertida (com [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="7d51c-123">The exception to this rule happens when [JetOpenTable](./jetopentable-function.md) is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="7d51c-124">Ao reverter uma transação, a tabela é fechada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7d51c-124">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="7d51c-125">Nesse caso, é um erro fechar a tabela com **JetCloseTable**.</span><span class="sxs-lookup"><span data-stu-id="7d51c-125">In this case, it is an error to close the table with **JetCloseTable**.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7d51c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d51c-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d51c-127"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7d51c-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7d51c-128">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7d51c-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d51c-129"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="7d51c-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7d51c-130">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7d51c-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d51c-131"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="7d51c-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7d51c-132">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="7d51c-132">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d51c-133"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="7d51c-133"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7d51c-134">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7d51c-134">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d51c-135"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7d51c-135"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7d51c-136">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7d51c-136">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7d51c-137">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7d51c-137">See Also</span></span>

[<span data-ttu-id="7d51c-138">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7d51c-138">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7d51c-139">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7d51c-139">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7d51c-140">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7d51c-140">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7d51c-141">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7d51c-141">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7d51c-142">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="7d51c-142">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="7d51c-143">JetRollback</span><span class="sxs-lookup"><span data-stu-id="7d51c-143">JetRollback</span></span>](./jetrollback-function.md)

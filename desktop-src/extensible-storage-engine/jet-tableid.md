---
description: 'Saiba mais sobre: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784993"
---
# <a name="jet_tableid"></a><span data-ttu-id="c1f54-103">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c1f54-103">JET_TABLEID</span></span>


<span data-ttu-id="c1f54-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c1f54-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tableid"></a><span data-ttu-id="c1f54-105">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c1f54-105">JET_TABLEID</span></span>

<span data-ttu-id="c1f54-106">O tipo de dados JET_TABLEID contém um identificador para o cursor de banco de dado a ser usado para uma chamada para a API do JET.</span><span class="sxs-lookup"><span data-stu-id="c1f54-106">The JET_TABLEID data type contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="c1f54-107">Um cursor só pode ser usado com a sessão que foi usada para abrir esse cursor.</span><span class="sxs-lookup"><span data-stu-id="c1f54-107">A cursor can only be used with the session that was used to open that cursor.</span></span>

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a><span data-ttu-id="c1f54-108">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="c1f54-108">Data Types</span></span>

<span data-ttu-id="c1f54-109">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c1f54-109">JET_TABLEID</span></span>

<span data-ttu-id="c1f54-110">**Nulo** ou [JET_tableidNil](./invalid-handle-constants.md) pode ser usado para indicar um identificador de cursor inválido.</span><span class="sxs-lookup"><span data-stu-id="c1f54-110">Either **NULL** or [JET_tableidNil](./invalid-handle-constants.md) can be used to indicate an invalid cursor handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="c1f54-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1f54-111">Remarks</span></span>

<span data-ttu-id="c1f54-112">Um cursor gerencia o uso de uma tabela para o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c1f54-112">A cursor manages the use of a table for the database engine.</span></span> <span data-ttu-id="c1f54-113">Um cursor pode executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="c1f54-113">A cursor can do the following tasks:</span></span>

  - <span data-ttu-id="c1f54-114">Verificar registros</span><span class="sxs-lookup"><span data-stu-id="c1f54-114">Scan records</span></span>

  - <span data-ttu-id="c1f54-115">Pesquisar por registros</span><span class="sxs-lookup"><span data-stu-id="c1f54-115">Search for records</span></span>

  - <span data-ttu-id="c1f54-116">Escolha a ordem de classificação efetiva e a visibilidade desses registros</span><span class="sxs-lookup"><span data-stu-id="c1f54-116">Choose the effective sort order and visibility of those records</span></span>

  - <span data-ttu-id="c1f54-117">Criar, atualizar ou excluir registros</span><span class="sxs-lookup"><span data-stu-id="c1f54-117">Create, update, or delete records</span></span>

  - <span data-ttu-id="c1f54-118">Modificar o esquema da tabela</span><span class="sxs-lookup"><span data-stu-id="c1f54-118">Modify the schema of the table</span></span>

<span data-ttu-id="c1f54-119">A funcionalidade com suporte do cursor pode mudar à medida que o status ou o tipo da tabela subjacente é alterado.</span><span class="sxs-lookup"><span data-stu-id="c1f54-119">The supported functionality of the cursor might change as the status or type of the underlying table changes.</span></span> <span data-ttu-id="c1f54-120">Por exemplo, uma tabela temporária pode não permitir a pesquisa de dados quando ela é aberta com determinadas opções.</span><span class="sxs-lookup"><span data-stu-id="c1f54-120">For example, a temporary table might disallow searching for data when it is opened with certain options.</span></span> <span data-ttu-id="c1f54-121">O cursor sempre está totalmente conectado à tabela subjacente e interage com esses dados diretamente sem qualquer cache.</span><span class="sxs-lookup"><span data-stu-id="c1f54-121">The cursor is always fully connected to the underlying table and interacts with that data directly without any caching.</span></span> <span data-ttu-id="c1f54-122">Quase todas as funcionalidades de ISAM principais que são expostas por esse mecanismo de banco de dados funcionam com o cursor.</span><span class="sxs-lookup"><span data-stu-id="c1f54-122">Almost all of the core ISAM functionality that is exposed by this database engine is works through the cursor.</span></span>

<span data-ttu-id="c1f54-123">Um cursor pode ser criado usando [JetOpenTable](./jetopentable-function.md) ou [JetOpenTempTable](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="c1f54-123">A cursor can be created using [JetOpenTable](./jetopentable-function.md) or [JetOpenTempTable](./jetopentemptable-function.md).</span></span> <span data-ttu-id="c1f54-124">Um cursor pode ser duplicado usando [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="c1f54-124">A cursor can be duplicated using [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="c1f54-125">Um cursor pode ser fechado explicitamente usando [JetCloseTable](./jetclosetable-function.md) ou implicitamente fechado usando [JetEndSession](./jetendsession-function.md) ou [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="c1f54-125">A cursor can be explicitly closed using [JetCloseTable](./jetclosetable-function.md) or implicitly closed using [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span> <span data-ttu-id="c1f54-126">Um cursor também pode ser fechado implicitamente pelo [JetRollback](./jetrollback-function.md) se ele foi aberto na transação que foi anulada.</span><span class="sxs-lookup"><span data-stu-id="c1f54-126">A cursor can also be implicitly closed by [JetRollback](./jetrollback-function.md) if it was opened in the transaction that was aborted.</span></span> <span data-ttu-id="c1f54-127">O número máximo de cursores que podem ser criados a qualquer momento é controlado por [JET_paramMaxCursors](./resource-parameters.md), que pode ser configurado usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="c1f54-127">The maximum number of cursors that can be created at any one time is controlled by [JET_paramMaxCursors](./resource-parameters.md), which can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="c1f54-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1f54-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1f54-129"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c1f54-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c1f54-130">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c1f54-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1f54-131"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c1f54-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c1f54-132">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c1f54-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1f54-133"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c1f54-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c1f54-134">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c1f54-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c1f54-135">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c1f54-135">See Also</span></span>

[<span data-ttu-id="c1f54-136">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="c1f54-136">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="c1f54-137">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="c1f54-137">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="c1f54-138">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="c1f54-138">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="c1f54-139">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="c1f54-139">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="c1f54-140">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="c1f54-140">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="c1f54-141">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="c1f54-141">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="c1f54-142">JetRollback</span><span class="sxs-lookup"><span data-stu-id="c1f54-142">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="c1f54-143">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="c1f54-143">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="c1f54-144">JetTerm</span><span class="sxs-lookup"><span data-stu-id="c1f54-144">JetTerm</span></span>](./jetterm-function.md)

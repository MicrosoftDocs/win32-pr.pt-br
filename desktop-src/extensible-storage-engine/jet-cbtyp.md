---
description: 'Saiba mais sobre: JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
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
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768531"
---
# <a name="jet_cbtyp"></a><span data-ttu-id="7376e-103">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="7376e-103">JET_CBTYP</span></span>


<span data-ttu-id="7376e-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7376e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_cbtyp"></a><span data-ttu-id="7376e-105">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="7376e-105">JET_CBTYP</span></span>

<span data-ttu-id="7376e-106">O **JET_CBTYP** grupo de constantes descreve todos os pontos possíveis em uma operação que o mecanismo de banco de dados notificará um aplicativo chamando a função de retorno de chamada [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="7376e-106">The **JET_CBTYP** group of constants describes all possible points in an operation that the database engine will notify an application by calling the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span> <span data-ttu-id="7376e-107">O mecanismo de banco de dados passa uma dessas constantes no parâmetro *cbtyp* da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7376e-107">The database engine passes one of these constants in the *cbtyp* parameter of the callback function.</span></span> <span data-ttu-id="7376e-108">O significado dos outros parâmetros passados pelo mecanismo de banco de dados nessa chamada depende do **JET_CBTYP** específico passado.</span><span class="sxs-lookup"><span data-stu-id="7376e-108">The meaning of the other parameters passed by the database engine in this call depend on the specific **JET_CBTYP** passed.</span></span>

<span data-ttu-id="7376e-109">**Windows XP:**  O **JET_CBTYP** grupo de constantes é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7376e-109">**Windows XP:**  The **JET_CBTYP** group of constants are introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7376e-110">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="7376e-110">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="7376e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7376e-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7376e-112">JET_cbtypNull</span><span class="sxs-lookup"><span data-stu-id="7376e-112">JET_cbtypNull</span></span><br />
<span data-ttu-id="7376e-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7376e-113">0x00000000</span></span></p></td>
<td><p><span data-ttu-id="7376e-114">Esse retorno de chamada é reservado e sempre considerado inválido.</span><span class="sxs-lookup"><span data-stu-id="7376e-114">This callback is reserved and always considered invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7376e-115">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="7376e-115">JET_cbtypFinalize</span></span><br />
<span data-ttu-id="7376e-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7376e-116">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="7376e-117">Esse retorno de chamada é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7376e-117">This callback is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7376e-118">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="7376e-118">JET_cbtypBeforeInsert</span></span><br />
<span data-ttu-id="7376e-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7376e-119">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="7376e-120">Esse retorno de chamada ocorrerá logo antes de um novo registro ser inserido em uma tabela por uma chamada para <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-120">This callback will occur just before a new record is inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="7376e-121">O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-121">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="7376e-122">Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-122">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="7376e-123">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-123">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-124"><em>sesid</em>: a sessão que tem o registro a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="7376e-124"><em>sesid</em>: The session that has the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-125"><em>DBID</em>: a ID do banco de dados da tabela que contém o registro a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="7376e-125"><em>dbid</em>: The database ID of the table that contains the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-126"><em>TableName</em>: o cursor que preparou o novo registro a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="7376e-126"><em>tableid</em>: The cursor that has prepared the new record to be inserted.</span></span> <span data-ttu-id="7376e-127">É importante observar que o valor de qualquer versão ou colunas de incremento automático podem não estar corretos no momento.</span><span class="sxs-lookup"><span data-stu-id="7376e-127">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="7376e-128"><em>pvArg1</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-128"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-129"><em>pvArg2</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-129"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-130"><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="7376e-130"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7376e-131"><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, a operação que originou o retorno de chamada falhará com esse erro.</span><span class="sxs-lookup"><span data-stu-id="7376e-131"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7376e-132">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="7376e-132">JET_cbtypAfterInsert</span></span><br />
<span data-ttu-id="7376e-133">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7376e-133">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="7376e-134">Esse retorno de chamada ocorrerá apenas depois que um novo registro tiver sido inserido em uma tabela por uma chamada para <a href="gg269288(v=exchg.10).md">JetUpdate</a> , mas antes de <a href="gg269288(v=exchg.10).md">JetUpdate</a> retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="7376e-134">This callback will occur just after a new record has been inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but before <a href="gg269288(v=exchg.10).md">JetUpdate</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="7376e-135">O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-135">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="7376e-136">Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-136">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="7376e-137">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-137">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-138"><em>sesid</em>: a sessão que tem o registro que acabou de ser inserido.</span><span class="sxs-lookup"><span data-stu-id="7376e-138"><em>sesid</em>: The session that has the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-139"><em>DBID</em>: a ID do banco de dados da tabela que contém o registro que acabou de ser inserido.</span><span class="sxs-lookup"><span data-stu-id="7376e-139"><em>dbid</em>: The database ID of the table that contains the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-140"><em>TableName</em>: um cursor na tabela no qual o registro acabou de ser inserido.</span><span class="sxs-lookup"><span data-stu-id="7376e-140"><em>tableid</em>: A cursor on the table into which the record that was just inserted.</span></span> <span data-ttu-id="7376e-141">Observe que o cursor ainda está posicionado na mesma entrada de índice que era no retorno de chamada antes de inserir.</span><span class="sxs-lookup"><span data-stu-id="7376e-141">Note that the cursor is still positioned on the same index entry as it was in the before insert callback.</span></span> <span data-ttu-id="7376e-142">Observe ainda que essa entrada de índice pode não estar relacionada de nenhuma forma ao registro que está sendo inserido.</span><span class="sxs-lookup"><span data-stu-id="7376e-142">Further note that this index entry may not be related in any way to the record being inserted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-143"><em>pvArg1</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-143"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-144"><em>pvArg2</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-144"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-145"><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="7376e-145"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7376e-146"><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7376e-146"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7376e-147">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="7376e-147">JET_cbtypBeforeReplace</span></span><br />
<span data-ttu-id="7376e-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7376e-148">0x00000008</span></span></p></td>
<td><p><span data-ttu-id="7376e-149">Esse retorno de chamada ocorrerá logo antes de um registro existente em uma tabela que está sendo alterada por uma chamada para <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-149">This callback will occur just prior to an existing record in a table being changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="7376e-150">O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-150">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="7376e-151">Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-151">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="7376e-152">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-152">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-153"><em>sesid</em>: a sessão que tem o registro a ser alterado.</span><span class="sxs-lookup"><span data-stu-id="7376e-153"><em>sesid</em>: The session that has the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="7376e-154"><em>DBID</em>: a ID do banco de dados da tabela que contém o registro a ser alterado.</span><span class="sxs-lookup"><span data-stu-id="7376e-154"><em>dbid</em>: The database ID of the table that contains the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="7376e-155"><em>TableName</em>: um cursor posicionado em uma entrada de índice associada ao registro a ser alterado.</span><span class="sxs-lookup"><span data-stu-id="7376e-155"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be changed.</span></span> <span data-ttu-id="7376e-156">É importante observar que o valor de qualquer versão ou colunas de incremento automático podem não estar corretos no momento.</span><span class="sxs-lookup"><span data-stu-id="7376e-156">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="7376e-157"><em>pvArg1</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-157"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-158"><em>pvArg2</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-158"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-159"><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="7376e-159"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7376e-160"><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, a operação que originou o retorno de chamada falhará com esse erro.</span><span class="sxs-lookup"><span data-stu-id="7376e-160"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7376e-161">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="7376e-161">JET_cbtypAfterReplace</span></span><br />
<span data-ttu-id="7376e-162">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7376e-162">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="7376e-163">Esse retorno de chamada ocorrerá apenas depois que um registro existente em uma tabela tiver sido alterado por uma chamada para <a href="gg269288(v=exchg.10).md">JetUpdate</a> , mas antes de <a href="gg269288(v=exchg.10).md">JetUpdate</a> retornar ao seu chamador.</span><span class="sxs-lookup"><span data-stu-id="7376e-163">This callback will occur just after an existing record in a table has been changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but prior to <a href="gg269288(v=exchg.10).md">JetUpdate</a> returning to its caller.</span></span></p>
<p><span data-ttu-id="7376e-164">O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-164">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="7376e-165">Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-165">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="7376e-166">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-166">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-167"><em>sesid</em>: a sessão que tem o registro que acabou de ser alterado.</span><span class="sxs-lookup"><span data-stu-id="7376e-167"><em>sesid</em>: The session that has the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="7376e-168"><em>DBID</em>: a ID do banco de dados da tabela que contém o registro que acabou de ser alterado.</span><span class="sxs-lookup"><span data-stu-id="7376e-168"><em>dbid</em>: The database ID of the table that contains the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="7376e-169"><em>TableName</em>: um cursor posicionado em uma entrada de índice associada ao registro que acabou de ser alterado.</span><span class="sxs-lookup"><span data-stu-id="7376e-169"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="7376e-170"><em>pvArg1</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-170"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-171"><em>pvArg2</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-171"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-172"><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="7376e-172"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7376e-173"><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7376e-173"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7376e-174">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="7376e-174">JET_cbtypBeforeDelete</span></span><br />
<span data-ttu-id="7376e-175">0x00000020</span><span class="sxs-lookup"><span data-stu-id="7376e-175">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="7376e-176">Esse retorno de chamada ocorrerá logo antes de um registro existente em uma tabela ser excluído por uma chamada para <a href="gg269315(v=exchg.10).md">JetDelete</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-176">This callback will occur just before an existing record in a table is deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a>.</span></span></p>
<p><span data-ttu-id="7376e-177">O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-177">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="7376e-178">Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-178">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="7376e-179">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-179">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-180"><em>sesid</em>: a sessão que tem o registro a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7376e-180"><em>sesid</em>: The session that has the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-181"><em>DBID</em>: a ID do banco de dados da tabela que contém o registro a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7376e-181"><em>dbid</em>: The database ID of the table that contains the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-182"><em>TableName</em>: um cursor posicionado em uma entrada de índice associada ao registro a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7376e-182"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-183"><em>pvArg1</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-183"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-184"><em>pvArg2</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-184"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-185"><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="7376e-185"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7376e-186"><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, a operação que originou o retorno de chamada falhará com esse erro.</span><span class="sxs-lookup"><span data-stu-id="7376e-186"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7376e-187">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="7376e-187">JET_cbtypAfterDelete</span></span><br />
<span data-ttu-id="7376e-188">0x00000040</span><span class="sxs-lookup"><span data-stu-id="7376e-188">0x00000040</span></span></p></td>
<td><p><span data-ttu-id="7376e-189">Esse retorno de chamada ocorrerá apenas depois que um registro existente em uma tabela tiver sido excluído por uma chamada para <a href="gg269315(v=exchg.10).md">JetDelete</a> , mas antes de <a href="gg269315(v=exchg.10).md">JetDelete</a> retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="7376e-189">This callback will occur just after an existing record in a table has been deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a> but before <a href="gg269315(v=exchg.10).md">JetDelete</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="7376e-190">O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-190">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="7376e-191">Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-191">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="7376e-192">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-192">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-193"><em>sesid</em>: a sessão que tem o registro que acabou de ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7376e-193"><em>sesid</em>: The session that has the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-194"><em>DBID</em>: a ID do banco de dados da tabela que contém o registro que acabou de ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7376e-194"><em>dbid</em>: The database ID of the table that contains the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-195"><em>TableName</em>: um cursor posicionado em uma entrada de índice associada ao registro que acabou de ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7376e-195"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="7376e-196"><em>pvArg1</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-196"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-197"><em>pvArg2</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-197"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-198"><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="7376e-198"><em>pvContext</em>: the context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7376e-199"><em>ulUnused</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-199"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="7376e-200">Se um erro for retornado pelo retorno de chamada, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7376e-200">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7376e-201">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="7376e-201">JET_cbtypUserDefinedDefaultValue</span></span><br />
<span data-ttu-id="7376e-202">0x00000080</span><span class="sxs-lookup"><span data-stu-id="7376e-202">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="7376e-203">Esse retorno de chamada ocorrerá quando o mecanismo precisar recuperar o valor padrão definido pelo usuário de uma coluna do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7376e-203">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="7376e-204">Esse retorno de chamada é essencialmente uma implementação limitada de <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> que é avaliada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7376e-204">This callback is essentially a limited implementation of <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> that is evaluated by the application.</span></span> <span data-ttu-id="7376e-205">Um máximo de um valor de coluna pode ser retornado para um valor padrão definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7376e-205">A maximum of one column value can be returned for a user defined default value.</span></span></p>
<p><span data-ttu-id="7376e-206">O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg294122(v=exchg.10).md">JetAddColumn</a> por meio de uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ou passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> em uma estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> em uma estrutura de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="7376e-206">The function pointer for this callback reason is either passed to <a href="gg294122(v=exchg.10).md">JetAddColumn</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure or passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure in a <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure in a <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure.</span></span></p>
<p><span data-ttu-id="7376e-207">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-207">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-208"><em>sesid</em>: a sessão que está computando o valor padrão definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="7376e-208"><em>sesid</em>: The session that is computing the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="7376e-209"><em>DBID</em>: a ID do banco de dados da tabela que contém o valor padrão definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="7376e-209"><em>dbid</em>: The database ID of the table that contains the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="7376e-210"><em>TableName</em>: um cursor posicionado no registro para o qual o valor padrão definido pelo usuário está sendo recuperado</span><span class="sxs-lookup"><span data-stu-id="7376e-210"><em>tableid</em>: A cursor positioned on the record for which the user defined default value is being retrieved</span></span></p></li>
<li><p><span data-ttu-id="7376e-211"><em>pvArg1</em>: o buffer de saída para o valor padrão definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="7376e-211"><em>pvArg1</em>: The output buffer for the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="7376e-212"><em>pvArg2</em>: on Input, esse é o tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="7376e-212"><em>pvArg2</em>: On input, this is the size of the output buffer.</span></span> <span data-ttu-id="7376e-213">Na saída, esse é o tamanho real do valor padrão definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7376e-213">On output, this is the actual size of the user defined default value.</span></span> <span data-ttu-id="7376e-214">em ambos os casos, o tamanho é um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7376e-214">in either case, the size is a 32-bit unsigned integer.</span></span></p></li>
<li><p><span data-ttu-id="7376e-215"><em>pvContext</em>: um ponteiro para um buffer que contém os dados de usuário especificados na estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> quando a coluna foi criada ou nula se nenhum contexto foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="7376e-215"><em>pvContext</em>: A pointer to a buffer containing the user data specified in the <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure when the column was created or NULL if no context was provided.</span></span></p></li>
<li><p><span data-ttu-id="7376e-216"><em>ulUnused</em>: a ID de coluna da coluna para a qual o valor padrão definido pelo usuário está sendo recuperado.</span><span class="sxs-lookup"><span data-stu-id="7376e-216"><em>ulUnused</em>: The column ID of the column for which the user defined default value is being retrieved.</span></span></p></li>
</ul>
<p><span data-ttu-id="7376e-217">Se um erro for retornado pelo retorno de chamada, a operação que originou o retorno de chamada falhará com esse erro.</span><span class="sxs-lookup"><span data-stu-id="7376e-217">If an error is returned by the callback then the operation originating the callback will fail with that error.</span></span></p>
<p><span data-ttu-id="7376e-218">Se JET_wrnBufferTruncated for retornado pelo retorno de chamada, a operação continuará, mas o valor inteiro não será recuperado durante o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7376e-218">If JET_wrnBufferTruncated is returned by the callback, the operation will continue, but the entire value is not retrieved during the callback.</span></span></p>
<p><span data-ttu-id="7376e-219">Se JET_wrnColumnNull for retornado pelo retorno de chamada, a operação continuará, mas o valor padrão definido pelo usuário para a coluna será nulo.</span><span class="sxs-lookup"><span data-stu-id="7376e-219">If JET_wrnColumnNull is returned by the callback, the operation will continue, but the user defined default value for the column is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7376e-220">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="7376e-220">JET_cbtypOnlineDefragCompleted</span></span><br />
<span data-ttu-id="7376e-221">0x00000100</span><span class="sxs-lookup"><span data-stu-id="7376e-221">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="7376e-222">Esse retorno de chamada ocorrerá quando a desfragmentação online de um banco de dados como iniciado pelo <a href="gg269317(v=exchg.10).md">JetDefragment</a> tiver sido interrompida devido à conclusão do processo ou ao limite de tempo que está sendo atingido.</span><span class="sxs-lookup"><span data-stu-id="7376e-222">This callback will occur when the online defragmentation of a database as initiated by <a href="gg269317(v=exchg.10).md">JetDefragment</a> has stopped due to either the process being completed or the time limit being reached.</span></span></p>
<p><span data-ttu-id="7376e-223">O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-223">The function pointer for this callback reason is passed to <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span> <span data-ttu-id="7376e-224">Para obter mais informações, consulte <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-224">For more information, see <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span></p>
<p><span data-ttu-id="7376e-225">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-225">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-226"><em>sesid</em>: a sessão usada para executar a desfragmentação online do banco de dados ou JET_sesidNil para um arquivo de streaming.</span><span class="sxs-lookup"><span data-stu-id="7376e-226"><em>sesid</em>: The session used to perform online defragmentation for the database or JET_sesidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="7376e-227"><em>DBID</em>: a ID do banco de dados que está sendo desfragmentado ou JET_dbidNil para um arquivo de streaming.</span><span class="sxs-lookup"><span data-stu-id="7376e-227"><em>dbid</em>: The database ID of the database being defragmented or JET_dbidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="7376e-228"><em>TableName</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="7376e-228"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="7376e-229"><em>pvArg1</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-229"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-230"><em>pvArg2</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-230"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-231"><em>pvContext</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-231"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-232"><em>ulUnused</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-232"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="7376e-233">Se um erro for retornado pelo retorno de chamada, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7376e-233">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7376e-234">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="7376e-234">JET_cbtypFreeCursorLS</span></span><br />
<span data-ttu-id="7376e-235">0x00000200</span><span class="sxs-lookup"><span data-stu-id="7376e-235">0x00000200</span></span></p></td>
<td><p><span data-ttu-id="7376e-236">Esse retorno de chamada ocorrerá quando o aplicativo precisar limpar o identificador de contexto para o armazenamento local associado a um cursor que está sendo liberado pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7376e-236">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="7376e-237">Para obter mais informações, consulte <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-237">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="7376e-238">O ponteiro de função para esse motivo de retorno de chamada é configurado por meio de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-238">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="7376e-239">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-239">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-240"><em>sesid</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="7376e-240"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="7376e-241"><em>DBID</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="7376e-241"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="7376e-242"><em>TableName</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="7376e-242"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="7376e-243"><em>pvArg1</em>: o conjunto de identificadores de contexto usando <a href="gg269243(v=exchg.10).md">JetSetLS</a></span><span class="sxs-lookup"><span data-stu-id="7376e-243"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a></span></span></p></li>
<li><p><span data-ttu-id="7376e-244"><em>pvArg2</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-244"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-245"><em>pvContext</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-245"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-246"><em>ulUnused</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-246"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="7376e-247">Se um erro for retornado pelo retorno de chamada, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7376e-247">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7376e-248">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="7376e-248">JET_cbtypFreeTableLS</span></span><br />
<span data-ttu-id="7376e-249">0x00000400</span><span class="sxs-lookup"><span data-stu-id="7376e-249">0x00000400</span></span></p></td>
<td><p><span data-ttu-id="7376e-250">Esse retorno de chamada ocorrerá como resultado da necessidade do aplicativo para limpar o identificador de contexto do armazenamento local associado a uma tabela que está sendo liberada pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7376e-250">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="7376e-251">Para obter mais informações, consulte <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-251">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="7376e-252">O ponteiro de função para esse motivo de retorno de chamada é configurado por meio de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-252">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="7376e-253">Os parâmetros de retorno de chamada terão os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7376e-253">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="7376e-254"><em>sesid</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="7376e-254"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="7376e-255"><em>DBID</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="7376e-255"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="7376e-256"><em>TableName</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="7376e-256"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="7376e-257"><em>pvArg1</em>: o identificador de contexto definido usando <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span><span class="sxs-lookup"><span data-stu-id="7376e-257"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p></li>
<li><p><span data-ttu-id="7376e-258"><em>pvArg2</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-258"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-259"><em>pvContext</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-259"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="7376e-260"><em>ulUnused</em>: <strong>nulo</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-260"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="7376e-261">Se um erro for retornado pelo retorno de chamada, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7376e-261">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="7376e-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7376e-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7376e-263"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7376e-264">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7376e-264">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7376e-265"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7376e-266">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7376e-266">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7376e-267"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="7376e-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7376e-268">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="7376e-268">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7376e-269">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7376e-269">See Also</span></span>

[<span data-ttu-id="7376e-270">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="7376e-270">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)

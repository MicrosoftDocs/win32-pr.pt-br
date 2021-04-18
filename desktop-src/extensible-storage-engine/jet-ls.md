---
description: 'Saiba mais sobre: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771315"
---
# <a name="jet_ls"></a><span data-ttu-id="8f079-103">JET_LS</span><span class="sxs-lookup"><span data-stu-id="8f079-103">JET_LS</span></span>


<span data-ttu-id="8f079-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8f079-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ls"></a><span data-ttu-id="8f079-105">JET_LS</span><span class="sxs-lookup"><span data-stu-id="8f079-105">JET_LS</span></span>

<span data-ttu-id="8f079-106">O tipo de dados **JET_LS** contém um identificador de contexto para armazenamento local (ls). Esse identificador pode ser associado a um cursor ou uma tabela e pode se referir a recursos alocados dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="8f079-106">The **JET_LS** data type contains a context handle to local storage (LS).This handle might be associated with a cursor or a table and might refer to dynamically allocated resources.</span></span>

<span data-ttu-id="8f079-107">**Windows XP: o JET_LS** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f079-107">**Windows XP:  JET_LS** is introduced in Windows XP.</span></span>

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a><span data-ttu-id="8f079-108">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="8f079-108">Data Types</span></span>

<span data-ttu-id="8f079-109">JET_LS</span><span class="sxs-lookup"><span data-stu-id="8f079-109">JET_LS</span></span>

<span data-ttu-id="8f079-110">Um valor de JET_LSNil indica um identificador de contexto inválido.</span><span class="sxs-lookup"><span data-stu-id="8f079-110">A value of JET_LSNil indicates an invalid context handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="8f079-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f079-111">Remarks</span></span>

<span data-ttu-id="8f079-112">Um identificador de contexto é inicialmente associado ao tipo de dados **JET_LS** , usando [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f079-112">A context handle is initially associated with the **JET_LS** data type, using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="8f079-113">O identificador de contexto pode ser recuperado do tipo de dados **JET_LS** , usando [JetGetLS](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f079-113">The context handle can be retrieved from the **JET_LS** data type, using [JetGetLS](./jetgetls-function.md).</span></span>

<span data-ttu-id="8f079-114">O identificador de contexto pode ser explicitamente desassociado do tipo de dados **JET_LS** usando [JetGetLS](./jetgetls-function.md) com JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="8f079-114">The context handle can be explicitly disassociated from the **JET_LS** data type using [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="8f079-115">Como alternativa, o identificador de contexto pode ser implicitamente desassociado do tipo de dados **JET_LS** quando o objeto subjacente é liberado pelo mecanismo de banco de dados como resultado de uma ação direta ou indireta pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8f079-115">Alternatively, the context handle can be implicitly disassociated from the **JET_LS** data type when the underlying object is released by the database engine as a result of direct or indirect action by the application.</span></span> <span data-ttu-id="8f079-116">No caso implícito, um retorno de chamada de tempo de execução é emitido para o aplicativo para que ele possa limpar o identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="8f079-116">In the implicit case, a runtime callback is issued to the application so that it can clean up the context handle.</span></span> <span data-ttu-id="8f079-117">Para obter mais informações sobre como desassociar implicitamente do tipo de dados **JET_LS** , consulte [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f079-117">For more information on implicitly disassociating from the **JET_LS** data type, see [JetSetLS](./jetsetls-function.md).</span></span>

<span data-ttu-id="8f079-118">Os sinalizadores a seguir são associados ao tipo de dados JET_LS.</span><span class="sxs-lookup"><span data-stu-id="8f079-118">The following flags are associated with the JET_LS data type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f079-119">Termo</span><span class="sxs-lookup"><span data-stu-id="8f079-119">Term</span></span></p></th>
<th><p><span data-ttu-id="8f079-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f079-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f079-121">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="8f079-121">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="8f079-122">O identificador de contexto é desassociado do objeto.</span><span class="sxs-lookup"><span data-stu-id="8f079-122">The context handle is disassociated from the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f079-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="8f079-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="8f079-124">Definir ou recuperar o armazenamento local associado a um cursor de tabela.</span><span class="sxs-lookup"><span data-stu-id="8f079-124">Set or retrieve the local storage associated with a table cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f079-125">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="8f079-125">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="8f079-126">Definir ou recuperar o armazenamento local associado a uma tabela.</span><span class="sxs-lookup"><span data-stu-id="8f079-126">Set or retrieve the local storage associated with a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f079-127">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="8f079-127">JET_LSNil</span></span></p></td>
<td><p><span data-ttu-id="8f079-128">O identificador de contexto é inválido.</span><span class="sxs-lookup"><span data-stu-id="8f079-128">The context handle is invalid.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="8f079-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f079-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f079-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8f079-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8f079-131">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f079-131">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f079-132"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="8f079-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8f079-133">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8f079-133">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f079-134"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="8f079-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8f079-135">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8f079-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8f079-136">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8f079-136">See Also</span></span>

[<span data-ttu-id="8f079-137">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="8f079-137">JetSetLS</span></span>](./jetsetls-function.md)  
[<span data-ttu-id="8f079-138">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="8f079-138">JetGetLS</span></span>](./jetgetls-function.md)

---
description: 'Saiba mais sobre: estrutura de JET_INSTANCE_INFO'
title: Estrutura de JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
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
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837070"
---
# <a name="jet_instance_info-structure"></a><span data-ttu-id="56b0d-103">Estrutura de JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="56b0d-103">JET_INSTANCE_INFO Structure</span></span>


<span data-ttu-id="56b0d-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="56b0d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance_info-structure"></a><span data-ttu-id="56b0d-105">Estrutura de JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="56b0d-105">JET_INSTANCE_INFO Structure</span></span>

<span data-ttu-id="56b0d-106">A estrutura de **JET_INSTANCE_INFO** recebe informações sobre a execução de instâncias de banco de dados quando usadas com as funções [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) e [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) .</span><span class="sxs-lookup"><span data-stu-id="56b0d-106">The **JET_INSTANCE_INFO** structure receives information about running database instances when used with the [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) and [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) functions.</span></span>

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a><span data-ttu-id="56b0d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="56b0d-107">Members</span></span>

<span data-ttu-id="56b0d-108">**hInstanceId**</span><span class="sxs-lookup"><span data-stu-id="56b0d-108">**hInstanceId**</span></span>

<span data-ttu-id="56b0d-109">O [JET_INSTANCE](./jet-instance.md) da instância fornecida.</span><span class="sxs-lookup"><span data-stu-id="56b0d-109">The [JET_INSTANCE](./jet-instance.md) of the given instance.</span></span>

<span data-ttu-id="56b0d-110">**szInstanceName**</span><span class="sxs-lookup"><span data-stu-id="56b0d-110">**szInstanceName**</span></span>

<span data-ttu-id="56b0d-111">O nome da instância do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="56b0d-111">The name of the database instance.</span></span> <span data-ttu-id="56b0d-112">Esse valor pode ser **nulo** se a instância não tiver um nome.</span><span class="sxs-lookup"><span data-stu-id="56b0d-112">This value can be **NULL** if the instance does not have a name.</span></span>

<span data-ttu-id="56b0d-113">**cDatabases**</span><span class="sxs-lookup"><span data-stu-id="56b0d-113">**cDatabases**</span></span>

<span data-ttu-id="56b0d-114">O número de bancos de dados que são anexados à instância de Database.</span><span class="sxs-lookup"><span data-stu-id="56b0d-114">The number of databases that are attached to the database instance.</span></span> <span data-ttu-id="56b0d-115">**cDatabases** também mantém o tamanho das matrizes de cadeias de caracteres que são retornadas em **szDatabaseFileName**, **szDatabaseDisplayName** e **szDatabaseSLVFileName**.</span><span class="sxs-lookup"><span data-stu-id="56b0d-115">**cDatabases** also holds the size of the arrays of strings that are returned in **szDatabaseFileName**, **szDatabaseDisplayName**, and **szDatabaseSLVFileName**.</span></span>

<span data-ttu-id="56b0d-116">**szDatabaseFileName**</span><span class="sxs-lookup"><span data-stu-id="56b0d-116">**szDatabaseFileName**</span></span>

<span data-ttu-id="56b0d-117">Uma matriz de cadeias de caracteres, cada uma mantendo o nome de arquivo de um banco de dados anexado à instância do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="56b0d-117">An array of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="56b0d-118">A matriz tem elementos **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="56b0d-118">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="56b0d-119">**szDatabaseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="56b0d-119">**szDatabaseDisplayName**</span></span>

<span data-ttu-id="56b0d-120">Uma matriz de cadeias de caracteres, cada uma mantendo o nome de exibição de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="56b0d-120">An array of strings, each holding the display name of a database.</span></span> <span data-ttu-id="56b0d-121">Atualmente, a cadeia de caracteres pode ser nula.</span><span class="sxs-lookup"><span data-stu-id="56b0d-121">Currently the string can be NULL.</span></span> <span data-ttu-id="56b0d-122">A matriz tem elementos **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="56b0d-122">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="56b0d-123">**szDatabaseSLVFileName**</span><span class="sxs-lookup"><span data-stu-id="56b0d-123">**szDatabaseSLVFileName**</span></span>

<span data-ttu-id="56b0d-124">Uma matriz de cadeias de caracteres, cada uma mantendo o nome de arquivo do arquivo SLV que está anexado à instância do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="56b0d-124">An array of strings, each holding the file name of the SLV file that is attached to the database instance.</span></span> <span data-ttu-id="56b0d-125">A matriz tem elementos **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="56b0d-125">The array has **cDatabases** elements.</span></span> <span data-ttu-id="56b0d-126">Não há suporte para arquivos SLV, portanto, esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="56b0d-126">SLV files are not supported, so this field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="56b0d-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="56b0d-127">Remarks</span></span>

<span data-ttu-id="56b0d-128">Cada instância de banco de dados pode ter vários bancos de dados anexados a ela.</span><span class="sxs-lookup"><span data-stu-id="56b0d-128">Each database instance can have several databases attached to it.</span></span>

<span data-ttu-id="56b0d-129">Para uma determinada estrutura de **JET_INSTANCE_INFO** , a matriz de cadeias de caracteres retornada para os bancos de dados está na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="56b0d-129">For a given **JET_INSTANCE_INFO** structure, the array of strings that is returned for the databases are in the same order.</span></span> <span data-ttu-id="56b0d-130">Por exemplo, "szDatabaseDisplayName \[ i \] " e "szDatabaseFileName \[ i \] " fazem referência ao mesmo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="56b0d-130">For example, "szDatabaseDisplayName\[ i \]" and "szDatabaseFileName\[ i \]" both refer to the same database.</span></span>

### <a name="requirements"></a><span data-ttu-id="56b0d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56b0d-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56b0d-132"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="56b0d-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="56b0d-133">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="56b0d-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b0d-134"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="56b0d-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="56b0d-135">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="56b0d-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b0d-136"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="56b0d-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="56b0d-137">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="56b0d-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b0d-138"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="56b0d-138"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="56b0d-139">Implementado como <strong>JET_INSTANCE_INFO_W</strong> (Unicode) e <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="56b0d-139">Implemented as <strong>JET_INSTANCE_INFO_W</strong> (Unicode) and <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="56b0d-140">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="56b0d-140">See Also</span></span>

[<span data-ttu-id="56b0d-141">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="56b0d-141">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="56b0d-142">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="56b0d-142">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="56b0d-143">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="56b0d-143">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="56b0d-144">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="56b0d-144">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)

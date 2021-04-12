---
description: 'Saiba mais sobre: função JetCloseDatabase'
title: Função JetCloseDatabase
TOCTitle: JetCloseDatabase Function
ms:assetid: e17a05dd-c30b-4e8f-8538-91a65e8052d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294123(v=EXCHG.10)
ms:contentKeyID: 32765737
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9088e0ebc3b4778d6968c999afc238e49fb2f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501295"
---
# <a name="jetclosedatabase-function"></a><span data-ttu-id="5abd4-103">Função JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="5abd4-103">JetCloseDatabase Function</span></span>


<span data-ttu-id="5abd4-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5abd4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosedatabase-function"></a><span data-ttu-id="5abd4-105">Função JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="5abd4-105">JetCloseDatabase Function</span></span>

<span data-ttu-id="5abd4-106">A função **JetCloseDatabase** fecha um arquivo de banco de dados que foi aberto anteriormente com [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="5abd4-106">The **JetCloseDatabase** function closes a database file that was previously opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5abd4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5abd4-107">Parameters</span></span>

<span data-ttu-id="5abd4-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5abd4-108">*sesid*</span></span>

<span data-ttu-id="5abd4-109">O contexto de sessão de banco de dados que será usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="5abd4-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="5abd4-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="5abd4-110">*dbid*</span></span>

<span data-ttu-id="5abd4-111">O banco de dados a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="5abd4-111">The database to be closed.</span></span>

<span data-ttu-id="5abd4-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5abd4-112">*grbit*</span></span>

<span data-ttu-id="5abd4-113">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5abd4-113">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="5abd4-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5abd4-114">Return Value</span></span>

<span data-ttu-id="5abd4-115">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="5abd4-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5abd4-116">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5abd4-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5abd4-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5abd4-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="5abd4-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5abd4-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5abd4-119">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="5abd4-119">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="5abd4-120">O banco de dados não foi aberto anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5abd4-120">The database was not previously opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5abd4-121">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="5abd4-121">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="5abd4-122">O parâmetro <em>DBID</em> não era um identificador de banco de dados válido.</span><span class="sxs-lookup"><span data-stu-id="5abd4-122">The <em>dbid</em> parameter was not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5abd4-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5abd4-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5abd4-124">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="5abd4-124">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="5abd4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5abd4-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5abd4-126"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5abd4-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5abd4-127">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5abd4-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5abd4-128"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="5abd4-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5abd4-129">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5abd4-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5abd4-130"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="5abd4-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5abd4-131">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5abd4-131">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5abd4-132"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="5abd4-132"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5abd4-133">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5abd4-133">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5abd4-134"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5abd4-134"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5abd4-135">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5abd4-135">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5abd4-136">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5abd4-136">See Also</span></span>

[<span data-ttu-id="5abd4-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5abd4-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5abd4-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5abd4-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5abd4-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5abd4-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5abd4-140">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5abd4-140">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5abd4-141">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="5abd4-141">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="5abd4-142">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="5abd4-142">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="5abd4-143">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="5abd4-143">JetOpenDatabase</span></span>](./jetopendatabase-function.md)

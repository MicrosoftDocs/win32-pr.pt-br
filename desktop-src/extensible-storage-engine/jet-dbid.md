---
description: 'Saiba mais sobre: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647118"
---
# <a name="jet_dbid"></a><span data-ttu-id="e987d-103">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="e987d-103">JET_DBID</span></span>


<span data-ttu-id="e987d-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e987d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbid"></a><span data-ttu-id="e987d-105">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="e987d-105">JET_DBID</span></span>

<span data-ttu-id="e987d-106">O tipo de dados **JET_DBID** contém o identificador para o banco de dado.</span><span class="sxs-lookup"><span data-stu-id="e987d-106">The **JET_DBID** data type contains the handle to the database.</span></span> <span data-ttu-id="e987d-107">Um identificador de banco de dados é usado para gerenciar o esquema de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e987d-107">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="e987d-108">Ele também pode ser usado para gerenciar as tabelas dentro desse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e987d-108">It can also be used to manage the tables inside of that database.</span></span>

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a><span data-ttu-id="e987d-109">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="e987d-109">Data Types</span></span>

<span data-ttu-id="e987d-110">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="e987d-110">JET_DBID</span></span>

<span data-ttu-id="e987d-111">Identificador para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e987d-111">Handle to the database.</span></span>

<span data-ttu-id="e987d-112">Um valor de JET_dbidNil indica que o identificador é inválido.</span><span class="sxs-lookup"><span data-stu-id="e987d-112">A value of JET_dbidNil indicates that the handle is invalid.</span></span>

### <a name="remarks"></a><span data-ttu-id="e987d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e987d-113">Remarks</span></span>

<span data-ttu-id="e987d-114">Um identificador de banco de dados é criado por meio de uma chamada para [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="e987d-114">A database handle is created by means of a call to [JetCreateDatabase](./jetcreatedatabase-function.md) or [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

<span data-ttu-id="e987d-115">Um identificador de banco de dados pode ser fechado explicitamente por [JetCloseDatabase](./jetclosedatabase-function.md) ou implicitamente fechado por [JetEndSession](./jetendsession-function.md) ou [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="e987d-115">A database handle can be explicitly closed by [JetCloseDatabase](./jetclosedatabase-function.md) or implicitly closed by [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="e987d-116">Um identificador de banco de dados pode ser usado somente dentro da sessão em que foi criado.</span><span class="sxs-lookup"><span data-stu-id="e987d-116">A database handle can be used only within the session in which it was created.</span></span> <span data-ttu-id="e987d-117">A existência de um identificador de banco de dados corresponde à abertura lógica de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e987d-117">The existence of a database handle corresponds to the logical open of a database.</span></span> <span data-ttu-id="e987d-118">Uma abertura lógica é diferente da abertura física de um banco de dados, o que acontece quando um banco de dados é anexado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="e987d-118">A logical open is different from the physical open of a database, which happens when a database is attached to the system.</span></span>

### <a name="requirements"></a><span data-ttu-id="e987d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e987d-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e987d-120"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e987d-120"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e987d-121">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e987d-121">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e987d-122"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e987d-122"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e987d-123">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e987d-123">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e987d-124"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e987d-124"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e987d-125">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e987d-125">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e987d-126">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e987d-126">See Also</span></span>

[<span data-ttu-id="e987d-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="e987d-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="e987d-128">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="e987d-128">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="e987d-129">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="e987d-129">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="e987d-130">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="e987d-130">JetEndSession</span></span>](./jetendsession-function.md)

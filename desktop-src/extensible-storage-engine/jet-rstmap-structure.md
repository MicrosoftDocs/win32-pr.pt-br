---
description: 'Saiba mais sobre: estrutura de JET_RSTMAP'
title: Estrutura de JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646913"
---
# <a name="jet_rstmap-structure"></a><span data-ttu-id="06c52-103">Estrutura de JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="06c52-103">JET_RSTMAP Structure</span></span>


<span data-ttu-id="06c52-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="06c52-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstmap-structure"></a><span data-ttu-id="06c52-105">Estrutura de JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="06c52-105">JET_RSTMAP Structure</span></span>

<span data-ttu-id="06c52-106">A estrutura de **JET_RSTMAP** permite o remapeamento de caminhos de arquivo de banco de dados que são armazenados nos logs de transação durante a recuperação, quando usados pelas funções [JetInit](./jetinit-function.md) e [JetExternalRestore](./jetexternalrestore-function.md) .</span><span class="sxs-lookup"><span data-stu-id="06c52-106">The **JET_RSTMAP** structure enables the remapping of database file paths that are stored in the transaction logs during recovery, when used by the [JetInit](./jetinit-function.md) and [JetExternalRestore](./jetexternalrestore-function.md) functions.</span></span> <span data-ttu-id="06c52-107">Isso permite que os bancos de dados sejam movidos quando offline ou restaurados do backup.</span><span class="sxs-lookup"><span data-stu-id="06c52-107">This enables the databases to be moved when offline or when restored from backup.</span></span>

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a><span data-ttu-id="06c52-108">Membros</span><span class="sxs-lookup"><span data-stu-id="06c52-108">Members</span></span>

<span data-ttu-id="06c52-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="06c52-109">**szDatabaseName**</span></span>

<span data-ttu-id="06c52-110">O caminho absoluto atual de um banco de dados que está associado aos logs de transação que são reproduzidos durante a recuperação.</span><span class="sxs-lookup"><span data-stu-id="06c52-110">The current absolute path of a database that is associated with the transaction logs that are replayed during recovery.</span></span>

<span data-ttu-id="06c52-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="06c52-111">**szNewDatabaseName**</span></span>

<span data-ttu-id="06c52-112">O novo caminho absoluto para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="06c52-112">The new absolute path for the database.</span></span>

### <a name="requirements"></a><span data-ttu-id="06c52-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06c52-113">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06c52-114"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="06c52-114"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="06c52-115">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="06c52-115">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06c52-116"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="06c52-116"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="06c52-117">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="06c52-117">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06c52-118"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="06c52-118"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="06c52-119">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="06c52-119">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06c52-120"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="06c52-120"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="06c52-121">Implementado como <strong>JET_RSTMAP_W</strong> (Unicode) e <strong>JET_RSTMAP_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="06c52-121">Implemented as <strong>JET_RSTMAP_W</strong> (Unicode) and <strong>JET_RSTMAP_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="06c52-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="06c52-122">See Also</span></span>

[<span data-ttu-id="06c52-123">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="06c52-123">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="06c52-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="06c52-124">JetInit</span></span>](./jetinit-function.md)

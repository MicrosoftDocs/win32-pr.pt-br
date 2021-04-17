---
description: 'Saiba mais sobre: estrutura de JET_SIGNATURE'
title: Estrutura de JET_SIGNATURE
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: d6210853e22fda5085980c2fb285411ba431bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783758"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="785d8-103">Estrutura de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="785d8-103">JET_SIGNATURE Structure</span></span>


<span data-ttu-id="785d8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="785d8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_signature-structure"></a><span data-ttu-id="785d8-105">Estrutura de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="785d8-105">JET_SIGNATURE Structure</span></span>

<span data-ttu-id="785d8-106">A estrutura de **JET_SIGNATURE** contém informações que identificam exclusivamente um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="785d8-106">The **JET_SIGNATURE** structure contains information that uniquely identifies a database.</span></span>

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a><span data-ttu-id="785d8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="785d8-107">Members</span></span>

<span data-ttu-id="785d8-108">**ulRandom**</span><span class="sxs-lookup"><span data-stu-id="785d8-108">**ulRandom**</span></span>

<span data-ttu-id="785d8-109">Um número atribuído aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="785d8-109">A randomly assigned number.</span></span>

<span data-ttu-id="785d8-110">**logtimeCreate**</span><span class="sxs-lookup"><span data-stu-id="785d8-110">**logtimeCreate**</span></span>

<span data-ttu-id="785d8-111">O [JET_LOGTIME](./jet-logtime-structure.md) no momento da [JetCreateDatabase](./jetcreatedatabase-function.md) é executado.</span><span class="sxs-lookup"><span data-stu-id="785d8-111">The [JET_LOGTIME](./jet-logtime-structure.md) at the time of [JetCreateDatabase](./jetcreatedatabase-function.md) is executed.</span></span>

<span data-ttu-id="785d8-112">**szComputerName**</span><span class="sxs-lookup"><span data-stu-id="785d8-112">**szComputerName**</span></span>

<span data-ttu-id="785d8-113">O valor de cadeia de caracteres opcional do nome NetBIOS para o computador.</span><span class="sxs-lookup"><span data-stu-id="785d8-113">The optional string value of the NetBIOS name for the computer.</span></span> <span data-ttu-id="785d8-114">Esse valor não pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="785d8-114">This value may not be set.</span></span>

### <a name="remarks"></a><span data-ttu-id="785d8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="785d8-115">Remarks</span></span>

<span data-ttu-id="785d8-116">Isso pode ser encontrado como um elemento de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span><span class="sxs-lookup"><span data-stu-id="785d8-116">This can be found as an element of [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="785d8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="785d8-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="785d8-118"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="785d8-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="785d8-119">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="785d8-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="785d8-120"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="785d8-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="785d8-121">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="785d8-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="785d8-122"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="785d8-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="785d8-123">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="785d8-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="785d8-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="785d8-124">See Also</span></span>

[<span data-ttu-id="785d8-125">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="785d8-125">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="785d8-126">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="785d8-126">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="785d8-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="785d8-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)

---
description: 'Saiba mais sobre: estrutura de JET_THREADSTATS'
title: Estrutura de JET_THREADSTATS
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797983"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="39f34-103">Estrutura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="39f34-103">JET_THREADSTATS Structure</span></span>


<span data-ttu-id="39f34-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="39f34-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_threadstats-structure"></a><span data-ttu-id="39f34-105">Estrutura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="39f34-105">JET_THREADSTATS Structure</span></span>

<span data-ttu-id="39f34-106">A estrutura de **JET_THREADSTATS** contém estatísticas cumulativas no trabalho executado pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="39f34-106">The **JET_THREADSTATS** structure contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="39f34-107">Essas informações são retornadas por meio de [JetGetThreadStats](./jetgetthreadstats-function.md).</span><span class="sxs-lookup"><span data-stu-id="39f34-107">This information is returned via [JetGetThreadStats](./jetgetthreadstats-function.md).</span></span>

<span data-ttu-id="39f34-108">**Windows Vista:**  A estrutura de **JET_THREADSTATS** é introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="39f34-108">**Windows Vista:**  The **JET_THREADSTATS** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a><span data-ttu-id="39f34-109">Membros</span><span class="sxs-lookup"><span data-stu-id="39f34-109">Members</span></span>

<span data-ttu-id="39f34-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="39f34-110">**cbStruct**</span></span>

<span data-ttu-id="39f34-111">O tamanho da estrutura de **JET_THREADSTATS** retornada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="39f34-111">The size of the returned **JET_THREADSTATS** structure, in bytes.</span></span>

<span data-ttu-id="39f34-112">**Observação**  A estrutura de **JET_THREADSTATS** será expandida no futuro para conter mais estatísticas.</span><span class="sxs-lookup"><span data-stu-id="39f34-112">**Note**  The **JET_THREADSTATS** structure will expand in the future to contain more statistics.</span></span> <span data-ttu-id="39f34-113">Novas estatísticas serão adicionadas ao final da estrutura e poderão ser recuperadas com um tamanho de buffer de saída maior.</span><span class="sxs-lookup"><span data-stu-id="39f34-113">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="39f34-114">A presença de estatísticas adicionais pode ser inferida por um valor **cbStruct** maior.</span><span class="sxs-lookup"><span data-stu-id="39f34-114">The presence of additional statistics can be inferred by a larger **cbStruct** value.</span></span>

<span data-ttu-id="39f34-115">**cPageReferenced**</span><span class="sxs-lookup"><span data-stu-id="39f34-115">**cPageReferenced**</span></span>

<span data-ttu-id="39f34-116">O número total de páginas de banco de dados visitadas pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="39f34-116">The total number of database pages visited by the database engine on the current thread.</span></span>

<span data-ttu-id="39f34-117">**cPageRead**</span><span class="sxs-lookup"><span data-stu-id="39f34-117">**cPageRead**</span></span>

<span data-ttu-id="39f34-118">O número total de páginas de banco de dados buscadas do disco pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="39f34-118">The total number of database pages fetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="39f34-119">**cPagePreread**</span><span class="sxs-lookup"><span data-stu-id="39f34-119">**cPagePreread**</span></span>

<span data-ttu-id="39f34-120">O número total de páginas de banco de dados pré-busca do disco pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="39f34-120">The total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="39f34-121">**cPageDirtied**</span><span class="sxs-lookup"><span data-stu-id="39f34-121">**cPageDirtied**</span></span>

<span data-ttu-id="39f34-122">O número total de páginas de banco de dados, sem alterações não gravadas, que foram modificadas pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="39f34-122">The total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="39f34-123">**cPageRedirtied**</span><span class="sxs-lookup"><span data-stu-id="39f34-123">**cPageRedirtied**</span></span>

<span data-ttu-id="39f34-124">O número total de páginas de banco de dados, com alterações não gravadas, que foram modificadas pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="39f34-124">The total number of database pages, with unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="39f34-125">**cLogRecord**</span><span class="sxs-lookup"><span data-stu-id="39f34-125">**cLogRecord**</span></span>

<span data-ttu-id="39f34-126">O número total de registros de log de transações que foram gerados pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="39f34-126">The total number of transaction log records that have been generated by the database engine on the current thread.</span></span>

<span data-ttu-id="39f34-127">**cbLogRecord**</span><span class="sxs-lookup"><span data-stu-id="39f34-127">**cbLogRecord**</span></span>

<span data-ttu-id="39f34-128">O tamanho total em bytes dos registros de log de transações que foram gerados pelo mecanismo de banco de dados no thread atual.</span><span class="sxs-lookup"><span data-stu-id="39f34-128">The total size in bytes of transaction log records that have been generated by the database engine on the current thread.</span></span>

### <a name="requirements"></a><span data-ttu-id="39f34-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39f34-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39f34-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="39f34-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="39f34-131">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="39f34-131">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39f34-132"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="39f34-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="39f34-133">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="39f34-133">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39f34-134"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="39f34-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="39f34-135">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="39f34-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="39f34-136">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="39f34-136">See Also</span></span>

[<span data-ttu-id="39f34-137">JetGetThreadStats</span><span class="sxs-lookup"><span data-stu-id="39f34-137">JetGetThreadStats</span></span>](./jetgetthreadstats-function.md)

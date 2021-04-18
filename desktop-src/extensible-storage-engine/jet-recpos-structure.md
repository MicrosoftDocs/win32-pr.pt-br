---
description: 'Saiba mais sobre: estrutura de JET_RECPOS'
title: Estrutura de JET_RECPOS
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793383"
---
# <a name="jet_recpos-structure"></a><span data-ttu-id="d3bf2-103">Estrutura de JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="d3bf2-103">JET_RECPOS Structure</span></span>


<span data-ttu-id="d3bf2-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d3bf2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recpos-structure"></a><span data-ttu-id="d3bf2-105">Estrutura de JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="d3bf2-105">JET_RECPOS Structure</span></span>

<span data-ttu-id="d3bf2-106">A estrutura de **JET_RECPOS** contém uma coleção de inteiros que representam uma posição fracionária dentro de um índice.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-106">The **JET_RECPOS** structure contains a collection of integers that represent a fractional position within an index.</span></span> <span data-ttu-id="d3bf2-107">**centriesLT** é o número de entradas de índice menor que a chave de índice atual.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-107">**centriesLT** is the number of index entries less than the current index key.</span></span> <span data-ttu-id="d3bf2-108">**centriesInRange** é o número de entradas de índice iguais à chave atual.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-108">**centriesInRange** is the number of index entries equal to the current key.</span></span> <span data-ttu-id="d3bf2-109">**centriesInRange** não tem suporte e sempre é retornado como 1.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-109">**centriesInRange** is not supported and is always returned as 1.</span></span> <span data-ttu-id="d3bf2-110">**centriesTotal** é o número de entradas de índice no índice.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-110">**centriesTotal** is the number of index entries in the index.</span></span> <span data-ttu-id="d3bf2-111">Todos os valores são aproximações sem nenhuma garantia de precisão.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-111">All values are approximations with no guarantee of accuracy.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a><span data-ttu-id="d3bf2-112">Membros</span><span class="sxs-lookup"><span data-stu-id="d3bf2-112">Members</span></span>

<span data-ttu-id="d3bf2-113">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d3bf2-113">**cbStruct**</span></span>

<span data-ttu-id="d3bf2-114">O tamanho da estrutura de [JET_RETINFO](./jet-retinfo-structure.md) , em bytes.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-114">The size of the [JET_RETINFO](./jet-retinfo-structure.md) structure, in bytes.</span></span> <span data-ttu-id="d3bf2-115">Esse valor confirma a presença dos campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-115">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="d3bf2-116">**centriesLT**</span><span class="sxs-lookup"><span data-stu-id="d3bf2-116">**centriesLT**</span></span>

<span data-ttu-id="d3bf2-117">O número aproximado de entradas de índice menores que a chave atual.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-117">The approximate number of index entries less than the current key.</span></span>

<span data-ttu-id="d3bf2-118">**centriesInRange**</span><span class="sxs-lookup"><span data-stu-id="d3bf2-118">**centriesInRange**</span></span>

<span data-ttu-id="d3bf2-119">O número aproximado de entradas de índice iguais à chave atual.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-119">The approximate number of index entries equal to the current key.</span></span> <span data-ttu-id="d3bf2-120">Esse campo é sempre definido como 1, independentemente do número de entradas de índice que são realmente iguais à chave atual.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-120">This field is always set to 1, regardless of the number of index entries that are actually equal to the current key.</span></span>

<span data-ttu-id="d3bf2-121">**centriesTotal**</span><span class="sxs-lookup"><span data-stu-id="d3bf2-121">**centriesTotal**</span></span>

<span data-ttu-id="d3bf2-122">O número aproximado de entradas no índice.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-122">The approximate number of entries in the index.</span></span>

### <a name="requirements"></a><span data-ttu-id="d3bf2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3bf2-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3bf2-124"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d3bf2-124"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d3bf2-125">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-125">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3bf2-126"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d3bf2-126"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d3bf2-127">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-127">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3bf2-128"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d3bf2-128"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d3bf2-129">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d3bf2-129">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d3bf2-130">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d3bf2-130">See Also</span></span>

[<span data-ttu-id="d3bf2-131">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="d3bf2-131">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="d3bf2-132">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="d3bf2-132">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)

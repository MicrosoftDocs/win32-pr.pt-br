---
description: 'Saiba mais sobre: método API. TrySetIndexRange'
title: Método API. TrySetIndexRange
TOCTitle: 'TrySetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trysetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100893
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d175fdfc931d24742d61f962a45e690a5c49c2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663345"
---
# <a name="apitrysetindexrange-method"></a><span data-ttu-id="fc54a-103">Método API. TrySetIndexRange</span><span class="sxs-lookup"><span data-stu-id="fc54a-103">Api.TrySetIndexRange method</span></span>

<span data-ttu-id="fc54a-104">Limita temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando JetMove para aqueles que começam da entrada de índice atual e terminam na entrada de índice que corresponde aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e os critérios de associação especificados.</span><span class="sxs-lookup"><span data-stu-id="fc54a-104">Temporarily limits the set of index entries that the cursor can walk using JetMove to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="fc54a-105">Uma chave de pesquisa deve ter sido construída anteriormente usando JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="fc54a-105">A search key must have been previously constructed using JetMakeKey.</span></span> <span data-ttu-id="fc54a-106">Retorna true se o intervalo de índice não estiver vazio; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="fc54a-106">Returns true if the index range is non-empty, false otherwise.</span></span>

<span data-ttu-id="fc54a-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fc54a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fc54a-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fc54a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fc54a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc54a-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbit
Dim returnValue As Boolean

returnValue = Api.TrySetIndexRange(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="fc54a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc54a-110">Parameters</span></span>

  - <span data-ttu-id="fc54a-111">sesid</span><span class="sxs-lookup"><span data-stu-id="fc54a-111">sesid</span></span>  
    <span data-ttu-id="fc54a-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fc54a-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fc54a-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="fc54a-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc54a-114">TableID</span><span class="sxs-lookup"><span data-stu-id="fc54a-114">tableid</span></span>  
    <span data-ttu-id="fc54a-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fc54a-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fc54a-116">O cursor a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="fc54a-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc54a-117">grbit</span><span class="sxs-lookup"><span data-stu-id="fc54a-117">grbit</span></span>  
    <span data-ttu-id="fc54a-118">Tipo: [Microsoft. ISAM. ESENT. Interop. SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fc54a-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="fc54a-119">Opção de busca.</span><span class="sxs-lookup"><span data-stu-id="fc54a-119">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fc54a-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc54a-120">Return value</span></span>

<span data-ttu-id="fc54a-121">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="fc54a-121">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="fc54a-122">True se a busca foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fc54a-122">True if the seek was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fc54a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc54a-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fc54a-124">Referência</span><span class="sxs-lookup"><span data-stu-id="fc54a-124">Reference</span></span>

[<span data-ttu-id="fc54a-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="fc54a-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fc54a-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="fc54a-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fc54a-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fc54a-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

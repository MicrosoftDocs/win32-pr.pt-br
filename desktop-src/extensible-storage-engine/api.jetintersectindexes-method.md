---
description: 'Saiba mais sobre: método API. JetIntersectIndexes'
title: Método API. JetIntersectIndexes
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bae632f386ef944e79a17813d1cc86451441e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922873"
---
# <a name="apijetintersectindexes-method"></a><span data-ttu-id="1a75a-103">Método API. JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="1a75a-103">Api.JetIntersectIndexes method</span></span>

<span data-ttu-id="1a75a-104">Computa a interseção entre vários conjuntos de entradas de índice de índices secundários diferentes na mesma tabela.</span><span class="sxs-lookup"><span data-stu-id="1a75a-104">Computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="1a75a-105">Essa operação é útil para localizar o conjunto de registros em uma tabela que corresponde a dois ou mais critérios que podem ser expressos usando intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="1a75a-105">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span> <span data-ttu-id="1a75a-106">Consulte também [IntersectIndexes (JET_SESID, \[ \] )](./api.intersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="1a75a-106">Also see [IntersectIndexes(JET_SESID, \[\])](./api.intersectindexes-method.md).</span></span>

<span data-ttu-id="1a75a-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a75a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a75a-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1a75a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a75a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a75a-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1a75a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a75a-110">Parameters</span></span>

  - <span data-ttu-id="1a75a-111">sesid</span><span class="sxs-lookup"><span data-stu-id="1a75a-111">sesid</span></span>  
    <span data-ttu-id="1a75a-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a75a-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1a75a-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="1a75a-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a75a-114">ranges</span><span class="sxs-lookup"><span data-stu-id="1a75a-114">ranges</span></span>  
    <span data-ttu-id="1a75a-115">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="1a75a-115">Type: \[\]</span></span>  
    
    <span data-ttu-id="1a75a-116">Um índice varia para interseção.</span><span class="sxs-lookup"><span data-stu-id="1a75a-116">An the index ranges to intersect.</span></span> <span data-ttu-id="1a75a-117">O tableids nos intervalos deve ter intervalos de índice definidos neles.</span><span class="sxs-lookup"><span data-stu-id="1a75a-117">The tableids in the ranges must have index ranges set on them.</span></span> <span data-ttu-id="1a75a-118">Use [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) para criar um intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="1a75a-118">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a75a-119">numRanges</span><span class="sxs-lookup"><span data-stu-id="1a75a-119">numRanges</span></span>  
    <span data-ttu-id="1a75a-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1a75a-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1a75a-121">O número de intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="1a75a-121">The number of index ranges.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a75a-122">registros da</span><span class="sxs-lookup"><span data-stu-id="1a75a-122">recordlist</span></span>  
    <span data-ttu-id="1a75a-123">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="1a75a-123">Type: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span></span>  
    
    <span data-ttu-id="1a75a-124">Retorna informações sobre a tabela temporária que contém os resultados da interseção.</span><span class="sxs-lookup"><span data-stu-id="1a75a-124">Returns information about the temporary table containing the intersection results.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a75a-125">grbit</span><span class="sxs-lookup"><span data-stu-id="1a75a-125">grbit</span></span>  
    <span data-ttu-id="1a75a-126">Tipo: [Microsoft. ISAM. ESENT. Interop. IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1a75a-126">Type: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1a75a-127">Opções de interseção.</span><span class="sxs-lookup"><span data-stu-id="1a75a-127">Intersection options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a75a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a75a-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a75a-129">Referência</span><span class="sxs-lookup"><span data-stu-id="1a75a-129">Reference</span></span>

[<span data-ttu-id="1a75a-130">Classe de API</span><span class="sxs-lookup"><span data-stu-id="1a75a-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1a75a-131">Membros da API</span><span class="sxs-lookup"><span data-stu-id="1a75a-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1a75a-132">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1a75a-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

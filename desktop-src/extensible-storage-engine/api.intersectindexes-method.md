---
description: 'Saiba mais sobre: método API. IntersectIndexes'
title: Método API. IntersectIndexes
TOCTitle: 'IntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.IntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.intersectindexes(v=EXCHG.10)
ms:contentKeyID: 55107220
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8dfe5784ecd5ab517e183f8eeeb5f79315fe585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501231"
---
# <a name="apiintersectindexes-method"></a><span data-ttu-id="9e565-103">Método API. IntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="9e565-103">Api.IntersectIndexes method</span></span>

<span data-ttu-id="9e565-104">Intersecte um grupo de intervalos de índice e retorne os indicadores dos registros que são encontrados em todos os intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="9e565-104">Intersect a group of index ranges and return the bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="9e565-105">Consulte também [JetIntersectIndexes (JET_SESID, \[ \] , Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="9e565-105">Also see [JetIntersectIndexes(JET_SESID, \[\], Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span></span>

<span data-ttu-id="9e565-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9e565-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9e565-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9e565-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9e565-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e565-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function IntersectIndexes ( _
    sesid As JET_SESID, _
    ParamArray tableids As JET_TABLEID() _
) As IEnumerable(Of Byte())
'Usage
Dim sesid As JET_SESID
Dim tableids As JET_TABLEID()
Dim returnValue As IEnumerable(Of Byte())

returnValue = Api.IntersectIndexes(sesid, _
    tableids)
```

``` csharp
public static IEnumerable<byte[]> IntersectIndexes(
    JET_SESID sesid,
    params JET_TABLEID[] tableids
)
```

#### <a name="parameters"></a><span data-ttu-id="9e565-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e565-109">Parameters</span></span>

  - <span data-ttu-id="9e565-110">sesid</span><span class="sxs-lookup"><span data-stu-id="9e565-110">sesid</span></span>  
    <span data-ttu-id="9e565-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9e565-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9e565-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9e565-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9e565-113">tableids</span><span class="sxs-lookup"><span data-stu-id="9e565-113">tableids</span></span>  
    <span data-ttu-id="9e565-114">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="9e565-114">Type: \[\]</span></span>  
    
    <span data-ttu-id="9e565-115">O tableids a ser usado.</span><span class="sxs-lookup"><span data-stu-id="9e565-115">The tableids to use.</span></span> <span data-ttu-id="9e565-116">Cada TableName deve ser de um índice diferente na mesma tabela e ter um intervalo de índice ativo.</span><span class="sxs-lookup"><span data-stu-id="9e565-116">Each tableid must be from a different index on the same table and have an active index range.</span></span> <span data-ttu-id="9e565-117">Use [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) para criar um intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="9e565-117">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9e565-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e565-118">Return value</span></span>

<span data-ttu-id="9e565-119">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span><span class="sxs-lookup"><span data-stu-id="9e565-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span></span>  
<span data-ttu-id="9e565-120">Os indicadores dos registros que são encontrados em todos os intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="9e565-120">The bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="9e565-121">Os indicadores são retornados na ordem de chave primária.</span><span class="sxs-lookup"><span data-stu-id="9e565-121">The bookmarks are returned in primary key order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9e565-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e565-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9e565-123">Referência</span><span class="sxs-lookup"><span data-stu-id="9e565-123">Reference</span></span>

[<span data-ttu-id="9e565-124">Classe de API</span><span class="sxs-lookup"><span data-stu-id="9e565-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9e565-125">Membros da API</span><span class="sxs-lookup"><span data-stu-id="9e565-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9e565-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9e565-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

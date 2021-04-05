---
description: 'Saiba mais sobre: método API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint64(v=EXCHG.10)
ms:contentKeyID: 55100858
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edd9c8a8495a56e14c655357397c5a693239062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826747"
---
# <a name="apiretrievecolumnasint64-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="539bb-103">Método API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="539bb-103">Api.RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="539bb-104">Recupera um valor de coluna única do registro atual.</span><span class="sxs-lookup"><span data-stu-id="539bb-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="539bb-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="539bb-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="539bb-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="539bb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="539bb-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="539bb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="539bb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="539bb-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Long)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Long)

returnValue = Api.RetrieveColumnAsInt64(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<long> RetrieveColumnAsInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="539bb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="539bb-109">Parameters</span></span>

  - <span data-ttu-id="539bb-110">sesid</span><span class="sxs-lookup"><span data-stu-id="539bb-110">sesid</span></span>  
    <span data-ttu-id="539bb-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="539bb-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="539bb-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="539bb-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="539bb-113">TableID</span><span class="sxs-lookup"><span data-stu-id="539bb-113">tableid</span></span>  
    <span data-ttu-id="539bb-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="539bb-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="539bb-115">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="539bb-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="539bb-116">columnid</span><span class="sxs-lookup"><span data-stu-id="539bb-116">columnid</span></span>  
    <span data-ttu-id="539bb-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="539bb-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="539bb-118">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="539bb-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="539bb-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="539bb-119">Return value</span></span>

<span data-ttu-id="539bb-120">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span><span class="sxs-lookup"><span data-stu-id="539bb-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span></span>  
<span data-ttu-id="539bb-121">Os dados recuperados da coluna como um longo.</span><span class="sxs-lookup"><span data-stu-id="539bb-121">The data retrieved from the column as a long.</span></span> <span data-ttu-id="539bb-122">NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="539bb-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="539bb-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="539bb-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="539bb-124">Referência</span><span class="sxs-lookup"><span data-stu-id="539bb-124">Reference</span></span>

[<span data-ttu-id="539bb-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="539bb-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="539bb-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="539bb-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="539bb-127">Sobrecarga de RetrieveColumnAsInt64</span><span class="sxs-lookup"><span data-stu-id="539bb-127">RetrieveColumnAsInt64 overload</span></span>](./api.retrievecolumnasint64-method.md)

[<span data-ttu-id="539bb-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="539bb-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

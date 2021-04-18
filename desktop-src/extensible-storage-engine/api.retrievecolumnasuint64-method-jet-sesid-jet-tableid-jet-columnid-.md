---
description: 'Saiba mais sobre: método API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint64(v=EXCHG.10)
ms:contentKeyID: 55100864
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ef62c1faa4a7060996d587a92838bdced560350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751162"
---
# <a name="apiretrievecolumnasuint64-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="dc8a5-103">Método API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="dc8a5-103">Api.RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="dc8a5-104">Recupera um valor de coluna UInt64 do registro atual.</span><span class="sxs-lookup"><span data-stu-id="dc8a5-104">Retrieves a uint64 column value from the current record.</span></span> <span data-ttu-id="dc8a5-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="dc8a5-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="dc8a5-106">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="dc8a5-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="dc8a5-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dc8a5-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dc8a5-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dc8a5-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dc8a5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc8a5-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of ULong)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of ULong)

returnValue = Api.RetrieveColumnAsUInt64(sesid, _
    tableid, columnid)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ulong> RetrieveColumnAsUInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="dc8a5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc8a5-110">Parameters</span></span>

  - <span data-ttu-id="dc8a5-111">sesid</span><span class="sxs-lookup"><span data-stu-id="dc8a5-111">sesid</span></span>  
    <span data-ttu-id="dc8a5-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dc8a5-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dc8a5-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="dc8a5-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="dc8a5-114">TableID</span><span class="sxs-lookup"><span data-stu-id="dc8a5-114">tableid</span></span>  
    <span data-ttu-id="dc8a5-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dc8a5-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="dc8a5-116">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="dc8a5-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="dc8a5-117">columnid</span><span class="sxs-lookup"><span data-stu-id="dc8a5-117">columnid</span></span>  
    <span data-ttu-id="dc8a5-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dc8a5-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="dc8a5-119">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="dc8a5-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="dc8a5-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc8a5-120">Return value</span></span>

<span data-ttu-id="dc8a5-121">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span><span class="sxs-lookup"><span data-stu-id="dc8a5-121">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span></span>  
<span data-ttu-id="dc8a5-122">Os dados recuperados da coluna como um UInt64.</span><span class="sxs-lookup"><span data-stu-id="dc8a5-122">The data retrieved from the column as an UInt64.</span></span> <span data-ttu-id="dc8a5-123">NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="dc8a5-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dc8a5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc8a5-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dc8a5-125">Referência</span><span class="sxs-lookup"><span data-stu-id="dc8a5-125">Reference</span></span>

[<span data-ttu-id="dc8a5-126">Classe de API</span><span class="sxs-lookup"><span data-stu-id="dc8a5-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dc8a5-127">Membros da API</span><span class="sxs-lookup"><span data-stu-id="dc8a5-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dc8a5-128">Sobrecarga de RetrieveColumnAsUInt64</span><span class="sxs-lookup"><span data-stu-id="dc8a5-128">RetrieveColumnAsUInt64 overload</span></span>](./api.retrievecolumnasuint64-method.md)

[<span data-ttu-id="dc8a5-129">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dc8a5-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

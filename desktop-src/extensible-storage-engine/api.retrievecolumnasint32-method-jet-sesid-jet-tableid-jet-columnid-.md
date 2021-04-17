---
description: 'Saiba mais sobre: método API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint32(v=EXCHG.10)
ms:contentKeyID: 55100894
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c2e6bb69ca1b278cbb930de7c20611645283ee59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785076"
---
# <a name="apiretrievecolumnasint32-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="6d2d7-103">Método API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="6d2d7-103">Api.RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="6d2d7-104">Recupera um valor de coluna única do registro atual.</span><span class="sxs-lookup"><span data-stu-id="6d2d7-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="6d2d7-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="6d2d7-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="6d2d7-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6d2d7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6d2d7-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6d2d7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d2d7-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnAsInt32(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnAsInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="6d2d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d2d7-109">Parameters</span></span>

  - <span data-ttu-id="6d2d7-110">sesid</span><span class="sxs-lookup"><span data-stu-id="6d2d7-110">sesid</span></span>  
    <span data-ttu-id="6d2d7-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6d2d7-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6d2d7-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6d2d7-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d2d7-113">TableID</span><span class="sxs-lookup"><span data-stu-id="6d2d7-113">tableid</span></span>  
    <span data-ttu-id="6d2d7-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6d2d7-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6d2d7-115">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="6d2d7-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d2d7-116">columnid</span><span class="sxs-lookup"><span data-stu-id="6d2d7-116">columnid</span></span>  
    <span data-ttu-id="6d2d7-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6d2d7-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6d2d7-118">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="6d2d7-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6d2d7-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d2d7-119">Return value</span></span>

<span data-ttu-id="6d2d7-120">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="6d2d7-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="6d2d7-121">Os dados recuperados da coluna como um int. NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="6d2d7-121">The data retrieved from the column as an int. Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6d2d7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d2d7-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6d2d7-123">Referência</span><span class="sxs-lookup"><span data-stu-id="6d2d7-123">Reference</span></span>

[<span data-ttu-id="6d2d7-124">Classe de API</span><span class="sxs-lookup"><span data-stu-id="6d2d7-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6d2d7-125">Membros da API</span><span class="sxs-lookup"><span data-stu-id="6d2d7-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6d2d7-126">Sobrecarga de RetrieveColumnAsInt32</span><span class="sxs-lookup"><span data-stu-id="6d2d7-126">RetrieveColumnAsInt32 overload</span></span>](./api.retrievecolumnasint32-method.md)

[<span data-ttu-id="6d2d7-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6d2d7-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

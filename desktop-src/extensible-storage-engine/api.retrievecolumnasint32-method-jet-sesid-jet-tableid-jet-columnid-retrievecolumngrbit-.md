---
description: 'Saiba mais sobre: método API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint32(v=EXCHG.10)
ms:contentKeyID: 55100859
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
ms.openlocfilehash: 5e9f963d298610fb36f6b1f9c9ff3a0bfbfa2501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501222"
---
# <a name="apiretrievecolumnasint32-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="fc6d4-103">Método API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="fc6d4-103">Api.RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="fc6d4-104">Recupera um valor de coluna Int32 do registro atual.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-104">Retrieves an int32 column value from the current record.</span></span> <span data-ttu-id="fc6d4-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="fc6d4-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fc6d4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fc6d4-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fc6d4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6d4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc6d4-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnAsInt32(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnAsInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="fc6d4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc6d4-109">Parameters</span></span>

  - <span data-ttu-id="fc6d4-110">sesid</span><span class="sxs-lookup"><span data-stu-id="fc6d4-110">sesid</span></span>  
    <span data-ttu-id="fc6d4-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fc6d4-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fc6d4-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc6d4-113">TableID</span><span class="sxs-lookup"><span data-stu-id="fc6d4-113">tableid</span></span>  
    <span data-ttu-id="fc6d4-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fc6d4-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fc6d4-115">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc6d4-116">columnid</span><span class="sxs-lookup"><span data-stu-id="fc6d4-116">columnid</span></span>  
    <span data-ttu-id="fc6d4-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fc6d4-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="fc6d4-118">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc6d4-119">grbit</span><span class="sxs-lookup"><span data-stu-id="fc6d4-119">grbit</span></span>  
    <span data-ttu-id="fc6d4-120">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fc6d4-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="fc6d4-121">Opções de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fc6d4-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc6d4-122">Return value</span></span>

<span data-ttu-id="fc6d4-123">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="fc6d4-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="fc6d4-124">Os dados recuperados da coluna como um int. NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-124">The data retrieved from the column as an int. Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fc6d4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc6d4-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fc6d4-126">Referência</span><span class="sxs-lookup"><span data-stu-id="fc6d4-126">Reference</span></span>

[<span data-ttu-id="fc6d4-127">Classe de API</span><span class="sxs-lookup"><span data-stu-id="fc6d4-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fc6d4-128">Membros da API</span><span class="sxs-lookup"><span data-stu-id="fc6d4-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fc6d4-129">Sobrecarga de RetrieveColumnAsInt32</span><span class="sxs-lookup"><span data-stu-id="fc6d4-129">RetrieveColumnAsInt32 overload</span></span>](./api.retrievecolumnasint32-method.md)

[<span data-ttu-id="fc6d4-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fc6d4-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

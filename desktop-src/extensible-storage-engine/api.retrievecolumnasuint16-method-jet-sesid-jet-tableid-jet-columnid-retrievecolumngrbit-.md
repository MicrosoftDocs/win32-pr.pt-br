---
description: 'Saiba mais sobre: método API. RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint16(v=EXCHG.10)
ms:contentKeyID: 55100902
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca82b1c2f5a9a1be7fa0ddbd5082e55820263a10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501218"
---
# <a name="apiretrievecolumnasuint16-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="db730-103">Método API. RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="db730-103">Api.RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="db730-104">Recupera um valor de coluna UInt16 do registro atual.</span><span class="sxs-lookup"><span data-stu-id="db730-104">Retrieves a uint16 column value from the current record.</span></span> <span data-ttu-id="db730-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="db730-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="db730-106">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="db730-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="db730-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db730-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db730-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="db730-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db730-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db730-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt16 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of UShort)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of UShort)

returnValue = Api.RetrieveColumnAsUInt16(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ushort> RetrieveColumnAsUInt16(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="db730-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db730-110">Parameters</span></span>

  - <span data-ttu-id="db730-111">sesid</span><span class="sxs-lookup"><span data-stu-id="db730-111">sesid</span></span>  
    <span data-ttu-id="db730-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db730-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="db730-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="db730-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="db730-114">TableID</span><span class="sxs-lookup"><span data-stu-id="db730-114">tableid</span></span>  
    <span data-ttu-id="db730-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db730-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="db730-116">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="db730-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="db730-117">columnid</span><span class="sxs-lookup"><span data-stu-id="db730-117">columnid</span></span>  
    <span data-ttu-id="db730-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db730-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="db730-119">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="db730-119">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="db730-120">grbit</span><span class="sxs-lookup"><span data-stu-id="db730-120">grbit</span></span>  
    <span data-ttu-id="db730-121">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="db730-121">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="db730-122">Opções de recuperação.</span><span class="sxs-lookup"><span data-stu-id="db730-122">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="db730-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db730-123">Return value</span></span>

<span data-ttu-id="db730-124">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span><span class="sxs-lookup"><span data-stu-id="db730-124">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span></span>  
<span data-ttu-id="db730-125">Os dados recuperados da coluna como UInt16.</span><span class="sxs-lookup"><span data-stu-id="db730-125">The data retrieved from the column as an UInt16.</span></span> <span data-ttu-id="db730-126">NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="db730-126">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="db730-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="db730-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db730-128">Referência</span><span class="sxs-lookup"><span data-stu-id="db730-128">Reference</span></span>

[<span data-ttu-id="db730-129">Classe de API</span><span class="sxs-lookup"><span data-stu-id="db730-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="db730-130">Membros da API</span><span class="sxs-lookup"><span data-stu-id="db730-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="db730-131">Sobrecarga de RetrieveColumnAsUInt16</span><span class="sxs-lookup"><span data-stu-id="db730-131">RetrieveColumnAsUInt16 overload</span></span>](./api.retrievecolumnasuint16-method.md)

[<span data-ttu-id="db730-132">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="db730-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

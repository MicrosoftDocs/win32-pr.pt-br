---
description: 'Saiba mais sobre: método API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint32(v=EXCHG.10)
ms:contentKeyID: 55100866
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17babe091d4ae6a2c0219d97b240ee3198260147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781212"
---
# <a name="apiretrievecolumnasuint32-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="5f178-103">Método API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="5f178-103">Api.RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="5f178-104">Recupera um valor de coluna UInt32 do registro atual.</span><span class="sxs-lookup"><span data-stu-id="5f178-104">Retrieves a uint32 column value from the current record.</span></span> <span data-ttu-id="5f178-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="5f178-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="5f178-106">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="5f178-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="5f178-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5f178-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5f178-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5f178-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5f178-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f178-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of UInteger)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of UInteger)

returnValue = Api.RetrieveColumnAsUInt32(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<uint> RetrieveColumnAsUInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5f178-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f178-110">Parameters</span></span>

  - <span data-ttu-id="5f178-111">sesid</span><span class="sxs-lookup"><span data-stu-id="5f178-111">sesid</span></span>  
    <span data-ttu-id="5f178-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5f178-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5f178-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5f178-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5f178-114">TableID</span><span class="sxs-lookup"><span data-stu-id="5f178-114">tableid</span></span>  
    <span data-ttu-id="5f178-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5f178-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5f178-116">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="5f178-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="5f178-117">columnid</span><span class="sxs-lookup"><span data-stu-id="5f178-117">columnid</span></span>  
    <span data-ttu-id="5f178-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5f178-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="5f178-119">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="5f178-119">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="5f178-120">grbit</span><span class="sxs-lookup"><span data-stu-id="5f178-120">grbit</span></span>  
    <span data-ttu-id="5f178-121">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5f178-121">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5f178-122">Opções de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5f178-122">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5f178-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f178-123">Return value</span></span>

<span data-ttu-id="5f178-124">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span><span class="sxs-lookup"><span data-stu-id="5f178-124">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span></span>  
<span data-ttu-id="5f178-125">Os dados recuperados da coluna como um UInt32.</span><span class="sxs-lookup"><span data-stu-id="5f178-125">The data retrieved from the column as an UInt32.</span></span> <span data-ttu-id="5f178-126">NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="5f178-126">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5f178-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f178-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5f178-128">Referência</span><span class="sxs-lookup"><span data-stu-id="5f178-128">Reference</span></span>

[<span data-ttu-id="5f178-129">Classe de API</span><span class="sxs-lookup"><span data-stu-id="5f178-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5f178-130">Membros da API</span><span class="sxs-lookup"><span data-stu-id="5f178-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5f178-131">Sobrecarga de RetrieveColumnAsUInt32</span><span class="sxs-lookup"><span data-stu-id="5f178-131">RetrieveColumnAsUInt32 overload</span></span>](./api.retrievecolumnasuint32-method.md)

[<span data-ttu-id="5f178-132">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5f178-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

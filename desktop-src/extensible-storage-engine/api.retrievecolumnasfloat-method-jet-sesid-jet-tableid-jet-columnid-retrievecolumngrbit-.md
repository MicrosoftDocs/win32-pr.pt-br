---
description: 'Saiba mais sobre: método API. RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsFloat method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsFloat(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasfloat(v=EXCHG.10)
ms:contentKeyID: 55100885
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsFloat
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dbf11f476325e87a07a1b61179ae5ce3b3d5709e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812116"
---
# <a name="apiretrievecolumnasfloat-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="4078c-103">Método API. RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="4078c-103">Api.RetrieveColumnAsFloat method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="4078c-104">Recupera um valor de coluna float do registro atual.</span><span class="sxs-lookup"><span data-stu-id="4078c-104">Retrieves a float column value from the current record.</span></span> <span data-ttu-id="4078c-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="4078c-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="4078c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4078c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4078c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4078c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4078c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4078c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsFloat ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Single)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Single)

returnValue = Api.RetrieveColumnAsFloat(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<float> RetrieveColumnAsFloat(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4078c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4078c-109">Parameters</span></span>

  - <span data-ttu-id="4078c-110">sesid</span><span class="sxs-lookup"><span data-stu-id="4078c-110">sesid</span></span>  
    <span data-ttu-id="4078c-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4078c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4078c-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4078c-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4078c-113">TableID</span><span class="sxs-lookup"><span data-stu-id="4078c-113">tableid</span></span>  
    <span data-ttu-id="4078c-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4078c-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4078c-115">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="4078c-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="4078c-116">columnid</span><span class="sxs-lookup"><span data-stu-id="4078c-116">columnid</span></span>  
    <span data-ttu-id="4078c-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4078c-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4078c-118">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="4078c-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="4078c-119">grbit</span><span class="sxs-lookup"><span data-stu-id="4078c-119">grbit</span></span>  
    <span data-ttu-id="4078c-120">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4078c-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4078c-121">Opções de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4078c-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4078c-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4078c-122">Return value</span></span>

<span data-ttu-id="4078c-123">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Single](/dotnet/api/system.single)\></span><span class="sxs-lookup"><span data-stu-id="4078c-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Single](/dotnet/api/system.single)\></span></span>  
<span data-ttu-id="4078c-124">Os dados recuperados da coluna como um float.</span><span class="sxs-lookup"><span data-stu-id="4078c-124">The data retrieved from the column as a float.</span></span> <span data-ttu-id="4078c-125">NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="4078c-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4078c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4078c-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4078c-127">Referência</span><span class="sxs-lookup"><span data-stu-id="4078c-127">Reference</span></span>

[<span data-ttu-id="4078c-128">Classe de API</span><span class="sxs-lookup"><span data-stu-id="4078c-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4078c-129">Membros da API</span><span class="sxs-lookup"><span data-stu-id="4078c-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4078c-130">Sobrecarga de RetrieveColumnAsFloat</span><span class="sxs-lookup"><span data-stu-id="4078c-130">RetrieveColumnAsFloat overload</span></span>](./api.retrievecolumnasfloat-method.md)

[<span data-ttu-id="4078c-131">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4078c-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

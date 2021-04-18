---
description: 'Saiba mais sobre: método API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.deserializeobjectfromcolumn(v=EXCHG.10)
ms:contentKeyID: 55100669
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe2bb9757216dc4b0a671ae9d5da6cdf4bd5eb7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763133"
---
# <a name="apideserializeobjectfromcolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="847c2-103">Método API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="847c2-103">Api.DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="847c2-104">Desserializar um objeto de uma coluna.</span><span class="sxs-lookup"><span data-stu-id="847c2-104">Deserialize an object from a column.</span></span>

<span data-ttu-id="847c2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="847c2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="847c2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="847c2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="847c2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="847c2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function DeserializeObjectFromColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Object
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Object

returnValue = Api.DeserializeObjectFromColumn(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Object DeserializeObjectFromColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="847c2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="847c2-108">Parameters</span></span>

  - <span data-ttu-id="847c2-109">sesid</span><span class="sxs-lookup"><span data-stu-id="847c2-109">sesid</span></span>  
    <span data-ttu-id="847c2-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="847c2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="847c2-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="847c2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="847c2-112">TableID</span><span class="sxs-lookup"><span data-stu-id="847c2-112">tableid</span></span>  
    <span data-ttu-id="847c2-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="847c2-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="847c2-114">A tabela da qual ler.</span><span class="sxs-lookup"><span data-stu-id="847c2-114">The table to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="847c2-115">columnid</span><span class="sxs-lookup"><span data-stu-id="847c2-115">columnid</span></span>  
    <span data-ttu-id="847c2-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="847c2-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="847c2-117">A coluna da qual ler.</span><span class="sxs-lookup"><span data-stu-id="847c2-117">The column to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="847c2-118">grbit</span><span class="sxs-lookup"><span data-stu-id="847c2-118">grbit</span></span>  
    <span data-ttu-id="847c2-119">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="847c2-119">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="847c2-120">As opções de recuperação a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="847c2-120">The retrieval options to use.</span></span>

#### <a name="return-value"></a><span data-ttu-id="847c2-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="847c2-121">Return value</span></span>

<span data-ttu-id="847c2-122">Tipo: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="847c2-122">Type: [System.Object](/dotnet/api/system.object)</span></span>  
<span data-ttu-id="847c2-123">O objeto desserializado.</span><span class="sxs-lookup"><span data-stu-id="847c2-123">The deserialized object.</span></span> <span data-ttu-id="847c2-124">NULL se a coluna fosse nula.</span><span class="sxs-lookup"><span data-stu-id="847c2-124">Null if the column was null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="847c2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="847c2-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="847c2-126">Referência</span><span class="sxs-lookup"><span data-stu-id="847c2-126">Reference</span></span>

[<span data-ttu-id="847c2-127">Classe de API</span><span class="sxs-lookup"><span data-stu-id="847c2-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="847c2-128">Membros da API</span><span class="sxs-lookup"><span data-stu-id="847c2-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="847c2-129">Sobrecarga de DeserializeObjectFromColumn</span><span class="sxs-lookup"><span data-stu-id="847c2-129">DeserializeObjectFromColumn overload</span></span>](./api.deserializeobjectfromcolumn-method.md)

[<span data-ttu-id="847c2-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="847c2-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

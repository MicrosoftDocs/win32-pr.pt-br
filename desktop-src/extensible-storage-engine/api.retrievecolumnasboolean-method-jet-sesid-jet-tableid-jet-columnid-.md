---
description: 'Saiba mais sobre: método API. RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsBoolean method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsBoolean(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasboolean(v=EXCHG.10)
ms:contentKeyID: 55100837
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsBoolean
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a2f7f38841248910bd23dd15b6cec06a638640d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501227"
---
# <a name="apiretrievecolumnasboolean-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="75f74-103">Método API. RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="75f74-103">Api.RetrieveColumnAsBoolean method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="75f74-104">Recupera um valor de coluna booliana do registro atual.</span><span class="sxs-lookup"><span data-stu-id="75f74-104">Retrieves a boolean column value from the current record.</span></span> <span data-ttu-id="75f74-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="75f74-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="75f74-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75f74-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75f74-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="75f74-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75f74-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75f74-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsBoolean ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Boolean)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Boolean)

returnValue = Api.RetrieveColumnAsBoolean(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<bool> RetrieveColumnAsBoolean(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="75f74-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75f74-109">Parameters</span></span>

  - <span data-ttu-id="75f74-110">sesid</span><span class="sxs-lookup"><span data-stu-id="75f74-110">sesid</span></span>  
    <span data-ttu-id="75f74-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="75f74-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="75f74-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="75f74-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="75f74-113">TableID</span><span class="sxs-lookup"><span data-stu-id="75f74-113">tableid</span></span>  
    <span data-ttu-id="75f74-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="75f74-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="75f74-115">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="75f74-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="75f74-116">columnid</span><span class="sxs-lookup"><span data-stu-id="75f74-116">columnid</span></span>  
    <span data-ttu-id="75f74-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="75f74-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="75f74-118">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="75f74-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="75f74-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75f74-119">Return value</span></span>

<span data-ttu-id="75f74-120">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Boolean](/dotnet/api/system.boolean)\></span><span class="sxs-lookup"><span data-stu-id="75f74-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Boolean](/dotnet/api/system.boolean)\></span></span>  
<span data-ttu-id="75f74-121">Os dados recuperados da coluna como um booliano.</span><span class="sxs-lookup"><span data-stu-id="75f74-121">The data retrieved from the column as a boolean.</span></span> <span data-ttu-id="75f74-122">NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="75f74-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="75f74-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="75f74-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75f74-124">Referência</span><span class="sxs-lookup"><span data-stu-id="75f74-124">Reference</span></span>

[<span data-ttu-id="75f74-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="75f74-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="75f74-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="75f74-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="75f74-127">Sobrecarga de RetrieveColumnAsBoolean</span><span class="sxs-lookup"><span data-stu-id="75f74-127">RetrieveColumnAsBoolean overload</span></span>](./api.retrievecolumnasboolean-method.md)

[<span data-ttu-id="75f74-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="75f74-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

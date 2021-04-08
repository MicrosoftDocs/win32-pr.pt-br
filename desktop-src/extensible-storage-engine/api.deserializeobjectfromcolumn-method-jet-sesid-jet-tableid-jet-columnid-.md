---
description: 'Saiba mais sobre: método API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.deserializeobjectfromcolumn(v=EXCHG.10)
ms:contentKeyID: 55100688
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
ms.openlocfilehash: e9ec3ca1f505c9d768e54b284caf05b335934451
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826753"
---
# <a name="apideserializeobjectfromcolumn-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="35969-103">Método API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="35969-103">Api.DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="35969-104">Desserializar um objeto de uma coluna.</span><span class="sxs-lookup"><span data-stu-id="35969-104">Deserialize an object from a column.</span></span>

<span data-ttu-id="35969-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="35969-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="35969-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="35969-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="35969-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35969-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function DeserializeObjectFromColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Object
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Object

returnValue = Api.DeserializeObjectFromColumn(sesid, _
    tableid, columnid)
```

``` csharp
public static Object DeserializeObjectFromColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="35969-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35969-108">Parameters</span></span>

  - <span data-ttu-id="35969-109">sesid</span><span class="sxs-lookup"><span data-stu-id="35969-109">sesid</span></span>  
    <span data-ttu-id="35969-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="35969-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="35969-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="35969-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="35969-112">TableID</span><span class="sxs-lookup"><span data-stu-id="35969-112">tableid</span></span>  
    <span data-ttu-id="35969-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="35969-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="35969-114">A tabela da qual ler.</span><span class="sxs-lookup"><span data-stu-id="35969-114">The table to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="35969-115">columnid</span><span class="sxs-lookup"><span data-stu-id="35969-115">columnid</span></span>  
    <span data-ttu-id="35969-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="35969-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="35969-117">A coluna da qual ler.</span><span class="sxs-lookup"><span data-stu-id="35969-117">The column to read from.</span></span>

#### <a name="return-value"></a><span data-ttu-id="35969-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35969-118">Return value</span></span>

<span data-ttu-id="35969-119">Tipo: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="35969-119">Type: [System.Object](/dotnet/api/system.object)</span></span>  
<span data-ttu-id="35969-120">O objeto desserializado.</span><span class="sxs-lookup"><span data-stu-id="35969-120">The deserialized object.</span></span> <span data-ttu-id="35969-121">NULL se a coluna fosse nula.</span><span class="sxs-lookup"><span data-stu-id="35969-121">Null if the column was null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="35969-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="35969-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="35969-123">Referência</span><span class="sxs-lookup"><span data-stu-id="35969-123">Reference</span></span>

[<span data-ttu-id="35969-124">Classe de API</span><span class="sxs-lookup"><span data-stu-id="35969-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="35969-125">Membros da API</span><span class="sxs-lookup"><span data-stu-id="35969-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="35969-126">Sobrecarga de DeserializeObjectFromColumn</span><span class="sxs-lookup"><span data-stu-id="35969-126">DeserializeObjectFromColumn overload</span></span>](./api.deserializeobjectfromcolumn-method.md)

[<span data-ttu-id="35969-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="35969-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

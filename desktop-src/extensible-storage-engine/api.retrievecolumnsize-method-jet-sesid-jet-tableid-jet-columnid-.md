---
description: 'Saiba mais sobre: método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100868
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f75ce51e942cfde7fddc4f9ec0154feae985e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781140"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="444f5-103">Método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="444f5-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="444f5-104">Recupera o tamanho de um valor de coluna única do registro atual.</span><span class="sxs-lookup"><span data-stu-id="444f5-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="444f5-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="444f5-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="444f5-106">Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor.</span><span class="sxs-lookup"><span data-stu-id="444f5-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="444f5-107">Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="444f5-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="444f5-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="444f5-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="444f5-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="444f5-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="444f5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="444f5-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="444f5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="444f5-111">Parameters</span></span>

  - <span data-ttu-id="444f5-112">sesid</span><span class="sxs-lookup"><span data-stu-id="444f5-112">sesid</span></span>  
    <span data-ttu-id="444f5-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="444f5-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="444f5-114">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="444f5-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="444f5-115">TableID</span><span class="sxs-lookup"><span data-stu-id="444f5-115">tableid</span></span>  
    <span data-ttu-id="444f5-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="444f5-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="444f5-117">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="444f5-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="444f5-118">columnid</span><span class="sxs-lookup"><span data-stu-id="444f5-118">columnid</span></span>  
    <span data-ttu-id="444f5-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="444f5-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="444f5-120">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="444f5-120">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="444f5-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="444f5-121">Return value</span></span>

<span data-ttu-id="444f5-122">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="444f5-122">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="444f5-123">O tamanho da coluna.</span><span class="sxs-lookup"><span data-stu-id="444f5-123">The size of the column.</span></span> <span data-ttu-id="444f5-124">0 se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="444f5-124">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="444f5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="444f5-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="444f5-126">Referência</span><span class="sxs-lookup"><span data-stu-id="444f5-126">Reference</span></span>

[<span data-ttu-id="444f5-127">Classe de API</span><span class="sxs-lookup"><span data-stu-id="444f5-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="444f5-128">Membros da API</span><span class="sxs-lookup"><span data-stu-id="444f5-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="444f5-129">Sobrecarga de RetrieveColumnSize</span><span class="sxs-lookup"><span data-stu-id="444f5-129">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="444f5-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="444f5-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Saiba mais sobre: método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100912
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
ms.openlocfilehash: afd09ecca0362487d6c8e78f8e7c8d943f2f3269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920644"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid-int32-retrievecolumngrbit"></a><span data-ttu-id="60b7f-103">Método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="60b7f-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="60b7f-104">Recupera o tamanho de um valor de coluna única do registro atual.</span><span class="sxs-lookup"><span data-stu-id="60b7f-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="60b7f-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="60b7f-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="60b7f-106">Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor.</span><span class="sxs-lookup"><span data-stu-id="60b7f-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="60b7f-107">Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="60b7f-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="60b7f-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="60b7f-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="60b7f-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="60b7f-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="60b7f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60b7f-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    itagSequence As Integer, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim itagSequence As Integer
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid, itagSequence, _
    grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int itagSequence,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="60b7f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60b7f-111">Parameters</span></span>

  - <span data-ttu-id="60b7f-112">sesid</span><span class="sxs-lookup"><span data-stu-id="60b7f-112">sesid</span></span>  
    <span data-ttu-id="60b7f-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="60b7f-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="60b7f-114">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="60b7f-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="60b7f-115">TableID</span><span class="sxs-lookup"><span data-stu-id="60b7f-115">tableid</span></span>  
    <span data-ttu-id="60b7f-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="60b7f-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="60b7f-117">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="60b7f-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="60b7f-118">columnid</span><span class="sxs-lookup"><span data-stu-id="60b7f-118">columnid</span></span>  
    <span data-ttu-id="60b7f-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="60b7f-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="60b7f-120">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="60b7f-120">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="60b7f-121">itagSequence</span><span class="sxs-lookup"><span data-stu-id="60b7f-121">itagSequence</span></span>  
    <span data-ttu-id="60b7f-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="60b7f-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="60b7f-123">O número de sequência do valor em uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="60b7f-123">The sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="60b7f-124">A matriz de valores é baseada em um.</span><span class="sxs-lookup"><span data-stu-id="60b7f-124">The array of values is one-based.</span></span> <span data-ttu-id="60b7f-125">O primeiro valor é Sequence 1, e não 0.</span><span class="sxs-lookup"><span data-stu-id="60b7f-125">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="60b7f-126">Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como itagSequence.</span><span class="sxs-lookup"><span data-stu-id="60b7f-126">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<!-- end list -->

  - <span data-ttu-id="60b7f-127">grbit</span><span class="sxs-lookup"><span data-stu-id="60b7f-127">grbit</span></span>  
    <span data-ttu-id="60b7f-128">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="60b7f-128">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="60b7f-129">Recuperar opções de coluna.</span><span class="sxs-lookup"><span data-stu-id="60b7f-129">Retrieve column options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="60b7f-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60b7f-130">Return value</span></span>

<span data-ttu-id="60b7f-131">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="60b7f-131">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="60b7f-132">O tamanho da coluna.</span><span class="sxs-lookup"><span data-stu-id="60b7f-132">The size of the column.</span></span> <span data-ttu-id="60b7f-133">0 se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="60b7f-133">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="60b7f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="60b7f-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="60b7f-135">Referência</span><span class="sxs-lookup"><span data-stu-id="60b7f-135">Reference</span></span>

[<span data-ttu-id="60b7f-136">Classe de API</span><span class="sxs-lookup"><span data-stu-id="60b7f-136">Api class</span></span>](./api-class.md)

[<span data-ttu-id="60b7f-137">Membros da API</span><span class="sxs-lookup"><span data-stu-id="60b7f-137">Api members</span></span>](./api-members.md)

[<span data-ttu-id="60b7f-138">Sobrecarga de RetrieveColumnSize</span><span class="sxs-lookup"><span data-stu-id="60b7f-138">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="60b7f-139">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="60b7f-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

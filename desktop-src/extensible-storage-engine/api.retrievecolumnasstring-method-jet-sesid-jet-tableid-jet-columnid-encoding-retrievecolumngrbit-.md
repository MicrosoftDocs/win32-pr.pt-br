---
description: 'Saiba mais sobre: método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificação, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificação, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100862
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2008726577bac37e129a887af2d8b1747323c81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763900"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding-retrievecolumngrbit"></a><span data-ttu-id="7a868-103">Método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificação, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="7a868-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="7a868-104">Recupera um valor de coluna de cadeia de caracteres do registro atual.</span><span class="sxs-lookup"><span data-stu-id="7a868-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="7a868-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="7a868-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="7a868-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a868-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7a868-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a868-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a868-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a868-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding, _
    grbit As RetrieveColumnGrbit _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim grbit As RetrieveColumnGrbit
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding, grbit)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7a868-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a868-109">Parameters</span></span>

  - <span data-ttu-id="7a868-110">sesid</span><span class="sxs-lookup"><span data-stu-id="7a868-110">sesid</span></span>  
    <span data-ttu-id="7a868-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7a868-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7a868-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7a868-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a868-113">TableID</span><span class="sxs-lookup"><span data-stu-id="7a868-113">tableid</span></span>  
    <span data-ttu-id="7a868-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7a868-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7a868-115">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="7a868-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a868-116">columnid</span><span class="sxs-lookup"><span data-stu-id="7a868-116">columnid</span></span>  
    <span data-ttu-id="7a868-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7a868-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="7a868-118">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="7a868-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a868-119">codificando</span><span class="sxs-lookup"><span data-stu-id="7a868-119">encoding</span></span>  
    <span data-ttu-id="7a868-120">Tipo: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="7a868-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="7a868-121">A codificação de cadeia de caracteres a ser usada ao converter dados.</span><span class="sxs-lookup"><span data-stu-id="7a868-121">The string encoding to use when converting data.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a868-122">grbit</span><span class="sxs-lookup"><span data-stu-id="7a868-122">grbit</span></span>  
    <span data-ttu-id="7a868-123">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7a868-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7a868-124">Opções de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7a868-124">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7a868-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a868-125">Return value</span></span>

<span data-ttu-id="7a868-126">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7a868-126">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="7a868-127">Os dados recuperados da coluna como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7a868-127">The data retrieved from the column as a string.</span></span> <span data-ttu-id="7a868-128">NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="7a868-128">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7a868-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a868-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a868-130">Referência</span><span class="sxs-lookup"><span data-stu-id="7a868-130">Reference</span></span>

[<span data-ttu-id="7a868-131">Classe de API</span><span class="sxs-lookup"><span data-stu-id="7a868-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7a868-132">Membros da API</span><span class="sxs-lookup"><span data-stu-id="7a868-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7a868-133">Sobrecarga de RetrieveColumnAsString</span><span class="sxs-lookup"><span data-stu-id="7a868-133">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="7a868-134">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7a868-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

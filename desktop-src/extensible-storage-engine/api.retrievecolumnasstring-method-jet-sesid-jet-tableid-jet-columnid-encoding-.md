---
description: 'Saiba mais sobre: método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificação)'
title: Método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificação)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100899
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d7ec3bac73f5b82f82d2762a34084de25b63f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761226"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding"></a><span data-ttu-id="ff35c-103">Método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificação)</span><span class="sxs-lookup"><span data-stu-id="ff35c-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)</span></span>

<span data-ttu-id="ff35c-104">Recupera um valor de coluna de cadeia de caracteres do registro atual.</span><span class="sxs-lookup"><span data-stu-id="ff35c-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="ff35c-105">O registro é aquele associado à entrada de índice na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="ff35c-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="ff35c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ff35c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ff35c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ff35c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ff35c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff35c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding
)
```

#### <a name="parameters"></a><span data-ttu-id="ff35c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff35c-109">Parameters</span></span>

  - <span data-ttu-id="ff35c-110">sesid</span><span class="sxs-lookup"><span data-stu-id="ff35c-110">sesid</span></span>  
    <span data-ttu-id="ff35c-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff35c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ff35c-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="ff35c-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff35c-113">TableID</span><span class="sxs-lookup"><span data-stu-id="ff35c-113">tableid</span></span>  
    <span data-ttu-id="ff35c-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff35c-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ff35c-115">O cursor do qual recuperar a coluna.</span><span class="sxs-lookup"><span data-stu-id="ff35c-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff35c-116">columnid</span><span class="sxs-lookup"><span data-stu-id="ff35c-116">columnid</span></span>  
    <span data-ttu-id="ff35c-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff35c-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ff35c-118">O columnid a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="ff35c-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff35c-119">codificando</span><span class="sxs-lookup"><span data-stu-id="ff35c-119">encoding</span></span>  
    <span data-ttu-id="ff35c-120">Tipo: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="ff35c-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="ff35c-121">A codificação de cadeia de caracteres a ser usada ao converter dados.</span><span class="sxs-lookup"><span data-stu-id="ff35c-121">The string encoding to use when converting data.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ff35c-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff35c-122">Return value</span></span>

<span data-ttu-id="ff35c-123">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ff35c-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="ff35c-124">Os dados recuperados da coluna como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ff35c-124">The data retrieved from the column as a string.</span></span> <span data-ttu-id="ff35c-125">NULL se a coluna for nula.</span><span class="sxs-lookup"><span data-stu-id="ff35c-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff35c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff35c-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff35c-127">Referência</span><span class="sxs-lookup"><span data-stu-id="ff35c-127">Reference</span></span>

[<span data-ttu-id="ff35c-128">Classe de API</span><span class="sxs-lookup"><span data-stu-id="ff35c-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ff35c-129">Membros da API</span><span class="sxs-lookup"><span data-stu-id="ff35c-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ff35c-130">Sobrecarga de RetrieveColumnAsString</span><span class="sxs-lookup"><span data-stu-id="ff35c-130">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="ff35c-131">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ff35c-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

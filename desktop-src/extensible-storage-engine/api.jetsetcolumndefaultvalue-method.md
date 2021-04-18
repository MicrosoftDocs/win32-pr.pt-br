---
description: 'Saiba mais sobre: método API. JetSetColumnDefaultValue'
title: Método API. JetSetColumnDefaultValue
TOCTitle: 'JetSetColumnDefaultValue method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumndefaultvalue(v=EXCHG.10)
ms:contentKeyID: 55100802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24fdb3a885e7aa558e1b3db3c4014fc65a28fcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807333"
---
# <a name="apijetsetcolumndefaultvalue-method"></a><span data-ttu-id="e91a4-103">Método API. JetSetColumnDefaultValue</span><span class="sxs-lookup"><span data-stu-id="e91a4-103">Api.JetSetColumnDefaultValue method</span></span>

<span data-ttu-id="e91a4-104">Altera o valor padrão de uma coluna existente.</span><span class="sxs-lookup"><span data-stu-id="e91a4-104">Changes the default value of an existing column.</span></span>

<span data-ttu-id="e91a4-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e91a4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e91a4-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e91a4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e91a4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e91a4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetColumnDefaultValue ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    columnName As String, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnDefaultValueGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim columnName As String
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnDefaultValueGrbitApi.JetSetColumnDefaultValue(sesid, _
    dbid, tableName, columnName, data, _
    dataSize, grbit)
```

``` csharp
public static void JetSetColumnDefaultValue(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string columnName,
    byte[] data,
    int dataSize,
    SetColumnDefaultValueGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e91a4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e91a4-108">Parameters</span></span>

  - <span data-ttu-id="e91a4-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e91a4-109">sesid</span></span>  
    <span data-ttu-id="e91a4-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e91a4-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e91a4-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e91a4-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e91a4-112">dbid</span><span class="sxs-lookup"><span data-stu-id="e91a4-112">dbid</span></span>  
    <span data-ttu-id="e91a4-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e91a4-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="e91a4-114">O banco de dados que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="e91a4-114">The database containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="e91a4-115">tableName</span><span class="sxs-lookup"><span data-stu-id="e91a4-115">tableName</span></span>  
    <span data-ttu-id="e91a4-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e91a4-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e91a4-117">O nome da tabela que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="e91a4-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="e91a4-118">columnName</span><span class="sxs-lookup"><span data-stu-id="e91a4-118">columnName</span></span>  
    <span data-ttu-id="e91a4-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e91a4-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e91a4-120">O nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="e91a4-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="e91a4-121">data</span><span class="sxs-lookup"><span data-stu-id="e91a4-121">data</span></span>  
    <span data-ttu-id="e91a4-122">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="e91a4-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="e91a4-123">O novo valor padrão.</span><span class="sxs-lookup"><span data-stu-id="e91a4-123">The new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="e91a4-124">dataSize</span><span class="sxs-lookup"><span data-stu-id="e91a4-124">dataSize</span></span>  
    <span data-ttu-id="e91a4-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e91a4-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e91a4-126">Tamanho do novo valor padrão.</span><span class="sxs-lookup"><span data-stu-id="e91a4-126">Size of the new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="e91a4-127">grbit</span><span class="sxs-lookup"><span data-stu-id="e91a4-127">grbit</span></span>  
    <span data-ttu-id="e91a4-128">Tipo: [Microsoft. ISAM. ESENT. Interop. SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e91a4-128">Type: [Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e91a4-129">Opções de valor padrão da coluna.</span><span class="sxs-lookup"><span data-stu-id="e91a4-129">Column default value options.</span></span>

## <a name="see-also"></a><span data-ttu-id="e91a4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e91a4-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e91a4-131">Referência</span><span class="sxs-lookup"><span data-stu-id="e91a4-131">Reference</span></span>

[<span data-ttu-id="e91a4-132">Classe de API</span><span class="sxs-lookup"><span data-stu-id="e91a4-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e91a4-133">Membros da API</span><span class="sxs-lookup"><span data-stu-id="e91a4-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e91a4-134">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e91a4-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

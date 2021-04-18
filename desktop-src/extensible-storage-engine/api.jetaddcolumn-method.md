---
description: 'Saiba mais sobre: método API. JetAddColumn'
title: Método API. JetAddColumn
TOCTitle: 'JetAddColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAddColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.JET_COLUMNID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetaddcolumn(v=EXCHG.10)
ms:contentKeyID: 55100651
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a864bab9c3b888622640e6226c3e7ee542a096d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810859"
---
# <a name="apijetaddcolumn-method"></a><span data-ttu-id="45923-103">Método API. JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="45923-103">Api.JetAddColumn method</span></span>

<span data-ttu-id="45923-104">Adicione uma nova coluna a uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="45923-104">Add a new column to an existing table.</span></span>

<span data-ttu-id="45923-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="45923-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="45923-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="45923-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="45923-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45923-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetAddColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    columndef As JET_COLUMNDEF, _
    defaultValue As Byte(), _
    defaultValueSize As Integer, _
    <OutAttribute> ByRef columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim columndef As JET_COLUMNDEF
Dim defaultValue As Byte()
Dim defaultValueSize As Integer
Dim columnid As JET_COLUMNIDApi.JetAddColumn(sesid, tableid, _
    column, columndef, defaultValue, _
    defaultValueSize, columnid)
```

``` csharp
public static void JetAddColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    JET_COLUMNDEF columndef,
    byte[] defaultValue,
    int defaultValueSize,
    out JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="45923-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45923-108">Parameters</span></span>

  - <span data-ttu-id="45923-109">sesid</span><span class="sxs-lookup"><span data-stu-id="45923-109">sesid</span></span>  
    <span data-ttu-id="45923-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="45923-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="45923-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="45923-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="45923-112">TableID</span><span class="sxs-lookup"><span data-stu-id="45923-112">tableid</span></span>  
    <span data-ttu-id="45923-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="45923-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="45923-114">A tabela à qual adicionar a coluna.</span><span class="sxs-lookup"><span data-stu-id="45923-114">The table to add the column to.</span></span>

<!-- end list -->

  - <span data-ttu-id="45923-115">coluna</span><span class="sxs-lookup"><span data-stu-id="45923-115">column</span></span>  
    <span data-ttu-id="45923-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="45923-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="45923-117">O nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="45923-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="45923-118">columndef</span><span class="sxs-lookup"><span data-stu-id="45923-118">columndef</span></span>  
    <span data-ttu-id="45923-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="45923-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="45923-120">A definição da coluna.</span><span class="sxs-lookup"><span data-stu-id="45923-120">The definition of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="45923-121">defaultValue</span><span class="sxs-lookup"><span data-stu-id="45923-121">defaultValue</span></span>  
    <span data-ttu-id="45923-122">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="45923-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="45923-123">O valor padrão da coluna.</span><span class="sxs-lookup"><span data-stu-id="45923-123">The default value of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="45923-124">DefaultValues</span><span class="sxs-lookup"><span data-stu-id="45923-124">defaultValueSize</span></span>  
    <span data-ttu-id="45923-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="45923-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="45923-126">O tamanho do valor padrão.</span><span class="sxs-lookup"><span data-stu-id="45923-126">The size of the default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="45923-127">columnid</span><span class="sxs-lookup"><span data-stu-id="45923-127">columnid</span></span>  
    <span data-ttu-id="45923-128">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="45923-128">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="45923-129">Retorna o columnid da nova coluna.</span><span class="sxs-lookup"><span data-stu-id="45923-129">Returns the columnid of the new column.</span></span>

## <a name="see-also"></a><span data-ttu-id="45923-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="45923-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="45923-131">Referência</span><span class="sxs-lookup"><span data-stu-id="45923-131">Reference</span></span>

[<span data-ttu-id="45923-132">Classe de API</span><span class="sxs-lookup"><span data-stu-id="45923-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="45923-133">Membros da API</span><span class="sxs-lookup"><span data-stu-id="45923-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="45923-134">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="45923-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

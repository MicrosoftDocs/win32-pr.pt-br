---
description: 'Saiba mais sobre: método API. SerializeObjectToColumn'
title: Método API. SerializeObjectToColumn
TOCTitle: 'SerializeObjectToColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.serializeobjecttocolumn(v=EXCHG.10)
ms:contentKeyID: 55100915
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21b0e421b68287b983fc43482e3a2385b2a160f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170184"
---
# <a name="apiserializeobjecttocolumn-method"></a><span data-ttu-id="592d9-103">Método API. SerializeObjectToColumn</span><span class="sxs-lookup"><span data-stu-id="592d9-103">Api.SerializeObjectToColumn method</span></span>

<span data-ttu-id="592d9-104">Gravar uma forma serializada de um objeto em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="592d9-104">Write a serialized form of an object to a column.</span></span>

<span data-ttu-id="592d9-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="592d9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="592d9-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="592d9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="592d9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="592d9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SerializeObjectToColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    value As Object _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim value As ObjectApi.SerializeObjectToColumn(sesid, _
    tableid, columnid, value)
```

``` csharp
public static void SerializeObjectToColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Object value
)
```

#### <a name="parameters"></a><span data-ttu-id="592d9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="592d9-108">Parameters</span></span>

  - <span data-ttu-id="592d9-109">sesid</span><span class="sxs-lookup"><span data-stu-id="592d9-109">sesid</span></span>  
    <span data-ttu-id="592d9-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="592d9-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="592d9-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="592d9-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="592d9-112">TableID</span><span class="sxs-lookup"><span data-stu-id="592d9-112">tableid</span></span>  
    <span data-ttu-id="592d9-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="592d9-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="592d9-114">A tabela na qual gravar.</span><span class="sxs-lookup"><span data-stu-id="592d9-114">The table to write to.</span></span> <span data-ttu-id="592d9-115">Uma atualização deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="592d9-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="592d9-116">columnid</span><span class="sxs-lookup"><span data-stu-id="592d9-116">columnid</span></span>  
    <span data-ttu-id="592d9-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="592d9-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="592d9-118">A coluna na qual gravar.</span><span class="sxs-lookup"><span data-stu-id="592d9-118">The column to write to.</span></span>

<!-- end list -->

  - <span data-ttu-id="592d9-119">value</span><span class="sxs-lookup"><span data-stu-id="592d9-119">value</span></span>  
    <span data-ttu-id="592d9-120">Tipo: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="592d9-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="592d9-121">O objeto a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="592d9-121">The object to write.</span></span> <span data-ttu-id="592d9-122">O objeto deve ser serializável.</span><span class="sxs-lookup"><span data-stu-id="592d9-122">The object must be serializable.</span></span>

## <a name="see-also"></a><span data-ttu-id="592d9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="592d9-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="592d9-124">Referência</span><span class="sxs-lookup"><span data-stu-id="592d9-124">Reference</span></span>

[<span data-ttu-id="592d9-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="592d9-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="592d9-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="592d9-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="592d9-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="592d9-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

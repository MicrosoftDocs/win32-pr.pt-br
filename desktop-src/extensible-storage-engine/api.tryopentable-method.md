---
description: 'Saiba mais sobre: método API. TryOpenTable'
title: Método API. TryOpenTable
TOCTitle: 'TryOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryopentable(v=EXCHG.10)
ms:contentKeyID: 55100889
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 556d3f12f24229326a6b26f357e5b19801119b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370631"
---
# <a name="apitryopentable-method"></a><span data-ttu-id="f5b28-103">Método API. TryOpenTable</span><span class="sxs-lookup"><span data-stu-id="f5b28-103">Api.TryOpenTable method</span></span>

<span data-ttu-id="f5b28-104">Tente abrir uma tabela.</span><span class="sxs-lookup"><span data-stu-id="f5b28-104">Try to open a table.</span></span>

<span data-ttu-id="f5b28-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f5b28-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f5b28-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f5b28-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b28-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5b28-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryOpenTable(sesid, _
    dbid, tablename, grbit, tableid)
```

``` csharp
public static bool TryOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="f5b28-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5b28-108">Parameters</span></span>

  - <span data-ttu-id="f5b28-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f5b28-109">sesid</span></span>  
    <span data-ttu-id="f5b28-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f5b28-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f5b28-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="f5b28-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5b28-112">dbid</span><span class="sxs-lookup"><span data-stu-id="f5b28-112">dbid</span></span>  
    <span data-ttu-id="f5b28-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f5b28-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="f5b28-114">O banco de dados para o qual procurar a tabela.</span><span class="sxs-lookup"><span data-stu-id="f5b28-114">The database to look for the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5b28-115">tablename</span><span class="sxs-lookup"><span data-stu-id="f5b28-115">tablename</span></span>  
    <span data-ttu-id="f5b28-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f5b28-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f5b28-117">O nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="f5b28-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5b28-118">grbit</span><span class="sxs-lookup"><span data-stu-id="f5b28-118">grbit</span></span>  
    <span data-ttu-id="f5b28-119">Tipo: [Microsoft. ISAM. ESENT. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f5b28-119">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f5b28-120">Opções de abertura de tabela.</span><span class="sxs-lookup"><span data-stu-id="f5b28-120">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5b28-121">TableID</span><span class="sxs-lookup"><span data-stu-id="f5b28-121">tableid</span></span>  
    <span data-ttu-id="f5b28-122">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f5b28-122">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f5b28-123">Retorna o TableName aberto.</span><span class="sxs-lookup"><span data-stu-id="f5b28-123">Returns the opened tableid.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f5b28-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5b28-124">Return value</span></span>

<span data-ttu-id="f5b28-125">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f5b28-125">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f5b28-126">True se a tabela tiver sido aberta, false se a tabela não existir.</span><span class="sxs-lookup"><span data-stu-id="f5b28-126">True if the table was opened, false if the table doesn't exist.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f5b28-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5b28-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f5b28-128">Referência</span><span class="sxs-lookup"><span data-stu-id="f5b28-128">Reference</span></span>

[<span data-ttu-id="f5b28-129">Classe de API</span><span class="sxs-lookup"><span data-stu-id="f5b28-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f5b28-130">Membros da API</span><span class="sxs-lookup"><span data-stu-id="f5b28-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f5b28-131">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f5b28-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

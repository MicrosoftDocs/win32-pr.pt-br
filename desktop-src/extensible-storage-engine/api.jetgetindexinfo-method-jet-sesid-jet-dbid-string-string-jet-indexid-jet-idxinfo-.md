---
description: 'Saiba mais sobre: método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)'
title: Método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100772
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac8a622f3b653885374888fa9fa6b2835ef8ede0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758663"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexid-jet_idxinfo"></a><span data-ttu-id="931b6-103">Método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="931b6-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</span></span>

<span data-ttu-id="931b6-104">Recupera informações sobre índices em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="931b6-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="931b6-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="931b6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="931b6-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="931b6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="931b6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="931b6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXID, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As JET_INDEXID
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out JET_INDEXID result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="931b6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="931b6-108">Parameters</span></span>

  - <span data-ttu-id="931b6-109">sesid</span><span class="sxs-lookup"><span data-stu-id="931b6-109">sesid</span></span>  
    <span data-ttu-id="931b6-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="931b6-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="931b6-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="931b6-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="931b6-112">dbid</span><span class="sxs-lookup"><span data-stu-id="931b6-112">dbid</span></span>  
    <span data-ttu-id="931b6-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="931b6-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="931b6-114">O banco de dados a ser usado.</span><span class="sxs-lookup"><span data-stu-id="931b6-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="931b6-115">tablename</span><span class="sxs-lookup"><span data-stu-id="931b6-115">tablename</span></span>  
    <span data-ttu-id="931b6-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="931b6-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="931b6-117">O nome da tabela sobre a qual recuperar informações de índice.</span><span class="sxs-lookup"><span data-stu-id="931b6-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="931b6-118">IndexName</span><span class="sxs-lookup"><span data-stu-id="931b6-118">indexname</span></span>  
    <span data-ttu-id="931b6-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="931b6-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="931b6-120">O nome do índice para o qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="931b6-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="931b6-121">result</span><span class="sxs-lookup"><span data-stu-id="931b6-121">result</span></span>  
    <span data-ttu-id="931b6-122">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="931b6-122">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="931b6-123">Preenchido com informações sobre índices na tabela.</span><span class="sxs-lookup"><span data-stu-id="931b6-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="931b6-124">infoLevel</span><span class="sxs-lookup"><span data-stu-id="931b6-124">infoLevel</span></span>  
    <span data-ttu-id="931b6-125">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="931b6-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="931b6-126">O tipo de informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="931b6-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="931b6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="931b6-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="931b6-128">Referência</span><span class="sxs-lookup"><span data-stu-id="931b6-128">Reference</span></span>

[<span data-ttu-id="931b6-129">Classe de API</span><span class="sxs-lookup"><span data-stu-id="931b6-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="931b6-130">Membros da API</span><span class="sxs-lookup"><span data-stu-id="931b6-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="931b6-131">Sobrecarga de JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="931b6-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="931b6-132">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="931b6-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

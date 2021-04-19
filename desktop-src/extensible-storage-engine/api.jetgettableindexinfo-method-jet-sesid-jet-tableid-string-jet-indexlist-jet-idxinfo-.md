---
description: 'Saiba mais sobre: método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)'
title: Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100749
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42a938b2114cb379752f9a4f749782dd2b5b1757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793652"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexlist-jet_idxinfo"></a><span data-ttu-id="edf38-103">Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="edf38-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)</span></span>

<span data-ttu-id="edf38-104">Recupera informações sobre índices em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="edf38-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="edf38-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="edf38-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="edf38-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="edf38-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="edf38-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edf38-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXLIST, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As JET_INDEXLIST
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXLIST result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="edf38-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edf38-108">Parameters</span></span>

  - <span data-ttu-id="edf38-109">sesid</span><span class="sxs-lookup"><span data-stu-id="edf38-109">sesid</span></span>  
    <span data-ttu-id="edf38-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="edf38-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="edf38-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="edf38-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="edf38-112">TableID</span><span class="sxs-lookup"><span data-stu-id="edf38-112">tableid</span></span>  
    <span data-ttu-id="edf38-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="edf38-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="edf38-114">A tabela da qual recuperar informações de índice.</span><span class="sxs-lookup"><span data-stu-id="edf38-114">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="edf38-115">IndexName</span><span class="sxs-lookup"><span data-stu-id="edf38-115">indexname</span></span>  
    <span data-ttu-id="edf38-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="edf38-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="edf38-117">O nome do índice.</span><span class="sxs-lookup"><span data-stu-id="edf38-117">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="edf38-118">result</span><span class="sxs-lookup"><span data-stu-id="edf38-118">result</span></span>  
    <span data-ttu-id="edf38-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="edf38-119">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="edf38-120">Preenchido com informações sobre índices na tabela.</span><span class="sxs-lookup"><span data-stu-id="edf38-120">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="edf38-121">infoLevel</span><span class="sxs-lookup"><span data-stu-id="edf38-121">infoLevel</span></span>  
    <span data-ttu-id="edf38-122">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="edf38-122">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="edf38-123">O tipo de informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="edf38-123">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="edf38-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="edf38-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="edf38-125">Referência</span><span class="sxs-lookup"><span data-stu-id="edf38-125">Reference</span></span>

[<span data-ttu-id="edf38-126">Classe de API</span><span class="sxs-lookup"><span data-stu-id="edf38-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="edf38-127">Membros da API</span><span class="sxs-lookup"><span data-stu-id="edf38-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="edf38-128">Sobrecarga de JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="edf38-128">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="edf38-129">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="edf38-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

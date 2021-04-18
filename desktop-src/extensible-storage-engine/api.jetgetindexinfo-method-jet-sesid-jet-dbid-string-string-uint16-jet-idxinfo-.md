---
description: 'Saiba mais sobre: método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)'
title: Método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100771
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 762437dba9e502de5c0650e4ae6df53d4629d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752212"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-uint16-jet_idxinfo"></a><span data-ttu-id="1b9cf-103">Método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="1b9cf-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="1b9cf-104">Recupera informações sobre índices em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="1b9cf-105">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="1b9cf-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1b9cf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1b9cf-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1b9cf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1b9cf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b9cf-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="1b9cf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b9cf-109">Parameters</span></span>

  - <span data-ttu-id="1b9cf-110">sesid</span><span class="sxs-lookup"><span data-stu-id="1b9cf-110">sesid</span></span>  
    <span data-ttu-id="1b9cf-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1b9cf-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1b9cf-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b9cf-113">dbid</span><span class="sxs-lookup"><span data-stu-id="1b9cf-113">dbid</span></span>  
    <span data-ttu-id="1b9cf-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1b9cf-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="1b9cf-115">O banco de dados a ser usado.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b9cf-116">tablename</span><span class="sxs-lookup"><span data-stu-id="1b9cf-116">tablename</span></span>  
    <span data-ttu-id="1b9cf-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1b9cf-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1b9cf-118">O nome da tabela sobre a qual recuperar informações de índice.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b9cf-119">IndexName</span><span class="sxs-lookup"><span data-stu-id="1b9cf-119">indexname</span></span>  
    <span data-ttu-id="1b9cf-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1b9cf-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1b9cf-121">O nome do índice para o qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-121">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b9cf-122">result</span><span class="sxs-lookup"><span data-stu-id="1b9cf-122">result</span></span>  
    <span data-ttu-id="1b9cf-123">Tipo: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="1b9cf-123">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="1b9cf-124">Preenchido com informações sobre índices na tabela.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-124">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b9cf-125">infoLevel</span><span class="sxs-lookup"><span data-stu-id="1b9cf-125">infoLevel</span></span>  
    <span data-ttu-id="1b9cf-126">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1b9cf-126">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="1b9cf-127">O tipo de informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-127">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b9cf-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b9cf-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1b9cf-129">Referência</span><span class="sxs-lookup"><span data-stu-id="1b9cf-129">Reference</span></span>

[<span data-ttu-id="1b9cf-130">Classe de API</span><span class="sxs-lookup"><span data-stu-id="1b9cf-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1b9cf-131">Membros da API</span><span class="sxs-lookup"><span data-stu-id="1b9cf-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1b9cf-132">Sobrecarga de JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="1b9cf-132">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="1b9cf-133">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1b9cf-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

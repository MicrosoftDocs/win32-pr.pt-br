---
description: 'Saiba mais sobre: método API. JetGetDatabaseInfo (JET_SESID, JET_DBID, Int32, JET_DbInfo)'
title: Método API. JetGetDatabaseInfo (JET_SESID, JET_DBID, Int32, JET_DbInfo)
TOCTitle: JetGetDatabaseInfo method (JET_SESID, JET_DBID, Int32, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabaseinfo(v=EXCHG.10)
ms:contentKeyID: 55100711
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 522b0bff93fe1bc224da4175725c89642547270f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461012"
---
# <a name="apijetgetdatabaseinfo-method-jet_sesid-jet_dbid-int32-jet_dbinfo"></a><span data-ttu-id="ea1ec-103">Método API. JetGetDatabaseInfo (JET_SESID, JET_DBID, Int32, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="ea1ec-103">Api.JetGetDatabaseInfo method (JET_SESID, JET_DBID, Int32, JET_DbInfo)</span></span>

<span data-ttu-id="ea1ec-104">Recupera determinadas informações sobre o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="ea1ec-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="ea1ec-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ea1ec-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ea1ec-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ea1ec-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ea1ec-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea1ec-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef value As Integer, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim value As Integer
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseInfo(sesid, dbid, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out int value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="ea1ec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea1ec-108">Parameters</span></span>

  - <span data-ttu-id="ea1ec-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ea1ec-109">sesid</span></span>  
    <span data-ttu-id="ea1ec-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ea1ec-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ea1ec-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="ea1ec-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ea1ec-112">dbid</span><span class="sxs-lookup"><span data-stu-id="ea1ec-112">dbid</span></span>  
    <span data-ttu-id="ea1ec-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ea1ec-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="ea1ec-114">O identificador do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ea1ec-114">The database identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="ea1ec-115">value</span><span class="sxs-lookup"><span data-stu-id="ea1ec-115">value</span></span>  
    <span data-ttu-id="ea1ec-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ea1ec-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ea1ec-117">O valor a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="ea1ec-117">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="ea1ec-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="ea1ec-118">infoLevel</span></span>  
    <span data-ttu-id="ea1ec-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ea1ec-119">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="ea1ec-120">Os dados específicos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="ea1ec-120">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea1ec-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea1ec-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ea1ec-122">Referência</span><span class="sxs-lookup"><span data-stu-id="ea1ec-122">Reference</span></span>

[<span data-ttu-id="ea1ec-123">Classe de API</span><span class="sxs-lookup"><span data-stu-id="ea1ec-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ea1ec-124">Membros da API</span><span class="sxs-lookup"><span data-stu-id="ea1ec-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ea1ec-125">Sobrecarga de JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="ea1ec-125">JetGetDatabaseInfo overload</span></span>](./api.jetgetdatabaseinfo-method.md)

[<span data-ttu-id="ea1ec-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ea1ec-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

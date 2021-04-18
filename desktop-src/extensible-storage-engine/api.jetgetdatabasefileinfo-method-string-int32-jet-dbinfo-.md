---
description: 'Saiba mais sobre: método API. JetGetDatabaseFileInfo (cadeia de caracteres, Int32 JET_DbInfo)'
title: Método API. JetGetDatabaseFileInfo (cadeia de caracteres, Int32 JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, Int32, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int32@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100698
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a7d873d3688d6c18ff01a20c5e5c53809fbcdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772703"
---
# <a name="apijetgetdatabasefileinfo-method-string-int32-jet_dbinfo"></a><span data-ttu-id="9f3d8-103">Método API. JetGetDatabaseFileInfo (cadeia de caracteres, Int32 JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="9f3d8-103">Api.JetGetDatabaseFileInfo method (String, Int32, JET_DbInfo)</span></span>

<span data-ttu-id="9f3d8-104">Recupera determinadas informações sobre o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="9f3d8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f3d8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f3d8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f3d8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f3d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f3d8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Integer, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Integer
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out int value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="9f3d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f3d8-108">Parameters</span></span>

  - <span data-ttu-id="9f3d8-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="9f3d8-109">databaseName</span></span>  
    <span data-ttu-id="9f3d8-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9f3d8-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9f3d8-111">O nome do arquivo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f3d8-112">value</span><span class="sxs-lookup"><span data-stu-id="9f3d8-112">value</span></span>  
    <span data-ttu-id="9f3d8-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9f3d8-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9f3d8-114">O valor a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f3d8-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="9f3d8-115">infoLevel</span></span>  
    <span data-ttu-id="9f3d8-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9f3d8-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="9f3d8-117">Os dados específicos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f3d8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f3d8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f3d8-119">Referência</span><span class="sxs-lookup"><span data-stu-id="9f3d8-119">Reference</span></span>

[<span data-ttu-id="9f3d8-120">Classe de API</span><span class="sxs-lookup"><span data-stu-id="9f3d8-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9f3d8-121">Membros da API</span><span class="sxs-lookup"><span data-stu-id="9f3d8-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9f3d8-122">Sobrecarga de JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="9f3d8-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="9f3d8-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9f3d8-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

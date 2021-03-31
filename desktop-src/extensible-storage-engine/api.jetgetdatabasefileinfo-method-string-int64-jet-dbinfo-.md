---
description: 'Saiba mais sobre: método API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)'
title: Método API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int64@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100700
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
ms.openlocfilehash: cc036a1c1eceedd39fd265bcf85a2dbaf779a432
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090146"
---
# <a name="apijetgetdatabasefileinfo-method-string-int64-jet_dbinfo"></a><span data-ttu-id="8169f-103">Método API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="8169f-103">Api.JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)</span></span>

<span data-ttu-id="8169f-104">Recupera determinadas informações sobre o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="8169f-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="8169f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8169f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8169f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8169f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8169f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8169f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Long, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Long
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out long value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="8169f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8169f-108">Parameters</span></span>

  - <span data-ttu-id="8169f-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="8169f-109">databaseName</span></span>  
    <span data-ttu-id="8169f-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8169f-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8169f-111">O nome do arquivo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8169f-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="8169f-112">value</span><span class="sxs-lookup"><span data-stu-id="8169f-112">value</span></span>  
    <span data-ttu-id="8169f-113">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="8169f-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="8169f-114">O valor a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="8169f-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="8169f-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="8169f-115">infoLevel</span></span>  
    <span data-ttu-id="8169f-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8169f-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="8169f-117">Os dados específicos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="8169f-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="8169f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8169f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8169f-119">Referência</span><span class="sxs-lookup"><span data-stu-id="8169f-119">Reference</span></span>

[<span data-ttu-id="8169f-120">Classe de API</span><span class="sxs-lookup"><span data-stu-id="8169f-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8169f-121">Membros da API</span><span class="sxs-lookup"><span data-stu-id="8169f-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8169f-122">Sobrecarga de JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="8169f-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="8169f-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8169f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

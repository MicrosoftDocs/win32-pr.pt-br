---
description: 'Saiba mais sobre: método API. JetGrowDatabase'
title: Método API. JetGrowDatabase
TOCTitle: 'JetGrowDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgrowdatabase(v=EXCHG.10)
ms:contentKeyID: 55100754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a51f0d55187b6f6eac66c0cba2ec7b9daa7d1dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827442"
---
# <a name="apijetgrowdatabase-method"></a><span data-ttu-id="cea71-103">Método API. JetGrowDatabase</span><span class="sxs-lookup"><span data-stu-id="cea71-103">Api.JetGrowDatabase method</span></span>

<span data-ttu-id="cea71-104">Estende o tamanho de um banco de dados que está aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="cea71-104">Extends the size of a database that is currently open.</span></span>

<span data-ttu-id="cea71-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cea71-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cea71-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cea71-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cea71-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cea71-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGrowDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetGrowDatabase(sesid, dbid, _
    desiredPages, actualPages)
```

``` csharp
public static void JetGrowDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="cea71-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cea71-108">Parameters</span></span>

  - <span data-ttu-id="cea71-109">sesid</span><span class="sxs-lookup"><span data-stu-id="cea71-109">sesid</span></span>  
    <span data-ttu-id="cea71-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cea71-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cea71-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="cea71-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cea71-112">dbid</span><span class="sxs-lookup"><span data-stu-id="cea71-112">dbid</span></span>  
    <span data-ttu-id="cea71-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cea71-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="cea71-114">O banco de dados a crescer.</span><span class="sxs-lookup"><span data-stu-id="cea71-114">The database to grow.</span></span>

<!-- end list -->

  - <span data-ttu-id="cea71-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="cea71-115">desiredPages</span></span>  
    <span data-ttu-id="cea71-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cea71-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="cea71-117">O tamanho desejado do banco de dados, em páginas.</span><span class="sxs-lookup"><span data-stu-id="cea71-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="cea71-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="cea71-118">actualPages</span></span>  
    <span data-ttu-id="cea71-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cea71-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="cea71-120">O tamanho do banco de dados, em páginas, após a chamada.</span><span class="sxs-lookup"><span data-stu-id="cea71-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="cea71-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="cea71-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cea71-122">Referência</span><span class="sxs-lookup"><span data-stu-id="cea71-122">Reference</span></span>

[<span data-ttu-id="cea71-123">Classe de API</span><span class="sxs-lookup"><span data-stu-id="cea71-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cea71-124">Membros da API</span><span class="sxs-lookup"><span data-stu-id="cea71-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cea71-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cea71-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

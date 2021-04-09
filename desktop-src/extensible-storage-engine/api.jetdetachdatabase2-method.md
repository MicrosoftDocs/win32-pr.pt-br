---
description: 'Saiba mais sobre: método API. JetDetachDatabase2'
title: Método API. JetDetachDatabase2
TOCTitle: 'JetDetachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55100685
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44cc8b5d03ba720f1acb7d0e8603bf29906a611e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090152"
---
# <a name="apijetdetachdatabase2-method"></a><span data-ttu-id="ae03e-103">Método API. JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="ae03e-103">Api.JetDetachDatabase2 method</span></span>

<span data-ttu-id="ae03e-104">Libera um arquivo de banco de dados que foi anexado anteriormente a uma sessão de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ae03e-104">Releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="ae03e-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae03e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae03e-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ae03e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae03e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae03e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDetachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As DetachDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As DetachDatabaseGrbitApi.JetDetachDatabase2(sesid, database, _
    grbit)
```

``` csharp
public static void JetDetachDatabase2(
    JET_SESID sesid,
    string database,
    DetachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ae03e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae03e-108">Parameters</span></span>

  - <span data-ttu-id="ae03e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ae03e-109">sesid</span></span>  
    <span data-ttu-id="ae03e-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ae03e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ae03e-111">A sessão de banco de dados a ser usada.</span><span class="sxs-lookup"><span data-stu-id="ae03e-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ae03e-112">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="ae03e-112">database</span></span>  
    <span data-ttu-id="ae03e-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ae03e-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ae03e-114">O banco de dados a ser desanexado.</span><span class="sxs-lookup"><span data-stu-id="ae03e-114">The database to detach.</span></span>

<!-- end list -->

  - <span data-ttu-id="ae03e-115">grbit</span><span class="sxs-lookup"><span data-stu-id="ae03e-115">grbit</span></span>  
    <span data-ttu-id="ae03e-116">Tipo: [Microsoft. ISAM. ESENT. Interop. DetachDatabaseGrbit](./detachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ae03e-116">Type: [Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit](./detachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ae03e-117">Opções de desanexação.</span><span class="sxs-lookup"><span data-stu-id="ae03e-117">Detach options.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae03e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae03e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae03e-119">Referência</span><span class="sxs-lookup"><span data-stu-id="ae03e-119">Reference</span></span>

[<span data-ttu-id="ae03e-120">Classe de API</span><span class="sxs-lookup"><span data-stu-id="ae03e-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ae03e-121">Membros da API</span><span class="sxs-lookup"><span data-stu-id="ae03e-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ae03e-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ae03e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

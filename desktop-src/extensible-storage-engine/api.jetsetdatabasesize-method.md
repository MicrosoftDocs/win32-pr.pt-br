---
description: 'Saiba mais sobre: método API. JetSetDatabaseSize'
title: Método API. JetSetDatabaseSize
TOCTitle: 'JetSetDatabaseSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetdatabasesize(v=EXCHG.10)
ms:contentKeyID: 55100807
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c90ba5ef2ebc96cbe6d50fa6c0888db9a09a0a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779513"
---
# <a name="apijetsetdatabasesize-method"></a><span data-ttu-id="5bc26-103">Método API. JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="5bc26-103">Api.JetSetDatabaseSize method</span></span>

<span data-ttu-id="5bc26-104">Define o tamanho de um arquivo de banco de dados não aberto.</span><span class="sxs-lookup"><span data-stu-id="5bc26-104">Sets the size of an unopened database file.</span></span>

<span data-ttu-id="5bc26-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5bc26-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5bc26-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5bc26-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc26-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bc26-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetDatabaseSize ( _
    sesid As JET_SESID, _
    database As String, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetSetDatabaseSize(sesid, database, _
    desiredPages, actualPages)
```

``` csharp
public static void JetSetDatabaseSize(
    JET_SESID sesid,
    string database,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="5bc26-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bc26-108">Parameters</span></span>

  - <span data-ttu-id="5bc26-109">sesid</span><span class="sxs-lookup"><span data-stu-id="5bc26-109">sesid</span></span>  
    <span data-ttu-id="5bc26-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5bc26-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5bc26-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5bc26-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bc26-112">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="5bc26-112">database</span></span>  
    <span data-ttu-id="5bc26-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5bc26-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5bc26-114">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5bc26-114">The name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bc26-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="5bc26-115">desiredPages</span></span>  
    <span data-ttu-id="5bc26-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5bc26-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5bc26-117">O tamanho desejado do banco de dados, em páginas.</span><span class="sxs-lookup"><span data-stu-id="5bc26-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bc26-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="5bc26-118">actualPages</span></span>  
    <span data-ttu-id="5bc26-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5bc26-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5bc26-120">O tamanho do banco de dados, em páginas, após a chamada.</span><span class="sxs-lookup"><span data-stu-id="5bc26-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bc26-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bc26-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5bc26-122">Referência</span><span class="sxs-lookup"><span data-stu-id="5bc26-122">Reference</span></span>

[<span data-ttu-id="5bc26-123">Classe de API</span><span class="sxs-lookup"><span data-stu-id="5bc26-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5bc26-124">Membros da API</span><span class="sxs-lookup"><span data-stu-id="5bc26-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5bc26-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5bc26-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

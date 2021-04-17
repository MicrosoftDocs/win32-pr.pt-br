---
description: 'Saiba mais sobre: método API. JetCreateIndex'
title: Método API. JetCreateIndex
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b3549461324f396408bb7d370531907248e8c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771405"
---
# <a name="apijetcreateindex-method"></a><span data-ttu-id="95442-103">Método API. JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="95442-103">Api.JetCreateIndex method</span></span>

<span data-ttu-id="95442-104">Cria um índice sobre os dados em um banco de dado ESE.</span><span class="sxs-lookup"><span data-stu-id="95442-104">Creates an index over data in an ESE database.</span></span> <span data-ttu-id="95442-105">Um índice pode ser usado para localizar dados específicos rapidamente.</span><span class="sxs-lookup"><span data-stu-id="95442-105">An index can be used to locate specific data quickly.</span></span>

<span data-ttu-id="95442-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="95442-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="95442-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="95442-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="95442-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95442-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a><span data-ttu-id="95442-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95442-109">Parameters</span></span>

  - <span data-ttu-id="95442-110">sesid</span><span class="sxs-lookup"><span data-stu-id="95442-110">sesid</span></span>  
    <span data-ttu-id="95442-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95442-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="95442-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="95442-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="95442-113">TableID</span><span class="sxs-lookup"><span data-stu-id="95442-113">tableid</span></span>  
    <span data-ttu-id="95442-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95442-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="95442-115">A tabela na qual criar o índice.</span><span class="sxs-lookup"><span data-stu-id="95442-115">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="95442-116">indexName</span><span class="sxs-lookup"><span data-stu-id="95442-116">indexName</span></span>  
    <span data-ttu-id="95442-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="95442-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="95442-118">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="95442-118">Pointer to a null-terminated string that specifies the name of the index to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="95442-119">grbit</span><span class="sxs-lookup"><span data-stu-id="95442-119">grbit</span></span>  
    <span data-ttu-id="95442-120">Tipo: [Microsoft. ISAM. ESENT. Interop. CreateIndexGrbit](./createindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="95442-120">Type: [Microsoft.Isam.Esent.Interop.CreateIndexGrbit](./createindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="95442-121">Opções de criação de índice.</span><span class="sxs-lookup"><span data-stu-id="95442-121">Index creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="95442-122">Descrição da</span><span class="sxs-lookup"><span data-stu-id="95442-122">keyDescription</span></span>  
    <span data-ttu-id="95442-123">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="95442-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="95442-124">Ponteiro para uma cadeia de caracteres dupla com terminação nula de tokens delimitados por nulo.</span><span class="sxs-lookup"><span data-stu-id="95442-124">Pointer to a double null-terminated string of null-delimited tokens.</span></span>

<!-- end list -->

  - <span data-ttu-id="95442-125">keyDescriptionLength</span><span class="sxs-lookup"><span data-stu-id="95442-125">keyDescriptionLength</span></span>  
    <span data-ttu-id="95442-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="95442-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="95442-127">O comprimento, em caracteres, de szKey, incluindo os dois nulos de terminação.</span><span class="sxs-lookup"><span data-stu-id="95442-127">The length, in characters, of szKey including the two terminating nulls.</span></span>

<!-- end list -->

  - <span data-ttu-id="95442-128">densidade</span><span class="sxs-lookup"><span data-stu-id="95442-128">density</span></span>  
    <span data-ttu-id="95442-129">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="95442-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="95442-130">Densidade inicial da árvore B +.</span><span class="sxs-lookup"><span data-stu-id="95442-130">Initial B+ tree density.</span></span>

## <a name="see-also"></a><span data-ttu-id="95442-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="95442-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="95442-132">Referência</span><span class="sxs-lookup"><span data-stu-id="95442-132">Reference</span></span>

[<span data-ttu-id="95442-133">Classe de API</span><span class="sxs-lookup"><span data-stu-id="95442-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="95442-134">Membros da API</span><span class="sxs-lookup"><span data-stu-id="95442-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="95442-135">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="95442-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

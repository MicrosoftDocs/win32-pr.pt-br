---
description: 'Saiba mais sobre: método API. JetRetrieveKey'
title: Método API. JetRetrieveKey
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebf130b4542992e18de49d58801f789d40106fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813692"
---
# <a name="apijetretrievekey-method"></a><span data-ttu-id="90476-103">Método API. JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="90476-103">Api.JetRetrieveKey method</span></span>

<span data-ttu-id="90476-104">Recupera a chave da entrada de índice na posição atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="90476-104">Retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="90476-105">Consulte também [RetrieveKey (JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="90476-105">Also see [RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).</span></span>

<span data-ttu-id="90476-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="90476-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="90476-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="90476-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="90476-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90476-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="90476-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90476-109">Parameters</span></span>

  - <span data-ttu-id="90476-110">sesid</span><span class="sxs-lookup"><span data-stu-id="90476-110">sesid</span></span>  
    <span data-ttu-id="90476-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="90476-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="90476-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="90476-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="90476-113">TableID</span><span class="sxs-lookup"><span data-stu-id="90476-113">tableid</span></span>  
    <span data-ttu-id="90476-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="90476-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="90476-115">O cursor do qual recuperar a chave.</span><span class="sxs-lookup"><span data-stu-id="90476-115">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="90476-116">data</span><span class="sxs-lookup"><span data-stu-id="90476-116">data</span></span>  
    <span data-ttu-id="90476-117">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="90476-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="90476-118">O buffer para o qual recuperar a chave.</span><span class="sxs-lookup"><span data-stu-id="90476-118">The buffer to retrieve the key into.</span></span>

<!-- end list -->

  - <span data-ttu-id="90476-119">dataSize</span><span class="sxs-lookup"><span data-stu-id="90476-119">dataSize</span></span>  
    <span data-ttu-id="90476-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="90476-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="90476-121">O tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="90476-121">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="90476-122">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="90476-122">actualDataSize</span></span>  
    <span data-ttu-id="90476-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="90476-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="90476-124">Retorna o tamanho real dos dados.</span><span class="sxs-lookup"><span data-stu-id="90476-124">Returns the actual size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="90476-125">grbit</span><span class="sxs-lookup"><span data-stu-id="90476-125">grbit</span></span>  
    <span data-ttu-id="90476-126">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="90476-126">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="90476-127">Recuperar opções de chave.</span><span class="sxs-lookup"><span data-stu-id="90476-127">Retrieve key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="90476-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="90476-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="90476-129">Referência</span><span class="sxs-lookup"><span data-stu-id="90476-129">Reference</span></span>

[<span data-ttu-id="90476-130">Classe de API</span><span class="sxs-lookup"><span data-stu-id="90476-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="90476-131">Membros da API</span><span class="sxs-lookup"><span data-stu-id="90476-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="90476-132">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="90476-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

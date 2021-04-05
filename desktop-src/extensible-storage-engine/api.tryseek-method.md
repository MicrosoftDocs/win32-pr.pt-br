---
description: 'Saiba mais sobre: método API. TrySeek'
title: Método API. TrySeek
TOCTitle: 'TrySeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryseek(v=EXCHG.10)
ms:contentKeyID: 55100941
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46472c59c14bd515e744a7ccfa908752783d27fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826941"
---
# <a name="apitryseek-method"></a><span data-ttu-id="0253c-103">Método API. TrySeek</span><span class="sxs-lookup"><span data-stu-id="0253c-103">Api.TrySeek method</span></span>

<span data-ttu-id="0253c-104">Posiciona com eficiência um cursor para uma entrada de índice que corresponda aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e à desigualdade especificada.</span><span class="sxs-lookup"><span data-stu-id="0253c-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="0253c-105">Uma chave de pesquisa deve ter sido construída anteriormente usando JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="0253c-105">A search key must have been previously constructed using JetMakeKey.</span></span>

<span data-ttu-id="0253c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0253c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0253c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0253c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0253c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0253c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As Boolean

returnValue = Api.TrySeek(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0253c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0253c-109">Parameters</span></span>

  - <span data-ttu-id="0253c-110">sesid</span><span class="sxs-lookup"><span data-stu-id="0253c-110">sesid</span></span>  
    <span data-ttu-id="0253c-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0253c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0253c-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="0253c-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0253c-113">TableID</span><span class="sxs-lookup"><span data-stu-id="0253c-113">tableid</span></span>  
    <span data-ttu-id="0253c-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0253c-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0253c-115">O cursor a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="0253c-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="0253c-116">grbit</span><span class="sxs-lookup"><span data-stu-id="0253c-116">grbit</span></span>  
    <span data-ttu-id="0253c-117">Tipo: [Microsoft. ISAM. ESENT. Interop. SeekGrbit](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0253c-117">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0253c-118">Opção de busca.</span><span class="sxs-lookup"><span data-stu-id="0253c-118">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0253c-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0253c-119">Return value</span></span>

<span data-ttu-id="0253c-120">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="0253c-120">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="0253c-121">True se um registro correspondente aos critérios for encontrado.</span><span class="sxs-lookup"><span data-stu-id="0253c-121">True if a record matching the criteria was found.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0253c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0253c-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0253c-123">Referência</span><span class="sxs-lookup"><span data-stu-id="0253c-123">Reference</span></span>

[<span data-ttu-id="0253c-124">Classe de API</span><span class="sxs-lookup"><span data-stu-id="0253c-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0253c-125">Membros da API</span><span class="sxs-lookup"><span data-stu-id="0253c-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0253c-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0253c-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

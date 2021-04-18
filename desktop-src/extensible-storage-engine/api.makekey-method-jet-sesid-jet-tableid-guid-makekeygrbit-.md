---
description: 'Saiba mais sobre: método API. MakeKey (JET_SESID, JET_TABLEID, GUID, MakeKeyGrbit)'
title: Método API. MakeKey (JET_SESID, JET_TABLEID, GUID, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Guid,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100823
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73096598f8173def29b40273bbeec28738d762a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814046"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-guid-makekeygrbit"></a><span data-ttu-id="0e2a0-103">Método API. MakeKey (JET_SESID, JET_TABLEID, GUID, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="0e2a0-103">Api.MakeKey method (JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)</span></span>

<span data-ttu-id="0e2a0-104">Constrói uma chave de pesquisa que pode ser usada por [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) e [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="0e2a0-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="0e2a0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0e2a0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0e2a0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0e2a0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e2a0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e2a0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Guid, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Guid
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    Guid data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0e2a0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e2a0-108">Parameters</span></span>

  - <span data-ttu-id="0e2a0-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0e2a0-109">sesid</span></span>  
    <span data-ttu-id="0e2a0-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0e2a0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0e2a0-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="0e2a0-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0e2a0-112">TableID</span><span class="sxs-lookup"><span data-stu-id="0e2a0-112">tableid</span></span>  
    <span data-ttu-id="0e2a0-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0e2a0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0e2a0-114">O cursor no qual criar a chave.</span><span class="sxs-lookup"><span data-stu-id="0e2a0-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="0e2a0-115">data</span><span class="sxs-lookup"><span data-stu-id="0e2a0-115">data</span></span>  
    <span data-ttu-id="0e2a0-116">Tipo: [System. GUID](/dotnet/api/system.guid)</span><span class="sxs-lookup"><span data-stu-id="0e2a0-116">Type: [System.Guid](/dotnet/api/system.guid)</span></span>  
    
    <span data-ttu-id="0e2a0-117">Dados da coluna para a coluna de chave atual do índice atual.</span><span class="sxs-lookup"><span data-stu-id="0e2a0-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="0e2a0-118">grbit</span><span class="sxs-lookup"><span data-stu-id="0e2a0-118">grbit</span></span>  
    <span data-ttu-id="0e2a0-119">Tipo: [Microsoft. ISAM. ESENT. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0e2a0-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0e2a0-120">Opções de chave.</span><span class="sxs-lookup"><span data-stu-id="0e2a0-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e2a0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e2a0-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e2a0-122">Referência</span><span class="sxs-lookup"><span data-stu-id="0e2a0-122">Reference</span></span>

[<span data-ttu-id="0e2a0-123">Classe de API</span><span class="sxs-lookup"><span data-stu-id="0e2a0-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0e2a0-124">Membros da API</span><span class="sxs-lookup"><span data-stu-id="0e2a0-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0e2a0-125">Sobrecarga de MakeKey</span><span class="sxs-lookup"><span data-stu-id="0e2a0-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="0e2a0-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0e2a0-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

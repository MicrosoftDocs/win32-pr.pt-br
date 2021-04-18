---
description: 'Saiba mais sobre: método API. JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)'
title: Método API. JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, Int32, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100765
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f6d77914a3dc4728626db8e4ffe271851099e5e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815464"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-int32-movegrbit"></a><span data-ttu-id="66261-103">Método API. JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</span><span class="sxs-lookup"><span data-stu-id="66261-103">Api.JetMove method (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</span></span>

<span data-ttu-id="66261-104">Navegar por um índice.</span><span class="sxs-lookup"><span data-stu-id="66261-104">Navigate through an index.</span></span> <span data-ttu-id="66261-105">O cursor pode ser posicionado no início ou no final do índice e movido para trás e encaminhado por um número especificado de entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="66261-105">The cursor can be positioned at the start or end of the index and moved backwards and forwards by a specified number of index entries.</span></span> <span data-ttu-id="66261-106">Consulte também [TryMoveFirst (JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast (JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext (JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious (JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span><span class="sxs-lookup"><span data-stu-id="66261-106">Also see [TryMoveFirst(JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast(JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext(JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious(JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span></span>

<span data-ttu-id="66261-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66261-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="66261-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="66261-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66261-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66261-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As Integer, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As Integer
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="66261-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66261-110">Parameters</span></span>

  - <span data-ttu-id="66261-111">sesid</span><span class="sxs-lookup"><span data-stu-id="66261-111">sesid</span></span>  
    <span data-ttu-id="66261-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66261-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="66261-113">A sessão a ser usada para a chamada.</span><span class="sxs-lookup"><span data-stu-id="66261-113">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="66261-114">TableID</span><span class="sxs-lookup"><span data-stu-id="66261-114">tableid</span></span>  
    <span data-ttu-id="66261-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66261-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="66261-116">O cursor a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="66261-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="66261-117">numRows</span><span class="sxs-lookup"><span data-stu-id="66261-117">numRows</span></span>  
    <span data-ttu-id="66261-118">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="66261-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="66261-119">Um deslocamento que indica a distância de movimentação do cursor.</span><span class="sxs-lookup"><span data-stu-id="66261-119">An offset which indicates how far to move the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="66261-120">grbit</span><span class="sxs-lookup"><span data-stu-id="66261-120">grbit</span></span>  
    <span data-ttu-id="66261-121">Tipo: [Microsoft. ISAM. ESENT. Interop. MoveGrbit](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="66261-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="66261-122">Opções de movimentação.</span><span class="sxs-lookup"><span data-stu-id="66261-122">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="66261-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="66261-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66261-124">Referência</span><span class="sxs-lookup"><span data-stu-id="66261-124">Reference</span></span>

[<span data-ttu-id="66261-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="66261-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="66261-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="66261-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="66261-127">Sobrecarga de JetMove</span><span class="sxs-lookup"><span data-stu-id="66261-127">JetMove overload</span></span>](./api.jetmove-method.md)

[<span data-ttu-id="66261-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="66261-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

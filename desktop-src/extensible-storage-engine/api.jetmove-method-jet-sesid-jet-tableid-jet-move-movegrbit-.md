---
description: 'Saiba mais sobre: método API. JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)'
title: Método API. JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100766
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5b6eeaf8d728cf63304141614caaf9598bcc6c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663240"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-jet_move-movegrbit"></a><span data-ttu-id="013a9-103">Método API. JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)</span><span class="sxs-lookup"><span data-stu-id="013a9-103">Api.JetMove method (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)</span></span>

<span data-ttu-id="013a9-104">Navegar por um índice.</span><span class="sxs-lookup"><span data-stu-id="013a9-104">Navigate through an index.</span></span> <span data-ttu-id="013a9-105">O cursor pode ser posicionado no início ou no final do índice e movido para trás e encaminhado por um número especificado de entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="013a9-105">The cursor can be positioned at the start or end of the index and moved backwards and forwards by a specified number of index entries.</span></span> <span data-ttu-id="013a9-106">Consulte também [TryMoveFirst (JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast (JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext (JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious (JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span><span class="sxs-lookup"><span data-stu-id="013a9-106">Also see [TryMoveFirst(JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast(JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext(JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious(JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span></span>

<span data-ttu-id="013a9-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="013a9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="013a9-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="013a9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="013a9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="013a9-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As JET_Move, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As JET_Move
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="013a9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="013a9-110">Parameters</span></span>

  - <span data-ttu-id="013a9-111">sesid</span><span class="sxs-lookup"><span data-stu-id="013a9-111">sesid</span></span>  
    <span data-ttu-id="013a9-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="013a9-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="013a9-113">A sessão a ser usada para a chamada.</span><span class="sxs-lookup"><span data-stu-id="013a9-113">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="013a9-114">TableID</span><span class="sxs-lookup"><span data-stu-id="013a9-114">tableid</span></span>  
    <span data-ttu-id="013a9-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="013a9-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="013a9-116">O cursor a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="013a9-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="013a9-117">numRows</span><span class="sxs-lookup"><span data-stu-id="013a9-117">numRows</span></span>  
    <span data-ttu-id="013a9-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_Move](./jet-move-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="013a9-118">Type: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span></span>  
    
    <span data-ttu-id="013a9-119">Um deslocamento que indica a distância de movimentação do cursor.</span><span class="sxs-lookup"><span data-stu-id="013a9-119">An offset which indicates how far to move the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="013a9-120">grbit</span><span class="sxs-lookup"><span data-stu-id="013a9-120">grbit</span></span>  
    <span data-ttu-id="013a9-121">Tipo: [Microsoft. ISAM. ESENT. Interop. MoveGrbit](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="013a9-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="013a9-122">Opções de movimentação.</span><span class="sxs-lookup"><span data-stu-id="013a9-122">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="013a9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="013a9-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="013a9-124">Referência</span><span class="sxs-lookup"><span data-stu-id="013a9-124">Reference</span></span>

[<span data-ttu-id="013a9-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="013a9-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="013a9-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="013a9-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="013a9-127">Sobrecarga de JetMove</span><span class="sxs-lookup"><span data-stu-id="013a9-127">JetMove overload</span></span>](./api.jetmove-method.md)

[<span data-ttu-id="013a9-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="013a9-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

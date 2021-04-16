---
description: 'Saiba mais sobre: método API. TryMove'
title: Método API. TryMove
TOCTitle: 'TryMove method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymove(v=EXCHG.10)
ms:contentKeyID: 55100883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMove
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d4b3aa596bb5e813d87dcc6f278112fe1e4cbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761245"
---
# <a name="apitrymove-method"></a><span data-ttu-id="31005-103">Método API. TryMove</span><span class="sxs-lookup"><span data-stu-id="31005-103">Api.TryMove method</span></span>

<span data-ttu-id="31005-104">Tente navegar por um índice.</span><span class="sxs-lookup"><span data-stu-id="31005-104">Try to navigate through an index.</span></span> <span data-ttu-id="31005-105">Se a navegação for realizada com sucesso, esse método retornará true.</span><span class="sxs-lookup"><span data-stu-id="31005-105">If the navigation succeeds this method returns true.</span></span> <span data-ttu-id="31005-106">Se não houver registro para navegar para esse método retornará false; uma exceção será lançada para outros erros.</span><span class="sxs-lookup"><span data-stu-id="31005-106">If there is no record to navigate to this method returns false; an exception will be thrown for other errors.</span></span>

<span data-ttu-id="31005-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="31005-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="31005-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="31005-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="31005-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31005-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    move As JET_Move, _
    grbit As MoveGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim move As JET_Move
Dim grbit As MoveGrbit
Dim returnValue As Boolean

returnValue = Api.TryMove(sesid, _
    tableid, move, grbit)
```

``` csharp
public static bool TryMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move move,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="31005-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31005-110">Parameters</span></span>

  - <span data-ttu-id="31005-111">sesid</span><span class="sxs-lookup"><span data-stu-id="31005-111">sesid</span></span>  
    <span data-ttu-id="31005-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="31005-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="31005-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="31005-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="31005-114">TableID</span><span class="sxs-lookup"><span data-stu-id="31005-114">tableid</span></span>  
    <span data-ttu-id="31005-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="31005-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="31005-116">O cursor a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="31005-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="31005-117">move</span><span class="sxs-lookup"><span data-stu-id="31005-117">move</span></span>  
    <span data-ttu-id="31005-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_Move](./jet-move-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="31005-118">Type: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span></span>  
    
    <span data-ttu-id="31005-119">A direção da movimentação.</span><span class="sxs-lookup"><span data-stu-id="31005-119">The direction to move in.</span></span>

<!-- end list -->

  - <span data-ttu-id="31005-120">grbit</span><span class="sxs-lookup"><span data-stu-id="31005-120">grbit</span></span>  
    <span data-ttu-id="31005-121">Tipo: [Microsoft. ISAM. ESENT. Interop. MoveGrbit](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="31005-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="31005-122">Opções de movimentação.</span><span class="sxs-lookup"><span data-stu-id="31005-122">Move options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31005-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31005-123">Return value</span></span>

<span data-ttu-id="31005-124">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="31005-124">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="31005-125">True se a movimentação tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="31005-125">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="31005-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="31005-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31005-127">Referência</span><span class="sxs-lookup"><span data-stu-id="31005-127">Reference</span></span>

[<span data-ttu-id="31005-128">Classe de API</span><span class="sxs-lookup"><span data-stu-id="31005-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="31005-129">Membros da API</span><span class="sxs-lookup"><span data-stu-id="31005-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="31005-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="31005-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Saiba mais sobre: método Windows8Api. JetSetCursorFilter'
title: Método Windows8Api. JetSetCursorFilter (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetSetCursorFilter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN[],Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetcursorfilter(v=EXCHG.10)
ms:contentKeyID: 55104447
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0137c25ee6ab548537d797af0a00a7ffcd1f6d5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761291"
---
# <a name="windows8apijetsetcursorfilter-method"></a><span data-ttu-id="5392d-103">Método Windows8Api. JetSetCursorFilter</span><span class="sxs-lookup"><span data-stu-id="5392d-103">Windows8Api.JetSetCursorFilter method</span></span>

<span data-ttu-id="5392d-104">Defina uma matriz de filtros simples para [JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span><span class="sxs-lookup"><span data-stu-id="5392d-104">Set an array of simple filters for [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span></span>

<span data-ttu-id="5392d-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5392d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="5392d-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5392d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5392d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5392d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCursorFilter ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    filters As JET_INDEX_COLUMN(), _
    grbit As CursorFilterGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim filters As JET_INDEX_COLUMN()
Dim grbit As CursorFilterGrbitWindows8Api.JetSetCursorFilter(sesid, tableid, _
    filters, grbit)
```

``` csharp
public static void JetSetCursorFilter(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_COLUMN[] filters,
    CursorFilterGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5392d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5392d-108">Parameters</span></span>

  - <span data-ttu-id="5392d-109">sesid</span><span class="sxs-lookup"><span data-stu-id="5392d-109">sesid</span></span>  
    <span data-ttu-id="5392d-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5392d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5392d-111">A sessão a ser usada para a chamada.</span><span class="sxs-lookup"><span data-stu-id="5392d-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="5392d-112">TableID</span><span class="sxs-lookup"><span data-stu-id="5392d-112">tableid</span></span>  
    <span data-ttu-id="5392d-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5392d-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5392d-114">O cursor a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="5392d-114">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="5392d-115">filtros</span><span class="sxs-lookup"><span data-stu-id="5392d-115">filters</span></span>  
    <span data-ttu-id="5392d-116">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="5392d-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="5392d-117">Filtros de registro simples.</span><span class="sxs-lookup"><span data-stu-id="5392d-117">Simple record filters.</span></span>

<!-- end list -->

  - <span data-ttu-id="5392d-118">grbit</span><span class="sxs-lookup"><span data-stu-id="5392d-118">grbit</span></span>  
    <span data-ttu-id="5392d-119">Tipo: [Microsoft. ISAM. ESENT. Interop. Windows8. CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5392d-119">Type: [Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5392d-120">Opções de movimentação.</span><span class="sxs-lookup"><span data-stu-id="5392d-120">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="5392d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5392d-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5392d-122">Referência</span><span class="sxs-lookup"><span data-stu-id="5392d-122">Reference</span></span>

[<span data-ttu-id="5392d-123">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="5392d-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="5392d-124">Membros do Windows8Api</span><span class="sxs-lookup"><span data-stu-id="5392d-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="5392d-125">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="5392d-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)

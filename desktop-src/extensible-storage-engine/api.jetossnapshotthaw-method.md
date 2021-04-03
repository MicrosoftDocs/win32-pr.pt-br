---
description: 'Saiba mais sobre: método API. JetOSSnapshotThaw'
title: Método API. JetOSSnapshotThaw
TOCTitle: 'JetOSSnapshotThaw method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.SnapshotThawGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotthaw(v=EXCHG.10)
ms:contentKeyID: 55100780
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f3fe0bc04586dddade7a9723720bbd3c994c516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837163"
---
# <a name="apijetossnapshotthaw-method"></a><span data-ttu-id="dbb88-103">Método API. JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="dbb88-103">Api.JetOSSnapshotThaw method</span></span>

<span data-ttu-id="dbb88-104">Notifica o mecanismo de que ele pode retomar as operações de e/s normais após um período de congelamento e um instantâneo bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dbb88-104">Notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="dbb88-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dbb88-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dbb88-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dbb88-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb88-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbb88-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotThaw ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotThawGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotThawGrbitApi.JetOSSnapshotThaw(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotThaw(
    JET_OSSNAPID snapshot,
    SnapshotThawGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="dbb88-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbb88-108">Parameters</span></span>

  - <span data-ttu-id="dbb88-109">instantâneo</span><span class="sxs-lookup"><span data-stu-id="dbb88-109">snapshot</span></span>  
    <span data-ttu-id="dbb88-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dbb88-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="dbb88-111">A ID do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="dbb88-111">The ID of the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="dbb88-112">grbit</span><span class="sxs-lookup"><span data-stu-id="dbb88-112">grbit</span></span>  
    <span data-ttu-id="dbb88-113">Tipo: [Microsoft. ISAM. ESENT. Interop. SnapshotThawGrbit](./snapshotthawgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dbb88-113">Type: [Microsoft.Isam.Esent.Interop.SnapshotThawGrbit](./snapshotthawgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="dbb88-114">Descongelar opções.</span><span class="sxs-lookup"><span data-stu-id="dbb88-114">Thaw options.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbb88-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbb88-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dbb88-116">Referência</span><span class="sxs-lookup"><span data-stu-id="dbb88-116">Reference</span></span>

[<span data-ttu-id="dbb88-117">Classe de API</span><span class="sxs-lookup"><span data-stu-id="dbb88-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dbb88-118">Membros da API</span><span class="sxs-lookup"><span data-stu-id="dbb88-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dbb88-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dbb88-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

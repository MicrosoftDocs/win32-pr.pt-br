---
description: 'Saiba mais sobre: método VistaApi. JetOSSnapshotEnd'
title: Método VistaApi. JetOSSnapshotEnd (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetOSSnapshotEnd method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotend(v=EXCHG.10)
ms:contentKeyID: 55104196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 291d83929940a9f66f4e16c5088e6ec08187f908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647338"
---
# <a name="vistaapijetossnapshotend-method"></a><span data-ttu-id="b0693-103">Método VistaApi. JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="b0693-103">VistaApi.JetOSSnapshotEnd method</span></span>

<span data-ttu-id="b0693-104">Notifica o mecanismo de que a sessão de instantâneo foi concluída.</span><span class="sxs-lookup"><span data-stu-id="b0693-104">Notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="b0693-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b0693-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b0693-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b0693-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0693-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0693-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotEnd ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotEndGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotEndGrbitVistaApi.JetOSSnapshotEnd(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotEnd(
    JET_OSSNAPID snapshot,
    SnapshotEndGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b0693-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0693-108">Parameters</span></span>

  - <span data-ttu-id="b0693-109">instantâneo</span><span class="sxs-lookup"><span data-stu-id="b0693-109">snapshot</span></span>  
    <span data-ttu-id="b0693-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b0693-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="b0693-111">O identificador da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b0693-111">The identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="b0693-112">grbit</span><span class="sxs-lookup"><span data-stu-id="b0693-112">grbit</span></span>  
    <span data-ttu-id="b0693-113">Tipo: [Microsoft. ISAM. ESENT. Interop. vista. SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b0693-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b0693-114">Opções de fim do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b0693-114">Snapshot end options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0693-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0693-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0693-116">Referência</span><span class="sxs-lookup"><span data-stu-id="b0693-116">Reference</span></span>

[<span data-ttu-id="b0693-117">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="b0693-117">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="b0693-118">Membros do VistaApi</span><span class="sxs-lookup"><span data-stu-id="b0693-118">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="b0693-119">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="b0693-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

---
description: 'Saiba mais sobre: método VistaApi. JetOSSnapshotTruncateLog'
title: Método VistaApi. JetOSSnapshotTruncateLog (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetOSSnapshotTruncateLog method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncatelog(v=EXCHG.10)
ms:contentKeyID: 55104308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0af8054bc414ea5dbd6c7225fa9e2cd7117c74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780213"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a><span data-ttu-id="424b2-103">Método VistaApi. JetOSSnapshotTruncateLog</span><span class="sxs-lookup"><span data-stu-id="424b2-103">VistaApi.JetOSSnapshotTruncateLog method</span></span>

<span data-ttu-id="424b2-104">Habilita o truncamento de log para todas as instâncias que fazem parte da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="424b2-104">Enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="424b2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="424b2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="424b2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="424b2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="424b2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="424b2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLog ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLog(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLog(
    JET_OSSNAPID snapshot,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="424b2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="424b2-108">Parameters</span></span>

  - <span data-ttu-id="424b2-109">instantâneo</span><span class="sxs-lookup"><span data-stu-id="424b2-109">snapshot</span></span>  
    <span data-ttu-id="424b2-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="424b2-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="424b2-111">O identificador do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="424b2-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="424b2-112">grbit</span><span class="sxs-lookup"><span data-stu-id="424b2-112">grbit</span></span>  
    <span data-ttu-id="424b2-113">Tipo: [Microsoft. ISAM. ESENT. Interop. vista. SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="424b2-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="424b2-114">Opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="424b2-114">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="424b2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="424b2-115">Remarks</span></span>

<span data-ttu-id="424b2-116">Essa função deve ser chamada somente se o instantâneo tiver sido criado com a opção [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) .</span><span class="sxs-lookup"><span data-stu-id="424b2-116">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="424b2-117">Caso contrário, a sessão de instantâneo termina após a chamada para [JetOSSnapshotThaw (JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span><span class="sxs-lookup"><span data-stu-id="424b2-117">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="424b2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="424b2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="424b2-119">Referência</span><span class="sxs-lookup"><span data-stu-id="424b2-119">Reference</span></span>

[<span data-ttu-id="424b2-120">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="424b2-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="424b2-121">Membros do VistaApi</span><span class="sxs-lookup"><span data-stu-id="424b2-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="424b2-122">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="424b2-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

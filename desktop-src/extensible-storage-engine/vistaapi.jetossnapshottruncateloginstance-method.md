---
description: 'Saiba mais sobre: método VistaApi. JetOSSnapshotTruncateLogInstance'
title: Método VistaApi. JetOSSnapshotTruncateLogInstance (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75d694629585a730f5c1c7b9b08bb7b06e735cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837444"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a><span data-ttu-id="6355c-103">Método VistaApi. JetOSSnapshotTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="6355c-103">VistaApi.JetOSSnapshotTruncateLogInstance method</span></span>

<span data-ttu-id="6355c-104">Trunca o log para uma instância especificada durante uma sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6355c-104">Truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="6355c-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6355c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="6355c-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6355c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6355c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6355c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6355c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6355c-108">Parameters</span></span>

  - <span data-ttu-id="6355c-109">instantâneo</span><span class="sxs-lookup"><span data-stu-id="6355c-109">snapshot</span></span>  
    <span data-ttu-id="6355c-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6355c-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="6355c-111">O identificador do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6355c-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="6355c-112">instance</span><span class="sxs-lookup"><span data-stu-id="6355c-112">instance</span></span>  
    <span data-ttu-id="6355c-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6355c-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="6355c-114">A instância para a qual truncar o log.</span><span class="sxs-lookup"><span data-stu-id="6355c-114">The instance to truncat the log for.</span></span>

<!-- end list -->

  - <span data-ttu-id="6355c-115">grbit</span><span class="sxs-lookup"><span data-stu-id="6355c-115">grbit</span></span>  
    <span data-ttu-id="6355c-116">Tipo: [Microsoft. ISAM. ESENT. Interop. vista. SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6355c-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6355c-117">Opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="6355c-117">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="6355c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6355c-118">Remarks</span></span>

<span data-ttu-id="6355c-119">Essa função deve ser chamada somente se o instantâneo tiver sido criado com a opção [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) .</span><span class="sxs-lookup"><span data-stu-id="6355c-119">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="6355c-120">Caso contrário, a sessão de instantâneo termina após a chamada para [JetOSSnapshotThaw (JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span><span class="sxs-lookup"><span data-stu-id="6355c-120">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6355c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6355c-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6355c-122">Referência</span><span class="sxs-lookup"><span data-stu-id="6355c-122">Reference</span></span>

[<span data-ttu-id="6355c-123">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="6355c-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="6355c-124">Membros do VistaApi</span><span class="sxs-lookup"><span data-stu-id="6355c-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="6355c-125">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="6355c-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

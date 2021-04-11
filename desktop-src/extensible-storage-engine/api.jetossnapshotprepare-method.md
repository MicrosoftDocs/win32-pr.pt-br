---
description: 'Saiba mais sobre: método API. JetOSSnapshotPrepare'
title: Método API. JetOSSnapshotPrepare
TOCTitle: 'JetOSSnapshotPrepare method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare(Microsoft.Isam.Esent.Interop.JET_OSSNAPID@,Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotprepare(v=EXCHG.10)
ms:contentKeyID: 55100779
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ac304cf522e7c99a2495925da8571b2139c0a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171766"
---
# <a name="apijetossnapshotprepare-method"></a><span data-ttu-id="bff37-103">Método API. JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="bff37-103">Api.JetOSSnapshotPrepare method</span></span>

<span data-ttu-id="bff37-104">Inicia a preparação para uma sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="bff37-104">Begins the preparations for a snapshot session.</span></span> <span data-ttu-id="bff37-105">Uma sessão de instantâneo é um intervalo de tempo curto no qual o mecanismo não emite nenhum IOs de gravação para o disco, para que o mecanismo possa participar de uma sessão de instantâneo de volume (quando controlada por um gravador de instantâneo).</span><span class="sxs-lookup"><span data-stu-id="bff37-105">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="bff37-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bff37-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bff37-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bff37-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bff37-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bff37-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepare ( _
    <OutAttribute> ByRef snapshot As JET_OSSNAPID, _
    grbit As SnapshotPrepareGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotPrepareGrbitApi.JetOSSnapshotPrepare(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotPrepare(
    out JET_OSSNAPID snapshot,
    SnapshotPrepareGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bff37-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bff37-109">Parameters</span></span>

  - <span data-ttu-id="bff37-110">instantâneo</span><span class="sxs-lookup"><span data-stu-id="bff37-110">snapshot</span></span>  
    <span data-ttu-id="bff37-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bff37-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="bff37-112">Retorna a ID da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="bff37-112">Returns the ID of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="bff37-113">grbit</span><span class="sxs-lookup"><span data-stu-id="bff37-113">grbit</span></span>  
    <span data-ttu-id="bff37-114">Tipo: [Microsoft. ISAM. ESENT. Interop. SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bff37-114">Type: [Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bff37-115">Opções de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="bff37-115">Snapshot options.</span></span>

## <a name="see-also"></a><span data-ttu-id="bff37-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="bff37-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bff37-117">Referência</span><span class="sxs-lookup"><span data-stu-id="bff37-117">Reference</span></span>

[<span data-ttu-id="bff37-118">Classe de API</span><span class="sxs-lookup"><span data-stu-id="bff37-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bff37-119">Membros da API</span><span class="sxs-lookup"><span data-stu-id="bff37-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bff37-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bff37-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

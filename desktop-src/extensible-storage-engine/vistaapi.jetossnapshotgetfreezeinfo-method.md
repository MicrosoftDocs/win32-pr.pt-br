---
description: 'Saiba mais sobre: método VistaApi. JetOSSnapshotGetFreezeInfo'
title: Método VistaApi. JetOSSnapshotGetFreezeInfo (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetOSSnapshotGetFreezeInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotgetfreezeinfo(v=EXCHG.10)
ms:contentKeyID: 55104199
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84b8f33f1fcac280e8fee65c1092c8fccdec3b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759686"
---
# <a name="vistaapijetossnapshotgetfreezeinfo-method"></a><span data-ttu-id="e9aaa-103">Método VistaApi. JetOSSnapshotGetFreezeInfo</span><span class="sxs-lookup"><span data-stu-id="e9aaa-103">VistaApi.JetOSSnapshotGetFreezeInfo method</span></span>

<span data-ttu-id="e9aaa-104">Recupera a lista de instâncias e bancos de dados que fazem parte da sessão de instantâneo em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="e9aaa-104">Retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="e9aaa-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e9aaa-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e9aaa-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e9aaa-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e9aaa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9aaa-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotGetFreezeInfo ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotGetFreezeInfoGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotGetFreezeInfoGrbitVistaApi.JetOSSnapshotGetFreezeInfo(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotGetFreezeInfo(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotGetFreezeInfoGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e9aaa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9aaa-108">Parameters</span></span>

  - <span data-ttu-id="e9aaa-109">instantâneo</span><span class="sxs-lookup"><span data-stu-id="e9aaa-109">snapshot</span></span>  
    <span data-ttu-id="e9aaa-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9aaa-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="e9aaa-111">O identificador da sessão de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="e9aaa-111">The identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9aaa-112">numInstances</span><span class="sxs-lookup"><span data-stu-id="e9aaa-112">numInstances</span></span>  
    <span data-ttu-id="e9aaa-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e9aaa-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e9aaa-114">Retorna o número de instâncias.</span><span class="sxs-lookup"><span data-stu-id="e9aaa-114">Returns the number of instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9aaa-115">instances</span><span class="sxs-lookup"><span data-stu-id="e9aaa-115">instances</span></span>  
    <span data-ttu-id="e9aaa-116">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="e9aaa-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="e9aaa-117">Retorna informações sobre as instâncias.</span><span class="sxs-lookup"><span data-stu-id="e9aaa-117">Returns information about the instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9aaa-118">grbit</span><span class="sxs-lookup"><span data-stu-id="e9aaa-118">grbit</span></span>  
    <span data-ttu-id="e9aaa-119">Tipo: [Microsoft. ISAM. ESENT. Interop. vista. SnapshotGetFreezeInfoGrbit](./snapshotgetfreezeinfogrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e9aaa-119">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit](./snapshotgetfreezeinfogrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e9aaa-120">Opções para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="e9aaa-120">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9aaa-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9aaa-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e9aaa-122">Referência</span><span class="sxs-lookup"><span data-stu-id="e9aaa-122">Reference</span></span>

[<span data-ttu-id="e9aaa-123">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="e9aaa-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="e9aaa-124">Membros do VistaApi</span><span class="sxs-lookup"><span data-stu-id="e9aaa-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="e9aaa-125">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="e9aaa-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

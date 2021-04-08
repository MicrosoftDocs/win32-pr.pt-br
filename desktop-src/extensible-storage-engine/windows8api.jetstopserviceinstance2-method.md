---
description: 'Saiba mais sobre: método Windows8Api. JetStopServiceInstance2'
title: Método Windows8Api. JetStopServiceInstance2 (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetStopServiceInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetstopserviceinstance2(v=EXCHG.10)
ms:contentKeyID: 55104460
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0821a00016eb9cd2c511ee37889e0ddaa0b76edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010641"
---
# <a name="windows8apijetstopserviceinstance2-method"></a><span data-ttu-id="05599-103">Método Windows8Api. JetStopServiceInstance2</span><span class="sxs-lookup"><span data-stu-id="05599-103">Windows8Api.JetStopServiceInstance2 method</span></span>

<span data-ttu-id="05599-104">Prepara uma instância para encerramento.</span><span class="sxs-lookup"><span data-stu-id="05599-104">Prepares an instance for termination.</span></span> <span data-ttu-id="05599-105">Também pode ser usado para retomar uma pausa anterior.</span><span class="sxs-lookup"><span data-stu-id="05599-105">Can also be used to resume a previous quiescing.</span></span>

<span data-ttu-id="05599-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="05599-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="05599-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="05599-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="05599-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05599-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetStopServiceInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As StopServiceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As StopServiceGrbitWindows8Api.JetStopServiceInstance2(instance, _
    grbit)
```

``` csharp
public static void JetStopServiceInstance2(
    JET_INSTANCE instance,
    StopServiceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="05599-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05599-109">Parameters</span></span>

  - <span data-ttu-id="05599-110">instance</span><span class="sxs-lookup"><span data-stu-id="05599-110">instance</span></span>  
    <span data-ttu-id="05599-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="05599-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="05599-112">A instância (em execução) a ser usada.</span><span class="sxs-lookup"><span data-stu-id="05599-112">The (running) instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="05599-113">grbit</span><span class="sxs-lookup"><span data-stu-id="05599-113">grbit</span></span>  
    <span data-ttu-id="05599-114">Tipo: [Microsoft. ISAM. ESENT. Interop. Windows8. StopServiceGrbit](./stopservicegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="05599-114">Type: [Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit](./stopservicegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="05599-115">As opções para parar ou retomar a instância.</span><span class="sxs-lookup"><span data-stu-id="05599-115">The options to stop or resume the instance.</span></span>

## <a name="see-also"></a><span data-ttu-id="05599-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="05599-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="05599-117">Referência</span><span class="sxs-lookup"><span data-stu-id="05599-117">Reference</span></span>

[<span data-ttu-id="05599-118">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="05599-118">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="05599-119">Membros do Windows8Api</span><span class="sxs-lookup"><span data-stu-id="05599-119">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="05599-120">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="05599-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)

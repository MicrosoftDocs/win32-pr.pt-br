---
description: 'Saiba mais sobre: método VistaApi. JetGetInstanceMiscInfo'
title: Método VistaApi. JetGetInstanceMiscInfo (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetGetInstanceMiscInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE@,Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetinstancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 55104187
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 204beee343a717d5b45d8003e123bbbe186437d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827676"
---
# <a name="vistaapijetgetinstancemiscinfo-method"></a><span data-ttu-id="7da0e-103">Método VistaApi. JetGetInstanceMiscInfo</span><span class="sxs-lookup"><span data-stu-id="7da0e-103">VistaApi.JetGetInstanceMiscInfo method</span></span>

<span data-ttu-id="7da0e-104">Recupera informações sobre uma instância do.</span><span class="sxs-lookup"><span data-stu-id="7da0e-104">Retrieves information about an instance.</span></span>

<span data-ttu-id="7da0e-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7da0e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="7da0e-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7da0e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7da0e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7da0e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceMiscInfo ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef signature As JET_SIGNATURE, _
    infoLevel As JET_InstanceMiscInfo _
)
'Usage
Dim instance As JET_INSTANCE
Dim signature As JET_SIGNATURE
Dim infoLevel As JET_InstanceMiscInfoVistaApi.JetGetInstanceMiscInfo(instance, _
    signature, infoLevel)
```

``` csharp
public static void JetGetInstanceMiscInfo(
    JET_INSTANCE instance,
    out JET_SIGNATURE signature,
    JET_InstanceMiscInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="7da0e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7da0e-108">Parameters</span></span>

  - <span data-ttu-id="7da0e-109">instance</span><span class="sxs-lookup"><span data-stu-id="7da0e-109">instance</span></span>  
    <span data-ttu-id="7da0e-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7da0e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7da0e-111">A instância da qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="7da0e-111">The instance to get information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="7da0e-112">assinatura</span><span class="sxs-lookup"><span data-stu-id="7da0e-112">signature</span></span>  
    <span data-ttu-id="7da0e-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7da0e-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="7da0e-114">Informações recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7da0e-114">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="7da0e-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="7da0e-115">infoLevel</span></span>  
    <span data-ttu-id="7da0e-116">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7da0e-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="7da0e-117">O tipo de informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7da0e-117">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="7da0e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7da0e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7da0e-119">Referência</span><span class="sxs-lookup"><span data-stu-id="7da0e-119">Reference</span></span>

[<span data-ttu-id="7da0e-120">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="7da0e-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="7da0e-121">Membros do VistaApi</span><span class="sxs-lookup"><span data-stu-id="7da0e-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="7da0e-122">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="7da0e-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

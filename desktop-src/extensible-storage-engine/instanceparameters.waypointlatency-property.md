---
description: 'Saiba mais sobre a propriedade: Instanceparameters. WaypointLatency'
title: Propriedade instanceparameters. WaypointLatency
TOCTitle: 'WaypointLatency property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55103325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_WaypointLatency
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d7d837d7fff804926529ec67780e319d85031f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796218"
---
# <a name="instanceparameterswaypointlatency-property"></a><span data-ttu-id="85765-103">Propriedade instanceparameters. WaypointLatency</span><span class="sxs-lookup"><span data-stu-id="85765-103">InstanceParameters.WaypointLatency property</span></span>

<span data-ttu-id="85765-104">Obtém ou define um número de logs para os quais o ESENT adiará as liberações de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="85765-104">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="85765-105">Isso pode ser usado para aumentar a capacidade de recuperação do banco de dados se as falhas causarem a perda de arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="85765-105">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="85765-106">Com suporte no Windows 7 e em cima.</span><span class="sxs-lookup"><span data-stu-id="85765-106">Supported on Windows 7 and up.</span></span> <span data-ttu-id="85765-107">Ignorado no Windows XP, no Windows Server 2003, no Windows Vista e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="85765-107">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="85765-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="85765-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="85765-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="85765-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="85765-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="85765-110">Syntax</span></span>

``` vb
'Declaration
Public Property WaypointLatency As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.WaypointLatency

instance.WaypointLatency = value
```

``` csharp
public int WaypointLatency { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="85765-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="85765-111">Property value</span></span>

<span data-ttu-id="85765-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="85765-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="85765-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="85765-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="85765-114">Referência</span><span class="sxs-lookup"><span data-stu-id="85765-114">Reference</span></span>

[<span data-ttu-id="85765-115">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="85765-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="85765-116">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="85765-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="85765-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="85765-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Saiba mais sobre a propriedade: Instanceparameters. EnableIndexChecking'
title: Propriedade instanceparameters. EnableIndexChecking
TOCTitle: 'EnableIndexChecking property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enableindexchecking(v=EXCHG.10)
ms:contentKeyID: 55103567
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableIndexChecking
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableIndexChecking
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a3090c1e5c1e42aca3758496b1367f3932e123c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783218"
---
# <a name="instanceparametersenableindexchecking-property"></a><span data-ttu-id="b53d0-103">Propriedade instanceparameters. EnableIndexChecking</span><span class="sxs-lookup"><span data-stu-id="b53d0-103">InstanceParameters.EnableIndexChecking property</span></span>

<span data-ttu-id="b53d0-104">Obtém ou define um valor que indica se [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) verificará se há índices que foram compilados usando uma versão mais antiga da biblioteca NLS no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b53d0-104">Gets or sets a value indicating whether [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will check for indexes that were build using an older version of the NLS library in the operating system.</span></span>

<span data-ttu-id="b53d0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b53d0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b53d0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b53d0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b53d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b53d0-107">Syntax</span></span>

``` vb
'Declaration
Public Property EnableIndexChecking As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.EnableIndexChecking

instance.EnableIndexChecking = value
```

``` csharp
public bool EnableIndexChecking { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b53d0-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b53d0-108">Property value</span></span>

<span data-ttu-id="b53d0-109">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b53d0-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b53d0-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="b53d0-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b53d0-111">Referência</span><span class="sxs-lookup"><span data-stu-id="b53d0-111">Reference</span></span>

[<span data-ttu-id="b53d0-112">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="b53d0-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="b53d0-113">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="b53d0-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="b53d0-114">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b53d0-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Saiba mais sobre a propriedade: Instanceparameters. MaxCursors'
title: Propriedade instanceparameters. MaxCursors
TOCTitle: 'MaxCursors property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxcursors(v=EXCHG.10)
ms:contentKeyID: 55103565
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxCursors
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 029ff7c41916e668f532be60f018870f30e487ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790351"
---
# <a name="instanceparametersmaxcursors-property"></a><span data-ttu-id="e6f1d-103">Propriedade instanceparameters. MaxCursors</span><span class="sxs-lookup"><span data-stu-id="e6f1d-103">InstanceParameters.MaxCursors property</span></span>

<span data-ttu-id="e6f1d-104">Obtém ou define o número de recursos de cursor reservados para esta instância.</span><span class="sxs-lookup"><span data-stu-id="e6f1d-104">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="e6f1d-105">Um recurso de cursor corresponde diretamente a um JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="e6f1d-105">A cursor resource directly corresponds to a JET_TABLEID.</span></span>

<span data-ttu-id="e6f1d-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6f1d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6f1d-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6f1d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f1d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6f1d-108">Syntax</span></span>

``` vb
'Declaration
Public Property MaxCursors As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxCursors

instance.MaxCursors = value
```

``` csharp
public int MaxCursors { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e6f1d-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e6f1d-109">Property value</span></span>

<span data-ttu-id="e6f1d-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e6f1d-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e6f1d-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6f1d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6f1d-112">Referência</span><span class="sxs-lookup"><span data-stu-id="e6f1d-112">Reference</span></span>

[<span data-ttu-id="e6f1d-113">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="e6f1d-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="e6f1d-114">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="e6f1d-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="e6f1d-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e6f1d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

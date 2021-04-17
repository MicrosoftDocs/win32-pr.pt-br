---
description: 'Saiba mais sobre a propriedade: Instanceparameters. OneDatabasePerSession'
title: Propriedade instanceparameters. OneDatabasePerSession
TOCTitle: 'OneDatabasePerSession property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.onedatabasepersession(v=EXCHG.10)
ms:contentKeyID: 55103319
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_OneDatabasePerSession
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_OneDatabasePerSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c130a00b8fcbcbcf6a8fc7bbdbbad6a4e36f218e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798235"
---
# <a name="instanceparametersonedatabasepersession-property"></a><span data-ttu-id="d40e3-103">Propriedade instanceparameters. OneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="d40e3-103">InstanceParameters.OneDatabasePerSession property</span></span>

<span data-ttu-id="d40e3-104">Obtém ou define um valor que indica se apenas um banco de dados pode ser aberto usando JetOpenDatabase por uma determinada sessão ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d40e3-104">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="d40e3-105">O banco de dados temporário é excluído dessa restrição.</span><span class="sxs-lookup"><span data-stu-id="d40e3-105">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="d40e3-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d40e3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d40e3-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d40e3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d40e3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d40e3-108">Syntax</span></span>

``` vb
'Declaration
Public Property OneDatabasePerSession As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.OneDatabasePerSession

instance.OneDatabasePerSession = value
```

``` csharp
public bool OneDatabasePerSession { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="d40e3-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d40e3-109">Property value</span></span>

<span data-ttu-id="d40e3-110">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="d40e3-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d40e3-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="d40e3-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d40e3-112">Referência</span><span class="sxs-lookup"><span data-stu-id="d40e3-112">Reference</span></span>

[<span data-ttu-id="d40e3-113">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="d40e3-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="d40e3-114">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="d40e3-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="d40e3-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d40e3-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

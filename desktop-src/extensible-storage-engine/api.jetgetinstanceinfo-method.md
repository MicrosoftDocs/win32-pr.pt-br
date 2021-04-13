---
description: 'Saiba mais sobre: método API. JetGetInstanceInfo'
title: Método API. JetGetInstanceInfo
TOCTitle: 'JetGetInstanceInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo(System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetinstanceinfo(v=EXCHG.10)
ms:contentKeyID: 55100729
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b618c0eb7bf6e861337ebb40a95cb75d4434038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164375"
---
# <a name="apijetgetinstanceinfo-method"></a><span data-ttu-id="380e1-103">Método API. JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="380e1-103">Api.JetGetInstanceInfo method</span></span>

<span data-ttu-id="380e1-104">Recupera informações sobre as instâncias que estão em execução.</span><span class="sxs-lookup"><span data-stu-id="380e1-104">Retrieves information about the instances that are running.</span></span>

<span data-ttu-id="380e1-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="380e1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="380e1-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="380e1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="380e1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="380e1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceInfo ( _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO() _
)
'Usage
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()

Api.JetGetInstanceInfo(numInstances, _
    instances)
```

``` csharp
public static void JetGetInstanceInfo(
    out int numInstances,
    out JET_INSTANCE_INFO[] instances
)
```

#### <a name="parameters"></a><span data-ttu-id="380e1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="380e1-108">Parameters</span></span>

  - <span data-ttu-id="380e1-109">numInstances</span><span class="sxs-lookup"><span data-stu-id="380e1-109">numInstances</span></span>  
    <span data-ttu-id="380e1-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="380e1-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="380e1-111">Retorna o número de instâncias.</span><span class="sxs-lookup"><span data-stu-id="380e1-111">Returns the number of instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="380e1-112">instances</span><span class="sxs-lookup"><span data-stu-id="380e1-112">instances</span></span>  
    <span data-ttu-id="380e1-113">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="380e1-113">Type: \[\]</span></span>  
    
    <span data-ttu-id="380e1-114">Retorna uma matriz de objetos de informações de instância, um para cada instância em execução.</span><span class="sxs-lookup"><span data-stu-id="380e1-114">Returns an array of instance info objects, one for each running instance.</span></span>

## <a name="see-also"></a><span data-ttu-id="380e1-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="380e1-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="380e1-116">Referência</span><span class="sxs-lookup"><span data-stu-id="380e1-116">Reference</span></span>

[<span data-ttu-id="380e1-117">Classe de API</span><span class="sxs-lookup"><span data-stu-id="380e1-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="380e1-118">Membros da API</span><span class="sxs-lookup"><span data-stu-id="380e1-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="380e1-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="380e1-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

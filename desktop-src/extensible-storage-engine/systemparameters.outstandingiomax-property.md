---
description: 'Saiba mais sobre: Propriedade SystemParameters. OutstandingIOMax'
title: Propriedade SystemParameters. OutstandingIOMax
TOCTitle: 'OutstandingIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.outstandingiomax(v=EXCHG.10)
ms:contentKeyID: 55104045
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.set_OutstandingIOMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7faf7af3aec16bc81fada5c8742b4c60595bedad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505938"
---
# <a name="systemparametersoutstandingiomax-property"></a><span data-ttu-id="a4d96-103">Propriedade SystemParameters. OutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="a4d96-103">SystemParameters.OutstandingIOMax property</span></span>

<span data-ttu-id="a4d96-104">Esse parâmetro controla quantas e/SS de arquivo de banco de dados podem ser enfileiradas por disco no sistema operacional do host ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a4d96-104">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="a4d96-105">Um valor maior para esse parâmetro pode ajudar significativamente o desempenho de um aplicativo de banco de dados grande.</span><span class="sxs-lookup"><span data-stu-id="a4d96-105">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="a4d96-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a4d96-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a4d96-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a4d96-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d96-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4d96-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property OutstandingIOMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.OutstandingIOMax

SystemParameters.OutstandingIOMax = value
```

``` csharp
public static int OutstandingIOMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="a4d96-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a4d96-109">Property value</span></span>

<span data-ttu-id="a4d96-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a4d96-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a4d96-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4d96-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a4d96-112">Referência</span><span class="sxs-lookup"><span data-stu-id="a4d96-112">Reference</span></span>

[<span data-ttu-id="a4d96-113">Classe SystemParameters</span><span class="sxs-lookup"><span data-stu-id="a4d96-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="a4d96-114">Membros do SystemParameters</span><span class="sxs-lookup"><span data-stu-id="a4d96-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="a4d96-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a4d96-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

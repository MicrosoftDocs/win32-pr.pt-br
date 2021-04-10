---
description: 'Saiba mais sobre: Propriedade SystemParameters. CacheSizeMax'
title: Propriedade SystemParameters. CacheSizeMax
TOCTitle: 'CacheSizeMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesizemax(v=EXCHG.10)
ms:contentKeyID: 55104037
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7b03df288a0263cf6b79281f5ed79330dfd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171615"
---
# <a name="systemparameterscachesizemax-property"></a><span data-ttu-id="f1588-103">Propriedade SystemParameters. CacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="f1588-103">SystemParameters.CacheSizeMax property</span></span>

<span data-ttu-id="f1588-104">Obtém ou define o tamanho máximo do cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f1588-104">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="f1588-105">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f1588-105">The size is in database pages.</span></span> <span data-ttu-id="f1588-106">Se esse parâmetro for deixado para seu valor padrão, o tamanho máximo do cache será definido como o tamanho da memória física quando JetInit for chamado.</span><span class="sxs-lookup"><span data-stu-id="f1588-106">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span>

<span data-ttu-id="f1588-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f1588-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f1588-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f1588-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f1588-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1588-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSizeMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSizeMax

SystemParameters.CacheSizeMax = value
```

``` csharp
public static int CacheSizeMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="f1588-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f1588-110">Property value</span></span>

<span data-ttu-id="f1588-111">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f1588-111">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f1588-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1588-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f1588-113">Referência</span><span class="sxs-lookup"><span data-stu-id="f1588-113">Reference</span></span>

[<span data-ttu-id="f1588-114">Classe SystemParameters</span><span class="sxs-lookup"><span data-stu-id="f1588-114">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="f1588-115">Membros do SystemParameters</span><span class="sxs-lookup"><span data-stu-id="f1588-115">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="f1588-116">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f1588-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

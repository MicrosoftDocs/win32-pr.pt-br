---
description: 'Saiba mais sobre: Propriedade SystemParameters. CacheSize'
title: Propriedade SystemParameters.. CacheSize
TOCTitle: 'CacheSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesize(v=EXCHG.10)
ms:contentKeyID: 55104109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0981f02df3b807ab56fa20922d1e245f00c2df34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171737"
---
# <a name="systemparameterscachesize-property"></a><span data-ttu-id="3a830-103">Propriedade SystemParameters.. CacheSize</span><span class="sxs-lookup"><span data-stu-id="3a830-103">SystemParameters.CacheSize property</span></span>

<span data-ttu-id="3a830-104">Obtém ou define o tamanho do cache de banco de dados em páginas.</span><span class="sxs-lookup"><span data-stu-id="3a830-104">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="3a830-105">Por padrão, o cache do banco de dados ajustará automaticamente seu tamanho, a definição dessa propriedade com um valor diferente de zero fará com que o cache se ajuste ao tamanho do destino.</span><span class="sxs-lookup"><span data-stu-id="3a830-105">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span>

<span data-ttu-id="3a830-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3a830-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3a830-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3a830-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3a830-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a830-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSize As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSize

SystemParameters.CacheSize = value
```

``` csharp
public static int CacheSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3a830-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3a830-109">Property value</span></span>

<span data-ttu-id="3a830-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3a830-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3a830-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a830-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3a830-112">Referência</span><span class="sxs-lookup"><span data-stu-id="3a830-112">Reference</span></span>

[<span data-ttu-id="3a830-113">Classe SystemParameters</span><span class="sxs-lookup"><span data-stu-id="3a830-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="3a830-114">Membros do SystemParameters</span><span class="sxs-lookup"><span data-stu-id="3a830-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="3a830-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3a830-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

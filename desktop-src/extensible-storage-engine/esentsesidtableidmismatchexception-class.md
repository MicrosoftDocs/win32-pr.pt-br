---
description: 'Saiba mais sobre: classe EsentSesidTableIdMismatchException'
title: Classe EsentSesidTableIdMismatchException
TOCTitle: EsentSesidTableIdMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSesidTableIdMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsesidtableidmismatchexception(v=EXCHG.10)
ms:contentKeyID: 55102692
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSesidTableIdMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSesidTableIdMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75bfffe6535b883ebfaf5342685192cfaaee4275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922859"
---
# <a name="esentsesidtableidmismatchexception-class"></a><span data-ttu-id="69efa-103">Classe EsentSesidTableIdMismatchException</span><span class="sxs-lookup"><span data-stu-id="69efa-103">EsentSesidTableIdMismatchException class</span></span>

<span data-ttu-id="69efa-104">Classe base para JET_err. SesidTableIdMismatch exceções.</span><span class="sxs-lookup"><span data-stu-id="69efa-104">Base class for JET_err.SesidTableIdMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="69efa-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="69efa-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="69efa-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="69efa-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="69efa-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="69efa-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="69efa-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="69efa-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="69efa-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="69efa-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="69efa-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="69efa-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="69efa-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="69efa-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="69efa-112">Microsoft. ISAM. ESENT. Interop. EsentSesidTableIdMismatchException</span><span class="sxs-lookup"><span data-stu-id="69efa-112">Microsoft.Isam.Esent.Interop.EsentSesidTableIdMismatchException</span></span>  

<span data-ttu-id="69efa-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69efa-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69efa-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69efa-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69efa-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="69efa-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSesidTableIdMismatchException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSesidTableIdMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSesidTableIdMismatchException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="69efa-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="69efa-116">Thread safety</span></span>

<span data-ttu-id="69efa-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="69efa-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="69efa-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="69efa-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="69efa-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="69efa-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69efa-120">Referência</span><span class="sxs-lookup"><span data-stu-id="69efa-120">Reference</span></span>

[<span data-ttu-id="69efa-121">Membros do EsentSesidTableIdMismatchException</span><span class="sxs-lookup"><span data-stu-id="69efa-121">EsentSesidTableIdMismatchException members</span></span>](./esentsesidtableidmismatchexception-members.md)

[<span data-ttu-id="69efa-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="69efa-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

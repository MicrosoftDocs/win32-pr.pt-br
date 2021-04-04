---
description: 'Saiba mais sobre: classe EsentSessionWriteConflictException'
title: Classe EsentSessionWriteConflictException
TOCTitle: EsentSessionWriteConflictException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessionwriteconflictexception(v=EXCHG.10)
ms:contentKeyID: 55107337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0725bc2d1215e4e71e0e68b2fa7e0d4246a96b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837367"
---
# <a name="esentsessionwriteconflictexception-class"></a><span data-ttu-id="367c6-103">Classe EsentSessionWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="367c6-103">EsentSessionWriteConflictException class</span></span>

<span data-ttu-id="367c6-104">Classe base para JET_err. SessionWriteConflict exceções.</span><span class="sxs-lookup"><span data-stu-id="367c6-104">Base class for JET_err.SessionWriteConflict exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="367c6-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="367c6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="367c6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="367c6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="367c6-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="367c6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="367c6-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="367c6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="367c6-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="367c6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="367c6-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="367c6-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="367c6-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="367c6-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="367c6-112">Microsoft. ISAM. ESENT. Interop. EsentSessionWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="367c6-112">Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException</span></span>  

<span data-ttu-id="367c6-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="367c6-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="367c6-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="367c6-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="367c6-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="367c6-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionWriteConflictException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionWriteConflictException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionWriteConflictException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="367c6-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="367c6-116">Thread safety</span></span>

<span data-ttu-id="367c6-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="367c6-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="367c6-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="367c6-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="367c6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="367c6-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="367c6-120">Referência</span><span class="sxs-lookup"><span data-stu-id="367c6-120">Reference</span></span>

[<span data-ttu-id="367c6-121">Membros do EsentSessionWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="367c6-121">EsentSessionWriteConflictException members</span></span>](./esentsessionwriteconflictexception-members.md)

[<span data-ttu-id="367c6-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="367c6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

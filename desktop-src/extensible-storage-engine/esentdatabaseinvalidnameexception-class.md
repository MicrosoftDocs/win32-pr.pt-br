---
description: 'Saiba mais sobre: classe EsentDatabaseInvalidNameException'
title: Classe EsentDatabaseInvalidNameException
TOCTitle: EsentDatabaseInvalidNameException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseinvalidnameexception(v=EXCHG.10)
ms:contentKeyID: 55101502
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1754ed199986a048d188a5cd6a5927f8e3307867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501572"
---
# <a name="esentdatabaseinvalidnameexception-class"></a><span data-ttu-id="a4356-103">Classe EsentDatabaseInvalidNameException</span><span class="sxs-lookup"><span data-stu-id="a4356-103">EsentDatabaseInvalidNameException class</span></span>

<span data-ttu-id="a4356-104">Classe base para JET_err. DatabaseInvalidName exceções.</span><span class="sxs-lookup"><span data-stu-id="a4356-104">Base class for JET_err.DatabaseInvalidName exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a4356-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="a4356-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a4356-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a4356-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a4356-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a4356-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a4356-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="a4356-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a4356-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a4356-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a4356-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a4356-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a4356-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="a4356-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a4356-112">Microsoft. ISAM. ESENT. Interop. EsentDatabaseInvalidNameException</span><span class="sxs-lookup"><span data-stu-id="a4356-112">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException</span></span>  

<span data-ttu-id="a4356-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a4356-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a4356-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a4356-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a4356-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4356-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseInvalidNameException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseInvalidNameException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseInvalidNameException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a4356-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="a4356-116">Thread safety</span></span>

<span data-ttu-id="a4356-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a4356-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a4356-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a4356-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4356-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4356-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a4356-120">Referência</span><span class="sxs-lookup"><span data-stu-id="a4356-120">Reference</span></span>

[<span data-ttu-id="a4356-121">Membros do EsentDatabaseInvalidNameException</span><span class="sxs-lookup"><span data-stu-id="a4356-121">EsentDatabaseInvalidNameException members</span></span>](./esentdatabaseinvalidnameexception-members.md)

[<span data-ttu-id="a4356-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a4356-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

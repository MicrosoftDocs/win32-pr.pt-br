---
description: 'Saiba mais sobre: classe EsentDatabaseInvalidPathException'
title: Classe EsentDatabaseInvalidPathException
TOCTitle: EsentDatabaseInvalidPathException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseinvalidpathexception(v=EXCHG.10)
ms:contentKeyID: 55101511
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd275a599aa8b2cb8fb6f072ef1a413706d2c175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786276"
---
# <a name="esentdatabaseinvalidpathexception-class"></a><span data-ttu-id="fbd37-103">Classe EsentDatabaseInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="fbd37-103">EsentDatabaseInvalidPathException class</span></span>

<span data-ttu-id="fbd37-104">Classe base para JET_err. DatabaseInvalidPath exceções.</span><span class="sxs-lookup"><span data-stu-id="fbd37-104">Base class for JET_err.DatabaseInvalidPath exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="fbd37-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="fbd37-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="fbd37-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="fbd37-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fbd37-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="fbd37-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fbd37-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="fbd37-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fbd37-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="fbd37-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="fbd37-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="fbd37-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="fbd37-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="fbd37-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="fbd37-112">Microsoft. ISAM. ESENT. Interop. EsentDatabaseInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="fbd37-112">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException</span></span>  

<span data-ttu-id="fbd37-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fbd37-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fbd37-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fbd37-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd37-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbd37-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseInvalidPathException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseInvalidPathException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseInvalidPathException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="fbd37-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="fbd37-116">Thread safety</span></span>

<span data-ttu-id="fbd37-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="fbd37-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fbd37-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="fbd37-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fbd37-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbd37-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fbd37-120">Referência</span><span class="sxs-lookup"><span data-stu-id="fbd37-120">Reference</span></span>

[<span data-ttu-id="fbd37-121">Membros do EsentDatabaseInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="fbd37-121">EsentDatabaseInvalidPathException members</span></span>](./esentdatabaseinvalidpathexception-members.md)

[<span data-ttu-id="fbd37-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fbd37-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

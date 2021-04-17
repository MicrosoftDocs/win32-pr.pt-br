---
description: 'Saiba mais sobre: classe EsentFileIORetryException'
title: Classe EsentFileIORetryException
TOCTitle: EsentFileIORetryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileIORetryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileioretryexception(v=EXCHG.10)
ms:contentKeyID: 55107269
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileIORetryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileIORetryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6077d77096061b584adc106fceeecf02c9d6953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813742"
---
# <a name="esentfileioretryexception-class"></a><span data-ttu-id="f8b1b-103">Classe EsentFileIORetryException</span><span class="sxs-lookup"><span data-stu-id="f8b1b-103">EsentFileIORetryException class</span></span>

<span data-ttu-id="f8b1b-104">Classe base para JET_err. FileIORetry exceções.</span><span class="sxs-lookup"><span data-stu-id="f8b1b-104">Base class for JET_err.FileIORetry exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f8b1b-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="f8b1b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f8b1b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f8b1b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f8b1b-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f8b1b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f8b1b-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="f8b1b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f8b1b-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f8b1b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f8b1b-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f8b1b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f8b1b-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="f8b1b-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="f8b1b-112">Microsoft. ISAM. ESENT. Interop. EsentFileIORetryException</span><span class="sxs-lookup"><span data-stu-id="f8b1b-112">Microsoft.Isam.Esent.Interop.EsentFileIORetryException</span></span>  

<span data-ttu-id="f8b1b-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8b1b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8b1b-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8b1b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b1b-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8b1b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileIORetryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentFileIORetryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileIORetryException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="f8b1b-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="f8b1b-116">Thread safety</span></span>

<span data-ttu-id="f8b1b-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="f8b1b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f8b1b-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="f8b1b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8b1b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8b1b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8b1b-120">Referência</span><span class="sxs-lookup"><span data-stu-id="f8b1b-120">Reference</span></span>

[<span data-ttu-id="f8b1b-121">Membros do EsentFileIORetryException</span><span class="sxs-lookup"><span data-stu-id="f8b1b-121">EsentFileIORetryException members</span></span>](./esentfileioretryexception-members.md)

[<span data-ttu-id="f8b1b-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f8b1b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

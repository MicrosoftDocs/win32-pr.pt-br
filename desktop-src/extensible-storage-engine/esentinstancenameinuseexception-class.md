---
description: 'Saiba mais sobre: classe EsentInstanceNameInUseException'
title: Classe EsentInstanceNameInUseException
TOCTitle: EsentInstanceNameInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInstanceNameInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinstancenameinuseexception(v=EXCHG.10)
ms:contentKeyID: 55101821
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInstanceNameInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInstanceNameInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c430bcc3c4d37adfbef69404a8c17f006092cf70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010577"
---
# <a name="esentinstancenameinuseexception-class"></a><span data-ttu-id="64990-103">Classe EsentInstanceNameInUseException</span><span class="sxs-lookup"><span data-stu-id="64990-103">EsentInstanceNameInUseException class</span></span>

<span data-ttu-id="64990-104">Classe base para JET_err. InstanceNameInUse exceções.</span><span class="sxs-lookup"><span data-stu-id="64990-104">Base class for JET_err.InstanceNameInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="64990-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="64990-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="64990-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="64990-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="64990-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="64990-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="64990-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="64990-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="64990-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="64990-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="64990-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="64990-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="64990-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="64990-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="64990-112">Microsoft. ISAM. ESENT. Interop. EsentInstanceNameInUseException</span><span class="sxs-lookup"><span data-stu-id="64990-112">Microsoft.Isam.Esent.Interop.EsentInstanceNameInUseException</span></span>  

<span data-ttu-id="64990-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="64990-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="64990-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="64990-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="64990-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="64990-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInstanceNameInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInstanceNameInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInstanceNameInUseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="64990-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="64990-116">Thread safety</span></span>

<span data-ttu-id="64990-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="64990-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="64990-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="64990-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="64990-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="64990-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="64990-120">Referência</span><span class="sxs-lookup"><span data-stu-id="64990-120">Reference</span></span>

[<span data-ttu-id="64990-121">Membros do EsentInstanceNameInUseException</span><span class="sxs-lookup"><span data-stu-id="64990-121">EsentInstanceNameInUseException members</span></span>](./esentinstancenameinuseexception-members.md)

[<span data-ttu-id="64990-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="64990-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

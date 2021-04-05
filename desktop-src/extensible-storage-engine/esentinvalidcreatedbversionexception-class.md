---
description: 'Saiba mais sobre: classe EsentInvalidCreateDbVersionException'
title: Classe EsentInvalidCreateDbVersionException
TOCTitle: EsentInvalidCreateDbVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcreatedbversionexception(v=EXCHG.10)
ms:contentKeyID: 55101905
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 273b00900fece4afbb1329e25a36e50074e031dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827688"
---
# <a name="esentinvalidcreatedbversionexception-class"></a><span data-ttu-id="a832e-103">Classe EsentInvalidCreateDbVersionException</span><span class="sxs-lookup"><span data-stu-id="a832e-103">EsentInvalidCreateDbVersionException class</span></span>

<span data-ttu-id="a832e-104">Classe base para JET_err. InvalidCreateDbVersion exceções.</span><span class="sxs-lookup"><span data-stu-id="a832e-104">Base class for JET_err.InvalidCreateDbVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a832e-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="a832e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a832e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a832e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a832e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a832e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a832e-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="a832e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a832e-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a832e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a832e-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="a832e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="a832e-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="a832e-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="a832e-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidCreateDbVersionException</span><span class="sxs-lookup"><span data-stu-id="a832e-112">Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException</span></span>  

<span data-ttu-id="a832e-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a832e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a832e-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a832e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a832e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a832e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidCreateDbVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentInvalidCreateDbVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidCreateDbVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="a832e-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="a832e-116">Thread safety</span></span>

<span data-ttu-id="a832e-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a832e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a832e-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a832e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a832e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a832e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a832e-120">Referência</span><span class="sxs-lookup"><span data-stu-id="a832e-120">Reference</span></span>

[<span data-ttu-id="a832e-121">Membros do EsentInvalidCreateDbVersionException</span><span class="sxs-lookup"><span data-stu-id="a832e-121">EsentInvalidCreateDbVersionException members</span></span>](./esentinvalidcreatedbversionexception-members.md)

[<span data-ttu-id="a832e-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a832e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

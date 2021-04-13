---
description: 'Saiba mais sobre: classe EsentFileInvalidTypeException'
title: Classe EsentFileInvalidTypeException
TOCTitle: EsentFileInvalidTypeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileinvalidtypeexception(v=EXCHG.10)
ms:contentKeyID: 55107272
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c2bf5cf30cb45734613fcabc446834085d5bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297481"
---
# <a name="esentfileinvalidtypeexception-class"></a><span data-ttu-id="a215e-103">Classe EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="a215e-103">EsentFileInvalidTypeException class</span></span>

<span data-ttu-id="a215e-104">Classe base para JET_err. Exceções fileinvalidtype.</span><span class="sxs-lookup"><span data-stu-id="a215e-104">Base class for JET_err.FileInvalidType exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a215e-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="a215e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a215e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a215e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a215e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a215e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a215e-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="a215e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a215e-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a215e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a215e-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="a215e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="a215e-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="a215e-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="a215e-112">Microsoft. ISAM. ESENT. Interop. EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="a215e-112">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>  

<span data-ttu-id="a215e-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a215e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a215e-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a215e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a215e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a215e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileInvalidTypeException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentFileInvalidTypeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileInvalidTypeException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="a215e-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="a215e-116">Thread safety</span></span>

<span data-ttu-id="a215e-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a215e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a215e-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a215e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a215e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a215e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a215e-120">Referência</span><span class="sxs-lookup"><span data-stu-id="a215e-120">Reference</span></span>

[<span data-ttu-id="a215e-121">Membros do EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="a215e-121">EsentFileInvalidTypeException members</span></span>](./esentfileinvalidtypeexception-members.md)

[<span data-ttu-id="a215e-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a215e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Saiba mais sobre: classe EsentSPAvailExtCorruptedException'
title: Classe EsentSPAvailExtCorruptedException
TOCTitle: EsentSPAvailExtCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentspavailextcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55107349
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 004bca3eb0890c2ec74e6881d6ed4b007a3fa581
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011269"
---
# <a name="esentspavailextcorruptedexception-class"></a><span data-ttu-id="0155f-103">Classe EsentSPAvailExtCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0155f-103">EsentSPAvailExtCorruptedException class</span></span>

<span data-ttu-id="0155f-104">Classe base para JET_err. SPAvailExtCorrupted exceções.</span><span class="sxs-lookup"><span data-stu-id="0155f-104">Base class for JET_err.SPAvailExtCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0155f-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="0155f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0155f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0155f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0155f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0155f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0155f-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="0155f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0155f-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0155f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0155f-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0155f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="0155f-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="0155f-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="0155f-112">Microsoft. ISAM. ESENT. Interop. EsentSPAvailExtCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0155f-112">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException</span></span>  

<span data-ttu-id="0155f-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0155f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0155f-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0155f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0155f-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0155f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSPAvailExtCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentSPAvailExtCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSPAvailExtCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="0155f-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="0155f-116">Thread safety</span></span>

<span data-ttu-id="0155f-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="0155f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0155f-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="0155f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0155f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0155f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0155f-120">Referência</span><span class="sxs-lookup"><span data-stu-id="0155f-120">Reference</span></span>

[<span data-ttu-id="0155f-121">Membros do EsentSPAvailExtCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0155f-121">EsentSPAvailExtCorruptedException members</span></span>](./esentspavailextcorruptedexception-members.md)

[<span data-ttu-id="0155f-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0155f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

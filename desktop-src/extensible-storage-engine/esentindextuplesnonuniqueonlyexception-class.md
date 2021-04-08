---
description: 'Saiba mais sobre: classe EsentIndexTuplesNonUniqueOnlyException'
title: Classe EsentIndexTuplesNonUniqueOnlyException
TOCTitle: EsentIndexTuplesNonUniqueOnlyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindextuplesnonuniqueonlyexception(v=EXCHG.10)
ms:contentKeyID: 55101858
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00273bb5ae126d2397b765e22453db7d3c79bd15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011582"
---
# <a name="esentindextuplesnonuniqueonlyexception-class"></a><span data-ttu-id="8f0f1-103">Classe EsentIndexTuplesNonUniqueOnlyException</span><span class="sxs-lookup"><span data-stu-id="8f0f1-103">EsentIndexTuplesNonUniqueOnlyException class</span></span>

<span data-ttu-id="8f0f1-104">Classe base para JET_err. IndexTuplesNonUniqueOnly exceções.</span><span class="sxs-lookup"><span data-stu-id="8f0f1-104">Base class for JET_err.IndexTuplesNonUniqueOnly exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8f0f1-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="8f0f1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8f0f1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8f0f1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8f0f1-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="8f0f1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8f0f1-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="8f0f1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8f0f1-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8f0f1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8f0f1-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="8f0f1-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="8f0f1-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="8f0f1-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="8f0f1-112">Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesNonUniqueOnlyException</span><span class="sxs-lookup"><span data-stu-id="8f0f1-112">Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException</span></span>  

<span data-ttu-id="8f0f1-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8f0f1-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8f0f1-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8f0f1-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8f0f1-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f0f1-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexTuplesNonUniqueOnlyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentIndexTuplesNonUniqueOnlyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexTuplesNonUniqueOnlyException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="8f0f1-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="8f0f1-116">Thread safety</span></span>

<span data-ttu-id="8f0f1-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="8f0f1-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8f0f1-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="8f0f1-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f0f1-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f0f1-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8f0f1-120">Referência</span><span class="sxs-lookup"><span data-stu-id="8f0f1-120">Reference</span></span>

[<span data-ttu-id="8f0f1-121">Membros do EsentIndexTuplesNonUniqueOnlyException</span><span class="sxs-lookup"><span data-stu-id="8f0f1-121">EsentIndexTuplesNonUniqueOnlyException members</span></span>](./esentindextuplesnonuniqueonlyexception-members.md)

[<span data-ttu-id="8f0f1-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8f0f1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

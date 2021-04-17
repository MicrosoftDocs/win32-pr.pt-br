---
description: 'Saiba mais sobre: classe EsentRecordPrimaryChangedException'
title: Classe EsentRecordPrimaryChangedException
TOCTitle: EsentRecordPrimaryChangedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordPrimaryChangedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordprimarychangedexception(v=EXCHG.10)
ms:contentKeyID: 55102532
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordPrimaryChangedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordPrimaryChangedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06fe56bb34c20ce45c99999526a3db279f72f085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791592"
---
# <a name="esentrecordprimarychangedexception-class"></a><span data-ttu-id="99a49-103">Classe EsentRecordPrimaryChangedException</span><span class="sxs-lookup"><span data-stu-id="99a49-103">EsentRecordPrimaryChangedException class</span></span>

<span data-ttu-id="99a49-104">Classe base para JET_err. RecordPrimaryChanged exceções.</span><span class="sxs-lookup"><span data-stu-id="99a49-104">Base class for JET_err.RecordPrimaryChanged exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="99a49-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="99a49-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="99a49-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="99a49-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="99a49-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="99a49-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="99a49-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="99a49-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="99a49-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="99a49-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="99a49-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="99a49-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="99a49-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="99a49-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="99a49-112">Microsoft. ISAM. ESENT. Interop. EsentRecordPrimaryChangedException</span><span class="sxs-lookup"><span data-stu-id="99a49-112">Microsoft.Isam.Esent.Interop.EsentRecordPrimaryChangedException</span></span>  

<span data-ttu-id="99a49-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99a49-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99a49-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="99a49-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99a49-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99a49-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordPrimaryChangedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRecordPrimaryChangedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordPrimaryChangedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="99a49-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="99a49-116">Thread safety</span></span>

<span data-ttu-id="99a49-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="99a49-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="99a49-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="99a49-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="99a49-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="99a49-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99a49-120">Referência</span><span class="sxs-lookup"><span data-stu-id="99a49-120">Reference</span></span>

[<span data-ttu-id="99a49-121">Membros do EsentRecordPrimaryChangedException</span><span class="sxs-lookup"><span data-stu-id="99a49-121">EsentRecordPrimaryChangedException members</span></span>](./esentrecordprimarychangedexception-members.md)

[<span data-ttu-id="99a49-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="99a49-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

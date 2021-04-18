---
description: 'Saiba mais sobre: classe EsentRecordNotDeletedException'
title: Classe EsentRecordNotDeletedException
TOCTitle: EsentRecordNotDeletedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordnotdeletedexception(v=EXCHG.10)
ms:contentKeyID: 55102578
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70eb38e960b127474415c9b7291e4765719fb7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765336"
---
# <a name="esentrecordnotdeletedexception-class"></a><span data-ttu-id="eadca-103">Classe EsentRecordNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="eadca-103">EsentRecordNotDeletedException class</span></span>

<span data-ttu-id="eadca-104">Classe base para JET_err. RecordNotDeleted exceções.</span><span class="sxs-lookup"><span data-stu-id="eadca-104">Base class for JET_err.RecordNotDeleted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="eadca-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="eadca-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="eadca-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="eadca-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="eadca-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="eadca-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="eadca-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="eadca-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="eadca-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="eadca-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="eadca-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="eadca-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="eadca-111">Microsoft. ISAM. ESENT. Interop. EsentRecordNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="eadca-111">Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException</span></span>  

<span data-ttu-id="eadca-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eadca-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eadca-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eadca-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eadca-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="eadca-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordNotDeletedException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentRecordNotDeletedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordNotDeletedException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="eadca-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="eadca-115">Thread safety</span></span>

<span data-ttu-id="eadca-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="eadca-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="eadca-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="eadca-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="eadca-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="eadca-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eadca-119">Referência</span><span class="sxs-lookup"><span data-stu-id="eadca-119">Reference</span></span>

[<span data-ttu-id="eadca-120">Membros do EsentRecordNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="eadca-120">EsentRecordNotDeletedException members</span></span>](./esentrecordnotdeletedexception-members.md)

[<span data-ttu-id="eadca-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="eadca-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

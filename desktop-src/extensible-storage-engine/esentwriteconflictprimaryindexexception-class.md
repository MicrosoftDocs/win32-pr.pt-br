---
description: 'Saiba mais sobre: classe EsentWriteConflictPrimaryIndexException'
title: Classe EsentWriteConflictPrimaryIndexException
TOCTitle: EsentWriteConflictPrimaryIndexException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentwriteconflictprimaryindexexception(v=EXCHG.10)
ms:contentKeyID: 55107366
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df38255376ddf4f17562f26eced109d417558852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796219"
---
# <a name="esentwriteconflictprimaryindexexception-class"></a><span data-ttu-id="9b314-103">Classe EsentWriteConflictPrimaryIndexException</span><span class="sxs-lookup"><span data-stu-id="9b314-103">EsentWriteConflictPrimaryIndexException class</span></span>

<span data-ttu-id="9b314-104">Classe base para JET_err. WriteConflictPrimaryIndex exceções.</span><span class="sxs-lookup"><span data-stu-id="9b314-104">Base class for JET_err.WriteConflictPrimaryIndex exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9b314-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="9b314-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9b314-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9b314-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9b314-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="9b314-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9b314-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="9b314-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9b314-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="9b314-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9b314-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="9b314-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="9b314-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="9b314-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="9b314-112">Microsoft. ISAM. ESENT. Interop. EsentWriteConflictPrimaryIndexException</span><span class="sxs-lookup"><span data-stu-id="9b314-112">Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException</span></span>  

<span data-ttu-id="9b314-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9b314-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9b314-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9b314-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9b314-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b314-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentWriteConflictPrimaryIndexException _
    Inherits EsentStateException
'Usage
Dim instance As EsentWriteConflictPrimaryIndexException
```

``` csharp
[SerializableAttribute]
public sealed class EsentWriteConflictPrimaryIndexException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="9b314-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="9b314-116">Thread safety</span></span>

<span data-ttu-id="9b314-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="9b314-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9b314-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="9b314-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b314-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b314-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9b314-120">Referência</span><span class="sxs-lookup"><span data-stu-id="9b314-120">Reference</span></span>

[<span data-ttu-id="9b314-121">Membros do EsentWriteConflictPrimaryIndexException</span><span class="sxs-lookup"><span data-stu-id="9b314-121">EsentWriteConflictPrimaryIndexException members</span></span>](./esentwriteconflictprimaryindexexception-members.md)

[<span data-ttu-id="9b314-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9b314-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

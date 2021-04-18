---
description: 'Saiba mais sobre: classe EsentException'
title: Classe EsentException (Microsoft. ISAM. ESENT)
TOCTitle: EsentException class
ms:assetid: T:Microsoft.Isam.Esent.EsentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100645
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.EsentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.EsentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 775d63c6b1d234696790b1187538a6d1ee734a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786169"
---
# <a name="esentexception-class"></a><span data-ttu-id="94d5c-103">Classe EsentException</span><span class="sxs-lookup"><span data-stu-id="94d5c-103">EsentException class</span></span>

<span data-ttu-id="94d5c-104">Classe base para exceções de ESENT.</span><span class="sxs-lookup"><span data-stu-id="94d5c-104">Base class for ESENT exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="94d5c-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="94d5c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="94d5c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="94d5c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="94d5c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="94d5c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    <span data-ttu-id="94d5c-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="94d5c-108">Microsoft.Isam.Esent.EsentException</span></span>  
      [<span data-ttu-id="94d5c-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="94d5c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
      [<span data-ttu-id="94d5c-110">Microsoft. ISAM. ESENT. Interop. EsentInvalidColumnException</span><span class="sxs-lookup"><span data-stu-id="94d5c-110">Microsoft.Isam.Esent.Interop.EsentInvalidColumnException</span></span>](./esentinvalidcolumnexception-class.md)  

<span data-ttu-id="94d5c-111">**Namespace:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="94d5c-111">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="94d5c-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="94d5c-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="94d5c-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94d5c-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentException _
    Inherits Exception
'Usage
Dim instance As EsentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentException : Exception
```

## <a name="thread-safety"></a><span data-ttu-id="94d5c-114">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="94d5c-114">Thread safety</span></span>

<span data-ttu-id="94d5c-115">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="94d5c-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="94d5c-116">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="94d5c-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="94d5c-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="94d5c-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="94d5c-118">Referência</span><span class="sxs-lookup"><span data-stu-id="94d5c-118">Reference</span></span>

[<span data-ttu-id="94d5c-119">Membros do EsentException</span><span class="sxs-lookup"><span data-stu-id="94d5c-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="94d5c-120">Namespace Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="94d5c-120">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)

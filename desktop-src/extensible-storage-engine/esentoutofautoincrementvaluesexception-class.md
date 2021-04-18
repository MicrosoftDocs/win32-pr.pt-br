---
description: 'Saiba mais sobre: classe EsentOutOfAutoincrementValuesException'
title: Classe EsentOutOfAutoincrementValuesException
TOCTitle: EsentOutOfAutoincrementValuesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofautoincrementvaluesexception(v=EXCHG.10)
ms:contentKeyID: 55102440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a37a25e508281083915cf549db5a1b65a4bdcadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798096"
---
# <a name="esentoutofautoincrementvaluesexception-class"></a><span data-ttu-id="cb809-103">Classe EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="cb809-103">EsentOutOfAutoincrementValuesException class</span></span>

<span data-ttu-id="cb809-104">Classe base para JET_err. OutOfAutoincrementValues exceções.</span><span class="sxs-lookup"><span data-stu-id="cb809-104">Base class for JET_err.OutOfAutoincrementValues exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="cb809-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="cb809-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="cb809-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="cb809-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="cb809-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="cb809-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="cb809-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="cb809-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="cb809-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="cb809-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="cb809-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="cb809-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="cb809-111">Microsoft. ISAM. ESENT. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="cb809-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="cb809-112">Microsoft. ISAM. ESENT. Interop. EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="cb809-112">Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException</span></span>  

<span data-ttu-id="cb809-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb809-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cb809-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb809-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb809-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb809-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfAutoincrementValuesException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfAutoincrementValuesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfAutoincrementValuesException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="cb809-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="cb809-116">Thread safety</span></span>

<span data-ttu-id="cb809-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="cb809-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="cb809-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="cb809-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb809-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb809-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb809-120">Referência</span><span class="sxs-lookup"><span data-stu-id="cb809-120">Reference</span></span>

[<span data-ttu-id="cb809-121">Membros do EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="cb809-121">EsentOutOfAutoincrementValuesException members</span></span>](./esentoutofautoincrementvaluesexception-members.md)

[<span data-ttu-id="cb809-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cb809-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

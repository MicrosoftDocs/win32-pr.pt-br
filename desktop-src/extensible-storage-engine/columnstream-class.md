---
description: 'Saiba mais sobre: classe ColumnStream'
title: Classe ColumnStream
TOCTitle: ColumnStream class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eea249347acd18ec71f03fcdc82b8a2baa1da9ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170182"
---
# <a name="columnstream-class"></a><span data-ttu-id="390c2-103">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="390c2-103">ColumnStream class</span></span>

<span data-ttu-id="390c2-104">Essa classe fornece uma interface de streaming para uma coluna de valor longo (ou seja, uma coluna do tipo [LongBinary](./jet-coltyp-enumeration.md) ou [LONGTEXT](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="390c2-104">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="390c2-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="390c2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="390c2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="390c2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="390c2-107">System.MarshalByRefObject</span><span class="sxs-lookup"><span data-stu-id="390c2-107">System.MarshalByRefObject</span></span>](/dotnet/api/system.marshalbyrefobject)  
    [<span data-ttu-id="390c2-108">System. IO. Stream</span><span class="sxs-lookup"><span data-stu-id="390c2-108">System.IO.Stream</span></span>](/dotnet/api/system.io.stream)  
      <span data-ttu-id="390c2-109">Microsoft. ISAM. ESENT. Interop. ColumnStream</span><span class="sxs-lookup"><span data-stu-id="390c2-109">Microsoft.Isam.Esent.Interop.ColumnStream</span></span>  

<span data-ttu-id="390c2-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="390c2-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="390c2-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="390c2-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="390c2-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="390c2-112">Syntax</span></span>

``` vb
'Declaration
Public Class ColumnStream _
    Inherits Stream
'Usage
Dim instance As ColumnStream
```

``` csharp
public class ColumnStream : Stream
```

## <a name="thread-safety"></a><span data-ttu-id="390c2-113">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="390c2-113">Thread safety</span></span>

<span data-ttu-id="390c2-114">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="390c2-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="390c2-115">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="390c2-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="390c2-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="390c2-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="390c2-117">Referência</span><span class="sxs-lookup"><span data-stu-id="390c2-117">Reference</span></span>

[<span data-ttu-id="390c2-118">Membros do ColumnStream</span><span class="sxs-lookup"><span data-stu-id="390c2-118">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="390c2-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="390c2-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

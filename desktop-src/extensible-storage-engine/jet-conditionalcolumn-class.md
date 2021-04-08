---
description: 'Saiba mais sobre: classe de JET_CONDITIONALCOLUMN'
title: Classe JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn(v=EXCHG.10)
ms:contentKeyID: 55107506
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23b116ce88b24702711d74f610c208a72c44addf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922188"
---
# <a name="jet_conditionalcolumn-class"></a><span data-ttu-id="27425-103">Classe JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="27425-103">JET_CONDITIONALCOLUMN class</span></span>

<span data-ttu-id="27425-104">Define como a indexação condicional é executada para um determinado índice.</span><span class="sxs-lookup"><span data-stu-id="27425-104">Defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="27425-105">Um índice condicional contém uma entrada de índice somente para as linhas que correspondem à condição especificada.</span><span class="sxs-lookup"><span data-stu-id="27425-105">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="27425-106">No entanto, a coluna condicional não faz parte da chave do índice, ela controla apenas a presença da entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="27425-106">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="27425-107">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="27425-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="27425-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="27425-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="27425-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="27425-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span></span>  

<span data-ttu-id="27425-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="27425-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="27425-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="27425-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="27425-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="27425-112">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_CONDITIONALCOLUMN _
    Implements IContentEquatable(Of JET_CONDITIONALCOLUMN), IDeepCloneable(Of JET_CONDITIONALCOLUMN)
'Usage
Dim instance As JET_CONDITIONALCOLUMN
```

``` csharp
[SerializableAttribute]
public sealed class JET_CONDITIONALCOLUMN : IContentEquatable<JET_CONDITIONALCOLUMN>, 
    IDeepCloneable<JET_CONDITIONALCOLUMN>
```

## <a name="thread-safety"></a><span data-ttu-id="27425-113">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="27425-113">Thread safety</span></span>

<span data-ttu-id="27425-114">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="27425-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="27425-115">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="27425-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="27425-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="27425-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="27425-117">Referência</span><span class="sxs-lookup"><span data-stu-id="27425-117">Reference</span></span>

[<span data-ttu-id="27425-118">Membros do JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="27425-118">JET_CONDITIONALCOLUMN members</span></span>](./jet-conditionalcolumn-members.md)

[<span data-ttu-id="27425-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="27425-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

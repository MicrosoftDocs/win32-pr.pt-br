---
description: 'Saiba mais sobre: estrutura de JET_INDEXID'
title: Estrutura de JET_INDEXID
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791456"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="46d64-103">Estrutura de JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="46d64-103">JET_INDEXID structure</span></span>

<span data-ttu-id="46d64-104">Mantém uma ID de índice.</span><span class="sxs-lookup"><span data-stu-id="46d64-104">Holds an index ID.</span></span> <span data-ttu-id="46d64-105">Uma ID de índice é uma dica usada para acelerar a seleção do índice atual usando JetSetCurrentIndex.</span><span class="sxs-lookup"><span data-stu-id="46d64-105">An index ID is a hint that is used to accelerate the selection of the current index using JetSetCurrentIndex.</span></span> <span data-ttu-id="46d64-106">Ele é mais útil quando há um número muito grande de índices em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="46d64-106">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="46d64-107">A ID do índice pode ser recuperada usando JetGetIndexInfo ou JetGetTableIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="46d64-107">The index ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo.</span></span>

<span data-ttu-id="46d64-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="46d64-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="46d64-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="46d64-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="46d64-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46d64-110">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a><span data-ttu-id="46d64-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="46d64-111">Remarks</span></span>

<span data-ttu-id="46d64-112">O atributo Pack é necessário porque a versão C++ é definida como uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="46d64-112">The Pack attribute is necessary because the C++ version is defined as a byte array.</span></span> <span data-ttu-id="46d64-113">Se o \# compilador C inserir o preenchimento normal entre o cbStruct uint e o IntPtr, a estrutura acabará muito grande.</span><span class="sxs-lookup"><span data-stu-id="46d64-113">If the C\# compiler inserts the usual padding between the uint cbStruct and the IntPtr, then the structure ends up too large.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="46d64-114">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="46d64-114">Thread safety</span></span>

<span data-ttu-id="46d64-115">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="46d64-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="46d64-116">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="46d64-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="46d64-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="46d64-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="46d64-118">Referência</span><span class="sxs-lookup"><span data-stu-id="46d64-118">Reference</span></span>

[<span data-ttu-id="46d64-119">Membros do JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="46d64-119">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="46d64-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="46d64-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

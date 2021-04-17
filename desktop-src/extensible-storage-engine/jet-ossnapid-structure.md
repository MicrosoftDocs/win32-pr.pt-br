---
description: 'Saiba mais sobre: estrutura de JET_OSSNAPID'
title: Estrutura de JET_OSSNAPID
TOCTitle: JET_OSSNAPID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_OSSNAPID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid(v=EXCHG.10)
ms:contentKeyID: 39515031
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 215bd8f096ba9c1788f4db70a014cab48b74afa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755019"
---
# <a name="jet_ossnapid-structure"></a><span data-ttu-id="aa6c6-103">Estrutura de JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="aa6c6-103">JET_OSSNAPID structure</span></span>

<span data-ttu-id="aa6c6-104">Um JET_OSSNAPID contém um identificador para um instantâneo de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-104">A JET_OSSNAPID contains a handle to a snapshot of a database.</span></span>

<span data-ttu-id="aa6c6-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa6c6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa6c6-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa6c6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6c6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa6c6-107">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_OSSNAPID _
    Implements IEquatable(Of JET_OSSNAPID), IFormattable
'Usage
Dim instance As JET_OSSNAPID
```

``` csharp
public struct JET_OSSNAPID : IEquatable<JET_OSSNAPID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="aa6c6-108">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="aa6c6-108">Thread safety</span></span>

<span data-ttu-id="aa6c6-109">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="aa6c6-110">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa6c6-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa6c6-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa6c6-112">Referência</span><span class="sxs-lookup"><span data-stu-id="aa6c6-112">Reference</span></span>

[<span data-ttu-id="aa6c6-113">Membros do JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="aa6c6-113">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="aa6c6-114">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="aa6c6-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

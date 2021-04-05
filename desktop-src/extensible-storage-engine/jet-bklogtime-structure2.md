---
description: 'Saiba mais sobre: estrutura de JET_BKLOGTIME'
title: Estrutura de JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime(v=EXCHG.10)
ms:contentKeyID: 39512194
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b718254082095592f097097500d2690be320dd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090889"
---
# <a name="jet_bklogtime-structure"></a><span data-ttu-id="5d912-103">Estrutura de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="5d912-103">JET_BKLOGTIME structure</span></span>

<span data-ttu-id="5d912-104">Descreve uma data/hora em que um backup ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5d912-104">Describes a date/time when a backup occured.</span></span>

<span data-ttu-id="5d912-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5d912-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5d912-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5d912-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5d912-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d912-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKLOGTIME _
    Implements IEquatable(Of JET_BKLOGTIME), IJET_LOGTIME,  _
    INullableJetStruct
'Usage
Dim instance As JET_BKLOGTIME
```

``` csharp
[SerializableAttribute]
public struct JET_BKLOGTIME : IEquatable<JET_BKLOGTIME>, 
    IJET_LOGTIME, INullableJetStruct
```

## <a name="thread-safety"></a><span data-ttu-id="5d912-108">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="5d912-108">Thread safety</span></span>

<span data-ttu-id="5d912-109">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="5d912-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5d912-110">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="5d912-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d912-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d912-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5d912-112">Referência</span><span class="sxs-lookup"><span data-stu-id="5d912-112">Reference</span></span>

[<span data-ttu-id="5d912-113">Membros do JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="5d912-113">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="5d912-114">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5d912-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

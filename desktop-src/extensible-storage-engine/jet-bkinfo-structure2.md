---
description: 'Saiba mais sobre: estrutura de JET_BKINFO'
title: Estrutura de JET_BKINFO
TOCTitle: JET_BKINFO structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo(v=EXCHG.10)
ms:contentKeyID: 39511166
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c3b0d3178abaa90fe507c06a2a997472492643c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171357"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="00c24-103">Estrutura de JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="00c24-103">JET_BKINFO structure</span></span>

<span data-ttu-id="00c24-104">Mantém uma coleção de dados sobre um evento de backup específico.</span><span class="sxs-lookup"><span data-stu-id="00c24-104">Holds a collection of data about a specific backup event.</span></span>

<span data-ttu-id="00c24-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="00c24-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="00c24-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="00c24-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="00c24-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="00c24-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKINFO _
    Implements IEquatable(Of JET_BKINFO), INullableJetStruct
'Usage
Dim instance As JET_BKINFO
```

``` csharp
[SerializableAttribute]
public struct JET_BKINFO : IEquatable<JET_BKINFO>, 
    INullableJetStruct
```

## <a name="thread-safety"></a><span data-ttu-id="00c24-108">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="00c24-108">Thread safety</span></span>

<span data-ttu-id="00c24-109">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="00c24-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="00c24-110">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="00c24-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="00c24-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="00c24-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="00c24-112">Referência</span><span class="sxs-lookup"><span data-stu-id="00c24-112">Reference</span></span>

[<span data-ttu-id="00c24-113">Membros do JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="00c24-113">JET_BKINFO members</span></span>](./jet-bkinfo-members.md)

[<span data-ttu-id="00c24-114">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="00c24-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

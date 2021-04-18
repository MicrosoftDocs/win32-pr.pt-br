---
description: 'Saiba mais sobre: método JET_LGPOS. CompareTo'
title: Método JET_LGPOS. CompareTo
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo(Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.compareto(v=EXCHG.10)
ms:contentKeyID: 39514516
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83012ed755ab876618147c013e99868927e16f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761431"
---
# <a name="jet_lgposcompareto-method"></a><span data-ttu-id="f6072-103">Método JET_LGPOS. CompareTo</span><span class="sxs-lookup"><span data-stu-id="f6072-103">JET_LGPOS.CompareTo method</span></span>

<span data-ttu-id="f6072-104">Compara essa posição de log com outra posição de log e determina se essa instância é anterior, a mesma que ou após a outra instância.</span><span class="sxs-lookup"><span data-stu-id="f6072-104">Compares this log position to another log position and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="f6072-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6072-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6072-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6072-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6072-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6072-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_LGPOS _
) As Integer
'Usage
Dim instance As JET_LGPOS
Dim other As JET_LGPOS
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_LGPOS other
)
```

#### <a name="parameters"></a><span data-ttu-id="f6072-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6072-108">Parameters</span></span>

  - <span data-ttu-id="f6072-109">outros</span><span class="sxs-lookup"><span data-stu-id="f6072-109">other</span></span>  
    <span data-ttu-id="f6072-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f6072-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="f6072-111">A posição do log para comparar com a instância atual.</span><span class="sxs-lookup"><span data-stu-id="f6072-111">The log position to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f6072-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6072-112">Return value</span></span>

<span data-ttu-id="f6072-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f6072-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="f6072-114">Um número assinado que indica as posições relativas dessa instância e o parâmetro de valor.</span><span class="sxs-lookup"><span data-stu-id="f6072-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="f6072-115">Implementações</span><span class="sxs-lookup"><span data-stu-id="f6072-115">Implements</span></span>

[<span data-ttu-id="f6072-116">IComparable \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="f6072-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="f6072-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6072-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6072-118">Referência</span><span class="sxs-lookup"><span data-stu-id="f6072-118">Reference</span></span>

[<span data-ttu-id="f6072-119">Estrutura de JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="f6072-119">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="f6072-120">Membros do JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="f6072-120">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="f6072-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f6072-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

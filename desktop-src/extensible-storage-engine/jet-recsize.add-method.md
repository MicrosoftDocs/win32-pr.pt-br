---
description: 'Saiba mais sobre: JET_RECSIZE. Adicionar método'
title: JET_RECSIZE. Método Add (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.add(v=EXCHG.10)
ms:contentKeyID: 39509872
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e12a78a0a32bcca02afec100b0b238f4444a6ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501312"
---
# <a name="jet_recsizeadd-method"></a><span data-ttu-id="b8d7e-103">JET_RECSIZE. Adicionar método</span><span class="sxs-lookup"><span data-stu-id="b8d7e-103">JET_RECSIZE.Add method</span></span>

<span data-ttu-id="b8d7e-104">Adicione os tamanhos em duas estruturas de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-104">Add the sizes in two JET_RECSIZE structures.</span></span>

<span data-ttu-id="b8d7e-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8d7e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b8d7e-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8d7e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d7e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8d7e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Add ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Add(s1, s2)
```

``` csharp
public static JET_RECSIZE Add(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a><span data-ttu-id="b8d7e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8d7e-108">Parameters</span></span>

  - <span data-ttu-id="b8d7e-109">s1</span><span class="sxs-lookup"><span data-stu-id="b8d7e-109">s1</span></span>  
    <span data-ttu-id="b8d7e-110">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b8d7e-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="b8d7e-111">O primeiro JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8d7e-112">S2</span><span class="sxs-lookup"><span data-stu-id="b8d7e-112">s2</span></span>  
    <span data-ttu-id="b8d7e-113">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b8d7e-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="b8d7e-114">A segunda JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b8d7e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8d7e-115">Return value</span></span>

<span data-ttu-id="b8d7e-116">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b8d7e-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="b8d7e-117">Uma JET_RECSIZE que contém o resultado da adição dos tamanhos em S1 e S2.</span><span class="sxs-lookup"><span data-stu-id="b8d7e-117">A JET_RECSIZE containing the result of adding the sizes in s1 and s2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b8d7e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8d7e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8d7e-119">Referência</span><span class="sxs-lookup"><span data-stu-id="b8d7e-119">Reference</span></span>

[<span data-ttu-id="b8d7e-120">Estrutura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="b8d7e-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="b8d7e-121">Membros do JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="b8d7e-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="b8d7e-122">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="b8d7e-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

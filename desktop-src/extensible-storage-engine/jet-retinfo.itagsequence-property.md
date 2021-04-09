---
description: 'Saiba mais sobre a propriedade: JET_RETINFO. itagSequence'
title: Propriedade JET_RETINFO. itagSequence
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103876
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_itagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df42b6a52b34ec265aceb5b069b06f39c0663b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171624"
---
# <a name="jet_retinfoitagsequence-property"></a><span data-ttu-id="ea4c8-103">Propriedade JET_RETINFO. itagSequence</span><span class="sxs-lookup"><span data-stu-id="ea4c8-103">JET_RETINFO.itagSequence property</span></span>

<span data-ttu-id="ea4c8-104">Obtém ou define o número de sequência do valor em uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-104">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="ea4c8-105">A matriz de valores é baseada em um.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-105">The array of values is one-based.</span></span> <span data-ttu-id="ea4c8-106">O primeiro valor é Sequence 1, e não 0.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-106">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="ea4c8-107">Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como itagSequence.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-107">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<span data-ttu-id="ea4c8-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ea4c8-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ea4c8-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ea4c8-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4c8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea4c8-110">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="ea4c8-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ea4c8-111">Property value</span></span>

<span data-ttu-id="ea4c8-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ea4c8-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="ea4c8-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea4c8-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ea4c8-114">Referência</span><span class="sxs-lookup"><span data-stu-id="ea4c8-114">Reference</span></span>

[<span data-ttu-id="ea4c8-115">Classe JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="ea4c8-115">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="ea4c8-116">Membros do JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="ea4c8-116">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="ea4c8-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ea4c8-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

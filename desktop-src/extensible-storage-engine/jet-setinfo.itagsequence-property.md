---
description: 'Saiba mais sobre a propriedade: JET_SETINFO. itagSequence'
title: Propriedade JET_SETINFO. itagSequence
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c409903f90633f15daa8d289c72530db943f1c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090117"
---
# <a name="jet_setinfoitagsequence-property"></a><span data-ttu-id="946a0-103">Propriedade JET_SETINFO. itagSequence</span><span class="sxs-lookup"><span data-stu-id="946a0-103">JET_SETINFO.itagSequence property</span></span>

<span data-ttu-id="946a0-104">Obtém ou define o número de sequência do valor em uma coluna de valores múltiplos a ser definida.</span><span class="sxs-lookup"><span data-stu-id="946a0-104">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="946a0-105">A matriz de valores é baseada em um.</span><span class="sxs-lookup"><span data-stu-id="946a0-105">The array of values is one-based.</span></span> <span data-ttu-id="946a0-106">O primeiro valor é Sequence 1, não 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="946a0-106">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="946a0-107">Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como itagSequence se esse valor estiver sendo substituído.</span><span class="sxs-lookup"><span data-stu-id="946a0-107">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="946a0-108">Um valor de 0 (zero) significa adicionar uma nova instância de valor de coluna ao final da sequência de valores de coluna.</span><span class="sxs-lookup"><span data-stu-id="946a0-108">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="946a0-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="946a0-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="946a0-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="946a0-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="946a0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="946a0-111">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="946a0-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="946a0-112">Property value</span></span>

<span data-ttu-id="946a0-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="946a0-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="946a0-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="946a0-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="946a0-115">Referência</span><span class="sxs-lookup"><span data-stu-id="946a0-115">Reference</span></span>

[<span data-ttu-id="946a0-116">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="946a0-116">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="946a0-117">Membros do JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="946a0-117">JET_SETINFO members</span></span>](./jet-setinfo-members.md)

[<span data-ttu-id="946a0-118">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="946a0-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

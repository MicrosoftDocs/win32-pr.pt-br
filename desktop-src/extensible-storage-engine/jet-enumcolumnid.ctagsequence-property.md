---
description: 'Saiba mais sobre a propriedade: JET_ENUMCOLUMNID. ctagSequence'
title: Propriedade JET_ENUMCOLUMNID. ctagSequence
TOCTitle: 'ctagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.ctagsequence(v=EXCHG.10)
ms:contentKeyID: 55107537
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_ctagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e12c8c6a102cbb20862b3cc9859f7e632ade8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766538"
---
# <a name="jet_enumcolumnidctagsequence-property"></a><span data-ttu-id="13dd8-103">Propriedade JET_ENUMCOLUMNID. ctagSequence</span><span class="sxs-lookup"><span data-stu-id="13dd8-103">JET_ENUMCOLUMNID.ctagSequence property</span></span>

<span data-ttu-id="13dd8-104">Obtém ou define a contagem de valores de coluna (por índice baseado em um) para enumerar para a ID de coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="13dd8-104">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="13dd8-105">Se ctagSequence for 0 (zero), rgtagSequence será ignorado e todos os valores de coluna para a ID de coluna especificada serão enumerados.</span><span class="sxs-lookup"><span data-stu-id="13dd8-105">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="13dd8-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="13dd8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="13dd8-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="13dd8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="13dd8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13dd8-108">Syntax</span></span>

``` vb
'Declaration
Public Property ctagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer

value = instance.ctagSequence

instance.ctagSequence = value
```

``` csharp
public int ctagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="13dd8-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="13dd8-109">Property value</span></span>

<span data-ttu-id="13dd8-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="13dd8-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="13dd8-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="13dd8-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="13dd8-112">Referência</span><span class="sxs-lookup"><span data-stu-id="13dd8-112">Reference</span></span>

[<span data-ttu-id="13dd8-113">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="13dd8-113">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="13dd8-114">Membros do JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="13dd8-114">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="13dd8-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="13dd8-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Saiba mais sobre a propriedade: JET_RECSIZE. cbDataCompressed'
title: Propriedade JET_RECSIZE. cbDataCompressed (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'cbDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cbdatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515358
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbDataCompressed
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 747c2f00077f6a9d13de059f742bacc9a7936d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646730"
---
# <a name="jet_recsizecbdatacompressed-property"></a><span data-ttu-id="e397f-103">Propriedade JET_RECSIZE. cbDataCompressed</span><span class="sxs-lookup"><span data-stu-id="e397f-103">JET_RECSIZE.cbDataCompressed property</span></span>

<span data-ttu-id="e397f-104">Obtém o tamanho compactado dos dados do usuário no registro.</span><span class="sxs-lookup"><span data-stu-id="e397f-104">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="e397f-105">Isso é o mesmo que [cbData](./jet-recsize.cbdata-property.md) se nenhum valor longo intrínseco for compactado).</span><span class="sxs-lookup"><span data-stu-id="e397f-105">This is the same as [cbData](./jet-recsize.cbdata-property.md) if no intrinsic long-values are compressed).</span></span>

<span data-ttu-id="e397f-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e397f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e397f-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e397f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e397f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e397f-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbDataCompressed
```

``` csharp
public long cbDataCompressed { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="e397f-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e397f-109">Property value</span></span>

<span data-ttu-id="e397f-110">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="e397f-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e397f-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="e397f-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e397f-112">Referência</span><span class="sxs-lookup"><span data-stu-id="e397f-112">Reference</span></span>

[<span data-ttu-id="e397f-113">Estrutura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="e397f-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="e397f-114">Membros do JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="e397f-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="e397f-115">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="e397f-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

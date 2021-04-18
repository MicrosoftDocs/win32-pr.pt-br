---
description: 'Saiba mais sobre a propriedade: JET_ERRINFOBASIC. rgCategoricalHierarchy'
title: Propriedade JET_ERRINFOBASIC. rgCategoricalHierarchy (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'rgCategoricalHierarchy property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic.rgcategoricalhierarchy(v=EXCHG.10)
ms:contentKeyID: 55104314
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.set_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.get_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37034ca35427c9470d69f5e90dd43a4640601574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785256"
---
# <a name="jet_errinfobasicrgcategoricalhierarchy-property"></a><span data-ttu-id="9bb3e-103">Propriedade JET_ERRINFOBASIC. rgCategoricalHierarchy</span><span class="sxs-lookup"><span data-stu-id="9bb3e-103">JET_ERRINFOBASIC.rgCategoricalHierarchy property</span></span>

<span data-ttu-id="9bb3e-104">Obtém ou define a hierarquia de erros.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-104">Gets or sets the hierarchy of errors.</span></span> <span data-ttu-id="9bb3e-105">A posição 0 é o nível mais alto na hierarquia e o restante é JET_errcatUnknown.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-105">Position 0 is the highest level in the hierarchy, and the rest are JET_errcatUnknown.</span></span>

<span data-ttu-id="9bb3e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9bb3e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="9bb3e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9bb3e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb3e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bb3e-108">Syntax</span></span>

``` vb
'Declaration
Public Property rgCategoricalHierarchy As JET_ERRCAT()
    Get
    Set
'Usage
Dim instance As JET_ERRINFOBASIC
Dim value As JET_ERRCAT()

value = instance.rgCategoricalHierarchy

instance.rgCategoricalHierarchy = value
```

``` csharp
public JET_ERRCAT[] rgCategoricalHierarchy { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="9bb3e-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9bb3e-109">Property value</span></span>

<span data-ttu-id="9bb3e-110">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="9bb3e-110">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bb3e-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bb3e-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9bb3e-112">Referência</span><span class="sxs-lookup"><span data-stu-id="9bb3e-112">Reference</span></span>

[<span data-ttu-id="9bb3e-113">Classe JET_ERRINFOBASIC</span><span class="sxs-lookup"><span data-stu-id="9bb3e-113">JET_ERRINFOBASIC class</span></span>](./jet-errinfobasic-class.md)

[<span data-ttu-id="9bb3e-114">Membros do JET_ERRINFOBASIC</span><span class="sxs-lookup"><span data-stu-id="9bb3e-114">JET_ERRINFOBASIC members</span></span>](./jet-errinfobasic-members.md)

[<span data-ttu-id="9bb3e-115">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="9bb3e-115">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)

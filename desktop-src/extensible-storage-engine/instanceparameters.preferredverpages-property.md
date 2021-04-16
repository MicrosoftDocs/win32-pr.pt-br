---
description: 'Saiba mais sobre a propriedade: Instanceparameters. PreferredVerPages'
title: Propriedade instanceparameters. PreferredVerPages
TOCTitle: 'PreferredVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.preferredverpages(v=EXCHG.10)
ms:contentKeyID: 55103322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PreferredVerPages
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 067d41cd3fb945b2f18d3cd6154b1eef6793b1e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772607"
---
# <a name="instanceparameterspreferredverpages-property"></a><span data-ttu-id="1f37a-103">Propriedade instanceparameters. PreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="1f37a-103">InstanceParameters.PreferredVerPages property</span></span>

<span data-ttu-id="1f37a-104">Obtém ou define o número preferencial de páginas de repositório de versão reservadas para esta instância.</span><span class="sxs-lookup"><span data-stu-id="1f37a-104">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="1f37a-105">Se o tamanho do repositório de versão exceder esse limite, todas as informações usadas apenas para tarefas em segundo plano opcionais, como a recuperação de espaço excluído no banco de dados, serão sacrificadas para preservar espaço para informações transacionais.</span><span class="sxs-lookup"><span data-stu-id="1f37a-105">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="1f37a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f37a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1f37a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1f37a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f37a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f37a-108">Syntax</span></span>

``` vb
'Declaration
Public Property PreferredVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PreferredVerPages

instance.PreferredVerPages = value
```

``` csharp
public int PreferredVerPages { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1f37a-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1f37a-109">Property value</span></span>

<span data-ttu-id="1f37a-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1f37a-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1f37a-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f37a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f37a-112">Referência</span><span class="sxs-lookup"><span data-stu-id="1f37a-112">Reference</span></span>

[<span data-ttu-id="1f37a-113">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="1f37a-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="1f37a-114">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="1f37a-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="1f37a-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1f37a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

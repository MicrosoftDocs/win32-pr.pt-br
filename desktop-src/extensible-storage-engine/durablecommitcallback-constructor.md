---
description: 'Saiba mais sobre: Construtor DurableCommitCallback'
title: Construtor DurableCommitCallback (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'DurableCommitCallback constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.durablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.DurableCommitCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade1952615b98d9ea41a7a1b83d0bf1a3c6fc8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663126"
---
# <a name="durablecommitcallback-constructor"></a><span data-ttu-id="35b4a-103">Construtor DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="35b4a-103">DurableCommitCallback constructor</span></span>

<span data-ttu-id="35b4a-104">Inicializa uma nova instância da classe [DurableCommitCallback](./durablecommitcallback-class.md) .</span><span class="sxs-lookup"><span data-stu-id="35b4a-104">Initializes a new instance of the [DurableCommitCallback](./durablecommitcallback-class.md) class.</span></span>

<span data-ttu-id="35b4a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="35b4a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="35b4a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="35b4a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="35b4a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35b4a-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE, _
    wrappedCallback As JET_PFNDURABLECOMMITCALLBACK _
)
'Usage
Dim instance As JET_INSTANCE
Dim wrappedCallback As JET_PFNDURABLECOMMITCALLBACK

Dim instance As New DurableCommitCallback(instance, _
    wrappedCallback)
```

``` csharp
public DurableCommitCallback(
    JET_INSTANCE instance,
    JET_PFNDURABLECOMMITCALLBACK wrappedCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="35b4a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35b4a-108">Parameters</span></span>

  - <span data-ttu-id="35b4a-109">instance</span><span class="sxs-lookup"><span data-stu-id="35b4a-109">instance</span></span>  
    <span data-ttu-id="35b4a-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="35b4a-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="35b4a-111">A instância com a qual associar o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="35b4a-111">The instance with which to associate the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="35b4a-112">wrappedCallback</span><span class="sxs-lookup"><span data-stu-id="35b4a-112">wrappedCallback</span></span>  
    <span data-ttu-id="35b4a-113">Tipo: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="35b4a-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span></span>  
    
    <span data-ttu-id="35b4a-114">O retorno de chamada de código gerenciado a ser chamado.</span><span class="sxs-lookup"><span data-stu-id="35b4a-114">The managed code callback to call.</span></span>

## <a name="see-also"></a><span data-ttu-id="35b4a-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="35b4a-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="35b4a-116">Referência</span><span class="sxs-lookup"><span data-stu-id="35b4a-116">Reference</span></span>

[<span data-ttu-id="35b4a-117">Classe DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="35b4a-117">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="35b4a-118">Membros do DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="35b4a-118">DurableCommitCallback members</span></span>](./durablecommitcallback-members.md)

[<span data-ttu-id="35b4a-119">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="35b4a-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)

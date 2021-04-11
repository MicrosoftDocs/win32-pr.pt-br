---
description: 'Saiba mais sobre: método DurableCommitCallback. ReleaseResource'
title: Método DurableCommitCallback. ReleaseResource (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 634dd081513e576c7aabaac17cc5f9d207a8769f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171945"
---
# <a name="durablecommitcallbackreleaseresource-method"></a><span data-ttu-id="137d4-103">Método DurableCommitCallback. ReleaseResource</span><span class="sxs-lookup"><span data-stu-id="137d4-103">DurableCommitCallback.ReleaseResource method</span></span>

<span data-ttu-id="137d4-104">Libera a sessão de confirmação durável.</span><span class="sxs-lookup"><span data-stu-id="137d4-104">Frees the durable commit session.</span></span>

<span data-ttu-id="137d4-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="137d4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="137d4-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="137d4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="137d4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="137d4-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="remarks"></a><span data-ttu-id="137d4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="137d4-108">Remarks</span></span>

<span data-ttu-id="137d4-109">Não tente definir o parâmetro de instância como NULL, pois o retorno de chamada é descartado após JetTerm e o retorno de chamada não pode ser definido após JetTerm.</span><span class="sxs-lookup"><span data-stu-id="137d4-109">Do not try to set the instance parameter to null, because the callback is disposed after JetTerm and the callback cannot be set after JetTerm.</span></span>

## <a name="see-also"></a><span data-ttu-id="137d4-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="137d4-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="137d4-111">Referência</span><span class="sxs-lookup"><span data-stu-id="137d4-111">Reference</span></span>

[<span data-ttu-id="137d4-112">Classe DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="137d4-112">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="137d4-113">Membros do DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="137d4-113">DurableCommitCallback members</span></span>](./durablecommitcallback-members.md)

[<span data-ttu-id="137d4-114">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="137d4-114">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)

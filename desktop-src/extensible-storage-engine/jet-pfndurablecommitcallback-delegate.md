---
description: 'Saiba mais sobre: JET_PFNDURABLECOMMITCALLBACK delegado'
title: JET_PFNDURABLECOMMITCALLBACK delegado (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JET_PFNDURABLECOMMITCALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_pfndurablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104327
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.Invoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK..ctor
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.BeginInvoke
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9ff2f613138103be56db3fe7084202965a949cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837353"
---
# <a name="jet_pfndurablecommitcallback-delegate"></a><span data-ttu-id="5b148-103">JET_PFNDURABLECOMMITCALLBACK delegado</span><span class="sxs-lookup"><span data-stu-id="5b148-103">JET_PFNDURABLECOMMITCALLBACK delegate</span></span>

<span data-ttu-id="5b148-104">Retorno de chamada para JET_paramDurableCommitCallback.</span><span class="sxs-lookup"><span data-stu-id="5b148-104">Callback for JET_paramDurableCommitCallback.</span></span>

<span data-ttu-id="5b148-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5b148-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="5b148-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5b148-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5b148-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b148-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNDURABLECOMMITCALLBACK ( _
    instance As JET_INSTANCE, _
    pCommitIdSeen As JET_COMMIT_ID, _
    grbit As DurableCommitCallbackGrbit _
) As JET_err
'Usage
Dim instance As New JET_PFNDURABLECOMMITCALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNDURABLECOMMITCALLBACK(
    JET_INSTANCE instance,
    JET_COMMIT_ID pCommitIdSeen,
    DurableCommitCallbackGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5b148-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b148-108">Parameters</span></span>

  - <span data-ttu-id="5b148-109">instance</span><span class="sxs-lookup"><span data-stu-id="5b148-109">instance</span></span>  
    <span data-ttu-id="5b148-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5b148-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="5b148-111">Instância a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5b148-111">Instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b148-112">pCommitIdSeen</span><span class="sxs-lookup"><span data-stu-id="5b148-112">pCommitIdSeen</span></span>  
    <span data-ttu-id="5b148-113">Tipo: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="5b148-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="5b148-114">Confirmação-ID que acabou de ser liberada.</span><span class="sxs-lookup"><span data-stu-id="5b148-114">Commit-id that has just been flushed.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b148-115">grbit</span><span class="sxs-lookup"><span data-stu-id="5b148-115">grbit</span></span>  
    <span data-ttu-id="5b148-116">Tipo: [Microsoft. ISAM. ESENT. Interop. Windows8. DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5b148-116">Type: [Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5b148-117">Reservado no momento.</span><span class="sxs-lookup"><span data-stu-id="5b148-117">Reserved currently.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5b148-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b148-118">Return value</span></span>

<span data-ttu-id="5b148-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5b148-119">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5b148-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b148-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b148-121">Referência</span><span class="sxs-lookup"><span data-stu-id="5b148-121">Reference</span></span>

[<span data-ttu-id="5b148-122">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="5b148-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)

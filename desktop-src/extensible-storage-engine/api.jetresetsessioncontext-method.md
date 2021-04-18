---
description: 'Saiba mais sobre: método API. JetResetSessionContext'
title: Método API. JetResetSessionContext
TOCTitle: 'JetResetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100785
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a34a6c2922c0041f0720b498855b15c4aed23f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807151"
---
# <a name="apijetresetsessioncontext-method"></a><span data-ttu-id="9bf27-103">Método API. JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="9bf27-103">Api.JetResetSessionContext method</span></span>

<span data-ttu-id="9bf27-104">Desassocia uma sessão do thread atual.</span><span class="sxs-lookup"><span data-stu-id="9bf27-104">Disassociates a session from the current thread.</span></span> <span data-ttu-id="9bf27-105">Isso deve ser usado em conjunto com [JetSetSessionContext (JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md).</span><span class="sxs-lookup"><span data-stu-id="9bf27-105">This should be used in conjunction with [JetSetSessionContext(JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md).</span></span>

<span data-ttu-id="9bf27-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9bf27-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9bf27-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9bf27-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf27-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bf27-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetSessionContext ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetResetSessionContext(sesid)
```

``` csharp
public static void JetResetSessionContext(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="9bf27-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bf27-109">Parameters</span></span>

  - <span data-ttu-id="9bf27-110">sesid</span><span class="sxs-lookup"><span data-stu-id="9bf27-110">sesid</span></span>  
    <span data-ttu-id="9bf27-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bf27-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9bf27-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9bf27-112">The session to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bf27-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bf27-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9bf27-114">Referência</span><span class="sxs-lookup"><span data-stu-id="9bf27-114">Reference</span></span>

[<span data-ttu-id="9bf27-115">Classe de API</span><span class="sxs-lookup"><span data-stu-id="9bf27-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9bf27-116">Membros da API</span><span class="sxs-lookup"><span data-stu-id="9bf27-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9bf27-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9bf27-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

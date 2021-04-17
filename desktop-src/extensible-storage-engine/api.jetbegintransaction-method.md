---
description: 'Saiba mais sobre: método API. JetBeginTransaction'
title: Método API. JetBeginTransaction
TOCTitle: 'JetBeginTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction(v=EXCHG.10)
ms:contentKeyID: 55107225
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b8812df332734ee109ea52820346e433e747751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791056"
---
# <a name="apijetbegintransaction-method"></a><span data-ttu-id="ac1fe-103">Método API. JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="ac1fe-103">Api.JetBeginTransaction method</span></span>

<span data-ttu-id="ac1fe-104">Faz com que uma sessão Insira uma transação ou crie um novo ponto de salvamento em uma transação existente.</span><span class="sxs-lookup"><span data-stu-id="ac1fe-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="ac1fe-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac1fe-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ac1fe-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ac1fe-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac1fe-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetBeginTransaction(sesid)
```

``` csharp
public static void JetBeginTransaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="ac1fe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac1fe-108">Parameters</span></span>

  - <span data-ttu-id="ac1fe-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ac1fe-109">sesid</span></span>  
    <span data-ttu-id="ac1fe-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ac1fe-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ac1fe-111">A sessão para a qual iniciar a transação.</span><span class="sxs-lookup"><span data-stu-id="ac1fe-111">The session to begin the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac1fe-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac1fe-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac1fe-113">Referência</span><span class="sxs-lookup"><span data-stu-id="ac1fe-113">Reference</span></span>

[<span data-ttu-id="ac1fe-114">Classe de API</span><span class="sxs-lookup"><span data-stu-id="ac1fe-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ac1fe-115">Membros da API</span><span class="sxs-lookup"><span data-stu-id="ac1fe-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ac1fe-116">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ac1fe-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

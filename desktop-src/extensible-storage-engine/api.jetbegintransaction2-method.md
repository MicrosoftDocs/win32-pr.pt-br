---
description: 'Saiba mais sobre: método API. JetBeginTransaction2'
title: Método API. JetBeginTransaction2
TOCTitle: 'JetBeginTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction2(v=EXCHG.10)
ms:contentKeyID: 55107226
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d41652c4688bd736ac5f5164ca9b487a24edf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501230"
---
# <a name="apijetbegintransaction2-method"></a><span data-ttu-id="aa133-103">Método API. JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="aa133-103">Api.JetBeginTransaction2 method</span></span>

<span data-ttu-id="aa133-104">Faz com que uma sessão Insira uma transação ou crie um novo ponto de salvamento em uma transação existente.</span><span class="sxs-lookup"><span data-stu-id="aa133-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="aa133-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa133-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa133-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa133-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa133-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa133-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction2 ( _
    sesid As JET_SESID, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As BeginTransactionGrbitApi.JetBeginTransaction2(sesid, _
    grbit)
```

``` csharp
public static void JetBeginTransaction2(
    JET_SESID sesid,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="aa133-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa133-108">Parameters</span></span>

  - <span data-ttu-id="aa133-109">sesid</span><span class="sxs-lookup"><span data-stu-id="aa133-109">sesid</span></span>  
    <span data-ttu-id="aa133-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aa133-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="aa133-111">A sessão para a qual iniciar a transação.</span><span class="sxs-lookup"><span data-stu-id="aa133-111">The session to begin the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="aa133-112">grbit</span><span class="sxs-lookup"><span data-stu-id="aa133-112">grbit</span></span>  
    <span data-ttu-id="aa133-113">Tipo: [Microsoft. ISAM. ESENT. Interop. BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="aa133-113">Type: [Microsoft.Isam.Esent.Interop.BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="aa133-114">Opções de transação.</span><span class="sxs-lookup"><span data-stu-id="aa133-114">Transaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa133-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa133-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa133-116">Referência</span><span class="sxs-lookup"><span data-stu-id="aa133-116">Reference</span></span>

[<span data-ttu-id="aa133-117">Classe de API</span><span class="sxs-lookup"><span data-stu-id="aa133-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="aa133-118">Membros da API</span><span class="sxs-lookup"><span data-stu-id="aa133-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="aa133-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="aa133-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

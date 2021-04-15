---
description: 'Saiba mais sobre: método Windows8Api. JetBeginTransaction3'
title: Método Windows8Api. JetBeginTransaction3 (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetBeginTransaction3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3(Microsoft.Isam.Esent.Interop.JET_SESID,System.Int64,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetbegintransaction3(v=EXCHG.10)
ms:contentKeyID: 55107825
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7605cdb44c66d929e6663caaad9e40d3c98737b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502211"
---
# <a name="windows8apijetbegintransaction3-method"></a><span data-ttu-id="38ecd-103">Método Windows8Api. JetBeginTransaction3</span><span class="sxs-lookup"><span data-stu-id="38ecd-103">Windows8Api.JetBeginTransaction3 method</span></span>

<span data-ttu-id="38ecd-104">Faz com que uma sessão Insira uma transação ou crie um novo ponto de salvamento em uma transação existente.</span><span class="sxs-lookup"><span data-stu-id="38ecd-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="38ecd-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="38ecd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="38ecd-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="38ecd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="38ecd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38ecd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction3 ( _
    sesid As JET_SESID, _
    userTransactionId As Long, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim userTransactionId As Long
Dim grbit As BeginTransactionGrbitWindows8Api.JetBeginTransaction3(sesid, _
    userTransactionId, grbit)
```

``` csharp
public static void JetBeginTransaction3(
    JET_SESID sesid,
    long userTransactionId,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="38ecd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38ecd-108">Parameters</span></span>

  - <span data-ttu-id="38ecd-109">sesid</span><span class="sxs-lookup"><span data-stu-id="38ecd-109">sesid</span></span>  
    <span data-ttu-id="38ecd-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="38ecd-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="38ecd-111">A sessão para a qual iniciar a transação.</span><span class="sxs-lookup"><span data-stu-id="38ecd-111">The session to begin the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="38ecd-112">usertransactid</span><span class="sxs-lookup"><span data-stu-id="38ecd-112">userTransactionId</span></span>  
    <span data-ttu-id="38ecd-113">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="38ecd-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="38ecd-114">Um identificador opcional fornecido pelo usuário para identificar a transação.</span><span class="sxs-lookup"><span data-stu-id="38ecd-114">An optional identifier supplied by the user for identifying the transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="38ecd-115">grbit</span><span class="sxs-lookup"><span data-stu-id="38ecd-115">grbit</span></span>  
    <span data-ttu-id="38ecd-116">Tipo: [Microsoft. ISAM. ESENT. Interop. BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="38ecd-116">Type: [Microsoft.Isam.Esent.Interop.BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="38ecd-117">Opções de transação.</span><span class="sxs-lookup"><span data-stu-id="38ecd-117">Transaction options.</span></span>

## <a name="remarks"></a><span data-ttu-id="38ecd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="38ecd-118">Remarks</span></span>

<span data-ttu-id="38ecd-119">Introduzido no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="38ecd-119">Introduced in Windows 8.</span></span>

## <a name="see-also"></a><span data-ttu-id="38ecd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="38ecd-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="38ecd-121">Referência</span><span class="sxs-lookup"><span data-stu-id="38ecd-121">Reference</span></span>

[<span data-ttu-id="38ecd-122">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="38ecd-122">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="38ecd-123">Membros do Windows8Api</span><span class="sxs-lookup"><span data-stu-id="38ecd-123">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="38ecd-124">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="38ecd-124">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)

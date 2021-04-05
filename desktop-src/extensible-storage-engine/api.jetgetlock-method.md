---
description: 'Saiba mais sobre: método API. JetGetLock'
title: Método API. JetGetLock
TOCTitle: 'JetGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetlock(v=EXCHG.10)
ms:contentKeyID: 55100732
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8480b6ac2eab84a0299e0bb3d480908e4f646fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826947"
---
# <a name="apijetgetlock-method"></a><span data-ttu-id="48389-103">Método API. JetGetLock</span><span class="sxs-lookup"><span data-stu-id="48389-103">Api.JetGetLock method</span></span>

<span data-ttu-id="48389-104">Reserve explicitamente a capacidade de atualizar uma linha, bloqueio de gravação ou impedir explicitamente que uma linha seja atualizada por qualquer outra sessão, bloqueio de leitura.</span><span class="sxs-lookup"><span data-stu-id="48389-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="48389-105">Normalmente, os bloqueios de gravação de linha são adquiridos implicitamente como resultado da atualização de linhas.</span><span class="sxs-lookup"><span data-stu-id="48389-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="48389-106">Os bloqueios de leitura geralmente não são necessários devido ao controle de versão de registro.</span><span class="sxs-lookup"><span data-stu-id="48389-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="48389-107">No entanto, em alguns casos, uma transação pode desejar bloquear explicitamente uma linha para impor a serialização ou para garantir que uma operação subsequente terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="48389-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="48389-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="48389-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="48389-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="48389-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="48389-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48389-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbitApi.JetGetLock(sesid, tableid, grbit)
```

``` csharp
public static void JetGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="48389-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48389-111">Parameters</span></span>

  - <span data-ttu-id="48389-112">sesid</span><span class="sxs-lookup"><span data-stu-id="48389-112">sesid</span></span>  
    <span data-ttu-id="48389-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="48389-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="48389-114">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="48389-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="48389-115">TableID</span><span class="sxs-lookup"><span data-stu-id="48389-115">tableid</span></span>  
    <span data-ttu-id="48389-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="48389-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="48389-117">O cursor a ser usado.</span><span class="sxs-lookup"><span data-stu-id="48389-117">The cursor to use.</span></span> <span data-ttu-id="48389-118">Um bloqueio será adquirido no registro atual.</span><span class="sxs-lookup"><span data-stu-id="48389-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="48389-119">grbit</span><span class="sxs-lookup"><span data-stu-id="48389-119">grbit</span></span>  
    <span data-ttu-id="48389-120">Tipo: [Microsoft. ISAM. ESENT. Interop. GetLockGrbit](./getlockgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="48389-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="48389-121">Opções de bloqueio, use esta opção para especificar o tipo de bloqueio a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="48389-121">Lock options, use this to specify which type of lock to obtain.</span></span>

## <a name="see-also"></a><span data-ttu-id="48389-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="48389-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="48389-123">Referência</span><span class="sxs-lookup"><span data-stu-id="48389-123">Reference</span></span>

[<span data-ttu-id="48389-124">Classe de API</span><span class="sxs-lookup"><span data-stu-id="48389-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="48389-125">Membros da API</span><span class="sxs-lookup"><span data-stu-id="48389-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="48389-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="48389-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

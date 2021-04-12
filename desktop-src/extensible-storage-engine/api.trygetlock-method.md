---
description: 'Saiba mais sobre: método API. TryGetLock'
title: Método API. TryGetLock
TOCTitle: 'TryGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trygetlock(v=EXCHG.10)
ms:contentKeyID: 55100934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ecd4e0e66226d438b4e5a78b2397f5637154096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171761"
---
# <a name="apitrygetlock-method"></a><span data-ttu-id="6816c-103">Método API. TryGetLock</span><span class="sxs-lookup"><span data-stu-id="6816c-103">Api.TryGetLock method</span></span>

<span data-ttu-id="6816c-104">Reserve explicitamente a capacidade de atualizar uma linha, bloqueio de gravação ou impedir explicitamente que uma linha seja atualizada por qualquer outra sessão, bloqueio de leitura.</span><span class="sxs-lookup"><span data-stu-id="6816c-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="6816c-105">Normalmente, os bloqueios de gravação de linha são adquiridos implicitamente como resultado da atualização de linhas.</span><span class="sxs-lookup"><span data-stu-id="6816c-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="6816c-106">Os bloqueios de leitura geralmente não são necessários devido ao controle de versão de registro.</span><span class="sxs-lookup"><span data-stu-id="6816c-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="6816c-107">No entanto, em alguns casos, uma transação pode desejar bloquear explicitamente uma linha para impor a serialização ou para garantir que uma operação subsequente terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="6816c-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="6816c-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6816c-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6816c-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6816c-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6816c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6816c-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbit
Dim returnValue As Boolean

returnValue = Api.TryGetLock(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TryGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6816c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6816c-111">Parameters</span></span>

  - <span data-ttu-id="6816c-112">sesid</span><span class="sxs-lookup"><span data-stu-id="6816c-112">sesid</span></span>  
    <span data-ttu-id="6816c-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6816c-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6816c-114">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6816c-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6816c-115">TableID</span><span class="sxs-lookup"><span data-stu-id="6816c-115">tableid</span></span>  
    <span data-ttu-id="6816c-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6816c-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6816c-117">O cursor a ser usado.</span><span class="sxs-lookup"><span data-stu-id="6816c-117">The cursor to use.</span></span> <span data-ttu-id="6816c-118">Um bloqueio será adquirido no registro atual.</span><span class="sxs-lookup"><span data-stu-id="6816c-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="6816c-119">grbit</span><span class="sxs-lookup"><span data-stu-id="6816c-119">grbit</span></span>  
    <span data-ttu-id="6816c-120">Tipo: [Microsoft. ISAM. ESENT. Interop. GetLockGrbit](./getlockgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6816c-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6816c-121">Opções de bloqueio, use esta opção para especificar o tipo de bloqueio a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="6816c-121">Lock options, use this to specify which type of lock to obtain.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6816c-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6816c-122">Return value</span></span>

<span data-ttu-id="6816c-123">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6816c-123">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="6816c-124">True se o bloqueio foi obtido; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="6816c-124">True if the lock was obtained, false otherwise.</span></span> <span data-ttu-id="6816c-125">Uma exceção será gerada se um erro inesperado for encontrado.</span><span class="sxs-lookup"><span data-stu-id="6816c-125">An exception is thrown if an unexpected error is encountered.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6816c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6816c-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6816c-127">Referência</span><span class="sxs-lookup"><span data-stu-id="6816c-127">Reference</span></span>

[<span data-ttu-id="6816c-128">Classe de API</span><span class="sxs-lookup"><span data-stu-id="6816c-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6816c-129">Membros da API</span><span class="sxs-lookup"><span data-stu-id="6816c-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6816c-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6816c-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Saiba mais sobre: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826934"
---
# <a name="jet_sesid"></a><span data-ttu-id="4766a-103">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4766a-103">JET_SESID</span></span>


<span data-ttu-id="4766a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4766a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_sesid"></a><span data-ttu-id="4766a-105">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4766a-105">JET_SESID</span></span>

<span data-ttu-id="4766a-106">O tipo de dados **JET_SESID** contém um identificador para a sessão a ser usado para uma chamada para a API do Jet.</span><span class="sxs-lookup"><span data-stu-id="4766a-106">The **JET_SESID** data type contains a handle to the session to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a><span data-ttu-id="4766a-107">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="4766a-107">Data Types</span></span>

<span data-ttu-id="4766a-108">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4766a-108">JET_SESID</span></span>

<span data-ttu-id="4766a-109">**Nulo** ou [JET_sesidNil](./invalid-handle-constants.md) pode ser usado para indicar um identificador de sessão inválido.</span><span class="sxs-lookup"><span data-stu-id="4766a-109">Either **NULL** or [JET_sesidNil](./invalid-handle-constants.md) can be used to indicate an invalid session handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="4766a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4766a-110">Remarks</span></span>

<span data-ttu-id="4766a-111">Uma sessão é o contexto de transação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4766a-111">A session is the transaction context of the database engine.</span></span> <span data-ttu-id="4766a-112">Ele pode ser usado para iniciar, confirmar ou anular transações que afetam a visibilidade e a durabilidade das alterações feitas por esta ou outras sessões.</span><span class="sxs-lookup"><span data-stu-id="4766a-112">It can be used to begin, commit, or abort transactions that affect the visibility and durability of changes that are made by this or other sessions.</span></span>

<span data-ttu-id="4766a-113">Uma transação pode ser iniciada usando [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="4766a-113">A transaction can be started using [JetBeginTransaction](./jetbegintransaction-function.md).</span></span> <span data-ttu-id="4766a-114">Uma sessão pode ser criada usando [JetBeginSession](./jetbeginsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="4766a-114">A session may be created using [JetBeginSession](./jetbeginsession-function.md).</span></span> <span data-ttu-id="4766a-115">O número máximo de sessões que podem ser criadas a qualquer momento é controlado por [JET_paramMaxSessions](./resource-parameters.md), que pode ser configurado por meio de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="4766a-115">The maximum number of sessions that can be created at any one time is controlled by [JET_paramMaxSessions](./resource-parameters.md), which can be configured by means of [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="4766a-116">Uma sessão é encerrada explicitamente por uma chamada para [JetEndSession](./jetendsession-function.md) ou encerrada implicitamente por uma chamada para [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="4766a-116">A session is explicitly ended by a call to [JetEndSession](./jetendsession-function.md) or implicitly ended by a call to [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="4766a-117">Cada sessão só pode ser usada por um thread por vez.</span><span class="sxs-lookup"><span data-stu-id="4766a-117">Each session can only be used by one thread at a time.</span></span> <span data-ttu-id="4766a-118">Além disso, o comportamento padrão do mecanismo é restringir o uso de uma sessão para o mesmo thread a partir do momento em que a primeira chamada para [JetBeginTransaction](./jetbegintransaction-function.md) é feita até o momento em que a chamada de correspondência para [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) é feita.</span><span class="sxs-lookup"><span data-stu-id="4766a-118">In addition, the default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to [JetBeginTransaction](./jetbegintransaction-function.md) is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="4766a-119">Esse comportamento pode ser alterado para remover essa segunda restrição definindo um contexto de sessão personalizado usando [JetSetSessionContext](./jetsetsessioncontext-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="4766a-119">This behavior can be changed to remove this second restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="4766a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4766a-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4766a-121"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4766a-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4766a-122">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4766a-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4766a-123"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="4766a-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4766a-124">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4766a-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4766a-125"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="4766a-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4766a-126">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4766a-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4766a-127">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4766a-127">See Also</span></span>

[<span data-ttu-id="4766a-128">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="4766a-128">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="4766a-129">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="4766a-129">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="4766a-130">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="4766a-130">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="4766a-131">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="4766a-131">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="4766a-132">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="4766a-132">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="4766a-133">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="4766a-133">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="4766a-134">JetRollback</span><span class="sxs-lookup"><span data-stu-id="4766a-134">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="4766a-135">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="4766a-135">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="4766a-136">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4766a-136">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="4766a-137">JetTerm</span><span class="sxs-lookup"><span data-stu-id="4766a-137">JetTerm</span></span>](./jetterm-function.md)

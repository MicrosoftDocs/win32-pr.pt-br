---
description: 'Saiba mais sobre: Enumeração CommitTransactionGrbit'
title: Enumeração CommitTransactionGrbit
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a93504d688d1eddfcde81ae23c87e62f70e0aab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812112"
---
# <a name="committransactiongrbit-enumeration"></a><span data-ttu-id="f55c6-103">Enumeração CommitTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="f55c6-103">CommitTransactionGrbit enumeration</span></span>

<span data-ttu-id="f55c6-104">Opções para JetCommitTransaction.</span><span class="sxs-lookup"><span data-stu-id="f55c6-104">Options for JetCommitTransaction.</span></span>

<span data-ttu-id="f55c6-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="f55c6-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f55c6-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f55c6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f55c6-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f55c6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f55c6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f55c6-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="f55c6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f55c6-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f55c6-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="f55c6-110">Member name</span></span></th>
<th><span data-ttu-id="f55c6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f55c6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f55c6-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f55c6-112">None</span></span></td>
<td><span data-ttu-id="f55c6-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="f55c6-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f55c6-114">LazyFlush</span><span class="sxs-lookup"><span data-stu-id="f55c6-114">LazyFlush</span></span></td>
<td><span data-ttu-id="f55c6-115">A transação é confirmada normalmente, mas essa API não espera que a transação seja liberada para o arquivo de log de transações antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="f55c6-115">The transaction is committed normally but this Api does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="f55c6-116">Isso reduz drasticamente a duração de uma operação de confirmação no custo da durabilidade.</span><span class="sxs-lookup"><span data-stu-id="f55c6-116">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="f55c6-117">Qualquer transação que não seja liberada para o log antes de uma falha será abortada automaticamente durante a recuperação de falha durante a próxima chamada para JetInit.</span><span class="sxs-lookup"><span data-stu-id="f55c6-117">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to JetInit.</span></span> <span data-ttu-id="f55c6-118">Se WaitLastLevel0Commit ou WaitAllLevel0Commit forem especificados, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="f55c6-118">If WaitLastLevel0Commit or WaitAllLevel0Commit are specified, this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f55c6-119">WaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="f55c6-119">WaitLastLevel0Commit</span></span></td>
<td><span data-ttu-id="f55c6-120">Se a sessão tiver confirmado anteriormente quaisquer transações e elas ainda não tiverem sido liberadas para o arquivo de log de transações, elas deverão ser liberadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f55c6-120">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="f55c6-121">Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="f55c6-121">This Api will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="f55c6-122">Isso será útil se o aplicativo tiver confirmado anteriormente várias transações usando JET_bitCommitLazyFlush e agora quiser liberar todas elas para o disco.</span><span class="sxs-lookup"><span data-stu-id="f55c6-122">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span>
<p><span data-ttu-id="f55c6-123">Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="f55c6-123">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="f55c6-124">Essa opção não pode ser usada em combinação com nenhuma outra opção.</span><span class="sxs-lookup"><span data-stu-id="f55c6-124">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f55c6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f55c6-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f55c6-126">Referência</span><span class="sxs-lookup"><span data-stu-id="f55c6-126">Reference</span></span>

[<span data-ttu-id="f55c6-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f55c6-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

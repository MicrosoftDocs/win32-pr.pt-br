---
description: 'Saiba mais sobre: membros do Server2003Grbits'
title: Membros Server2003Grbits (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21008153606a6c35c76daf3c2758211f3fcdd42e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828636"
---
# <a name="server2003grbits-members"></a><span data-ttu-id="f844c-103">Membros do Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="f844c-103">Server2003Grbits members</span></span>

<span data-ttu-id="f844c-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="f844c-104">Include protected members</span></span>  
<span data-ttu-id="f844c-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="f844c-105">Include inherited members</span></span>  

<span data-ttu-id="f844c-106">Grbits que foram adicionados à versão 2003 do Windows Server do ESENT.</span><span class="sxs-lookup"><span data-stu-id="f844c-106">Grbits that have been added to the Windows Server 2003 version of ESENT.</span></span>

<span data-ttu-id="f844c-107">O tipo [Server2003Grbits](./server2003grbits-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f844c-107">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="f844c-108">Campos</span><span class="sxs-lookup"><span data-stu-id="f844c-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f844c-109">Nome</span><span class="sxs-lookup"><span data-stu-id="f844c-109">Name</span></span></th>
<th><span data-ttu-id="f844c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f844c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f844c-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span><span class="sxs-lookup"><span data-stu-id="f844c-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="f844c-114">Se uma determinada coluna não estiver presente no registro e tiver um valor padrão definido pelo usuário, nenhum valor de coluna será retornado.</span><span class="sxs-lookup"><span data-stu-id="f844c-114">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="f844c-115">Essa opção impedirá o retorno de chamada que computa o valor padrão definido pelo usuário para que a coluna seja chamada ao enumerar os valores para essa coluna.</span><span class="sxs-lookup"><span data-stu-id="f844c-115">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f844c-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span><span class="sxs-lookup"><span data-stu-id="f844c-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="f844c-119">Essa opção solicita que a tabela temporária só seja criada se o Gerenciador de tabelas temporárias puder usar a implementação otimizada para resultados de consulta intermediários.</span><span class="sxs-lookup"><span data-stu-id="f844c-119">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="f844c-120">Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="f844c-120">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="f844c-121">Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="f844c-121">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="f844c-122">Consulte <a href="hh558517(v=exchg.10).md">exclusivo</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f844c-122">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f844c-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="f844c-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="f844c-126">Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberadas para o arquivo de log de transações serão liberadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f844c-126">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="f844c-127">Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="f844c-127">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="f844c-128">Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="f844c-128">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="f844c-129">Essa opção não pode ser usada em combinação com nenhuma outra opção.</span><span class="sxs-lookup"><span data-stu-id="f844c-129">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f844c-130">Parte superior</span><span class="sxs-lookup"><span data-stu-id="f844c-130">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f844c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f844c-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f844c-132">Referência</span><span class="sxs-lookup"><span data-stu-id="f844c-132">Reference</span></span>

[<span data-ttu-id="f844c-133">Classe Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="f844c-133">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="f844c-134">Namespace Microsoft. ISAM. ESENT. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="f844c-134">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

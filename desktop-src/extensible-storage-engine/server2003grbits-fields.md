---
description: 'Saiba mais sobre: campos Server2003Grbits'
title: Campos Server2003Grbits (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ed7a99118674d955fc6a882ac08407e45837af77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569014"
---
# <a name="server2003grbits-fields"></a><span data-ttu-id="f4940-103">Campos Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="f4940-103">Server2003Grbits fields</span></span>

<span data-ttu-id="f4940-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="f4940-104">Include protected members</span></span>  
<span data-ttu-id="f4940-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="f4940-105">Include inherited members</span></span>  

<span data-ttu-id="f4940-106">O tipo [Server2003Grbits](./server2003grbits-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4940-106">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="f4940-107">Campos</span><span class="sxs-lookup"><span data-stu-id="f4940-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f4940-108">Nome</span><span class="sxs-lookup"><span data-stu-id="f4940-108">Name</span></span></th>
<th><span data-ttu-id="f4940-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4940-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f4940-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span><span class="sxs-lookup"><span data-stu-id="f4940-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="f4940-113">Se uma determinada coluna não estiver presente no registro e tiver um valor padrão definido pelo usuário, nenhum valor de coluna será retornado.</span><span class="sxs-lookup"><span data-stu-id="f4940-113">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="f4940-114">Essa opção impedirá o retorno de chamada que computa o valor padrão definido pelo usuário para que a coluna seja chamada ao enumerar os valores para essa coluna.</span><span class="sxs-lookup"><span data-stu-id="f4940-114">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f4940-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span><span class="sxs-lookup"><span data-stu-id="f4940-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="f4940-118">Essa opção solicita que a tabela temporária só seja criada se o Gerenciador de tabelas temporárias puder usar a implementação otimizada para resultados de consulta intermediários.</span><span class="sxs-lookup"><span data-stu-id="f4940-118">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="f4940-119">Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="f4940-119">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="f4940-120">Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="f4940-120">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="f4940-121">Consulte <a href="hh558517(v=exchg.10).md">exclusivo</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f4940-121">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="f4940-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="f4940-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="f4940-125">Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberadas para o arquivo de log de transações serão liberadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f4940-125">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="f4940-126">Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="f4940-126">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="f4940-127">Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="f4940-127">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="f4940-128">Essa opção não pode ser usada em combinação com nenhuma outra opção.</span><span class="sxs-lookup"><span data-stu-id="f4940-128">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f4940-129">Parte superior</span><span class="sxs-lookup"><span data-stu-id="f4940-129">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f4940-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4940-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f4940-131">Referência</span><span class="sxs-lookup"><span data-stu-id="f4940-131">Reference</span></span>

[<span data-ttu-id="f4940-132">Classe Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="f4940-132">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="f4940-133">Namespace Microsoft. ISAM. ESENT. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="f4940-133">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

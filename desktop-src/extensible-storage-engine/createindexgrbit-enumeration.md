---
description: 'Saiba mais sobre: Enumeração CreateIndexGrbit'
title: Enumeração CreateIndexGrbit
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793942"
---
# <a name="createindexgrbit-enumeration"></a><span data-ttu-id="5504b-103">Enumeração CreateIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="5504b-103">CreateIndexGrbit enumeration</span></span>

<span data-ttu-id="5504b-104">Opções para JetCreateIndex.</span><span class="sxs-lookup"><span data-stu-id="5504b-104">Options for JetCreateIndex.</span></span>

<span data-ttu-id="5504b-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="5504b-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="5504b-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5504b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5504b-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5504b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5504b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5504b-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
```

## <a name="members"></a><span data-ttu-id="5504b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="5504b-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="5504b-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="5504b-110">Member name</span></span></th>
<th><span data-ttu-id="5504b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5504b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5504b-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5504b-112">None</span></span></td>
<td><span data-ttu-id="5504b-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="5504b-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5504b-114">IndexUnique</span><span class="sxs-lookup"><span data-stu-id="5504b-114">IndexUnique</span></span></td>
<td><span data-ttu-id="5504b-115">Entradas de índice duplicadas (chaves) não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="5504b-115">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="5504b-116">Isso é imposto quando JetUpdate é chamado, não quando JetSetColumn é chamado.</span><span class="sxs-lookup"><span data-stu-id="5504b-116">This is enforced when JetUpdate is called, not when JetSetColumn is called.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5504b-117">IndexPrimary</span><span class="sxs-lookup"><span data-stu-id="5504b-117">IndexPrimary</span></span></td>
<td><span data-ttu-id="5504b-118">O índice é um índice primário (clusterizado).</span><span class="sxs-lookup"><span data-stu-id="5504b-118">The index is a primary (clustered) index.</span></span> <span data-ttu-id="5504b-119">Cada tabela deve ter exatamente um índice primário.</span><span class="sxs-lookup"><span data-stu-id="5504b-119">Every table must have exactly one primary index.</span></span> <span data-ttu-id="5504b-120">Se nenhum índice primário for explicitamente definido em uma tabela, o mecanismo de banco de dados criará seu próprio índice primário.</span><span class="sxs-lookup"><span data-stu-id="5504b-120">If no primary index is explicitly defined over a table, then the database engine will create its own primary index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5504b-121">IndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="5504b-121">IndexDisallowNull</span></span></td>
<td><span data-ttu-id="5504b-122">Nenhuma das colunas sobre as quais o índice é criado pode conter um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="5504b-122">None of the columns over which the index is created may contain a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5504b-123">IndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="5504b-123">IndexIgnoreNull</span></span></td>
<td><span data-ttu-id="5504b-124">Não adicione uma entrada de índice para uma linha se todas as colunas que estão sendo indexadas forem nulas.</span><span class="sxs-lookup"><span data-stu-id="5504b-124">Do not add an index entry for a row if all of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5504b-125">IndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="5504b-125">IndexIgnoreAnyNull</span></span></td>
<td><span data-ttu-id="5504b-126">Não adicione uma entrada de índice para uma linha se qualquer uma das colunas que estão sendo indexadas for nula.</span><span class="sxs-lookup"><span data-stu-id="5504b-126">Do not add an index entry for a row if any of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5504b-127">IndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="5504b-127">IndexIgnoreFirstNull</span></span></td>
<td><span data-ttu-id="5504b-128">Não adicione uma entrada de índice para uma linha se a primeira coluna que está sendo indexada for nula.</span><span class="sxs-lookup"><span data-stu-id="5504b-128">Do not add an index entry for a row if the first column being indexed is NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5504b-129">IndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="5504b-129">IndexLazyFlush</span></span></td>
<td><span data-ttu-id="5504b-130">Especifica que as operações de índice serão registradas lentamente.</span><span class="sxs-lookup"><span data-stu-id="5504b-130">Specifies that the index operations will be logged lazily.</span></span> <span data-ttu-id="5504b-131">JET_bitIndexLazyFlush não afeta a ociosa das atualizações de dados.</span><span class="sxs-lookup"><span data-stu-id="5504b-131">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="5504b-132">Se as operações de indexação forem interrompidas pelo encerramento do processo, a recuperação simples ainda poderá obter o banco de dados para um estado consistente, mas o índice poderá não estar presente.</span><span class="sxs-lookup"><span data-stu-id="5504b-132">If the indexing operations is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5504b-133">IndexEmpty</span><span class="sxs-lookup"><span data-stu-id="5504b-133">IndexEmpty</span></span></td>
<td><span data-ttu-id="5504b-134">Não tente Compilar o índice, pois todas as entradas seriam avaliadas como nulas.</span><span class="sxs-lookup"><span data-stu-id="5504b-134">Do not attempt to build the index, because all entries would evaluate to NULL.</span></span> <span data-ttu-id="5504b-135">grbit também deve especificar JET_bitIgnoreAnyNull quando JET_bitIndexEmpty for passado.</span><span class="sxs-lookup"><span data-stu-id="5504b-135">grbit MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="5504b-136">Esse é um aprimoramento de desempenho.</span><span class="sxs-lookup"><span data-stu-id="5504b-136">This is a performance enhancement.</span></span> <span data-ttu-id="5504b-137">Por exemplo, se uma nova coluna for adicionada a uma tabela, um índice será criado nessa coluna recém-adicionada, todos os registros na tabela seriam verificados mesmo que nunca sejam adicionados ao índice mesmo assim.</span><span class="sxs-lookup"><span data-stu-id="5504b-137">For example if a new column is added to a table, then an index is created over this newly added column, all of the records in the table would be scanned even though they would never get added to the index anyway.</span></span> <span data-ttu-id="5504b-138">Especificar JET_bitIndexEmpty ignora a verificação da tabela, o que pode levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="5504b-138">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5504b-139">IndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="5504b-139">IndexUnversioned</span></span></td>
<td><span data-ttu-id="5504b-140">Faz com que a criação do índice seja visível para outras transações.</span><span class="sxs-lookup"><span data-stu-id="5504b-140">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="5504b-141">Normalmente, uma sessão em uma transação não poderá ver uma operação de criação de índice em outra sessão.</span><span class="sxs-lookup"><span data-stu-id="5504b-141">Normally a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="5504b-142">Esse sinalizador pode ser útil se outra transação for provavelmente criar o mesmo índice, de modo que o segundo índice-Create simplesmente falhará em vez de causar muitas operações desnecessárias de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5504b-142">This flag can be useful if another transaction is likely to create the same index, so that the second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="5504b-143">A segunda transação pode não ser capaz de usar o índice imediatamente.</span><span class="sxs-lookup"><span data-stu-id="5504b-143">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="5504b-144">A operação de criação de índice precisa ser concluída antes de ser utilizável.</span><span class="sxs-lookup"><span data-stu-id="5504b-144">The index creation operation needs to complete before it is usable.</span></span> <span data-ttu-id="5504b-145">A sessão não deve estar em uma transação no momento para criar um índice sem informações de versão.</span><span class="sxs-lookup"><span data-stu-id="5504b-145">The session must not currently be in a transaction to create an index without version information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5504b-146">IndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="5504b-146">IndexSortNullsHigh</span></span></td>
<td><span data-ttu-id="5504b-147">A especificação desse sinalizador faz com que valores nulos sejam classificados após os dados de todas as colunas no índice.</span><span class="sxs-lookup"><span data-stu-id="5504b-147">Specifying this flag causes NULL values to be sorted after data for all columns in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5504b-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="5504b-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5504b-149">Referência</span><span class="sxs-lookup"><span data-stu-id="5504b-149">Reference</span></span>

[<span data-ttu-id="5504b-150">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5504b-150">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

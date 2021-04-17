---
description: 'Saiba mais sobre: Enumeração TempTableGrbit'
title: Enumeração TempTableGrbit
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813011"
---
# <a name="temptablegrbit-enumeration"></a><span data-ttu-id="816d6-103">Enumeração TempTableGrbit</span><span class="sxs-lookup"><span data-stu-id="816d6-103">TempTableGrbit enumeration</span></span>

<span data-ttu-id="816d6-104">Opções para a criação de tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="816d6-104">Options for temporary table creation.</span></span>

<span data-ttu-id="816d6-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="816d6-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="816d6-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="816d6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="816d6-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="816d6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="816d6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="816d6-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
```

## <a name="members"></a><span data-ttu-id="816d6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="816d6-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="816d6-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="816d6-110">Member name</span></span></th>
<th><span data-ttu-id="816d6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="816d6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="816d6-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="816d6-112">None</span></span></td>
<td><span data-ttu-id="816d6-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="816d6-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="816d6-114">Indexa</span><span class="sxs-lookup"><span data-stu-id="816d6-114">Indexed</span></span></td>
<td><span data-ttu-id="816d6-115">Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir o uso de JetSeek para pesquisar registros por chave de índice.</span><span class="sxs-lookup"><span data-stu-id="816d6-115">This option requests that the temporary table be flexible enough to permit the use of JetSeek to lookup records by index key.</span></span> <span data-ttu-id="816d6-116">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="816d6-116">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="816d6-117">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="816d6-117">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="816d6-118">Exclusivo</span><span class="sxs-lookup"><span data-stu-id="816d6-118">Unique</span></span></td>
<td><span data-ttu-id="816d6-119">Essa opção solicita que os registros com chaves de índice duplicados sejam removidos do conjunto final de registros na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="816d6-119">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span> <span data-ttu-id="816d6-120">Antes do Windows Server 2003, o mecanismo de banco de dados sempre assumiu que essa opção está em vigor devido ao fato de que todos os índices clusterizados também devem ser uma chave primária e, portanto, devem ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="816d6-120">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="816d6-121">A partir do Windows Server 2003, agora é possível criar uma tabela temporária que não remove duplicatas quando a opção <a href="dn351284(v=exchg.10).md">ForwardOnly</a> também é especificada.</span><span class="sxs-lookup"><span data-stu-id="816d6-121">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the <a href="dn351284(v=exchg.10).md">ForwardOnly</a> option is also specified.</span></span> <span data-ttu-id="816d6-122">Não é possível saber qual duplicata será vencedora e quais duplicatas serão descartadas em geral.</span><span class="sxs-lookup"><span data-stu-id="816d6-122">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="816d6-123">No entanto, quando a opção ErrorOnDuplicateInsertion é solicitada, o primeiro registro com uma determinada chave de índice a ser inserido na tabela temporária sempre vencerá.</span><span class="sxs-lookup"><span data-stu-id="816d6-123">However, when the ErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="816d6-124">Atualizável</span><span class="sxs-lookup"><span data-stu-id="816d6-124">Updatable</span></span></td>
<td><span data-ttu-id="816d6-125">Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros que foram inseridos anteriormente sejam alterados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="816d6-125">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="816d6-126">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="816d6-126">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="816d6-127">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="816d6-127">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="816d6-128">Rolável</span><span class="sxs-lookup"><span data-stu-id="816d6-128">Scrollable</span></span></td>
<td><span data-ttu-id="816d6-129">Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros sejam verificados em ordem e direção arbitrárias usando <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="816d6-129">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span> <span data-ttu-id="816d6-130">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="816d6-130">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="816d6-131">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="816d6-131">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="816d6-132">SortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="816d6-132">SortNullsHigh</span></span></td>
<td><span data-ttu-id="816d6-133">Essa opção solicita que os valores da coluna de chave nula se aproximem do final do índice que os valores de coluna de chave não nulos.</span><span class="sxs-lookup"><span data-stu-id="816d6-133">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="816d6-134">ForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="816d6-134">ForceMaterialization</span></span></td>
<td><span data-ttu-id="816d6-135">Essa opção força o Gerenciador de tabelas temporária a abandonar qualquer tentativa de escolher uma estratégia inteligente para gerenciar a tabela temporária que resultará em desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="816d6-135">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="816d6-136">ErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="816d6-136">ErrorOnDuplicateInsertion</span></span></td>
<td><span data-ttu-id="816d6-137">Essa opção solicita que qualquer tentativa de inserir um registro com a mesma chave de índice que um registro inserido anteriormente falhe imediatamente com <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span><span class="sxs-lookup"><span data-stu-id="816d6-137">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span></span> <span data-ttu-id="816d6-138">Se essa opção não for solicitada, uma duplicata poderá ser detectada imediatamente e falhará ou poderá ser removida silenciosamente mais tarde, dependendo da estratégia escolhida pelo mecanismo de banco de dados para implementar a tabela temporária com base na funcionalidade solicitada.</span><span class="sxs-lookup"><span data-stu-id="816d6-138">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span> <span data-ttu-id="816d6-139">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="816d6-139">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="816d6-140">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="816d6-140">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="816d6-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="816d6-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="816d6-142">Referência</span><span class="sxs-lookup"><span data-stu-id="816d6-142">Reference</span></span>

[<span data-ttu-id="816d6-143">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="816d6-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="816d6-144">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="816d6-144">ForwardOnly</span></span>](./server2003grbits.forwardonly-field.md)

[<span data-ttu-id="816d6-145">IntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="816d6-145">IntrinsicLVsOnly</span></span>](./windows7grbits.intrinsiclvsonly-field.md)

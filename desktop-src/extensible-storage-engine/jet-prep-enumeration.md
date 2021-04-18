---
description: 'Saiba mais sobre: enumeração de JET_prep'
title: Enumeração de JET_prep
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788942"
---
# <a name="jet_prep-enumeration"></a><span data-ttu-id="b7cb6-103">Enumeração de JET_prep</span><span class="sxs-lookup"><span data-stu-id="b7cb6-103">JET_prep enumeration</span></span>

<span data-ttu-id="b7cb6-104">Tipos de atualização para JetPrepareUpdate.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-104">Update types for JetPrepareUpdate.</span></span>

<span data-ttu-id="b7cb6-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7cb6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7cb6-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b7cb6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7cb6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7cb6-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a><span data-ttu-id="b7cb6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b7cb6-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b7cb6-109">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="b7cb6-109">Member name</span></span></th>
<th><span data-ttu-id="b7cb6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7cb6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b7cb6-111">Inserir</span><span class="sxs-lookup"><span data-stu-id="b7cb6-111">Insert</span></span></td>
<td><span data-ttu-id="b7cb6-112">Esse sinalizador faz com que o cursor se prepare para uma inserção de um novo registro.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-112">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="b7cb6-113">Todos os dados são inicializados para o estado padrão do registro.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-113">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="b7cb6-114">Se a tabela tiver uma coluna de incremento automático, um novo valor será atribuído a esse registro, independentemente de a atualização ter êxito ou não ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-114">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b7cb6-115">Substitua</span><span class="sxs-lookup"><span data-stu-id="b7cb6-115">Replace</span></span></td>
<td><span data-ttu-id="b7cb6-116">Esse sinalizador faz com que o cursor se prepare para uma substituição do registro atual.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-116">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="b7cb6-117">Se a tabela tiver uma coluna de versão, a coluna versão será definida como o próximo valor em sua sequência.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-117">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="b7cb6-118">Se essa atualização não for concluída, o valor da versão no registro não será afetado.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-118">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="b7cb6-119">Um bloqueio de atualização é obtido no registro para impedir que outras sessões atualizem esse registro antes da conclusão desta sessão.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-119">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b7cb6-120">Cancelar</span><span class="sxs-lookup"><span data-stu-id="b7cb6-120">Cancel</span></span></td>
<td><span data-ttu-id="b7cb6-121">Esse sinalizador faz com que JetPrepareUpdate cancele a atualização para este cursor.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-121">This flag causes JetPrepareUpdate to cancel the update for this cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b7cb6-122">ReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="b7cb6-122">ReplaceNoLock</span></span></td>
<td><span data-ttu-id="b7cb6-123">Esse sinalizador é semelhante a JET_prepReplace, mas nenhum bloqueio é usado para impedir que outras sessões atualizem esse registro.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-123">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="b7cb6-124">Em vez disso, essa sessão pode receber JET_errWriteConflict quando chama JetUpdate para concluir a atualização.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-124">Instead, this session may receive JET_errWriteConflict when it calls JetUpdate to complete the update.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b7cb6-125">InsertCopy</span><span class="sxs-lookup"><span data-stu-id="b7cb6-125">InsertCopy</span></span></td>
<td><span data-ttu-id="b7cb6-126">Esse sinalizador faz com que o cursor se prepare para uma inserção de uma cópia do registro existente.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-126">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="b7cb6-127">Deve haver um registro atual se essa opção for usada.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-127">There must be a current record if this option is used.</span></span> <span data-ttu-id="b7cb6-128">O estado inicial do novo registro é copiado do registro atual.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-128">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="b7cb6-129">Valores longos armazenados fora do registro são praticamente copiados.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-129">Long values that are stored off-record are virtually copied.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b7cb6-130">InsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="b7cb6-130">InsertCopyDeleteOriginal</span></span></td>
<td><span data-ttu-id="b7cb6-131">Esse sinalizador faz com que o cursor se prepare para uma inserção do mesmo registro e um Delete ou o registro original.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-131">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="b7cb6-132">Ele é usado em casos em que a chave primária foi alterada.</span><span class="sxs-lookup"><span data-stu-id="b7cb6-132">It is used in cases in which the primary key has changed.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b7cb6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7cb6-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7cb6-134">Referência</span><span class="sxs-lookup"><span data-stu-id="b7cb6-134">Reference</span></span>

[<span data-ttu-id="b7cb6-135">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b7cb6-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

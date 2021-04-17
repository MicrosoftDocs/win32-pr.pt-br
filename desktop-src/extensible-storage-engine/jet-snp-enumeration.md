---
description: 'Saiba mais sobre: enumeração de JET_SNP'
title: Enumeração de JET_SNP
TOCTitle: JET_SNP enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNP
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snp(v=EXCHG.10)
ms:contentKeyID: 39511218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10061d0c00d90aa5ca4e0778cba046d2e6f62f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763821"
---
# <a name="jet_snp-enumeration"></a><span data-ttu-id="142ed-103">Enumeração de JET_SNP</span><span class="sxs-lookup"><span data-stu-id="142ed-103">JET_SNP enumeration</span></span>

<span data-ttu-id="142ed-104">O tipo de operação em que o progresso está sendo relatado.</span><span class="sxs-lookup"><span data-stu-id="142ed-104">The type of operation that progress is being reported for.</span></span>

<span data-ttu-id="142ed-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="142ed-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="142ed-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="142ed-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="142ed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="142ed-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNP
'Usage
Dim instance As JET_SNP
```

``` csharp
public enum JET_SNP
```

## <a name="members"></a><span data-ttu-id="142ed-108">Membros</span><span class="sxs-lookup"><span data-stu-id="142ed-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="142ed-109">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="142ed-109">Member name</span></span></th>
<th><span data-ttu-id="142ed-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="142ed-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="142ed-111">Reparar</span><span class="sxs-lookup"><span data-stu-id="142ed-111">Repair</span></span></td>
<td><span data-ttu-id="142ed-112">O retorno de chamada é para uma opção de reparo.</span><span class="sxs-lookup"><span data-stu-id="142ed-112">Callback is for a repair option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="142ed-113">Compacto</span><span class="sxs-lookup"><span data-stu-id="142ed-113">Compact</span></span></td>
<td><span data-ttu-id="142ed-114">O retorno de chamada é para desfragmentação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="142ed-114">Callback is for database defragmentation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="142ed-115">Restaurar</span><span class="sxs-lookup"><span data-stu-id="142ed-115">Restore</span></span></td>
<td><span data-ttu-id="142ed-116">O retorno de chamada é para uma opção de restauração.</span><span class="sxs-lookup"><span data-stu-id="142ed-116">Callback is for a restore options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="142ed-117">Backup</span><span class="sxs-lookup"><span data-stu-id="142ed-117">Backup</span></span></td>
<td><span data-ttu-id="142ed-118">O retorno de chamada é para uma opção de backup.</span><span class="sxs-lookup"><span data-stu-id="142ed-118">Callback is for a backup options.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="142ed-119">Scrubbing</span><span class="sxs-lookup"><span data-stu-id="142ed-119">Scrub</span></span></td>
<td><span data-ttu-id="142ed-120">O retorno de chamada é para zeroing de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="142ed-120">Callback is for database zeroing.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="142ed-121">UpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="142ed-121">UpgradeRecordFormat</span></span></td>
<td><span data-ttu-id="142ed-122">O retorno de chamada é para o processo de atualização do formato de registro de todas as páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="142ed-122">Callback is for the process of upgrading the record format of all database pages.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="142ed-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="142ed-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="142ed-124">Referência</span><span class="sxs-lookup"><span data-stu-id="142ed-124">Reference</span></span>

[<span data-ttu-id="142ed-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="142ed-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

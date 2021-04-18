---
description: 'Saiba mais sobre: Enumeração BackupGrbit'
title: Enumeração BackupGrbit
TOCTitle: BackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.backupgrbit(v=EXCHG.10)
ms:contentKeyID: 39512196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bda9754efcae8ebe353b8272ba57c5640ecdf946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764724"
---
# <a name="backupgrbit-enumeration"></a><span data-ttu-id="02687-103">Enumeração BackupGrbit</span><span class="sxs-lookup"><span data-stu-id="02687-103">BackupGrbit enumeration</span></span>

<span data-ttu-id="02687-104">Opções para [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="02687-104">Options for [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<span data-ttu-id="02687-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="02687-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="02687-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02687-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02687-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02687-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02687-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02687-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BackupGrbit
'Usage
Dim instance As BackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BackupGrbit
```

## <a name="members"></a><span data-ttu-id="02687-109">Membros</span><span class="sxs-lookup"><span data-stu-id="02687-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="02687-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="02687-110">Member name</span></span></th>
<th><span data-ttu-id="02687-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="02687-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="02687-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="02687-112">None</span></span></td>
<td><span data-ttu-id="02687-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="02687-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="02687-114">Incremental</span><span class="sxs-lookup"><span data-stu-id="02687-114">Incremental</span></span></td>
<td><span data-ttu-id="02687-115">Cria um backup incremental em oposição a um backup completo.</span><span class="sxs-lookup"><span data-stu-id="02687-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="02687-116">Isso significa que somente os arquivos de log criados desde o último backup completo ou incremental serão submetidos a backup.</span><span class="sxs-lookup"><span data-stu-id="02687-116">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="02687-117">Atômica</span><span class="sxs-lookup"><span data-stu-id="02687-117">Atomic</span></span></td>
<td><span data-ttu-id="02687-118">Cria um backup completo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="02687-118">Creates a full backup of the database.</span></span> <span data-ttu-id="02687-119">Isso permite a preservação de um backup existente no mesmo diretório se o novo backup falhar.</span><span class="sxs-lookup"><span data-stu-id="02687-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="02687-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="02687-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02687-121">Referência</span><span class="sxs-lookup"><span data-stu-id="02687-121">Reference</span></span>

[<span data-ttu-id="02687-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="02687-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

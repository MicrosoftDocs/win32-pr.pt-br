---
description: 'Saiba mais sobre: Enumeração BeginExternalBackupGrbit'
title: Enumeração BeginExternalBackupGrbit
TOCTitle: BeginExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.beginexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39509773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b68cbfc75d0a71eacedb4bbd462fcd8a93d43690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781009"
---
# <a name="beginexternalbackupgrbit-enumeration"></a><span data-ttu-id="281b7-103">Enumeração BeginExternalBackupGrbit</span><span class="sxs-lookup"><span data-stu-id="281b7-103">BeginExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="281b7-104">Opções para [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="281b7-104">Options for [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="281b7-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="281b7-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="281b7-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="281b7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="281b7-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="281b7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="281b7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="281b7-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginExternalBackupGrbit
'Usage
Dim instance As BeginExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="281b7-109">Membros</span><span class="sxs-lookup"><span data-stu-id="281b7-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="281b7-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="281b7-110">Member name</span></span></th>
<th><span data-ttu-id="281b7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="281b7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="281b7-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="281b7-112">None</span></span></td>
<td><span data-ttu-id="281b7-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="281b7-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="281b7-114">Incremental</span><span class="sxs-lookup"><span data-stu-id="281b7-114">Incremental</span></span></td>
<td><span data-ttu-id="281b7-115">Cria um backup incremental em oposição a um backup completo.</span><span class="sxs-lookup"><span data-stu-id="281b7-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="281b7-116">Isso significa que somente os arquivos de log desde o último backup completo ou incremental serão submetidos a backup.</span><span class="sxs-lookup"><span data-stu-id="281b7-116">This means that only the log files since the last full or incremental backup will be backed up.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="281b7-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="281b7-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="281b7-118">Referência</span><span class="sxs-lookup"><span data-stu-id="281b7-118">Reference</span></span>

[<span data-ttu-id="281b7-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="281b7-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

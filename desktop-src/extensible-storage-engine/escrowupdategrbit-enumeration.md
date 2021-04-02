---
description: 'Saiba mais sobre: Enumeração EscrowUpdateGrbit'
title: Enumeração EscrowUpdateGrbit
TOCTitle: EscrowUpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.escrowupdategrbit(v=EXCHG.10)
ms:contentKeyID: 39514160
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d301ef801a5685057a9e33beb794f3b6cf13e646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922764"
---
# <a name="escrowupdategrbit-enumeration"></a><span data-ttu-id="03d33-103">Enumeração EscrowUpdateGrbit</span><span class="sxs-lookup"><span data-stu-id="03d33-103">EscrowUpdateGrbit enumeration</span></span>

<span data-ttu-id="03d33-104">Opções para JetEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="03d33-104">Options for JetEscrowUpdate.</span></span>

<span data-ttu-id="03d33-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="03d33-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="03d33-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="03d33-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="03d33-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="03d33-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="03d33-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03d33-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EscrowUpdateGrbit
'Usage
Dim instance As EscrowUpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum EscrowUpdateGrbit
```

## <a name="members"></a><span data-ttu-id="03d33-109">Membros</span><span class="sxs-lookup"><span data-stu-id="03d33-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="03d33-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="03d33-110">Member name</span></span></th>
<th><span data-ttu-id="03d33-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="03d33-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="03d33-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="03d33-112">None</span></span></td>
<td><span data-ttu-id="03d33-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="03d33-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="03d33-114">Norollback</span><span class="sxs-lookup"><span data-stu-id="03d33-114">NoRollback</span></span></td>
<td><span data-ttu-id="03d33-115">Mesmo que a sessão que executa a atualização de caução tenha sua reversão de transação, essa atualização não será desfeita.</span><span class="sxs-lookup"><span data-stu-id="03d33-115">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="03d33-116">Como os registros de log podem não ser liberados para o disco, as atualizações de caução recentes feitas com esse sinalizador podem ser perdidas se houver uma falha.</span><span class="sxs-lookup"><span data-stu-id="03d33-116">As the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="03d33-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="03d33-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="03d33-118">Referência</span><span class="sxs-lookup"><span data-stu-id="03d33-118">Reference</span></span>

[<span data-ttu-id="03d33-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="03d33-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

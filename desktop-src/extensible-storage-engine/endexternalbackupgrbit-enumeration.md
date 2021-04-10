---
description: 'Saiba mais sobre: Enumeração EndExternalBackupGrbit'
title: Enumeração EndExternalBackupGrbit
TOCTitle: EndExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.endexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39516835
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bb3fb2f3e959d41c042589f3a280e6466fe4970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171943"
---
# <a name="endexternalbackupgrbit-enumeration"></a><span data-ttu-id="b4f19-103">Enumeração EndExternalBackupGrbit</span><span class="sxs-lookup"><span data-stu-id="b4f19-103">EndExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="b4f19-104">Opções para [JetEndExternalBackupInstance (JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="b4f19-104">Options for [JetEndExternalBackupInstance(JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="b4f19-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="b4f19-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="b4f19-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4f19-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4f19-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4f19-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4f19-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4f19-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EndExternalBackupGrbit
'Usage
Dim instance As EndExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum EndExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="b4f19-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b4f19-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b4f19-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="b4f19-110">Member name</span></span></th>
<th><span data-ttu-id="b4f19-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4f19-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b4f19-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b4f19-112">None</span></span></td>
<td><span data-ttu-id="b4f19-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="b4f19-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b4f19-114">Normal</span><span class="sxs-lookup"><span data-stu-id="b4f19-114">Normal</span></span></td>
<td><span data-ttu-id="b4f19-115">O aplicativo cliente concluiu o backup completamente e está terminando normalmente.</span><span class="sxs-lookup"><span data-stu-id="b4f19-115">The client application finished the backup completely, and is ending normally.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b4f19-116">Anular</span><span class="sxs-lookup"><span data-stu-id="b4f19-116">Abort</span></span></td>
<td><span data-ttu-id="b4f19-117">O aplicativo cliente está anulando o backup.</span><span class="sxs-lookup"><span data-stu-id="b4f19-117">The client application is aborting the backup.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b4f19-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4f19-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4f19-119">Referência</span><span class="sxs-lookup"><span data-stu-id="b4f19-119">Reference</span></span>

[<span data-ttu-id="b4f19-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b4f19-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

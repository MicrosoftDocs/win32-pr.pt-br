---
description: 'Saiba mais sobre: Enumeração GetLockGrbit'
title: Enumeração GetLockGrbit
TOCTitle: GetLockGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetLockGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getlockgrbit(v=EXCHG.10)
ms:contentKeyID: 39512424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cfcad088fa93d73910a0333d3aca9a700e97996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921228"
---
# <a name="getlockgrbit-enumeration"></a><span data-ttu-id="dae9d-103">Enumeração GetLockGrbit</span><span class="sxs-lookup"><span data-stu-id="dae9d-103">GetLockGrbit enumeration</span></span>

<span data-ttu-id="dae9d-104">Opções para JetGetLock.</span><span class="sxs-lookup"><span data-stu-id="dae9d-104">Options for JetGetLock.</span></span>

<span data-ttu-id="dae9d-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="dae9d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="dae9d-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dae9d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dae9d-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dae9d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dae9d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dae9d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetLockGrbit
'Usage
Dim instance As GetLockGrbit
```

``` csharp
[FlagsAttribute]
public enum GetLockGrbit
```

## <a name="members"></a><span data-ttu-id="dae9d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="dae9d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="dae9d-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="dae9d-110">Member name</span></span></th>
<th><span data-ttu-id="dae9d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="dae9d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="dae9d-112">Ler</span><span class="sxs-lookup"><span data-stu-id="dae9d-112">Read</span></span></td>
<td><span data-ttu-id="dae9d-113">Adquirir um bloqueio de leitura no registro atual.</span><span class="sxs-lookup"><span data-stu-id="dae9d-113">Acquire a read lock on the current record.</span></span> <span data-ttu-id="dae9d-114">Os bloqueios de leitura são incompatíveis com os bloqueios de gravação já mantidos por outras sessões, mas são compatíveis com bloqueios de leitura mantidos por outras sessões.</span><span class="sxs-lookup"><span data-stu-id="dae9d-114">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="dae9d-115">Gravar</span><span class="sxs-lookup"><span data-stu-id="dae9d-115">Write</span></span></td>
<td><span data-ttu-id="dae9d-116">Adquirir um bloqueio de gravação no registro atual.</span><span class="sxs-lookup"><span data-stu-id="dae9d-116">Acquire a write lock on the current record.</span></span> <span data-ttu-id="dae9d-117">Os bloqueios de gravação não são compatíveis com bloqueios de gravação ou leitura mantidos por outras sessões, mas são compatíveis com bloqueios de leitura mantidos pela mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="dae9d-117">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="dae9d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="dae9d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dae9d-119">Referência</span><span class="sxs-lookup"><span data-stu-id="dae9d-119">Reference</span></span>

[<span data-ttu-id="dae9d-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dae9d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

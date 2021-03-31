---
description: 'Saiba mais sobre: Enumeração TermGrbit'
title: Enumeração TermGrbit
TOCTitle: TermGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TermGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.termgrbit(v=EXCHG.10)
ms:contentKeyID: 39511147
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TermGrbit.None
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49b466b298a78d7bfd6822904aed977e7117b927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663017"
---
# <a name="termgrbit-enumeration"></a><span data-ttu-id="9f01a-103">Enumeração TermGrbit</span><span class="sxs-lookup"><span data-stu-id="9f01a-103">TermGrbit enumeration</span></span>

<span data-ttu-id="9f01a-104">Opções para [JetTerm2 (JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span><span class="sxs-lookup"><span data-stu-id="9f01a-104">Options for [JetTerm2(JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span></span>

<span data-ttu-id="9f01a-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="9f01a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="9f01a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f01a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f01a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f01a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f01a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f01a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TermGrbit
'Usage
Dim instance As TermGrbit
```

``` csharp
[FlagsAttribute]
public enum TermGrbit
```

## <a name="members"></a><span data-ttu-id="9f01a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="9f01a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9f01a-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="9f01a-110">Member name</span></span></th>
<th><span data-ttu-id="9f01a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f01a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9f01a-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9f01a-112">None</span></span></td>
<td><span data-ttu-id="9f01a-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="9f01a-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9f01a-114">Concluir</span><span class="sxs-lookup"><span data-stu-id="9f01a-114">Complete</span></span></td>
<td><span data-ttu-id="9f01a-115">Solicita que a instância seja desligada corretamente.</span><span class="sxs-lookup"><span data-stu-id="9f01a-115">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="9f01a-116">Qualquer trabalho de limpeza opcional que normalmente seria feito em segundo plano em tempo de execução é concluído imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9f01a-116">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9f01a-117">Abrupta</span><span class="sxs-lookup"><span data-stu-id="9f01a-117">Abrupt</span></span></td>
<td><span data-ttu-id="9f01a-118">Solicita que a instância seja desligada o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="9f01a-118">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="9f01a-119">Qualquer trabalho opcional que normalmente seria feito em segundo plano em tempo de execução é abandonado.</span><span class="sxs-lookup"><span data-stu-id="9f01a-119">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9f01a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f01a-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f01a-121">Referência</span><span class="sxs-lookup"><span data-stu-id="9f01a-121">Reference</span></span>

[<span data-ttu-id="9f01a-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9f01a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="9f01a-123">Bit</span><span class="sxs-lookup"><span data-stu-id="9f01a-123">Dirty</span></span>](./windows7grbits.dirty-field.md)

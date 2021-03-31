---
description: 'Saiba mais sobre: Enumeração MoveGrbit'
title: Enumeração MoveGrbit
TOCTitle: MoveGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MoveGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.movegrbit(v=EXCHG.10)
ms:contentKeyID: 39513771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81f047cd69bca668a5eae2b5147d8c0a137011e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011111"
---
# <a name="movegrbit-enumeration"></a><span data-ttu-id="5a36b-103">Enumeração MoveGrbit</span><span class="sxs-lookup"><span data-stu-id="5a36b-103">MoveGrbit enumeration</span></span>

<span data-ttu-id="5a36b-104">Opções para JetMove.</span><span class="sxs-lookup"><span data-stu-id="5a36b-104">Options for JetMove.</span></span>

<span data-ttu-id="5a36b-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="5a36b-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="5a36b-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a36b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a36b-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a36b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a36b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a36b-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MoveGrbit
'Usage
Dim instance As MoveGrbit
```

``` csharp
[FlagsAttribute]
public enum MoveGrbit
```

## <a name="members"></a><span data-ttu-id="5a36b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="5a36b-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="5a36b-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="5a36b-110">Member name</span></span></th>
<th><span data-ttu-id="5a36b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a36b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5a36b-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5a36b-112">None</span></span></td>
<td><span data-ttu-id="5a36b-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="5a36b-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5a36b-114">MoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="5a36b-114">MoveKeyNE</span></span></td>
<td><span data-ttu-id="5a36b-115">Move o cursor para frente ou para trás pelo número de entradas de índice necessárias para ignorar o número solicitado de valores de chave de índice encontrados no índice.</span><span class="sxs-lookup"><span data-stu-id="5a36b-115">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="5a36b-116">Isso tem o efeito de recolher entradas de índice com valores de chave duplicados em uma única entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="5a36b-116">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5a36b-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a36b-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a36b-118">Referência</span><span class="sxs-lookup"><span data-stu-id="5a36b-118">Reference</span></span>

[<span data-ttu-id="5a36b-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5a36b-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

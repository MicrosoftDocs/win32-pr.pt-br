---
description: 'Saiba mais sobre: Enumeração SeekGrbit'
title: Enumeração SeekGrbit
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757987"
---
# <a name="seekgrbit-enumeration"></a><span data-ttu-id="10d2b-103">Enumeração SeekGrbit</span><span class="sxs-lookup"><span data-stu-id="10d2b-103">SeekGrbit enumeration</span></span>

<span data-ttu-id="10d2b-104">Opções para JetSeek.</span><span class="sxs-lookup"><span data-stu-id="10d2b-104">Options for JetSeek.</span></span>

<span data-ttu-id="10d2b-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="10d2b-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="10d2b-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10d2b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10d2b-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="10d2b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10d2b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10d2b-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
```

## <a name="members"></a><span data-ttu-id="10d2b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="10d2b-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="10d2b-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="10d2b-110">Member name</span></span></th>
<th><span data-ttu-id="10d2b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="10d2b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="10d2b-112">SeekEQ</span><span class="sxs-lookup"><span data-stu-id="10d2b-112">SeekEQ</span></span></td>
<td><span data-ttu-id="10d2b-113">O cursor será posicionado na entrada de índice mais próxima do início do índice que corresponde exatamente à chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="10d2b-113">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="10d2b-114">SeekLT</span><span class="sxs-lookup"><span data-stu-id="10d2b-114">SeekLT</span></span></td>
<td><span data-ttu-id="10d2b-115">O cursor será posicionado na entrada de índice mais próxima do final do índice que for menor que uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="10d2b-115">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="10d2b-116">SeekLE</span><span class="sxs-lookup"><span data-stu-id="10d2b-116">SeekLE</span></span></td>
<td><span data-ttu-id="10d2b-117">O cursor será posicionado na entrada de índice mais próxima do final do índice que for menor ou igual a uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="10d2b-117">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="10d2b-118">SeekGE</span><span class="sxs-lookup"><span data-stu-id="10d2b-118">SeekGE</span></span></td>
<td><span data-ttu-id="10d2b-119">O cursor será posicionado na entrada de índice mais próxima do início do índice que seja maior ou igual a uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="10d2b-119">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="10d2b-120">SeekGT</span><span class="sxs-lookup"><span data-stu-id="10d2b-120">SeekGT</span></span></td>
<td><span data-ttu-id="10d2b-121">O cursor será posicionado na entrada de índice mais próxima do início do índice que é maior que uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="10d2b-121">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="10d2b-122">SetIndexRange</span><span class="sxs-lookup"><span data-stu-id="10d2b-122">SetIndexRange</span></span></td>
<td><span data-ttu-id="10d2b-123">Um intervalo de índice será automaticamente configurado para todas as chaves que correspondem exatamente à chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="10d2b-123">An index range will automatically be setup for all keys that exactly match the search key.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="10d2b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="10d2b-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10d2b-125">Referência</span><span class="sxs-lookup"><span data-stu-id="10d2b-125">Reference</span></span>

[<span data-ttu-id="10d2b-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="10d2b-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

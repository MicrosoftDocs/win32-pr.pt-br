---
description: 'Saiba mais sobre: Enumeração MakeKeyGrbit'
title: Enumeração MakeKeyGrbit
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090109"
---
# <a name="makekeygrbit-enumeration"></a><span data-ttu-id="87596-103">Enumeração MakeKeyGrbit</span><span class="sxs-lookup"><span data-stu-id="87596-103">MakeKeyGrbit enumeration</span></span>

<span data-ttu-id="87596-104">Opções para JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="87596-104">Options for JetMakeKey.</span></span>

<span data-ttu-id="87596-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="87596-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="87596-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="87596-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="87596-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="87596-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="87596-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87596-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
```

## <a name="members"></a><span data-ttu-id="87596-109">Membros</span><span class="sxs-lookup"><span data-stu-id="87596-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="87596-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="87596-110">Member name</span></span></th>
<th><span data-ttu-id="87596-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="87596-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="87596-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="87596-112">None</span></span></td>
<td><span data-ttu-id="87596-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="87596-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="87596-114">NewKey</span><span class="sxs-lookup"><span data-stu-id="87596-114">NewKey</span></span></td>
<td><span data-ttu-id="87596-115">Uma nova chave de pesquisa deve ser construída.</span><span class="sxs-lookup"><span data-stu-id="87596-115">A new search key should be constructed.</span></span> <span data-ttu-id="87596-116">Qualquer chave de pesquisa existente anteriormente é descartada.</span><span class="sxs-lookup"><span data-stu-id="87596-116">Any previously existing search key is discarded.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="87596-117">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="87596-117">NormalizedKey</span></span></td>
<td><span data-ttu-id="87596-118">Quando essa opção é especificada, todas as outras opções são ignoradas, qualquer chave de pesquisa existente anteriormente é descartada e o conteúdo do buffer de entrada é carregado como a nova chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="87596-118">When this option is specified, all other options are ignored, any previously existing search key is discarded, and the contents of the input buffer are loaded as the new search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="87596-119">KeyDataZeroLength</span><span class="sxs-lookup"><span data-stu-id="87596-119">KeyDataZeroLength</span></span></td>
<td><span data-ttu-id="87596-120">Se o tamanho do buffer de entrada for zero e a coluna de chave atual for uma coluna de comprimento variável, essa opção indicará que o buffer de entrada contém um valor de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="87596-120">If the size of the input buffer is zero and the current key column is a variable length column, this option indicates that the input buffer contains a zero length value.</span></span> <span data-ttu-id="87596-121">Caso contrário, um tamanho de buffer de entrada igual a zero indicaria um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="87596-121">Otherwise, an input buffer size of zero would indicate a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="87596-122">StrLimit</span><span class="sxs-lookup"><span data-stu-id="87596-122">StrLimit</span></span></td>
<td><span data-ttu-id="87596-123">Essa opção indica que a chave de pesquisa deve ser construída de modo que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</span><span class="sxs-lookup"><span data-stu-id="87596-123">This option indicates that the search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="87596-124">SubStrLimit</span><span class="sxs-lookup"><span data-stu-id="87596-124">SubStrLimit</span></span></td>
<td><span data-ttu-id="87596-125">Essa opção indica que a chave de pesquisa deve ser construída de modo que a coluna de chave atual seja considerada um curinga de prefixo e que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</span><span class="sxs-lookup"><span data-stu-id="87596-125">This option indicates that the search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="87596-126">FullColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="87596-126">FullColumnStartLimit</span></span></td>
<td><span data-ttu-id="87596-127">A chave de pesquisa deve ser construída de modo que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</span><span class="sxs-lookup"><span data-stu-id="87596-127">The search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="87596-128">FullColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="87596-128">FullColumnEndLimit</span></span></td>
<td><span data-ttu-id="87596-129">A chave de pesquisa deve ser construída de forma que as colunas de chave que vierem após a coluna de chave atual sejam consideradas curingas.</span><span class="sxs-lookup"><span data-stu-id="87596-129">The search key should be constructed in such a way that any key columns that come after the current key column are considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="87596-130">PartialColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="87596-130">PartialColumnStartLimit</span></span></td>
<td><span data-ttu-id="87596-131">A chave de pesquisa deve ser construída de modo que a coluna de chave atual seja considerada um curinga de prefixo e que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</span><span class="sxs-lookup"><span data-stu-id="87596-131">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="87596-132">PartialColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="87596-132">PartialColumnEndLimit</span></span></td>
<td><span data-ttu-id="87596-133">A chave de pesquisa deve ser construída de modo que a coluna de chave atual seja considerada um curinga de prefixo e que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</span><span class="sxs-lookup"><span data-stu-id="87596-133">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="87596-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="87596-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="87596-135">Referência</span><span class="sxs-lookup"><span data-stu-id="87596-135">Reference</span></span>

[<span data-ttu-id="87596-136">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="87596-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Saiba mais sobre: Enumeração RetrieveColumnGrbit'
title: Enumeração RetrieveColumnGrbit
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811035"
---
# <a name="retrievecolumngrbit-enumeration"></a><span data-ttu-id="8dd6d-103">Enumeração RetrieveColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="8dd6d-103">RetrieveColumnGrbit enumeration</span></span>

<span data-ttu-id="8dd6d-104">Opções para JetRetrieveColumn.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-104">Options for JetRetrieveColumn.</span></span>

<span data-ttu-id="8dd6d-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8dd6d-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8dd6d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8dd6d-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8dd6d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd6d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dd6d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
```

## <a name="members"></a><span data-ttu-id="8dd6d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8dd6d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8dd6d-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="8dd6d-110">Member name</span></span></th>
<th><span data-ttu-id="8dd6d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8dd6d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8dd6d-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8dd6d-112">None</span></span></td>
<td><span data-ttu-id="8dd6d-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8dd6d-114">RetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="8dd6d-114">RetrieveCopy</span></span></td>
<td><span data-ttu-id="8dd6d-115">Esse sinalizador faz com que a coluna de recuperação recupere o valor modificado em vez do valor original.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-115">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="8dd6d-116">Se o valor não tiver sido modificado, o valor original será recuperado.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-116">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="8dd6d-117">Dessa forma, um valor que ainda não foi inserido ou atualizado pode ser recuperado durante a operação de inserção ou atualização de um registro.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-117">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8dd6d-118">RetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="8dd6d-118">RetrieveFromIndex</span></span></td>
<td><span data-ttu-id="8dd6d-119">Essa opção é usada para recuperar valores de coluna do índice, se possível, sem acessar o registro.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-119">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="8dd6d-120">Dessa forma, o carregamento desnecessário de registros pode ser evitado quando os dados necessários estão disponíveis nas próprias entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-120">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8dd6d-121">RetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="8dd6d-121">RetrieveFromPrimaryBookmark</span></span></td>
<td><span data-ttu-id="8dd6d-122">Essa opção é usada para recuperar valores de coluna do indicador de índice e pode ser diferente do valor de índice quando uma coluna aparece no índice primário e no índice atual.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-122">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="8dd6d-123">Essa opção não deverá ser especificada se o índice atual for o índice clusterizado ou primário.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-123">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="8dd6d-124">Esse bit não poderá ser definido se RetrieveFromIndex também for definido.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-124">This bit cannot be set if RetrieveFromIndex is also set.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8dd6d-125">RetrieveTag</span><span class="sxs-lookup"><span data-stu-id="8dd6d-125">RetrieveTag</span></span></td>
<td><span data-ttu-id="8dd6d-126">Essa opção é usada para recuperar o número de sequência de um valor de coluna com valores múltiplos em JET_RETINFO. itagSequence.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-126">This option is used to retrieve the sequence number of a multi-valued column value in JET_RETINFO.itagSequence.</span></span> <span data-ttu-id="8dd6d-127">A recuperação do número de sequência pode ser uma operação dispendiosa e só deve ser feita se necessário.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-127">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8dd6d-128">RetrieveNull</span><span class="sxs-lookup"><span data-stu-id="8dd6d-128">RetrieveNull</span></span></td>
<td><span data-ttu-id="8dd6d-129">Essa opção é usada para recuperar valores nulos de coluna de vários valores.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-129">This option is used to retrieve multi-valued column NULL values.</span></span> <span data-ttu-id="8dd6d-130">Se essa opção não for especificada, os valores nulos da coluna com valores múltiplos serão automaticamente ignorados.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-130">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8dd6d-131">RetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="8dd6d-131">RetrieveIgnoreDefault</span></span></td>
<td><span data-ttu-id="8dd6d-132">Essa opção afeta apenas as colunas com valores múltiplos e faz com que um valor nulo seja retornado quando o número de sequência solicitado é 1 e não há valores definidos para a coluna no registro.</span><span class="sxs-lookup"><span data-stu-id="8dd6d-132">This option affects only multi-valued columns and causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8dd6d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8dd6d-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8dd6d-134">Referência</span><span class="sxs-lookup"><span data-stu-id="8dd6d-134">Reference</span></span>

[<span data-ttu-id="8dd6d-135">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8dd6d-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

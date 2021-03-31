---
description: 'Saiba mais sobre: Enumeração BeginTransactionGrbit'
title: Enumeração BeginTransactionGrbit
TOCTitle: BeginTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.begintransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39515115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f407c54b7b6e76ab63dcfb97d1307458ba15277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662978"
---
# <a name="begintransactiongrbit-enumeration"></a><span data-ttu-id="5611e-103">Enumeração BeginTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="5611e-103">BeginTransactionGrbit enumeration</span></span>

<span data-ttu-id="5611e-104">Opções para [JetBeginTransaction2 (JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span><span class="sxs-lookup"><span data-stu-id="5611e-104">Options for [JetBeginTransaction2(JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span></span>

<span data-ttu-id="5611e-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="5611e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="5611e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5611e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5611e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5611e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5611e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5611e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginTransactionGrbit
'Usage
Dim instance As BeginTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="5611e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="5611e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="5611e-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="5611e-110">Member name</span></span></th>
<th><span data-ttu-id="5611e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5611e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5611e-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5611e-112">None</span></span></td>
<td><span data-ttu-id="5611e-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="5611e-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5611e-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="5611e-114">ReadOnly</span></span></td>
<td><span data-ttu-id="5611e-115">A transação não modificará o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5611e-115">The transaction will not modify the database.</span></span> <span data-ttu-id="5611e-116">Se uma atualização for tentada, essa operação falhará com o <a href="hh564840(v=exchg.10).md">transreadonly</a>.</span><span class="sxs-lookup"><span data-stu-id="5611e-116">If an update is attempted, that operation will fail with <a href="hh564840(v=exchg.10).md">TransReadOnly</a>.</span></span> <span data-ttu-id="5611e-117">Essa opção é ignorada a menos que seja solicitada quando a sessão especificada ainda não estiver em uma transação.</span><span class="sxs-lookup"><span data-stu-id="5611e-117">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5611e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5611e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5611e-119">Referência</span><span class="sxs-lookup"><span data-stu-id="5611e-119">Reference</span></span>

[<span data-ttu-id="5611e-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5611e-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

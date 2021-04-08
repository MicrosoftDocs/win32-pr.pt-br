---
description: 'Saiba mais sobre: Enumeração LsGrbit'
title: Enumeração LsGrbit
TOCTitle: LsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.LsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.lsgrbit(v=EXCHG.10)
ms:contentKeyID: 39514518
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fc0a60d039d0eb1307558d42a3e7a3c7e99eb86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010557"
---
# <a name="lsgrbit-enumeration"></a><span data-ttu-id="89687-103">Enumeração LsGrbit</span><span class="sxs-lookup"><span data-stu-id="89687-103">LsGrbit enumeration</span></span>

<span data-ttu-id="89687-104">Opções para [JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) e [JetGetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="89687-104">Options for [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) and [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span></span>

<span data-ttu-id="89687-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="89687-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="89687-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89687-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89687-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89687-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89687-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89687-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration LsGrbit
'Usage
Dim instance As LsGrbit
```

``` csharp
[FlagsAttribute]
public enum LsGrbit
```

## <a name="members"></a><span data-ttu-id="89687-109">Membros</span><span class="sxs-lookup"><span data-stu-id="89687-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="89687-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="89687-110">Member name</span></span></th>
<th><span data-ttu-id="89687-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="89687-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="89687-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="89687-112">None</span></span></td>
<td><span data-ttu-id="89687-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="89687-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="89687-114">Redefinir</span><span class="sxs-lookup"><span data-stu-id="89687-114">Reset</span></span></td>
<td><span data-ttu-id="89687-115">O identificador de contexto para o objeto escolhido deve ser redefinido para JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="89687-115">The context handle for the chosen object should be reset to JET_LSNil.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="89687-116">Cursor</span><span class="sxs-lookup"><span data-stu-id="89687-116">Cursor</span></span></td>
<td><span data-ttu-id="89687-117">Especifica que o identificador de contexto deve ser associado ao cursor fornecido.</span><span class="sxs-lookup"><span data-stu-id="89687-117">Specifies the context handle should be associated with the given cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="89687-118">Tabela</span><span class="sxs-lookup"><span data-stu-id="89687-118">Table</span></span></td>
<td><span data-ttu-id="89687-119">Especifica que o identificador de contexto deve ser associado à tabela associada ao cursor fornecido.</span><span class="sxs-lookup"><span data-stu-id="89687-119">Specifies that the context handle should be associated with the table associated with the given cursor.</span></span> <span data-ttu-id="89687-120">É ilegal usar essa opção com cursor.</span><span class="sxs-lookup"><span data-stu-id="89687-120">It is illegal to use this option with Cursor.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="89687-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="89687-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89687-122">Referência</span><span class="sxs-lookup"><span data-stu-id="89687-122">Reference</span></span>

[<span data-ttu-id="89687-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="89687-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

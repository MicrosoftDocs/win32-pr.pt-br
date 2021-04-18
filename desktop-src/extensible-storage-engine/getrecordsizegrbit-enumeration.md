---
description: 'Saiba mais sobre: Enumeração GetRecordSizeGrbit'
title: Enumeração GetRecordSizeGrbit
TOCTitle: GetRecordSizeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getrecordsizegrbit(v=EXCHG.10)
ms:contentKeyID: 39514742
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee95d29ed1913993aa37062137807bf8d635eecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753067"
---
# <a name="getrecordsizegrbit-enumeration"></a><span data-ttu-id="25c63-103">Enumeração GetRecordSizeGrbit</span><span class="sxs-lookup"><span data-stu-id="25c63-103">GetRecordSizeGrbit enumeration</span></span>

<span data-ttu-id="25c63-104">Opções para [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span><span class="sxs-lookup"><span data-stu-id="25c63-104">Options for [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span></span>

<span data-ttu-id="25c63-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="25c63-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="25c63-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25c63-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25c63-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25c63-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25c63-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25c63-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetRecordSizeGrbit
'Usage
Dim instance As GetRecordSizeGrbit
```

``` csharp
[FlagsAttribute]
public enum GetRecordSizeGrbit
```

## <a name="members"></a><span data-ttu-id="25c63-109">Membros</span><span class="sxs-lookup"><span data-stu-id="25c63-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="25c63-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="25c63-110">Member name</span></span></th>
<th><span data-ttu-id="25c63-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="25c63-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="25c63-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="25c63-112">None</span></span></td>
<td><span data-ttu-id="25c63-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="25c63-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="25c63-114">InCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="25c63-114">InCopyBuffer</span></span></td>
<td><span data-ttu-id="25c63-115">Recupere o tamanho do registro que está no buffer de cópia preparado ou atualize.</span><span class="sxs-lookup"><span data-stu-id="25c63-115">Retrieve the size of the record that is in the copy buffer prepared or update.</span></span> <span data-ttu-id="25c63-116">Caso contrário, a TableName deve ser posicionada em um registro e esse registro será usado.</span><span class="sxs-lookup"><span data-stu-id="25c63-116">Otherwise, the tableid must be positioned on a record, and that record will be used.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="25c63-117">RunningTotal</span><span class="sxs-lookup"><span data-stu-id="25c63-117">RunningTotal</span></span></td>
<td><span data-ttu-id="25c63-118">O JET_RECSIZE não é zerado antes de preencher o conteúdo, agindo efetivamente como um acúmulo das estatísticas de vários registros visitados ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="25c63-118">The JET_RECSIZE is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="25c63-119">Local</span><span class="sxs-lookup"><span data-stu-id="25c63-119">Local</span></span></td>
<td><span data-ttu-id="25c63-120">Ignore valores longos não intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="25c63-120">Ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="25c63-121">Somente o registro local na página será usado.</span><span class="sxs-lookup"><span data-stu-id="25c63-121">Only the local record on the page will be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="25c63-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="25c63-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25c63-123">Referência</span><span class="sxs-lookup"><span data-stu-id="25c63-123">Reference</span></span>

[<span data-ttu-id="25c63-124">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="25c63-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

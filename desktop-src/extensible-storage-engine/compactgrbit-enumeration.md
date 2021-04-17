---
description: 'Saiba mais sobre: Enumeração CompactGrbit'
title: Enumeração CompactGrbit
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748114"
---
# <a name="compactgrbit-enumeration"></a><span data-ttu-id="60ba6-103">Enumeração CompactGrbit</span><span class="sxs-lookup"><span data-stu-id="60ba6-103">CompactGrbit enumeration</span></span>

<span data-ttu-id="60ba6-104">Opções para [JetCompact (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span><span class="sxs-lookup"><span data-stu-id="60ba6-104">Options for [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span></span>

<span data-ttu-id="60ba6-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="60ba6-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="60ba6-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="60ba6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="60ba6-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="60ba6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="60ba6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60ba6-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
```

## <a name="members"></a><span data-ttu-id="60ba6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="60ba6-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="60ba6-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="60ba6-110">Member name</span></span></th>
<th><span data-ttu-id="60ba6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="60ba6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="60ba6-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="60ba6-112">None</span></span></td>
<td><span data-ttu-id="60ba6-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="60ba6-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="60ba6-114">Estatísticas</span><span class="sxs-lookup"><span data-stu-id="60ba6-114">Stats</span></span></td>
<td><span data-ttu-id="60ba6-115">Faz com que o JetCompact despeje estatísticas no banco de dados de origem em um arquivo chamado DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="60ba6-115">Causes JetCompact to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="60ba6-116">As estatísticas incluem o nome de cada tabela no banco de dados de origem, o número de linhas em cada tabela, o tamanho total em bytes de todas as linhas em cada tabela, tamanho total em bytes de todas as colunas do tipo <a href="hh577895(v=exchg.10).md">LONGTEXT</a> ou <a href="hh577895(v=exchg.10).md">LongBinary</a> que foram grandes o suficiente para serem armazenados separados do registro, número de páginas de folha de índice clusterizado e número de páginas de folha de valor longo</span><span class="sxs-lookup"><span data-stu-id="60ba6-116">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="hh577895(v=exchg.10).md">LongText</a> or <a href="hh577895(v=exchg.10).md">LongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="60ba6-117">Além disso, estatísticas de resumo, incluindo o tamanho do banco de dados de origem, banco de dados de destino, tempo necessário para compactação de banco de dados, o espaço de banco de dados temporário também são todos despejados.</span><span class="sxs-lookup"><span data-stu-id="60ba6-117">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="60ba6-118">Reparar</span><span class="sxs-lookup"><span data-stu-id="60ba6-118">Repair</span></span></td>
<td><span data-ttu-id="60ba6-119"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="60ba6-119"><strong>Obsolete.</strong></span></span> <span data-ttu-id="60ba6-120">Usado quando o banco de dados de origem é conhecido como corrompido.</span><span class="sxs-lookup"><span data-stu-id="60ba6-120">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="60ba6-121">Ele permite que um conjunto completo de novos comportamentos se destinasse a recuperar o máximo de dados possível do banco de dado de origem.</span><span class="sxs-lookup"><span data-stu-id="60ba6-121">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="60ba6-122">JetCompact com esse conjunto de opções pode retornar <a href="hh564840(v=exchg.10).md">êxito</a> , mas não copiar todos os dados criados no banco de dado de origem.</span><span class="sxs-lookup"><span data-stu-id="60ba6-122">JetCompact with this option set may return <a href="hh564840(v=exchg.10).md">Success</a> but not copy all of the data created in the source database.</span></span> <span data-ttu-id="60ba6-123">Os dados que estavam em partes danificadas do banco de dados de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="60ba6-123">Data that was in damaged portions of the source database will be skipped.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="60ba6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="60ba6-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="60ba6-125">Referência</span><span class="sxs-lookup"><span data-stu-id="60ba6-125">Reference</span></span>

[<span data-ttu-id="60ba6-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="60ba6-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Saiba mais sobre: estrutura de JET_CONDITIONALCOLUMN'
title: Estrutura de JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779932"
---
# <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="72ae0-103">Estrutura de JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="72ae0-103">JET_CONDITIONALCOLUMN Structure</span></span>


<span data-ttu-id="72ae0-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="72ae0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="72ae0-105">Estrutura de JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="72ae0-105">JET_CONDITIONALCOLUMN Structure</span></span>

<span data-ttu-id="72ae0-106">A estrutura de **JET_CONDITIONALCOLUMN** define como a indexação condicional é executada para um determinado índice.</span><span class="sxs-lookup"><span data-stu-id="72ae0-106">The **JET_CONDITIONALCOLUMN** structure defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="72ae0-107">Um índice condicional contém uma entrada de índice somente para as linhas que correspondem à condição especificada.</span><span class="sxs-lookup"><span data-stu-id="72ae0-107">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="72ae0-108">No entanto, a coluna condicional não faz parte da chave do índice, ela controla apenas a presença da entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="72ae0-108">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a><span data-ttu-id="72ae0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="72ae0-109">Members</span></span>

<span data-ttu-id="72ae0-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="72ae0-110">**cbStruct**</span></span>

<span data-ttu-id="72ae0-111">Esse campo deve ser inicializado para sizeof (JET_CONDITIONALCOLUMN), em bytes.</span><span class="sxs-lookup"><span data-stu-id="72ae0-111">This field must be initialized to sizeof( JET_CONDITIONALCOLUMN ), in bytes.</span></span>

<span data-ttu-id="72ae0-112">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="72ae0-112">**szColumnName**</span></span>

<span data-ttu-id="72ae0-113">O nome da coluna que contém os dados nos quais o mecanismo de banco de dados está indexando condicionalmente a linha.</span><span class="sxs-lookup"><span data-stu-id="72ae0-113">The name of the column that contains the data on which the database engine is conditionally indexing the row.</span></span>

<span data-ttu-id="72ae0-114">**grbit** Um grupo de bits que fornece as opções para o índice condicional.</span><span class="sxs-lookup"><span data-stu-id="72ae0-114">**grbit** A group of bits that gives the options for the conditional index.</span></span> <span data-ttu-id="72ae0-115">A passagem de zero ou valores logicamente **ou** Ed não é válida para **JET_CONDITIONALCOLUMN**.</span><span class="sxs-lookup"><span data-stu-id="72ae0-115">Passing in zero or logically-**OR** ed values is not valid for **JET_CONDITIONALCOLUMN**.</span></span> <span data-ttu-id="72ae0-116">O campo de bits deve ser exatamente um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="72ae0-116">The bit field must be exactly one of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72ae0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="72ae0-117">Value</span></span></p></th>
<th><p><span data-ttu-id="72ae0-118">Significado</span><span class="sxs-lookup"><span data-stu-id="72ae0-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72ae0-119">JET_bitIndexColumnMustBeNull</span><span class="sxs-lookup"><span data-stu-id="72ae0-119">JET_bitIndexColumnMustBeNull</span></span></p></td>
<td><p><span data-ttu-id="72ae0-120">A coluna especificada pelo parâmetro <em>szColumnName</em> deve ser nula para que uma entrada de índice de uma determinada linha apareça neste índice.</span><span class="sxs-lookup"><span data-stu-id="72ae0-120">The column specified by the <em>szColumnName</em> parameter must be NULL for an index entry for a given row to appear in this index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72ae0-121">JET_bitIndexColumnMustBeNonNull</span><span class="sxs-lookup"><span data-stu-id="72ae0-121">JET_bitIndexColumnMustBeNonNull</span></span></p></td>
<td><p><span data-ttu-id="72ae0-122">A coluna especificada pelo parâmetro <em>szColumnName</em> deve ser não nula para uma entrada de índice para que uma determinada linha apareça nesse índice.</span><span class="sxs-lookup"><span data-stu-id="72ae0-122">The column specified by the <em>szColumnName</em> parameter must be non-NULL for an index entry in order for a given row to appear in this index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="72ae0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="72ae0-123">Remarks</span></span>

<span data-ttu-id="72ae0-124">Um índice condicional contém uma entrada de índice somente para as linhas que correspondem à condição especificada.</span><span class="sxs-lookup"><span data-stu-id="72ae0-124">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="72ae0-125">Por exemplo, uma coluna pode ser nomeada "marcada" e, quando uma linha é marcada, a coluna é definida como um valor não nulo.</span><span class="sxs-lookup"><span data-stu-id="72ae0-125">For example, a column could be named "Marked", and when a row is marked, the column is set to a non-NULL value.</span></span> <span data-ttu-id="72ae0-126">Um JET_bitIndexColumnMustBeNonNull índice condicional nessa coluna mostrará todas as linhas marcadas e um JET_bitIndexColumnMustBeNull índice condicional mostrará as linhas que não estão marcadas.</span><span class="sxs-lookup"><span data-stu-id="72ae0-126">A JET_bitIndexColumnMustBeNonNull conditional index on this column will show all rows that are marked, and a JET_bitIndexColumnMustBeNull conditional index will show rows that are not marked.</span></span> <span data-ttu-id="72ae0-127">Essa também é uma maneira conveniente de executar uma exclusão de sinalizador e um índice de coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="72ae0-127">This is also a convenient way to perform a flag deletion and garbage collecting index.</span></span>

### <a name="requirements"></a><span data-ttu-id="72ae0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72ae0-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72ae0-129"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="72ae0-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="72ae0-130">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="72ae0-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72ae0-131"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="72ae0-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="72ae0-132">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="72ae0-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72ae0-133"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="72ae0-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="72ae0-134">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="72ae0-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72ae0-135"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="72ae0-135"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="72ae0-136">Implementado como <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) e <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="72ae0-136">Implemented as <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) and <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="72ae0-137">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="72ae0-137">See Also</span></span>

[<span data-ttu-id="72ae0-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="72ae0-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="72ae0-139">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="72ae0-139">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)

---
description: 'Saiba mais sobre: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826811"
---
# <a name="jet_columnid"></a><span data-ttu-id="3c4e8-103">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="3c4e8-103">JET_COLUMNID</span></span>


<span data-ttu-id="3c4e8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3c4e8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnid"></a><span data-ttu-id="3c4e8-105">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="3c4e8-105">JET_COLUMNID</span></span>

<span data-ttu-id="3c4e8-106">O tipo de dados **JET_COLUMNID** identifica uma coluna dentro de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-106">The **JET_COLUMNID** data type identifies a column within a table.</span></span>

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a><span data-ttu-id="3c4e8-107">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="3c4e8-107">Data Types</span></span>

<span data-ttu-id="3c4e8-108">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="3c4e8-108">JET_COLUMNID</span></span>

<span data-ttu-id="3c4e8-109">Identifica uma coluna dentro de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-109">Identifies a column within a table.</span></span>

### <a name="remarks"></a><span data-ttu-id="3c4e8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c4e8-110">Remarks</span></span>

<span data-ttu-id="3c4e8-111">As IDs de coluna são exclusivas em uma única tabela.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-111">Column IDs are unique within a single table.</span></span> <span data-ttu-id="3c4e8-112">Depois que uma coluna tiver uma determinada ID de coluna, ela sempre terá essa ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-112">Once a column is known to have a certain column ID, it will always have that column ID.</span></span> <span data-ttu-id="3c4e8-113">A restauração do backup não alterará o valor de uma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-113">Restore from backup will not change the value of a column ID.</span></span> <span data-ttu-id="3c4e8-114">No entanto, se uma ou mais colunas de tabela, antes de uma coluna de tabela específica, forem excluídas, um banco de dados compacto poderá alterar o valor de uma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-114">However, if one or more table columns, prior to a specific table column, are deleted, a compact database can then change the value of a column ID.</span></span>

<span data-ttu-id="3c4e8-115">Em alguns casos, as IDs de coluna são os únicos meios de identificar colunas.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-115">In some cases, column IDs are the only means of identifying columns.</span></span> <span data-ttu-id="3c4e8-116">Quando uma tabela temporária é criada, suas colunas não têm nomes, mas uma matriz de IDs de coluna é retornada pela função de criação.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-116">When a temporary table is created, its columns do not have names, but an array of column IDs is returned by the create function.</span></span>

<span data-ttu-id="3c4e8-117">As colunas em tabelas diferentes podem ter a mesma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-117">Columns in different tables can have the same column ID.</span></span>

### <a name="requirements"></a><span data-ttu-id="3c4e8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c4e8-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c4e8-119"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3c4e8-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3c4e8-120">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c4e8-121"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3c4e8-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3c4e8-122">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c4e8-123"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3c4e8-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3c4e8-124">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3c4e8-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


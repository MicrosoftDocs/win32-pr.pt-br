---
description: 'Saiba mais sobre: estrutura de JET_SETINFO'
title: Estrutura de JET_SETINFO
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104506549"
---
# <a name="jet_setinfo-structure"></a><span data-ttu-id="ba168-103">Estrutura de JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="ba168-103">JET_SETINFO Structure</span></span>


<span data-ttu-id="ba168-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ba168-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setinfo-structure"></a><span data-ttu-id="ba168-105">Estrutura de JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="ba168-105">JET_SETINFO Structure</span></span>

<span data-ttu-id="ba168-106">A estrutura de **JET_SETINFO** contém parâmetros de entrada opcionais para [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="ba168-106">The **JET_SETINFO** structure contains optional input parameters for [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="ba168-107">Um ponteiro **nulo** pode ser passado onde um ponteiro para essa estrutura, de outra forma, seria passado.</span><span class="sxs-lookup"><span data-stu-id="ba168-107">A **NULL** pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="ba168-108">O significado de passar um **NULL** é o mesmo que passar **JET_SETINFO** com **cbStruct** definido como sizeof (JET_SETINFO), **ibLongValue** definido como 0 (zero) e **itagSequence** definido como 1.</span><span class="sxs-lookup"><span data-stu-id="ba168-108">The meaning of passing a **NULL** is the same as passing **JET_SETINFO** with **cbStruct** set to sizeof(JET_SETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a><span data-ttu-id="ba168-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ba168-109">Members</span></span>

<span data-ttu-id="ba168-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="ba168-110">**cbStruct**</span></span>

<span data-ttu-id="ba168-111">O tamanho, em bytes, do **JET_SETINFO**.</span><span class="sxs-lookup"><span data-stu-id="ba168-111">The size, in bytes, of the **JET_SETINFO**.</span></span> <span data-ttu-id="ba168-112">Esse valor confirma a presença dos campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba168-112">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="ba168-113">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="ba168-113">**ibLongValue**</span></span>

<span data-ttu-id="ba168-114">O deslocamento para o primeiro byte a ser definido em uma coluna do tipo [JET_coltypLongBinary](./jet-coltyp.md) ou [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="ba168-114">The offset to the first byte to be set in a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="ba168-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="ba168-115">**itagSequence**</span></span>

<span data-ttu-id="ba168-116">Descreve o número de sequência do valor em uma coluna de valores múltiplos a ser definida.</span><span class="sxs-lookup"><span data-stu-id="ba168-116">Describes the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="ba168-117">A matriz de valores é baseada em um.</span><span class="sxs-lookup"><span data-stu-id="ba168-117">The array of values is one-based.</span></span> <span data-ttu-id="ba168-118">O primeiro valor é Sequence 1, não 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ba168-118">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="ba168-119">Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como **itagSequence** se esse valor estiver sendo substituído.</span><span class="sxs-lookup"><span data-stu-id="ba168-119">If the record column has only one value then 1 should be passed as the **itagSequence** if that value is being replaced.</span></span> <span data-ttu-id="ba168-120">Um valor de 0 (zero) significa adicionar uma nova instância de valor de coluna ao final da sequência de valores de coluna.</span><span class="sxs-lookup"><span data-stu-id="ba168-120">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="ba168-121">Com uma coluna que pode conter vários valores, só é possível usar um número de sequência maior que 1 em [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) ou 0 em [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="ba168-121">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="ba168-122">Na implementação atual do mecanismo, qualquer coluna criada com JET_bitColumnTagged pode conter vários valores.</span><span class="sxs-lookup"><span data-stu-id="ba168-122">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="ba168-123">Colunas criadas com JET_bitColumnMultiValued diferem de colunas marcadas com vários valores apenas na forma como são indexadas.</span><span class="sxs-lookup"><span data-stu-id="ba168-123">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="ba168-124">Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ba168-124">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

### <a name="requirements"></a><span data-ttu-id="ba168-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba168-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba168-126"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ba168-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ba168-127">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ba168-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba168-128"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ba168-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ba168-129">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ba168-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba168-130"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ba168-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ba168-131">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ba168-131">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ba168-132">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ba168-132">See Also</span></span>

[<span data-ttu-id="ba168-133">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="ba168-133">JetSetColumn</span></span>](./jetsetcolumn-function.md)

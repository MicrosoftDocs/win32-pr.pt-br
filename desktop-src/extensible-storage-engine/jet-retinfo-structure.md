---
description: 'Saiba mais sobre: estrutura de JET_RETINFO'
title: Estrutura de JET_RETINFO
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827313"
---
# <a name="jet_retinfo-structure"></a><span data-ttu-id="36c2b-103">Estrutura de JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="36c2b-103">JET_RETINFO Structure</span></span>


<span data-ttu-id="36c2b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="36c2b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retinfo-structure"></a><span data-ttu-id="36c2b-105">Estrutura de JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="36c2b-105">JET_RETINFO Structure</span></span>

<span data-ttu-id="36c2b-106">A estrutura de **JET_RETINFO** contém parâmetros de entrada e saída opcionais para [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="36c2b-106">The **JET_RETINFO** structure contains optional input and output parameters for [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span> <span data-ttu-id="36c2b-107">Um ponteiro nulo pode ser passado onde um ponteiro para essa estrutura, de outra forma, seria passado.</span><span class="sxs-lookup"><span data-stu-id="36c2b-107">A null pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="36c2b-108">Passar um ponteiro NULL é o mesmo que passar **JET_RETINFO** com **cbStruct** definido como sizeof (JET_RETINFO), **ibLongValue** definido como 0 (zero) e **itagSequence** definido como 1.</span><span class="sxs-lookup"><span data-stu-id="36c2b-108">Passing a null pointer is the same as passing **JET_RETINFO** with **cbStruct** set to sizeof(JET_RETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a><span data-ttu-id="36c2b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="36c2b-109">Members</span></span>

<span data-ttu-id="36c2b-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="36c2b-110">**cbStruct**</span></span>

<span data-ttu-id="36c2b-111">Deve ser definido como o tamanho da estrutura de **JET_RETINFO** , em bytes, e serve para confirmar a presença dos campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="36c2b-111">Must be set to the size of the **JET_RETINFO** structure, in bytes, and serves to confirm the presence of the following fields.</span></span>

<span data-ttu-id="36c2b-112">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="36c2b-112">**ibLongValue**</span></span>

<span data-ttu-id="36c2b-113">O deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo [JET_coltypLongBinary](./jet-coltyp.md)ou [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="36c2b-113">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span> <span data-ttu-id="36c2b-114">Observe que a quantidade de dados recuperados desse deslocamento é menor do que o tamanho do buffer de saída e do tamanho dos dados no valor real após esse deslocamento.</span><span class="sxs-lookup"><span data-stu-id="36c2b-114">Note that the amount of data retrieved from this offset is the lower of the size of the output buffer and the size of data in the actual value after this offset.</span></span>

<span data-ttu-id="36c2b-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="36c2b-115">**itagSequence**</span></span>

<span data-ttu-id="36c2b-116">Descreve o número de sequência do valor em uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="36c2b-116">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="36c2b-117">Observe que a matriz de valores é baseada em um.</span><span class="sxs-lookup"><span data-stu-id="36c2b-117">Note that the array of values is one-based.</span></span> <span data-ttu-id="36c2b-118">O primeiro valor é Sequence 1, e não 0.</span><span class="sxs-lookup"><span data-stu-id="36c2b-118">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="36c2b-119">Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como o **itagSequence**</span><span class="sxs-lookup"><span data-stu-id="36c2b-119">If the record column has only one value then 1 should be passed as the **itagSequence**</span></span>

<span data-ttu-id="36c2b-120">Com uma coluna que pode conter vários valores, só é possível usar um número de sequência maior que 1 em [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) ou 0 em [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="36c2b-120">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="36c2b-121">Na implementação atual do mecanismo, qualquer coluna criada com JET_bitColumnTagged pode conter vários valores.</span><span class="sxs-lookup"><span data-stu-id="36c2b-121">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="36c2b-122">Colunas criadas com JET_bitColumnMultiValued diferem de colunas marcadas com vários valores apenas na forma como são indexadas.</span><span class="sxs-lookup"><span data-stu-id="36c2b-122">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="36c2b-123">Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="36c2b-123">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

<span data-ttu-id="36c2b-124">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="36c2b-124">**columnidNextTagged**</span></span>

<span data-ttu-id="36c2b-125">Retorna o columnid da coluna undeleted, multi-Value ou esparso, quando todas as colunas marcadas são recuperadas passando 0 como columnid para [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="36c2b-125">Returns the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="36c2b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36c2b-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36c2b-127"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="36c2b-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="36c2b-128">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="36c2b-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36c2b-129"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="36c2b-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="36c2b-130">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="36c2b-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36c2b-131"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="36c2b-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="36c2b-132">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="36c2b-132">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="36c2b-133">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="36c2b-133">See Also</span></span>

[<span data-ttu-id="36c2b-134">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="36c2b-134">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="36c2b-135">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="36c2b-135">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="36c2b-136">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="36c2b-136">JET_RETINFO</span></span>]()  
[<span data-ttu-id="36c2b-137">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="36c2b-137">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

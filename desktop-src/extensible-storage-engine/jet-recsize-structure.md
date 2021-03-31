---
description: 'Saiba mais sobre: estrutura de JET_RECSIZE'
title: Estrutura de JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646738"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="9a3b1-103">Estrutura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="9a3b1-103">JET_RECSIZE Structure</span></span>


<span data-ttu-id="9a3b1-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9a3b1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize-structure"></a><span data-ttu-id="9a3b1-105">Estrutura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="9a3b1-105">JET_RECSIZE Structure</span></span>

<span data-ttu-id="9a3b1-106">A estrutura de **JET_RECSIZE** é usada pelo [JetGetRecordSize](./jetgetrecordsize-function.md) para retornar informações sobre os requisitos de uso de um registro no espaço de dados do usuário, o número de colunas definidas, o número de valores e o espaço de sobrecarga da estrutura de registro do ESE.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-106">The **JET_RECSIZE** structure is used by [JetGetRecordSize](./jetgetrecordsize-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="9a3b1-107">**Windows Vista:** A estrutura de **JET_RECSIZE** é introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-107">**Windows Vista:** The **JET_RECSIZE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a><span data-ttu-id="9a3b1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9a3b1-108">Members</span></span>

<span data-ttu-id="9a3b1-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="9a3b1-109">**cbData**</span></span>

<span data-ttu-id="9a3b1-110">Conjunto de dados do usuário no registro.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-110">User data set in the record.</span></span>

<span data-ttu-id="9a3b1-111">**Observação**  O tamanho da chave não está incluído neste.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="9a3b1-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="9a3b1-112">**cbLongValueData**</span></span>

<span data-ttu-id="9a3b1-113">Dados de usuário associados ao registro, mas armazenados na árvore de valor longo.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="9a3b1-114">**Observação**  Isso não conta os valores intrínsecos longos.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="9a3b1-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="9a3b1-115">**cbOverhead**</span></span>

<span data-ttu-id="9a3b1-116">A sobrecarga da estrutura do registro ESE para esse registro.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="9a3b1-117">Isso inclui o tamanho da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-117">This includes the record's key size.</span></span>

<span data-ttu-id="9a3b1-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="9a3b1-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="9a3b1-119">A sobrecarga dos dados de valor longo.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="9a3b1-120">**Observação**  Isso não conta os valores intrínsecos longos.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="9a3b1-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="9a3b1-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="9a3b1-122">Número total de colunas fixas e variáveis definidas neste registro.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="9a3b1-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="9a3b1-123">**cTaggedColumns**</span></span>

<span data-ttu-id="9a3b1-124">Número total de colunas marcadas definidas neste registro.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="9a3b1-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="9a3b1-125">**cLongValues**</span></span>

<span data-ttu-id="9a3b1-126">Número total de valores longos armazenados na árvore de valor longo deste registro.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="9a3b1-127">**Observação**  Isso não conta os valores intrínsecos longos.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="9a3b1-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="9a3b1-128">**cMultiValues**</span></span>

<span data-ttu-id="9a3b1-129">A acumulação do número total de valores além do primeiro para todas as colunas no registro.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

### <a name="remarks"></a><span data-ttu-id="9a3b1-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a3b1-130">Remarks</span></span>

<span data-ttu-id="9a3b1-131">O número total de valores no registro seria **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-131">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

### <a name="requirements"></a><span data-ttu-id="9a3b1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a3b1-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a3b1-133"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9a3b1-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9a3b1-134">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-134">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a3b1-135"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9a3b1-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9a3b1-136">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-136">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a3b1-137"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9a3b1-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9a3b1-138">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-138">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9a3b1-139">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9a3b1-139">See Also</span></span>

[<span data-ttu-id="9a3b1-140">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="9a3b1-140">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

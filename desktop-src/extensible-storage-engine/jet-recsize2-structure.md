---
description: 'Saiba mais sobre: estrutura de JET_RECSIZE2'
title: Estrutura de JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
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
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791504"
---
# <a name="jet_recsize2-structure"></a><span data-ttu-id="9c8ac-103">Estrutura de JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="9c8ac-103">JET_RECSIZE2 Structure</span></span>


<span data-ttu-id="9c8ac-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9c8ac-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize2-structure"></a><span data-ttu-id="9c8ac-105">Estrutura de JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="9c8ac-105">JET_RECSIZE2 Structure</span></span>

<span data-ttu-id="9c8ac-106">A estrutura de **JET_RECSIZE2** é usada pelo [JetGetRecordSize2](./jetgetrecordsize2-function.md) para retornar informações sobre os requisitos de uso de um registro no espaço de dados do usuário, o número de colunas definidas, o número de valores e o espaço de sobrecarga da estrutura de registro do ESE.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-106">The **JET_RECSIZE2** structure is used by [JetGetRecordSize2](./jetgetrecordsize2-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="9c8ac-107">**Windows 7:** A estrutura de **JET_RECSIZE2** é introduzida no sistema operacional Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-107">**Windows 7:** The **JET_RECSIZE2** structure is introduced in the Windows 7 operating system.</span></span>

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
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
```

### <a name="members"></a><span data-ttu-id="9c8ac-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9c8ac-108">Members</span></span>

<span data-ttu-id="9c8ac-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-109">**cbData**</span></span>

<span data-ttu-id="9c8ac-110">Conjunto de dados do usuário no registro.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-110">User data set in the record.</span></span>

<span data-ttu-id="9c8ac-111">**Observação**  O tamanho da chave não está incluído neste.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="9c8ac-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-112">**cbLongValueData**</span></span>

<span data-ttu-id="9c8ac-113">Dados de usuário associados ao registro, mas armazenados na árvore de valor longo.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="9c8ac-114">**Observação**  Isso não conta os valores intrínsecos longos.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="9c8ac-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-115">**cbOverhead**</span></span>

<span data-ttu-id="9c8ac-116">A sobrecarga da estrutura do registro ESE para esse registro.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="9c8ac-117">Isso inclui o tamanho da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-117">This includes the record's key size.</span></span>

<span data-ttu-id="9c8ac-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="9c8ac-119">A sobrecarga dos dados de valor longo.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="9c8ac-120">**Observação**  Isso não conta os valores intrínsecos longos.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="9c8ac-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="9c8ac-122">Número total de colunas fixas e variáveis definidas neste registro.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="9c8ac-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-123">**cTaggedColumns**</span></span>

<span data-ttu-id="9c8ac-124">Número total de colunas marcadas definidas neste registro.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="9c8ac-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-125">**cLongValues**</span></span>

<span data-ttu-id="9c8ac-126">Número total de valores longos armazenados na árvore de valor longo deste registro.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="9c8ac-127">**Observação**  Isso não conta os valores intrínsecos longos.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="9c8ac-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-128">**cMultiValues**</span></span>

<span data-ttu-id="9c8ac-129">A acumulação do número total de valores além do primeiro para todas as colunas no registro.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

<span data-ttu-id="9c8ac-130">**cCompressedColumns**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-130">**cCompressedColumns**</span></span>

<span data-ttu-id="9c8ac-131">O número total de colunas compactadas.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-131">The total number of compressed columns.</span></span>

<span data-ttu-id="9c8ac-132">**cbDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-132">**cbDataCompressed**</span></span>

<span data-ttu-id="9c8ac-133">O tamanho compactado dos dados do usuário neste registro.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-133">The compressed size of user data in this record.</span></span> <span data-ttu-id="9c8ac-134">Isso é o mesmo que cbData se nenhum valor longo intrínseco for compactado.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-134">This is the same as cbData if no intrinsic long-values are compressed.</span></span>

<span data-ttu-id="9c8ac-135">**cbLongValueDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="9c8ac-135">**cbLongValueDataCompressed**</span></span>

<span data-ttu-id="9c8ac-136">O tamanho compactado dos dados do usuário na árvore de valor longo.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-136">The compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="9c8ac-137">Isso é o mesmo que os dados de cbLongValue se nenhum valor longo separado for compactado.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-137">This is the same as cbLongValue data if no separated long values are compressed.</span></span>

### <a name="remarks"></a><span data-ttu-id="9c8ac-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c8ac-138">Remarks</span></span>

<span data-ttu-id="9c8ac-139">O número total de valores no registro seria **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-139">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

<span data-ttu-id="9c8ac-140">Os dados lógicos no registro são (cbData + cbLongValueData) e o tamanho físico dos dados é (cbDataCompressed + cbLongValueDataCompressed).</span><span class="sxs-lookup"><span data-stu-id="9c8ac-140">The logical data in the record is (cbData+cbLongValueData) and the physical size of the data is (cbDataCompressed+cbLongValueDataCompressed).</span></span> <span data-ttu-id="9c8ac-141">Isso pode ser usado para calcular a taxa de compactação de dados armazenados.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-141">This can be used to calculate the compression ratio of stored data.</span></span>

### <a name="requirements"></a><span data-ttu-id="9c8ac-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c8ac-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c8ac-143"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9c8ac-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9c8ac-144">Requer o sistema operacional Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-144">Requires Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c8ac-145"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9c8ac-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9c8ac-146">Requer o sistema operacional Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-146">Requires Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c8ac-147"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9c8ac-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9c8ac-148">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9c8ac-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9c8ac-149">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9c8ac-149">See Also</span></span>

[<span data-ttu-id="9c8ac-150">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="9c8ac-150">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)  
[<span data-ttu-id="9c8ac-151">JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="9c8ac-151">JetGetRecordSize2</span></span>](./jetgetrecordsize2-function.md)

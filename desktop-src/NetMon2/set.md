---
description: A estrutura definida define um conjunto de valores.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: DEFINIR estrutura (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169517"
---
# <a name="set-structure"></a><span data-ttu-id="e73d1-103">DEFINIR estrutura</span><span class="sxs-lookup"><span data-stu-id="e73d1-103">SET structure</span></span>

<span data-ttu-id="e73d1-104">A estrutura **definida** define um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="e73d1-104">The **SET** structure defines a set of values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e73d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e73d1-105">Syntax</span></span>


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a><span data-ttu-id="e73d1-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e73d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e73d1-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="e73d1-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-108">Número total de entradas em um conjunto.</span><span class="sxs-lookup"><span data-stu-id="e73d1-108">Total number of entries in a set.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-109">**lpByteTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-109">**lpByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-110">Ponteiro para uma matriz de valores de BYTE.</span><span class="sxs-lookup"><span data-stu-id="e73d1-110">Pointer to an array of BYTE values.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-111">**lpWordTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-111">**lpWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-112">Ponteiro para uma matriz de valores de palavra.</span><span class="sxs-lookup"><span data-stu-id="e73d1-112">Pointer to an array of WORD values.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-113">**lpDwordTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-113">**lpDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-114">Ponteiro para uma matriz de valores DWORD.</span><span class="sxs-lookup"><span data-stu-id="e73d1-114">Pointer to an array of DWORD values.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-115">**lpLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-115">**lpLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-116">Ponteiro para uma matriz de estruturas [LARGEINT](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="e73d1-116">Pointer to an array of [LARGEINT](largeint.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-117">**lpSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-117">**lpSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-118">Ponteiro para uma matriz de valores de SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="e73d1-118">Pointer to an array of SYSTEMTIME values.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-119">**lpLabeledByteTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-119">**lpLabeledByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-120">Ponteiro para uma matriz de estruturas de [ \_ byte rotuladas](labeled-byte.md) .</span><span class="sxs-lookup"><span data-stu-id="e73d1-120">Pointer to an array of [LABELED\_BYTE](labeled-byte.md) structures.</span></span> <span data-ttu-id="e73d1-121">Cada estrutura de **\_ bytes rotulada** define um valor e um rótulo.</span><span class="sxs-lookup"><span data-stu-id="e73d1-121">Each **LABELED\_BYTE** structure defines a value and label.</span></span> <span data-ttu-id="e73d1-122">Monitor de Rede exibirá um rótulo se encontrar um valor correspondente no pacote de protocolo.</span><span class="sxs-lookup"><span data-stu-id="e73d1-122">Network Monitor displays a label if it finds a corresponding value in the protocol packet.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-123">**lpLabeledWordTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-123">**lpLabeledWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-124">Ponteiro para uma matriz de estruturas de [ \_ palavras rotuladas](labeled-word.md) que definem um conjunto de valores e rótulos de palavra.</span><span class="sxs-lookup"><span data-stu-id="e73d1-124">Pointer to an array of [LABELED\_WORD](labeled-word.md) structures that define a set of WORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-125">**lpLabeledDwordTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-125">**lpLabeledDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-126">Ponteiro para uma matriz de estruturas [ \_ DWORD rotuladas](labeled-dword.md) que definem um conjunto de valores e rótulos DWORD.</span><span class="sxs-lookup"><span data-stu-id="e73d1-126">Pointer to an array of [LABELED\_DWORD](labeled-dword.md) structures that define a set of DWORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-127">**lpLabeledLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-127">**lpLabeledLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-128">Ponteiro para uma matriz de estruturas [ \_ LARGEINT rotuladas](labeled-largeint.md) que definem um conjunto de valores e rótulos LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="e73d1-128">Pointer to an array of [LABELED\_LARGEINT](labeled-largeint.md) structures that define a set of LARGEINT values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-129">**lpLabeledSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-129">**lpLabeledSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-130">Ponteiro para uma matriz de estruturas [ \_ SYSTEMTIME rotuladas](labeled-systemtime.md) que definem um conjunto de valores e rótulos do sistema.</span><span class="sxs-lookup"><span data-stu-id="e73d1-130">Pointer to an array of [LABELED\_SYSTEMTIME](labeled-systemtime.md) structures that define a set of SYSTEM values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-131">**lpLabeledBit**</span><span class="sxs-lookup"><span data-stu-id="e73d1-131">**lpLabeledBit**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-132">Ponteiro para uma matriz de estruturas de [ \_ bits rotuladas](labeled-bit.md) que definem um conjunto de pares de bits rotulados.</span><span class="sxs-lookup"><span data-stu-id="e73d1-132">Pointer to an array of [LABELED\_BIT](labeled-bit.md) structures that define a set of labeled BIT pairs.</span></span> <span data-ttu-id="e73d1-133">Cada BIT pode especificar dois rótulos um rótulo para cada Estado (0 ou 1) do BIT.</span><span class="sxs-lookup"><span data-stu-id="e73d1-133">Each BIT can specify two labels   one label for each state (0 or 1) of the BIT.</span></span>

</dd> <dt>

<span data-ttu-id="e73d1-134">**lpVoidTable**</span><span class="sxs-lookup"><span data-stu-id="e73d1-134">**lpVoidTable**</span></span>
</dt> <dd>

<span data-ttu-id="e73d1-135">Ponteiro para uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="e73d1-135">Pointer to an array of values.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e73d1-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="e73d1-136">Remarks</span></span>

<span data-ttu-id="e73d1-137">A estrutura **definida** é usada para definir um conjunto de dados de comparação que monitor de rede pode usar para interpretar o valor de uma propriedade em um pacote de protocolo.</span><span class="sxs-lookup"><span data-stu-id="e73d1-137">The **SET** structure is used to define a set of comparison data that Network Monitor can use to interpret the value of a property in a protocol packet.</span></span> <span data-ttu-id="e73d1-138">Quando um conjunto de dados de comparação é necessário, um ponteiro para a estrutura do **conjunto** é especificado no membro **LpSet** da estrutura [PROPERTYINFO](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e73d1-138">When a set of comparison data is required, a pointer to the **SET** structure is specified in the **lpSet** member of the [PROPERTYINFO](propertyinfo.md) structure.</span></span>

<span data-ttu-id="e73d1-139">A DLL do analisador pode fornecer um conjunto de valores e um conjunto de rótulos.</span><span class="sxs-lookup"><span data-stu-id="e73d1-139">The parser DLL can provide a value set and a label set.</span></span> <span data-ttu-id="e73d1-140">O membro da **União** que você seleciona em uma estrutura de **conjunto** aponta para uma matriz de estruturas que define cada membro de um conjunto.</span><span class="sxs-lookup"><span data-stu-id="e73d1-140">The member of the **UNION** that you select in a **SET** structure points to an array of structures that define each member of a set.</span></span>

-   <span data-ttu-id="e73d1-141">Conjunto de valores</span><span class="sxs-lookup"><span data-stu-id="e73d1-141">Value set</span></span>

    <span data-ttu-id="e73d1-142">Um conjunto de valores é usado quando você deseja que Monitor de Rede inclua um indicador em conjunto ou não em conjunto com o valor encontrado no pacote de protocolo.</span><span class="sxs-lookup"><span data-stu-id="e73d1-142">A value set is used when you want Network Monitor to include an in-set or not-in-set indicator with the value found in the protocol packet.</span></span> <span data-ttu-id="e73d1-143">Por exemplo, se um conjunto DWORD for especificado, Monitor de Rede exibirá um rótulo para cada valor DWORD encontrado no pacote de protocolo, indicando que o DWORD está ou não está especificado no conjunto.</span><span class="sxs-lookup"><span data-stu-id="e73d1-143">For example, if a DWORD set is specified, Network Monitor displays a label for each DWORD value found in the protocol packet, indicating that the DWORD is or is not specified in the set.</span></span>

    <span data-ttu-id="e73d1-144">Um conjunto de valores pode ser baseado em tipos de dados BYTE, WORD, DWORD, LARGEINT e SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="e73d1-144">A value set can be based on BYTE, WORD, DWORD, LARGEINT, and SYSTEMTIME data types.</span></span>

-   <span data-ttu-id="e73d1-145">Conjunto de rótulos</span><span class="sxs-lookup"><span data-stu-id="e73d1-145">Label set</span></span>

    <span data-ttu-id="e73d1-146">Um conjunto de rótulos é usado quando você deseja que Monitor de Rede exiba um rótulo definido pelo usuário em vez dos valores de propriedade especificados em um conjunto.</span><span class="sxs-lookup"><span data-stu-id="e73d1-146">A label set is used when you want Network Monitor to display a user-defined label instead of the property values specified in a set.</span></span>

    <span data-ttu-id="e73d1-147">Um conjunto de rótulos pode ser baseado em pares BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME e de rótulo de bits.</span><span class="sxs-lookup"><span data-stu-id="e73d1-147">A label set can be based on BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME and BIT label pairs.</span></span>

## <a name="requirements"></a><span data-ttu-id="e73d1-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e73d1-148">Requirements</span></span>



| <span data-ttu-id="e73d1-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="e73d1-149">Requirement</span></span> | <span data-ttu-id="e73d1-150">Valor</span><span class="sxs-lookup"><span data-stu-id="e73d1-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e73d1-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e73d1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e73d1-152">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e73d1-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e73d1-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e73d1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e73d1-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e73d1-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e73d1-155">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e73d1-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="e73d1-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e73d1-156"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e73d1-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="e73d1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e73d1-158">BIT ROTULAdo \_</span><span class="sxs-lookup"><span data-stu-id="e73d1-158">LABELED\_BIT</span></span>](labeled-bit.md)
</dt> <dt>

[<span data-ttu-id="e73d1-159">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="e73d1-159">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 





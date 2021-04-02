---
description: 'Saiba mais sobre: estrutura de JET_TUPLELIMITS'
title: Estrutura de JET_TUPLELIMITS
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
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
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922844"
---
# <a name="jet_tuplelimits-structure"></a><span data-ttu-id="df4bb-103">Estrutura de JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="df4bb-103">JET_TUPLELIMITS Structure</span></span>


<span data-ttu-id="df4bb-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="df4bb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tuplelimits-structure"></a><span data-ttu-id="df4bb-105">Estrutura de JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="df4bb-105">JET_TUPLELIMITS Structure</span></span>

<span data-ttu-id="df4bb-106">A estrutura de **JET_TUPLELIMITS** permite a personalização das características de índice de tupla em uma base por índice, em vez de uma base por instância, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="df4bb-106">The **JET_TUPLELIMITS** structure allows customization of the tuple index characteristics on a per-index basis, rather than a per-instance basis, using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="df4bb-107">**Windows Server 2003:** A estrutura de **JET_TUPLELIMITS** é introduzida no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="df4bb-107">**Windows Server 2003:** The **JET_TUPLELIMITS** structure is introduced in Windows Server 2003.</span></span>

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a><span data-ttu-id="df4bb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="df4bb-108">Members</span></span>

<span data-ttu-id="df4bb-109">**chLengthMin**</span><span class="sxs-lookup"><span data-stu-id="df4bb-109">**chLengthMin**</span></span>

<span data-ttu-id="df4bb-110">O comprimento mínimo de uma tupla.</span><span class="sxs-lookup"><span data-stu-id="df4bb-110">The minimum length of a tuple.</span></span> <span data-ttu-id="df4bb-111">O valor padrão é 3.</span><span class="sxs-lookup"><span data-stu-id="df4bb-111">The default value is 3.</span></span>

<span data-ttu-id="df4bb-112">**chLengthMax**</span><span class="sxs-lookup"><span data-stu-id="df4bb-112">**chLengthMax**</span></span>

<span data-ttu-id="df4bb-113">O comprimento máximo de uma tupla.</span><span class="sxs-lookup"><span data-stu-id="df4bb-113">The maximum length of a tuple.</span></span> <span data-ttu-id="df4bb-114">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="df4bb-114">The default value is 10.</span></span>

<span data-ttu-id="df4bb-115">**chToIndexMax**</span><span class="sxs-lookup"><span data-stu-id="df4bb-115">**chToIndexMax**</span></span>

<span data-ttu-id="df4bb-116">O comprimento máximo de uma cadeia de caracteres a ser indexada.</span><span class="sxs-lookup"><span data-stu-id="df4bb-116">The maximum length of a string to index.</span></span> <span data-ttu-id="df4bb-117">Por exemplo, se uma coluna tiver 100 caracteres de comprimento e **chToIndexMax** for definido como 60, somente os primeiros 60 caracteres da coluna serão indexados.</span><span class="sxs-lookup"><span data-stu-id="df4bb-117">For example, if a column is 100 characters long, and **chToIndexMax** is set to 60, then only the first 60 characters of the column will be indexed.</span></span> <span data-ttu-id="df4bb-118">O valor padrão é 32767.</span><span class="sxs-lookup"><span data-stu-id="df4bb-118">The default value is 32767.</span></span>

<span data-ttu-id="df4bb-119">**cchIncrement**</span><span class="sxs-lookup"><span data-stu-id="df4bb-119">**cchIncrement**</span></span>

<span data-ttu-id="df4bb-120">Isso permite que o stride seja configurado em uma base por índice.</span><span class="sxs-lookup"><span data-stu-id="df4bb-120">This allows the stride to be configured on a per index basis.</span></span>

<span data-ttu-id="df4bb-121">**Windows Vista:** O membro **cchIncrement** é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df4bb-121">**Windows Vista:** The **cchIncrement** member is introduced in Windows Vista.</span></span> <span data-ttu-id="df4bb-122">Antes do Windows Vista, o valor para mudar a janela (o "Stride") era sempre 1, como é mostrado no exemplo na seção comentários.</span><span class="sxs-lookup"><span data-stu-id="df4bb-122">Prior to Windows Vista, the amount to shift the window (the "stride") was always 1, as is shown in the example in the remarks section.</span></span>

<span data-ttu-id="df4bb-123">**ichStart**</span><span class="sxs-lookup"><span data-stu-id="df4bb-123">**ichStart**</span></span>

<span data-ttu-id="df4bb-124">O deslocamento no valor para começar a recuperar tuplas do valor.</span><span class="sxs-lookup"><span data-stu-id="df4bb-124">The offset into the value to begin taking retrieving tuples from the value.</span></span>

<span data-ttu-id="df4bb-125">**Windows Vista:** O membro **ichStart** é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df4bb-125">**Windows Vista:** The **ichStart** member is introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="df4bb-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="df4bb-126">Remarks</span></span>

<span data-ttu-id="df4bb-127">Um índice de tupla percorre uma cadeia de caracteres e indexa todas as subcadeias de caracteres possíveis de **chLengthMax**.</span><span class="sxs-lookup"><span data-stu-id="df4bb-127">A tuple index walks a string and indexes all of its possible substrings of **chLengthMax**.</span></span> <span data-ttu-id="df4bb-128">No final da cadeia de caracteres (ou na posição **chToIndexMax**, o que ocorrer primeiro), as subcadeias de pelo menos **chLengthMin** serão indexadas.</span><span class="sxs-lookup"><span data-stu-id="df4bb-128">At the end of the string (or at position **chToIndexMax**, whichever occurs first), the substrings of at least **chLengthMin** will be indexed.</span></span>

<span data-ttu-id="df4bb-129">Um índice de tupla pode ser usado para pesquisar cadeias de caracteres com curingas à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="df4bb-129">A tuple index can be used for searching strings with both leading and trailing wildcards.</span></span>

<span data-ttu-id="df4bb-130">Supondo uma linha com um campo de texto de "chuva na Espanha \! ", se um índice de tupla for criado com os parâmetros **chLengthMin**= 2 e **chLengthMax**= 3, as seguintes entradas serão criadas no índice:</span><span class="sxs-lookup"><span data-stu-id="df4bb-130">Assuming a row with a text field of "RAIN IN SPAIN\!", if a tuple index gets created with parameters **chLengthMin**=2, and **chLengthMax**=3, the following entries are created in the index:</span></span>

<span data-ttu-id="df4bb-131">"RAI"</span><span class="sxs-lookup"><span data-stu-id="df4bb-131">"RAI"</span></span>  
<span data-ttu-id="df4bb-132">Ain</span><span class="sxs-lookup"><span data-stu-id="df4bb-132">"AIN"</span></span>  
<span data-ttu-id="df4bb-133">NO</span><span class="sxs-lookup"><span data-stu-id="df4bb-133">"IN "</span></span>  
<span data-ttu-id="df4bb-134">"N I"</span><span class="sxs-lookup"><span data-stu-id="df4bb-134">"N I"</span></span>  
<span data-ttu-id="df4bb-135">NO</span><span class="sxs-lookup"><span data-stu-id="df4bb-135">" IN"</span></span>  
<span data-ttu-id="df4bb-136">NO</span><span class="sxs-lookup"><span data-stu-id="df4bb-136">"IN "</span></span>  
<span data-ttu-id="df4bb-137">"N S"</span><span class="sxs-lookup"><span data-stu-id="df4bb-137">"N S"</span></span>  
<span data-ttu-id="df4bb-138">SP3</span><span class="sxs-lookup"><span data-stu-id="df4bb-138">" SP"</span></span>  
<span data-ttu-id="df4bb-139">AUTENTICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="df4bb-139">"SPA"</span></span>  
<span data-ttu-id="df4bb-140">"PAI"</span><span class="sxs-lookup"><span data-stu-id="df4bb-140">"PAI"</span></span>  
<span data-ttu-id="df4bb-141">Ain</span><span class="sxs-lookup"><span data-stu-id="df4bb-141">"AIN"</span></span>  
<span data-ttu-id="df4bb-142">"IN \! "</span><span class="sxs-lookup"><span data-stu-id="df4bb-142">"IN\!"</span></span>  
<span data-ttu-id="df4bb-143">"N \! "</span><span class="sxs-lookup"><span data-stu-id="df4bb-143">"N\!"</span></span>

<span data-ttu-id="df4bb-144">Observe que "IN" ocorre duas vezes e que a última entrada ("N \! ") é menor que 3 (**chLengthMax**).</span><span class="sxs-lookup"><span data-stu-id="df4bb-144">Note that "IN " occurs twice, and that the last entry ("N\!") is shorter than 3 (**chLengthMax**).</span></span> <span data-ttu-id="df4bb-145">Observe também que o algoritmo de divisão não está ciente de espaços ou palavras e trata todos os caracteres de forma idêntica.</span><span class="sxs-lookup"><span data-stu-id="df4bb-145">Also note that the splitting algorithm is not aware of spaces or words, and treats all characters identically.</span></span>

<span data-ttu-id="df4bb-146">**Windows XP:** O Windows XP dá suporte a índices de tupla, mas não tem **JET_TUPLELIMITS**.</span><span class="sxs-lookup"><span data-stu-id="df4bb-146">**Windows XP:** Windows XP supports tuple indexes, but does not have **JET_TUPLELIMITS**.</span></span> <span data-ttu-id="df4bb-147">O mecanismo de banco de dados usará os valores padrão (**chLengthMin**= 3, **chLengthMax**= 10, **chToIndexMax**= 32767).</span><span class="sxs-lookup"><span data-stu-id="df4bb-147">The database engine will used the default values (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767).</span></span> <span data-ttu-id="df4bb-148">Ainda é possível alterar esses valores, mas eles são definidos em uma base por instância usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)e [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="df4bb-148">It is still possible to change these values, but they are set on a per-instance basis using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md), and [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="df4bb-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df4bb-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df4bb-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="df4bb-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="df4bb-151">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df4bb-151">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df4bb-152"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="df4bb-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="df4bb-153">Requer o Windows Server 2008, o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="df4bb-153">Requires Windows Server 2008, Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df4bb-154"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="df4bb-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="df4bb-155">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="df4bb-155">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="df4bb-156">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="df4bb-156">See Also</span></span>

[<span data-ttu-id="df4bb-157">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="df4bb-157">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="df4bb-158">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="df4bb-158">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="df4bb-159">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="df4bb-159">JET_TUPLELIMITS</span></span>]()  
[<span data-ttu-id="df4bb-160">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="df4bb-160">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)

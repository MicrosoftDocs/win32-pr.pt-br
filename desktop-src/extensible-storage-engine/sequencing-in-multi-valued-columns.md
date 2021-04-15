---
description: 'Saiba mais sobre: sequenciamento em colunas com valores múltiplos'
title: Sequenciamento em colunas com valores múltiplos
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569660"
---
# <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="6749d-103">Sequenciamento em colunas com valores múltiplos</span><span class="sxs-lookup"><span data-stu-id="6749d-103">Sequencing in Multi-Valued Columns</span></span>


<span data-ttu-id="6749d-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6749d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="6749d-105">Sequenciamento em colunas com valores múltiplos</span><span class="sxs-lookup"><span data-stu-id="6749d-105">Sequencing in Multi-Valued Columns</span></span>

<span data-ttu-id="6749d-106">Os valores em uma coluna com valores múltiplos são identificados por um número de índice chamado *itagSequence*.</span><span class="sxs-lookup"><span data-stu-id="6749d-106">The values in a multi-valued column are identified by an index number called the *itagSequence*.</span></span> <span data-ttu-id="6749d-107">Esse número é uma referência a um único valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="6749d-107">This number is a reference to a single value of the column.</span></span> <span data-ttu-id="6749d-108">Esse número é usado quando novos valores são definidos, recuperados ou enumerados na coluna.</span><span class="sxs-lookup"><span data-stu-id="6749d-108">This number is used when new values are set, retrieved, or enumerated in the column.</span></span> <span data-ttu-id="6749d-109">O *itagSequence* é usado em várias estruturas, incluindo:</span><span class="sxs-lookup"><span data-stu-id="6749d-109">The *itagSequence* is used in various structures, including:</span></span>

  - [<span data-ttu-id="6749d-110">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="6749d-110">JET_RETINFO</span></span>](./jet-retinfo-structure.md)

  - [<span data-ttu-id="6749d-111">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="6749d-111">JET_SETINFO</span></span>](./jet-setinfo-structure.md)

  - [<span data-ttu-id="6749d-112">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="6749d-112">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)

  - [<span data-ttu-id="6749d-113">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6749d-113">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)

  - [<span data-ttu-id="6749d-114">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="6749d-114">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)

<span data-ttu-id="6749d-115">Esse *itagSequence* começa em 1 para cada valor na coluna de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="6749d-115">This *itagSequence* starts at 1 for every value in the multi-valued column.</span></span> <span data-ttu-id="6749d-116">O número de sequência aumenta quando novos valores são adicionados à coluna.</span><span class="sxs-lookup"><span data-stu-id="6749d-116">The sequence number is increased when new values are added to the column.</span></span> <span data-ttu-id="6749d-117">Definir um valor em uma coluna com um *itagSequence* de 0 indica que o valor deve ser acrescentado ao conjunto de valores já existentes nessa coluna.</span><span class="sxs-lookup"><span data-stu-id="6749d-117">Setting a value in a column with an *itagSequence* of 0 indicates that the value is to be appended to the set of values already in that column.</span></span> <span data-ttu-id="6749d-118">O uso de um *itagSequence* maior que o número de valores atualmente definidos para uma coluna terá o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="6749d-118">Using an *itagSequence* greater than the number of values currently set for a column will have the same effect.</span></span> <span data-ttu-id="6749d-119">Especificar o *itagSequence* de um valor existente substituirá esse valor, não inserirá um novo.</span><span class="sxs-lookup"><span data-stu-id="6749d-119">Specifying the *itagSequence* of an existing value will overwrite that value, not insert a new one.</span></span> <span data-ttu-id="6749d-120">A definição de um valor existente como NULL removerá esse valor do conjunto de valores já existentes nessa coluna.</span><span class="sxs-lookup"><span data-stu-id="6749d-120">Setting an existing value to NULL will remove that value from the set of values already in that column.</span></span> <span data-ttu-id="6749d-121">Isso moverá todos os valores subsequentes na coluna por um slot de modo que o acesso subsequente a esses valores por *itagSequence* seja de um número menor do que o usado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6749d-121">This will move all the subsequent values in the column down by one slot such that subsequent access to those values by *itagSequence* will be by a number one less than what was previously used.</span></span>

<span data-ttu-id="6749d-122">O diagrama a seguir mostra um *itagSequence* em uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="6749d-122">The following diagram shows an *itagSequence* in a multi-valued column.</span></span> <span data-ttu-id="6749d-123">A coluna chamada ColA tem três entradas: val1, Val2 e Val3 com *itagSequence* de 1, 2 e 3, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6749d-123">The column named ColA has three entries: Val1, Val2 and Val3 with *itagSequence* of 1, 2, and 3 respectively.</span></span>

<span data-ttu-id="6749d-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="6749d-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>

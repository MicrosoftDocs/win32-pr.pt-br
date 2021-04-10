---
title: Pesquisando uma subparte
description: Pesquisando uma subparte
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- e/s de arquivo multimídia, pesquisando a parte do RIFF
- e/s de arquivo, pesquisando a parte do RIFF
- entrada e saída (e/s), pesquisando a parte do RIFF
- E/s (entrada e saída), pesquisando a parte do RIFF
- pesquisando a parte do RIFF
- formato de arquivo de intercâmbio de recursos (RIFF)
- RIFF (formato de arquivo de intercâmbio de recursos)
- E/S DO RIFF
- Parte do RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294052"
---
# <a name="searching-for-a-subchunk"></a><span data-ttu-id="e20d0-112">Pesquisando uma subparte</span><span class="sxs-lookup"><span data-stu-id="e20d0-112">Searching for a Subchunk</span></span>

<span data-ttu-id="e20d0-113">O exemplo a seguir usa a função [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) para procurar a parte "fmt" na parte "riff" do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="e20d0-113">The following example uses the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function to search for the "FMT" chunk in the "RIFF" chunk of the previous example.</span></span>


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



<span data-ttu-id="e20d0-114">Para pesquisar uma subparte (ou seja, qualquer parte que não seja uma parte "RIFF" ou "lista"), identifique sua parte pai no parâmetro *lpckParent* da função [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) .</span><span class="sxs-lookup"><span data-stu-id="e20d0-114">To search for a subchunk (that is, any chunk other than a "RIFF" or "LIST" chunk), identify its parent chunk in the *lpckParent* parameter of the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function.</span></span>

<span data-ttu-id="e20d0-115">Se você não especificar uma parte pai, a posição atual do arquivo deverá estar no início de uma parte antes de chamar a função **mmioDescend** .</span><span class="sxs-lookup"><span data-stu-id="e20d0-115">If you do not specify a parent chunk, the current file position should be at the beginning of a chunk before you call the **mmioDescend** function.</span></span> <span data-ttu-id="e20d0-116">Se você especificar uma parte pai, a posição atual do arquivo poderá estar em qualquer lugar nessa parte.</span><span class="sxs-lookup"><span data-stu-id="e20d0-116">If you do specify a parent chunk, the current file position can be anywhere in that chunk.</span></span>

<span data-ttu-id="e20d0-117">Se a pesquisa de uma subparte falhar, a posição atual do arquivo será indefinida.</span><span class="sxs-lookup"><span data-stu-id="e20d0-117">If the search for a subchunk fails, the current file position is undefined.</span></span> <span data-ttu-id="e20d0-118">Você pode usar a função [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) e o membro **DwDataOffset** da estrutura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) descrevendo a parte pai para buscar de volta até o início da parte pai, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="e20d0-118">You can use the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function and the **dwDataOffset** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure describing the parent chunk to seek back to the beginning of the parent chunk, as in the following example:</span></span>


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



<span data-ttu-id="e20d0-119">Como **dwDataOffset** especifica o deslocamento para o início da parte de dados da parte, você deve procurar quatro bytes após **dwDataOffset** para definir a posição do arquivo após o tipo de formulário.</span><span class="sxs-lookup"><span data-stu-id="e20d0-119">Because **dwDataOffset** specifies the offset to the beginning of the data portion of the chunk, you must seek 4 bytes past **dwDataOffset** to set the file position after the form type.</span></span>

 

 
---
title: Criando uma parte do RIFF
description: Criando uma parte do RIFF
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- e/s de arquivo multimídia, criando parte do RIFF
- e/s de arquivo, criando a parte RIFF
- entrada e saída (e/s), criando parte do RIFF
- E/s (entrada e saída), criando a parte do RIFF
- Criando parte do RIFF
- função mmioCreateChunk
- formato de arquivo de intercâmbio de recursos (RIFF)
- RIFF (formato de arquivo de intercâmbio de recursos)
- E/S DO RIFF
- Parte do RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823718"
---
# <a name="creating-a-riff-chunk"></a><span data-ttu-id="69d57-113">Criando uma parte do RIFF</span><span class="sxs-lookup"><span data-stu-id="69d57-113">Creating a RIFF Chunk</span></span>

<span data-ttu-id="69d57-114">O exemplo a seguir usa a função [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) para criar uma parte com um identificador de parte de "riff" e um tipo de formulário de "RDIB".</span><span class="sxs-lookup"><span data-stu-id="69d57-114">The following example uses the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function to create a chunk with a chunk identifier of "RIFF" and a form type of "RDIB".</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



<span data-ttu-id="69d57-115">Se você estiver criando uma parte "RIFF" ou "lista", deverá especificar o tipo de formulário ou de lista no membro **fccType** da estrutura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) .</span><span class="sxs-lookup"><span data-stu-id="69d57-115">If you are creating a "RIFF" or "LIST" chunk, you must specify the form type or list type in the **fccType** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure.</span></span> <span data-ttu-id="69d57-116">No exemplo anterior, "RDIB" é o tipo de formulário.</span><span class="sxs-lookup"><span data-stu-id="69d57-116">In the previous example, "RDIB" is the form type.</span></span>

<span data-ttu-id="69d57-117">Se você souber o tamanho do campo de dados em uma nova parte, poderá definir o membro **cksize** da estrutura **MMCKINFO** ao criar a parte.</span><span class="sxs-lookup"><span data-stu-id="69d57-117">If you know the size of the data field in a new chunk, you can set the **cksize** member of the **MMCKINFO** structure when you create the chunk.</span></span> <span data-ttu-id="69d57-118">Esse valor será gravado no campo tamanho dos dados na nova parte.</span><span class="sxs-lookup"><span data-stu-id="69d57-118">This value will be written to the data size field in the new chunk.</span></span> <span data-ttu-id="69d57-119">Se esse valor não estiver correto quando você chamar [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) para marcar o final da parte, ele será reescrito automaticamente para refletir o tamanho correto do campo de dados.</span><span class="sxs-lookup"><span data-stu-id="69d57-119">If this value is not correct when you call [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) to mark the end of the chunk, it will be automatically rewritten to reflect the correct size of the data field.</span></span>

<span data-ttu-id="69d57-120">Depois de criar uma parte usando a função [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) , a posição do arquivo é definida como o campo de dados da parte (8 bytes a partir do início da parte).</span><span class="sxs-lookup"><span data-stu-id="69d57-120">After you create a chunk by using the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function, the file position is set to the data field of the chunk (8 bytes from the beginning of the chunk).</span></span> <span data-ttu-id="69d57-121">Se a parte for uma parte "RIFF" ou "lista", a posição do arquivo será definida como o local após o tipo de formulário ou tipo de lista (12 bytes a partir do início da parte).</span><span class="sxs-lookup"><span data-stu-id="69d57-121">If the chunk is a "RIFF" or "LIST" chunk, the file position is set to the location following the form type or list type (12 bytes from the beginning of the chunk).</span></span>

 

 
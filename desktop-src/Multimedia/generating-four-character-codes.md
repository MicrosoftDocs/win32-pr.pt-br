---
title: Gerando códigos de Four-Character
description: Gerando códigos de Four-Character
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- e/s de arquivo multimídia, códigos de quatro caracteres
- e/s de arquivo, códigos de quatro caracteres
- código de entrada e saída (e/s), códigos de quatro caracteres
- E/s (entrada e saída), códigos de quatro caracteres
- códigos de quatro caracteres
- função mmioStringToFOURCC
- macro mmioFOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640555"
---
# <a name="generating-four-character-codes"></a><span data-ttu-id="0be67-110">Gerando códigos de Four-Character</span><span class="sxs-lookup"><span data-stu-id="0be67-110">Generating Four-Character Codes</span></span>

<span data-ttu-id="0be67-111">Você pode usar a macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) ou a função [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) para gerar códigos de quatro caracteres.</span><span class="sxs-lookup"><span data-stu-id="0be67-111">You can use the [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) macro or the [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) function to generate four-character codes.</span></span> <span data-ttu-id="0be67-112">O exemplo a seguir usa **mmioFOURCC** para gerar um código de quatro caracteres para "Wave".</span><span class="sxs-lookup"><span data-stu-id="0be67-112">The following example uses **mmioFOURCC** to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



<span data-ttu-id="0be67-113">O exemplo a seguir usa [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) para gerar um código de quatro caracteres para "Wave".</span><span class="sxs-lookup"><span data-stu-id="0be67-113">The following example uses [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



<span data-ttu-id="0be67-114">O segundo parâmetro em [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) especifica sinalizadores para converter a cadeia de caracteres em um código de quatro caracteres.</span><span class="sxs-lookup"><span data-stu-id="0be67-114">The second parameter in [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) specifies flags for converting the string to a four-character code.</span></span> <span data-ttu-id="0be67-115">Se você especificar o \_ sinalizador MMIO TOUPPER, **mmioStringToFOURCC** converterá todos os caracteres alfabéticos na cadeia de caracteres em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="0be67-115">If you specify the MMIO\_TOUPPER flag, **mmioStringToFOURCC** converts all alphabetic characters in the string to uppercase.</span></span> <span data-ttu-id="0be67-116">Isso é útil quando você precisa especificar um código de quatro caracteres para identificar um procedimento de e/s personalizado porque códigos de quatro caracteres identificando nomes de extensão de arquivo devem estar em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="0be67-116">This is useful when you need to specify a four-character code to identify a custom I/O procedure because four-character codes identifying file-extension names must be all uppercase.</span></span>

 

 
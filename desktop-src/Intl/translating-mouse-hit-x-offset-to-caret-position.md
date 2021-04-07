---
description: De forma convencional, o usuário pode selecionar a posição do cursor (CP) clicando na metade de caractere à direita &\# 0034; CP-1&\# 0034; ou na metade de caractere à esquerda &\# 0034; CP&\# 0034;.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Convertendo o deslocamento de clique do mouse X na posição do cursor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f993de35ebffac4740b367927d1a8edf864a813e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828572"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a><span data-ttu-id="4e5bd-103">Convertendo o deslocamento de clique do mouse X na posição do cursor</span><span class="sxs-lookup"><span data-stu-id="4e5bd-103">Translating Mouse Hit X Offset to Caret Position</span></span>

<span data-ttu-id="4e5bd-104">De forma convencional, o usuário pode selecionar a posição do cursor (CP) clicando na metade direita do caractere "CP-1" ou na metade de caractere "CP" à esquerda.</span><span class="sxs-lookup"><span data-stu-id="4e5bd-104">Conventionally, the user can select caret position (cp) by clicking either the trailing half of character "cp-1" or the leading half of character "cp".</span></span> <span data-ttu-id="4e5bd-105">Um aplicativo pode implementar a tradução do deslocamento x de clique do mouse para a posição do cursor da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4e5bd-105">An application can implement the translation of mouse hit x offset to caret position as follows:</span></span>


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



<span data-ttu-id="4e5bd-106">Para scripts que encaixam o cursor em limites de cluster, uma chamada para [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) retorna com *fTrailing* definido como 0 ou a largura do cluster em pontos de código.</span><span class="sxs-lookup"><span data-stu-id="4e5bd-106">For scripts that snap the caret to cluster boundaries, a call to [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) returns with *fTrailing* set to either 0 or the width of the cluster in code points.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e5bd-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e5bd-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e5bd-108">Usando o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="4e5bd-108">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




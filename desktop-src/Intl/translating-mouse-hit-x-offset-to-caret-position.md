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
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>Convertendo o deslocamento de clique do mouse X na posição do cursor

De forma convencional, o usuário pode selecionar a posição do cursor (CP) clicando na metade direita do caractere "CP-1" ou na metade de caractere "CP" à esquerda. Um aplicativo pode implementar a tradução do deslocamento x de clique do mouse para a posição do cursor da seguinte maneira:


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



Para scripts que encaixam o cursor em limites de cluster, uma chamada para [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) retorna com *fTrailing* definido como 0 ou a largura do cluster em pontos de código.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




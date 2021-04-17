---
description: No texto unidirecional, a posição do cursor não tem nenhuma ambiguidade porque a borda esquerda de um caractere está no mesmo local que a borda direita do caractere anterior.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Exibindo o cursor em cadeias bidirecionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748994"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a>Exibindo o cursor em cadeias bidirecionais

No texto unidirecional, a posição do cursor não tem nenhuma ambiguidade porque a borda esquerda de um caractere está no mesmo local que a borda direita do caractere anterior. No entanto, no texto bidirecional, a posição do cursor entre as execuções de direção oposta é ambígua. Por exemplo, no parágrafo da esquerda para a direita "hellosalaam", a última letra de "Olá" precede imediatamente a primeira letra de "Salaam". A melhor posição na qual exibir o cursor depende se é considerado seguir o "o" de "Olá" ou preceder o "s" de "Salaam".

O Uniscribe usa as convenções de posicionamento do cursor mostradas na tabela a seguir.



| Situação       | Posicionamento do cursor Visual                       |
|-----------------|----------------------------------------------|
| Digitação          | Borda direita do último caractere digitado.       |
| Colando         | Borda direita do último caractere colado.      |
| Avançando no cursor | Borda direita do último caractere passada. |
| Desativação do cursor  | Borda esquerda do último caractere passada.  |
| Página Inicial            | Borda à esquerda da linha.                        |
| End             | Borda à direita da linha.                       |



 

O cursor pode ser posicionado conforme mostrado no exemplo a seguir:


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



O posicionamento do cursor pode ser mais simples, como mostrado abaixo, dado um valor *fAdvancing* restrito a **true** ou **false**:


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) manipula as posições fora do intervalo logicamente. Ele retorna a borda à esquerda da execução para *iCharPos* <0 e a borda à direita da execução de *iCharPos* >= Length. Para obter mais informações, consulte [Gerenciando o posicionamento do cursor e teste de clique](managing-caret-placement-and-hit-testing.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




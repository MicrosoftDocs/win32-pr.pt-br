---
description: No modo de sombreamento simples, a seguinte pirâmide é exibida com uma borda nítida entre rostos adjacentes. No modo de sombreamento Gouraud, no entanto, os valores de sombreamento são interpolados na borda e a aparência final é de uma superfície curvada.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Comparando modos de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089685"
---
# <a name="comparing-shading-modes-direct3d-9"></a>Comparando modos de sombreamento (Direct3D 9)

No modo de sombreamento simples, a seguinte pirâmide é exibida com uma borda nítida entre rostos adjacentes. No modo de sombreamento Gouraud, no entanto, os valores de sombreamento são interpolados na borda e a aparência final é de uma superfície curvada.

![ilustração de uma pirâmide com bordas nítidas e setas que apontam para a face normal](images/shade2.png)

O sombreamento Gouraud ilumina as superfícies simples de forma realista do que o sombreamento simples. Uma face no modo de sombreamento simples é uma cor uniforme, mas o sombreamento Gouraud permite que a luz caia em um rosto mais corretamente. Esse efeito é particularmente óbvio se houver uma fonte de ponto próximo.

O sombreamento de Gouraud suaviza as bordas nítidas entre polígonos visíveis com sombreamento simples. No entanto, isso pode resultar em bandas de Mach, que são faixas de cor ou luz que não são mescladas suavemente entre polígonos adjacentes. Seu aplicativo pode reduzir a aparência das bandas de Mach aumentando o número de polígonos em um objeto, aumentando a resolução da tela ou aumentando a intensidade da cor do aplicativo.

O sombreamento Gouraud pode perder alguns detalhes. Por exemplo, na ilustração a seguir, um destaque está completamente contido em uma face de polígono.

![ilustração de um Spotlight em uma face de polígono](images/gouraud.png)

Nesse caso, o sombreamento Gouraud, que interpola entre vértices, perderia o destaque completamente; a face seria renderizada como se o Spotlight não existisse.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreamento](shading.md)
</dt> </dl>

 

 




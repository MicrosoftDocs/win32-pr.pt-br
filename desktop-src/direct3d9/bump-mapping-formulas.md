---
description: O Direct3D aplica as fórmulas a seguir aos componentes DU e DV em cada pixel do mapa de relevo.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Fórmulas de mapeamento de relevo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089686"
---
# <a name="bump-mapping-formulas-direct3d-9"></a>Fórmulas de mapeamento de relevo (Direct3D 9)

O Direct3D aplica as fórmulas a seguir aos componentes D<sub>U</sub> e d<sub>V</sub> em cada pixel do mapa de relevo.

![fórmulas de transformações de matriz de mapeamento de relevo](images/dudv-transform.png)

Nessas fórmulas, as variáveis D<sub>U</sub> e d<sub>V</sub> são obtidas diretamente de um pixel de mapa de relevo e transformadas por uma matriz 2x2 para produzir os valores Delta de saída D<sub>U</sub>' e D<sub>V</sub>'. O sistema usa os valores de saída para modificar as coordenadas de textura que abordam o mapa de ambiente no próximo estágio de textura. Os coeficientes da matriz de transformação são definidos por meio dos \_ Estados D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 e D3DTSS \_ BUMPENVMAT11 de estágio de textura.

Além dos valores Delta de você e v, o sistema pode calcular um valor de luminância que ele usa para modular a cor do mapa de ambiente no próximo estágio de mesclagem, conforme mostrado na fórmula a seguir.

![fórmula para luminância de saída, computada do fator de escala e do deslocamento](images/l-transform.png)

Nesta fórmula, L ' é a luminância de saída sendo computada. A variável L é o valor de luminância obtido de um pixel de mapa de relevo, que é multiplicado pelo fator de dimensionamento, S e offset pelo valor na variável O. Os \_ Estados de estágio de textura D3DTSS BUMPENVLSCALE e D3DTSS \_ BUMPENVLOFFSET controlam os valores das variáveis S e o na fórmula. Esta fórmula só é aplicada quando a operação de mesclagem de textura para o estágio que contém o mapa de relevo é definida como D3DTOP \_ BUMPENVMAPLUMINANCE. Ao usar D3DTOP \_ BUMPENVMAP, o sistema usa um valor de 1,0 para L '.

Depois de computar os valores Delta de saída D<sub>U</sub>' e D<sub>V</sub>', o sistema os adiciona às coordenadas de textura no próximo estágio de textura e modula a cor escolhida pela luminância para produzir a cor aplicada ao polígono.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de relevo](bump-mapping.md)
</dt> </dl>

 

 




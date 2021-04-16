---
description: Mapas de ambiente esféricos, ou mapas de esfera, são texturas especiais que contêm uma imagem da cena em torno de um objeto ou os efeitos de iluminação em torno do objeto.
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: Mapeamento de ambiente esférico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b0e7aaa123478ecc7cc327dca0b13a8aae3d0c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758501"
---
# <a name="spherical-environment-mapping-direct3d-9"></a>Mapeamento de ambiente esférico (Direct3D 9)

Mapas de ambiente esféricos, ou mapas de esfera, são texturas especiais que contêm uma imagem da cena em torno de um objeto ou os efeitos de iluminação em torno do objeto. Ao contrário dos mapas de ambiente cúbico, os mapas de esfera não representam diretamente os arredores de um objeto. O tópico imagem bule no [mapeamento de ambiente (Direct3D 9)](environment-mapping.md) mostra os efeitos de reflexão que você pode obter com o mapeamento de esfera. Um mapa de esfera é uma representação 2D da exibição de 360 graus completa da cena em torno de um objeto, como se fosse feito por meio de uma lente olho-de-peixe, como mostrado na ilustração a seguir.

![ilustração de um mapa de esfera do interior de um edifício](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>Coordenadas de textura para mapas de ambiente esféricos

As coordenadas de textura que você especifica para cada vértice que recebe um mapeamento de ambiente devem endereçar a textura como uma função da distorção refletida criada pela curvatura da superfície. Os aplicativos devem computar essas coordenadas de textura para cada vértice para alcançar o efeito desejado. Uma maneira simples e eficaz de gerar coordenadas de textura usa o vértice normal como entrada. Embora existam vários métodos, a equação a seguir é comum entre aplicativos que executam o mapeamento de ambiente com mapas de esfera.

![equação de coordenadas de textura de computação para um mapa de esfera](images/spheremap-formula.png)

Nessas fórmulas, você e v são as coordenadas de textura sendo computadas, e N<sub>x</sub> e n<sub>Y</sub> são os componentes X e Y do vértice de espaço da câmera normal. A fórmula é simples, mas eficaz. Se o normal tiver um componente x positivo, os pontos normais à direita e a coordenada u serão ajustados para tratar a textura adequadamente. Da mesma forma, para a coordenada v: y positivo indica que o normal aponta para cima. O oposto é verdadeiro para valores negativos em cada componente.

Se os pontos normais estiverem diretamente na câmera, as coordenadas resultantes não devem receber nenhuma distorção. A tendência de + 0,5 para ambas as coordenadas coloca o ponto de distorção zero no centro do mapa de esfera e um vértice normal de (0, 0, z) atende a esse ponto. Essa fórmula não conta com o componente z do normal, mas os aplicativos que usam a fórmula podem otimizar cálculos ignorando vértices com um normal que tenha um elemento z positivo. Isso funciona para objetos com sombreamento simples porque, no espaço da câmera, se os pontos normais longe da câmera (z positivo), o vértice será retirado quando o objeto for renderizado. Para objetos Gouraud, um normal pode apontar para fora da câmera (x positivo) e o triângulo que contém o vértice ainda pode estar visível. Se você não calcular você e v para este vértice, a face ainda poderá ser usada, resultando em um comportamento inesperado.

## <a name="applying-spherical-environment-maps"></a>Aplicando mapas de ambiente esféricos

Você aplica um mapa de ambiente a objetos da mesma maneira que para qualquer outra textura, definindo a textura para o estágio de textura apropriado com o método [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) . Defina o primeiro parâmetro para o índice para o estágio de textura desejado e defina o segundo parâmetro como o endereço da interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) retornado quando você criou a textura para o mapa de ambiente. Você pode definir as operações de mesclagem de cor e alfa e os argumentos conforme necessário para atingir os efeitos de mesclagem de textura desejados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de ambiente](environment-mapping.md)
</dt> </dl>

 

 

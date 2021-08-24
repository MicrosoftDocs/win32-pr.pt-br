---
description: Mapas de ambiente esférico, ou mapas de esfera, são texturas especiais que contêm uma imagem da cena em torno de um objeto ou os efeitos de iluminação ao redor do objeto.
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: Mapeamento de ambiente esférico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be4347b71a041aaa8d7057ac2bb7523bfa235fe59f84fe1ba54c54283cd2159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746376"
---
# <a name="spherical-environment-mapping-direct3d-9"></a>Mapeamento de ambiente esférico (Direct3D 9)

Mapas de ambiente esférico, ou mapas de esfera, são texturas especiais que contêm uma imagem da cena em torno de um objeto ou os efeitos de iluminação ao redor do objeto. Ao contrário dos mapas de ambiente cúbica, os mapas de esfera não representam diretamente o ambiente de um objeto. O tópico imagem de bule no [Mapeamento de Ambiente (Direct3D 9)](environment-mapping.md) mostra os efeitos de reflexão que você pode obter com o mapeamento de esfera. Um mapa de esferas é uma representação 2D da exibição completa de 360 graus da cena ao redor de um objeto, como se fosse feito por meio de uma lente de olho de peixo, conforme mostrado na ilustração a seguir.

![ilustração de um mapa de esfera do dentro de um prédio](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>Coordenadas de textura para ambiente esférico Mapas

As coordenadas de textura especificadas para cada vértice que recebe um mapeamento de ambiente devem abordar a textura como uma função da distorção reflexiva criada pela curvatura da superfície. Os aplicativos devem calcular essas coordenadas de textura para cada vértice para obter o efeito desejado. Uma maneira simples e eficaz de gerar coordenadas de textura usa o vértice normal como entrada. Embora existam vários métodos, a equação a seguir é comum entre aplicativos que executam o mapeamento de ambiente com mapas de esfera.

![equação de coordenadas de textura de computação para um mapa de esfera](images/spheremap-formula.png)

Nessas fórmulas, você e v são as coordenadas de textura que estão sendo computadas e N<sub>X</sub> e N<sub>Y</sub> são os componentes x e y do vértice de espaço da câmera normal. A fórmula é simples, mas eficaz. Se o normal tiver um componente x positivo, o normal aponta para a direita e a coordenada u é ajustada para tratar a textura adequadamente. Da mesma forma para a coordenada v: y positivo indica que o normal aponta para cima. O oposto é verdadeiro para valores negativos em cada componente.

Se o normal aponta diretamente para a câmera, as coordenadas resultantes não devem receber distorção. O desvio de +0,5 para ambas as coordenadas coloca o ponto de distorção zero no centro do mapa de esfera e um vértice normal de (0, 0, z) aborda esse ponto. Essa fórmula não conta para o componente z do normal, mas os aplicativos que usam a fórmula podem otimizar cálculos ignorando vértices com um normal que tem um elemento z positivo. Isso funciona para objetos sombreados simples porque, no espaço da câmera, se o normal aponta para fora da câmera (positivo z), o vértice é eliminado quando o objeto é renderizado. Para objetos sombreados pelo Gouraud, um normal pode apontar para a câmera (positivo x) e o triângulo que contém o vértice ainda pode estar visível. Se você não computar você e v para esse vtex, o rosto ainda poderá ser usado, resultando em comportamento inesperado.

## <a name="applying-spherical-environment-maps"></a>Aplicando o ambiente esférico Mapas

Você aplica um mapa de ambiente a objetos da mesma maneira que para qualquer outra textura, definindo a textura para o estágio de textura apropriado com o [**método IDirect3DDevice9::SetTexture.**](/windows/desktop/api) De definir o primeiro parâmetro como o índice para o estágio de textura desejado e definir o segundo parâmetro como o endereço da interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) retornado quando você criou a textura para o mapa de ambiente. Você pode definir a cor e as operações e os argumentos de mesclagem alfa conforme necessário para obter os efeitos desejados de mesclagem de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de ambiente](environment-mapping.md)
</dt> </dl>

 

 

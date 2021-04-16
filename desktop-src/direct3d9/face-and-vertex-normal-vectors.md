---
description: Cada face em uma malha tem um vetor normal de unidade perpendicular, conforme mostrado na ilustração a seguir.
ms.assetid: 86e2a460-7b58-4612-8f72-5a4e864ceb58
title: Vetores normais de face e vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0ef6fd8eba85b770cbfe71477655ddbafd8ee7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550093"
---
# <a name="face-and-vertex-normal-vectors-direct3d-9"></a>Vetores normais de face e vértice (Direct3D 9)

Cada face em uma malha tem um vetor normal de unidade perpendicular, conforme mostrado na ilustração a seguir. Direção do vetor é determinada pela ordem em que os vértices são definidos, e se o sistema de coordenadas é orientado à direita ou esquerda. A face normal aponta para longe do lado frontal da face. No Direct3D, somente a frente de um rosto fica visível. Uma face frontal é aquela na qual os vértices estão definidos em ordem no sentido horário.

![ilustração de um vetor normal para uma face frontal](images/nrmlvect.png)

Qualquer face que não é uma face frontal é uma face traseira. O Direct3D nem sempre renderiza faces de volta; Portanto, os faces posteriores são considerados como sendo escolhidos. Você pode alterar o modo de remoção para renderizar faces traseiras se desejar. Consulte [estado de remoção (Direct3D 9)](culling-state.md) para obter mais informações.

O Direct3D usa as normais de unidade de vértice para os efeitos de sombreamento Gouraud, iluminação e texturização. A ilustração a seguir mostra os exemplos normais.

![ilustração de Normals de vértice](images/vertnrml.png)

Ao aplicar o sombreamento Gourard em um polígono, o Direct3D usa as normais de vértice para calcular o ângulo entre a fonte de luz e a superfície. Ele calcula os valores de cor e intensidade para os vértices e os interpola para cada ponto entre todas as superfícies do primitivo. O Direct3D calcula o valor de intensidade de luz, usando o ângulo. Quanto maior o ângulo, menos a luz chega à superfície.

Se você estiver criando um objeto simples, defina o vértice Normals como ponto perpendicular à superfície, conforme mostrado na ilustração a seguir.

![ilustração de uma superfície plana composta de dois triângulos com o vértice Normals](images/flatvert.png)

No entanto, é mais provável que seu objeto seja composto de faixas de triângulo e os triângulos não sejam coplanars. Uma maneira simples de alcançar o sombreamento suave entre todos os triângulos na faixa é primeiro calcular o vetor normal de superfície para cada face poligonal à qual o vértice está associado. A normal de vértice pode ser definida para fazer um ângulo igual com cada superfície normal. No entanto, esse método talvez não seja eficiente o suficiente para primitivos complexos.

Esse método é ilustrado pelo diagrama a seguir, que mostra duas superfícies, S1 e S2 vistas a partir de cima. Os vetores normais de S1 e S2 são mostrados em azul. O vetor normal de vértice é mostrado em vermelho. O ângulo que o vetor normal de vértice faz com a superfície normal de S1 é igual ao ângulo entre a normal de vértice e a normal de superfície de S2. Quando essas duas superfícies são iluminadas e sombreadas com sombreamento Gouraud, o resultado é uma borda suavemente sombreada, suavemente arredondada entre eles.

![diagrama de duas superfícies (S1 e S2) e seus vetores normais e vetor normal de vértice](images/gvert.png)

Se a normal de vértice estiver em direção a uma das faces com a qual ela está associada, ela fará com que a intensidade de luz aumente ou diminua para os pontos nessa surface, dependendo do ângulo que ela faz com a fonte de luz. O diagrama a seguir mostra um exemplo. Novamente, essas superfícies são vistas como Edge-on. A normal de vértice está na direção C1, fazendo com que ela tenha um ângulo menor com a fonte de luz do que se a normal de vértice tivesse ângulos iguais com as normais de superfície.

![diagrama de duas superfícies (S1 e S2) com um vetor normal de vértice que se inclina em direção a uma face](images/gvert2.png)

Você pode usar o sombreamento Gouraud para exibir alguns objetos em uma cena 3D com bordas afiadas. Para fazer isso, duplique os vetores normais de vértice em qualquer interseção de faces em que uma borda nítida é necessária, conforme mostrado na ilustração a seguir.

![ilustração de vetores normais de vértice duplicados em bordas nítidas](images/shade1.png)

Se você usar os métodos DrawPrimitive para renderizar a cena, defina o objeto com bordas afiadas como uma lista de triângulos, em vez de uma faixa de triângulos. Quando você define um objeto como uma faixa triangular, o Direct3D trata isso como um único polígono composto de várias faces triangulares. O sombreamento Gouraud é aplicado em cada face do polígono e entre as faces adjacentes. O resultado é um objeto que é suavemente sombreado de face para face. Como uma lista de triângulos é um polígono composto de uma série de faces triangulares separadas, o Direct3D aplica o sombreamento Gouraud em cada face do polígono. No entanto, ele não é aplicado de face para face. Se dois ou mais triângulos de uma lista de triângulos forem adjacentes, eles aparentam ter uma borda afiada entre eles.

Outra alternativa é alterar para o sombreamento simples ao renderizar objetos com bordas afiadas. Computacionalmente, este é o método mais eficiente, mas isso resultar em objetos na cena que não são renderizados de forma tão realista quanto os objetos que estão com sombreamento Gouraud.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coordenar sistemas e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 




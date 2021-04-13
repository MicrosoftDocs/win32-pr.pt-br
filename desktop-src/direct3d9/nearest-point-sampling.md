---
description: Os apps não são obrigados a usar filtragem de textura.
ms.assetid: bba0e485-ac5a-4e43-9eb7-25cd0c90d316
title: Amostragem de Nearest-Point (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11cf98ee917b124b35f3c30ff263365ec3c46e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370185"
---
# <a name="nearest-point-sampling-direct3d-9"></a>Amostragem de Nearest-Point (Direct3D 9)

Os apps não são obrigados a usar filtragem de textura. O Direct3D pode ser definido para calcular o endereço de texel, que geralmente não avalia como inteiros e copia a cor de texel com o endereço inteiro mais próximo. Esse processo é chamado de amostragem do ponto mais próximo. Isso pode ser uma maneira rápida e eficiente de processar texturas se o tamanho da textura for semelhante ao tamanho da imagem primitiva na tela. Caso contrário, a textura deve ser ampliada ou minificada. O resultado pode ser uma imagem em partes, com alias ou borrada.

Seu aplicativo C++ pode selecionar a amostragem de ponto mais próximo chamando o método [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Defina o valor do primeiro parâmetro como o número de índice inteiro (0-7) da textura para a qual você está selecionando um método de filtragem de textura. Pass D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER para o segundo parâmetro para definir o filtro de ampliação, minificação ou mipmapping. Passe D3DTEXF \_ Point no terceiro parâmetro.

Você deve usar a amostragem de ponto mais próximo com cuidado, pois pode, às vezes, causar artefatos gráficos quando a textura é amostrada no limite entre duas texels. Esse limite é a posição ao longo da textura (u ou v) em que as transições de texel amostradas fazem as transições de um texel para o próximo. Quando a amostragem de pontos é usada, o sistema escolhe uma amostra texel ou a outra, e o resultado pode mudar abruptamente de um texel para o outro à medida que o limite é ultrapassado. Esse efeito pode aparecer como artefatos gráficos indesejados na textura exibida. Quando a filtragem linear for usada, o texel resultante é calculado a partir de ambos os texels adjacentes e se combina perfeitamente entre eles à medida que o índice de textura percorre o limite.

Esse efeito pode ser observado ao mapear uma textura muito pequena para um polígono muito grande: uma operação geralmente chamada de ampliação. Por exemplo, ao usar uma textura que se parece com um quadriculado, o exemplo de ponto mais próximo resulta em um quadriculado maior com bordas distintas. Por outro lado, a filtragem de textura linear resulta em uma imagem em que o quadriculado varia no polígono.

Na maioria dos casos, os apps recebem os melhores resultados ao evitar o exemplo de ponto mais próximo sempre que possível. A maioria do hardware atual é otimizado para filtragem linear, portanto, o app não deve ter o desempenho prejudicado. Se o efeito desejado exigir o uso do exemplo de ponto próximo, como ao usar texturas para exibir caracteres de texto legível, então o app deve ter cuidado para evitar a amostragem nos limites de texel, o que pode resultar em efeitos indesejados. A ilustração a seguir mostra a possível aparência desses artefatos.

![ilustração de uma caixa divididas em seções seis com linhas horizontais não contínuas nos dois quadrados superiores à direita](images/ptrtfct.png)

Observe que os dois quadrados no canto superior direito do grupo parecem diferentes de seus vizinhos, com deslocamentos diagonais sendo executados por meio deles. Para evitar artefatos gráficos como estes, você deve estar familiarizado com as regras de amostragem de textura do Direct3D para filtragem do ponto mais próximo. O Direct3D mapeia uma coordenada de textura de ponto flutuante, variando de \[ 0,0, 1,0 \] (0,0 a 1,0, inclusive) para um valor de espaço Texel inteiro que varia de \[ -0,5, n-0,5 \] , em que n é o número de texels em uma determinada dimensão na textura. O índice de textura resultante é arredondado para o inteiro mais próximo. Esse mapeamento pode introduzir imprecisões de amostragem nos limites de texel.

Para um exemplo simples, imagine um aplicativo que renderiza polígonos com o modo de \_ endereçamento de textura D3DTADDRESS Wrap. Usando o mapeamento empregado por Direct3D, o índice de textura u é mapeado como mostrado no diagrama a seguir para uma textura com 4 texels de largura.

![diagrama de coordenadas de textura 0,0 e 1,0 no limite entre texels](images/ptsmpprb.png)

Observe que as coordenadas de textura, 0,0 e 1,0 para esta ilustração, estão exatamente no limite entre texels. Usando o método pelo qual o Direct3D mapeia valores, a textura coordena o intervalo de \[ -0,5, 4-0,5 \] , em que 4 é a largura da textura. Nesse caso, a amostra de texel é o texel 0 para um índice de textura de 1,0. No entanto, se a coordenada de textura foi somente um pouco menor do que 1,0, a amostra de texel seria o texel n em vez do texel 0.

A implicação disso é que ao ampliar uma pequena textura usando coordenadas de textura de 0,0 e 1,0 com filtragem de ponto mais próximo ponto triângulo alinhado no espaço da tela resulta em pixels para os quais é feita a amostragem do mapa de textura com o limite entre texels do limite. Qualquer imprecisões no cálculo de coordenadas de textura, porém pequenos, resulta em artefatos ao longo as áreas em que a imagem renderizada que correspondem até as bordas de texel do mapa de textura.

O mapeamento de coordenadas de textura de ponto flutuante em texels inteiros com precisão é difícil, requer tempo para os cálculos e, em geral, não é necessário. A maioria das implementações de hardware usa uma abordagem iterativa para calcular as coordenadas de textura em cada local de pixel em um triângulo. As abordagens iterativas tendem a ocultar esses imprecisões porque os erros são acumulados de modo uniforme durante a iteração.

O rasterizador de referência do Direct3D usa uma abordagem de avaliação direta para o cálculos dos índices de textura em cada local de pixel. A avaliação direta difere da abordagem iterativa em que qualquer imprecisão na operação apresenta uma distribuição de erro mais aleatória. O resultado é que os erros de amostragem nos limites podem ser mais perceptíveis, pois o rasterizador de referência não executa essa operação com precisão.

A melhor abordagem é usar a filtragem de ponto mais próximo somente quando necessário. Quando for necessário deve usá-la, é recomendável deslocar as coordenadas de textura das posições de limite para evitar artefatos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtragem de textura](texture-filtering.md)
</dt> </dl>

 

 

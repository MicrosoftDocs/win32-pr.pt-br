---
description: Em resumo, a quebra de textura altera a maneira básica que o Direct3D rasteriza polígonos texturizado usando as coordenadas de textura especificadas para cada vértice.
ms.assetid: 00683d3f-3e3c-4ee4-9aec-a0d7fd9c8941
title: Quebra de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c29ebe78bcfa237f46eacb247432185adedd1e53ae0774e767807269bb3bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984711"
---
# <a name="texture-wrapping-direct3d-9"></a>Quebra de textura (Direct3D 9)

Em resumo, a quebra de textura altera a maneira básica que o Direct3D rasteriza polígonos texturizado usando as coordenadas de textura especificadas para cada vértice. Durante a rasterização de um polígono, o sistema faz a interpolação entre as coordenadas de textura em cada um dos vértices do polígono para determinar os texels que devem ser usados para cada pixel do polígono. Normalmente, o sistema trata a textura como um plano 2D, interpolando novos texels pegando a rota mais curta do ponto A de uma textura ao ponto B. Se o ponto A representar a posição u, v (0.8, 0.1) e o ponto B estiver em (0.1,0.1), a linha de interpolação terá a aparência do diagrama a seguir.

![diagrama de uma linha de interpolação entre dois pontos](images/interp1.png)

Observe que a distância mais curta entre A e B nesta ilustração passa basicamente pelo meio da textura. Habilitar o encapsulamento das coordenadas de textura u ou textura v muda a forma como o Direct3D identifica a rota mais curta entre as coordenadas de textura na direção u e na direção v. Por definição, o encapsulamento de textura faz com que o rasterizador pegue a rota mais curta entre os conjuntos de coordenadas de textura, presumindo que 0.0 e 1.0 sejam coincidentes. O último bit é a parte complicada: você pode imaginar que habilitar o encapsulamento de textura em uma direção faz com que o sistema trate uma textura como se estivesse encapsulada em um cilindro. Por exemplo, considere o seguinte diagrama:

![diagrama de uma textura e dois pontos encapsulados em um cilindro](images/interp2.png)

A ilustração anterior mostra como o encapsulamento na direção u afeta a forma como o sistema interpola as coordenadas de textura. Usando os mesmos pontos do exemplo para texturas normais, ou não encapsuladas, você pode ver que a rota mais curta entre os pontos A e B não está mais no meio da textura; agora está na borda em que 0.0 e 1.0 coexistem. O encapsulamento na direção v é similar, exceto que ele encapsula a textura em torno de um cilindro disposto de lado. O encapsulamento na direção u e na direção v é mais complexo. Nessa situação, você pode imaginar a textura como uma tora ou rosca.

A aplicação prática mais comum do encapsulamento de textura é executar o mapeamento do ambiente. Geralmente, um objeto texturizado com um mapa do ambiente parece muito refletivo, mostrando uma imagem espelhada dos arredores do objeto na cena. Para o âmbito desta discussão, imagine uma sala com quatro paredes, cada uma delas pintada com uma letra R, G, B, Y e as cores correspondentes: vermelho, verde, azul e amarelo. O mapa do ambiente para essa sala simples pode se parecer com a ilustração a seguir.

![ilustração de faixas verticais de vermelho, verde, azul e amarelo](images/envmap.png)

Imagine que o teto da sala seja sustentado por um pilar quadrilátero perfeitamente refletivo. Mapear a textura do mapa do ambiente para o pilar é simples; fazer o pilar parecer que está refletindo as letras e as cores não é tão fácil. O diagrama a seguir mostra um esboço do pilar com as coordenadas de textura aplicáveis listadas próximo aos vértices superiores. A fenda onde o encapsulamento cruzará as bordas da textura é mostrada com uma linha pontilhada.

![diagrama de um retângulo com uma linha pontilhada bifurcada](images/seam.png)

Com o encapsulado habilitado na direção u, o pilar texturizado mostra as cores e os símbolos do mapa do ambiente adequadamente e, na fenda na frente da textura, o rasterizador escolhe corretamente a rota mais curta entre as coordenadas de textura, presumindo que as coordenadas u 0.0 e 1.0 compartilhem o mesmo local. O pilar texturizado se parece com a ilustração a seguir.

![ilustração de um pilar que consiste em quadrantes nas cores vermelho, verde, azul e amarelo](images/tex-seam.png)

Se o encapsulamento de textura não estiver habilitado, o rasterizador não fará a interpolação na direção necessária para gerar uma imagem refletida verossímil. Em vez disso, a área na frente do pilar contém uma versão compactada horizontalmente dos texels entre as coordenadas u 0.175 e 0.875, pois passam pelo centro da textura. O efeito de encapsulamento está arruinado.

## <a name="using-texture-wrapping"></a>Usando a quebra de textura

Para habilitar a quebra de textura, chame o método [**IDirect3DDevice9::SetRenderState,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) conforme mostrado no exemplo de código abaixo.


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



O primeiro parâmetro aceito por [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) é um estado de renderização a ser definido. Especifique um dos valores enumerados D3DRS \_ WRAP0 a D3DRS WRAP7 que especificam para qual nível de textura \_ definir o wrap. Especifique os sinalizadores D3DWRAPCOORD 0 a \_ D3DWRAPCOORD 3 no segundo parâmetro para habilitar a quebra de textura na direção correspondente ou combiná-los para habilitar o empacotamento em várias \_ direções. Se você omitir um sinalizador, a quebra de textura na direção correspondente será desabilitada. Para desabilitar a quebra de textura para um conjunto de coordenadas de textura, de definido o valor para o estado de renderização correspondente como 0.

Não confunda encapsulamento de textura com os modos de endereçamento de textura de nomes similares. O encapsulamento de textura é executado antes do endereçamento de textura. Certifique-se de que os dados de quebra de textura não contenham nenhuma coordenada de textura fora do intervalo de \[ 0,0, 1,0 porque isso produzirá resultados \] indefinido. Para obter mais informações sobre o endereçamento de textura, consulte Modos de [endereçamento de textura (Direct3D 9)](texture-addressing-modes.md).

## <a name="displacement-map-wrapping"></a>Empacotamento do mapa de deslocamento

Os mapas de deslocamento são interpolados pelo mecanismo de mosaico. Como o modo de encapsulamento não pode ser especificado para o mecanismo de mosaico, o encapsulamento de textura não pode ser executado com mapas de deslocamento. Um aplicativo é capaz de usar um conjunto de vértices que força a interpolação para encapsular em qualquer direção. O aplicativo também pode especificar a interpolação para ser feita como uma simples interpolação linear.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas Direct3D](direct3d-textures.md)
</dt> </dl>

 

 

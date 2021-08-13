---
description: O exemplo PRTDemo e o simulador PRTCmdLine incluídos no SDK do DirectX representam vetores de transferência nos vértices de uma malha.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Representando o PRT com texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e827e24258d75a91aa75c9eb51ed6563d476ab16f75fedc31a7071bca28a4a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797912"
---
# <a name="representing-prt-with-textures-direct3d-9"></a>Representando o PRT com texturas (Direct3D 9)

O exemplo PRTDemo e o simulador PRTCmdLine incluídos no SDK do DirectX representam vetores de transferência nos vértices de uma malha. Para representar o sinal de PRT com precisão, isso pode exigir mosaicos que podem ser impraticável para jogos atuais. Representar vetores de transferência em mapas de textura é uma abordagem alternativa que tem o mesmo custo de dados independente da complexidade da malha. Há várias maneiras de gerar mapas de textura de vetor de transferência usando a biblioteca D3DX PRT.

## <a name="precomputing-transfer-vectors"></a>Computação de vetores de transferência

Uma abordagem seria modificar os exemplos de PRTDemo e PRTCmdLine para calcular um vetor de transferência a cada Texel em uma parametrização de uma superfície. Para fazer isso:

1.  Modifique a chamada para [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) para extrair coordenadas de textura da malha (ExtractUVs deve ser **true**)
2.  Substitua chamadas [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) com [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) usando o mesmo tamanho de textura.

Todos os métodos ID3DXPRTEngine funcionam com simulações por Texel, exceto para: ComputeBounceAdaptive, ComputeSSAdaptive, Computess e ComputeDirectLightingSHAdaptive. Embora a simulação de espaço de textura gere o resultado correto, ela geralmente pode ser razoavelmente lenta, já que provavelmente estará computando os vetores de transferência em uma alta densidade.

Outra abordagem é computar uma simulação de PRT adaptável por vértice (com coordenadas de textura que serão usadas para os dados por Texel) e, em seguida, chamar [**ID3DXPRTEngine:: ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (usando um buffer de saída criado usando [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) na resolução apropriada). Isso funciona com toda a funcionalidade de PRT D3DX no SDK e, muitas vezes, pode ser muito mais eficiente do que a computação direta de um buffer de transferência por Texel.

## <a name="runtime-calculations"></a>Cálculos de tempo de execução

Se um único cluster for usado, os resultados poderão ser filtrados e não mapeados de MIP como qualquer outra textura e o sombreador de pixel será idêntico ao código do sombreador de vértice fornecido com PRTDemo.

Se a compactação gerar vários clusters, você não poderá filtrar ou mipmapr os dados porque os índices de clustering não são contínuos. Aqui estão algumas alternativas para lidar com dados de vários clusters:

-   Faça toda a filtragem no sombreador de pixel. Infelizmente, isso geralmente não é prático por motivos de desempenho.
-   Se as texturas forem texturas não incluídas em baixa resolução (isto é, mapas de luz), é mais provável que seja mais eficiente apenas calcular a iluminação diretamente no espaço de textura, onde não ocorrerá nenhuma filtragem e renderizar o objeto com uma textura sombreada. Isso é essencialmente um mapa claro dinâmico que é criado inteiramente na GPU.
-   Se um Atlas de textura for usado (consulte [usando o UVAtlas (Direct3D 9)](using-uvatlas.md)), você poderá clusterizar manualmente a cena fazendo com que todos os vetores de transferência em um componente conectado no espaço de textura estejam no mesmo cluster. Dessa forma, você pode filtrar a textura porque todas as texels acessadas estaria no mesmo cluster por meio da construção. A ID do cluster para uma face determinada pode ser propagada a partir do sombreador de vértice.

Os sombreadores de pixel têm muito menos registros constantes que não podem ser indexados, portanto, o sombreador de pixel é um pouco diferente do sombreador de vértice. Armazenar o trabalho por cluster em uma textura dinâmica de baixa resolução e usar cargas de textura seria a maneira mais eficiente de renderizar ao usar vários clusters.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferência de radiante preputada](precomputed-radiance-transfer.md)
</dt> <dt>

[Exemplo de demonstração de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)
</dt> <dt>

[Simulador de PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)
</dt> </dl>

 

 




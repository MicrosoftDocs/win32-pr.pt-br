---
description: Recursos do Direct3D 10,1
ms.assetid: e60c6116-e2f9-46b7-aed8-13e3e5ae2b90
title: Recursos do Direct3D 10,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99935941f60a984407c688e4ae67f0a125b0130d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764414"
---
# <a name="direct3d-101-features"></a>Recursos do Direct3D 10,1

O Direct3D 10,1 estende o conjunto de recursos do Direct3D 10,0 com os seguintes novos recursos:

-   Modos de mesclagem – modos de mesclagem independentes por destino de renderização usando a nova interface de estado de mesclagem (consulte a [**interface ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)). As operações de mesclagem de fonte dupla são restritas para processar o slot de destino 0; Você não pode gravar em outras saídas ou ter destinos de renderização ligados a slots que não sejam o slot 0.
-   Comportamento de remoção – rostos de área zero são automaticamente escolhidos; Isso afeta somente a renderização de wireframe.
-   Regras de ponto flutuante – usa as mesmas regras IEEE-754 para ponto flutuante, exceto as operações de ponto flutuante de 32 bits foram reforçadas para produzir um resultado dentro de 0,5 unidade-último local (0,5 ULP) do resultado infinitamente preciso. Isso se aplica a adição, subtração e multiplicação. (precisão de 0,5 ULP para multiplicar, 1,0 ULP para recíproco).
-   Formatos-a precisão da mistura de float16 aumentou para 0,5 ULP. A mesclagem também é necessária para os formatos UNORM16/SNORM16/SNORM8.
-   Suavização de multiamostragens-a multiamostragem foi aprimorada para generalizar a transparência baseada na cobertura e tornar o trabalho de várias amostras mais eficiente com a renderização multipassada. Para conseguir isso, todas as semânticas de multiamostragem são definidas como se o sombreador de pixel sempre for executado uma vez por amostra (frequência de amostragem), computando uma cor separada por amostra. Se um sombreador de pixel não usar nenhum atributo por amostra, ele calculará o mesmo valor para cada amostra coberta em um pixel. Nesse caso, é equivalente ao hardware que executa o sombreador uma vez por pixel (frequência de pixels), replicando o resultado para todos os exemplos abordados. Naturalmente, a execução com frequência de pixels sempre produz os mesmos resultados que a execução do mesmo sombreador em frequência de amostra, quando os atributos são amostrados em uma frequência de pixels. A estatística do pipeline PSInvocations é incrementada na frequência de amostragem, a menos que o sombreador esteja sendo executado em frequência de pixels.
-   Largura de banda do estágio do pipeline – aumentou a quantidade de dados que podem ser passados entre os estágios do sombreador: 

    | Recurso                        | Limites                    |
    |---------------------------------|---------------------------|
    | Registros entre os estágios do sombreador | 32 (32-bit x 4-Component) |
    | Registros de entrada do sombreador de vértice   | 32                        |
    | Slots de entrada do assembler de entrada     | 32                        |

    

     

-   Regras de rasterização – as regras para rasterização foram alteradas para linhas, além disso, uma nova funcionalidade foi adicionada.
    -   MultisampleEnable afeta apenas a rasterização de linha (pontos e triângulos não são afetados) e é usado para escolher um algoritmo de desenho de linha. Isso significa que não há mais suporte para algumas rasterização multiamostras do Direct3D 10.
    -   Nova execução de sombreador de pixel com frequência de exemplo com rasterização primitiva.
-   Resources – o CopyResource está habilitado em dois novos cenários:
    -   As superfícies de MSAA de cor e de profundidade/estêncil agora podem ser usadas com CopyResource como origem ou destino
    -   Conversão de formato ao copiar entre certos tipos de 32/64/128 bits preestruturados, recursos tipados e representações compactadas das mesmas larguras de bits.
-   Amostragem de textura – exemplos \_ c e exemplo \_ c \_ LZ instruções são definidas para trabalhar com Texture2DArrays e TextureCubeArrays, use o membro Location (o componente alfa) para especificar um índice de matriz.
-   Views-TextureCube e o novo TextureCubeArray (consulte [**d3d10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)) não são recursos reais, mas são novas exibições em um recurso Texture2DArray. Crie um modo de exibição de recurso de um recurso Texture2DArray com um novo sinalizador de uso (D3D10 \_ recurso \_ misc \_ TEXTURECUBE), use a nova interface de [**interface ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) para associar uma exibição de textura de cubo ao pipeline.

Os novos recursos exigem um tipo de dispositivo 10,1 (consulte a [**interface ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)) que pode ser criado chamando [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1)ou você pode criar o dispositivo e a cadeia de permuta ao mesmo tempo chamando [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1).

No Windows Vista Service Pack 1, as DLLs do Direct3D 10,0 e do Direct3D 10,1 existem lado a lado no sistema. Para acessar os recursos do 10,1, siga um destes procedimentos:

## <a name="accessing-101-features-on-vista-gold-and-vista-service-pack-1"></a>Acessando os recursos do 10,1 no Vista Gold e Vista Service Pack 1

Os desenvolvedores que desejarem dar suporte ao vista Gold, bem como ao SP1, precisarão considerar a falta das novas extensões de API 10,1 no Vista Gold. O DXUT e o D3DX10 fornecerão funções de conveniência para criar o dispositivo apropriado, com base nas DLLs disponíveis no sistema e no hardware disponível (10,0 ou 10,1). O dispositivo 10,1 herda do dispositivo 10,0 e pode ser recuperado usando QueryInterface (). É recomendável que cada aplicativo acompanhe o tipo de dispositivo e mantenha um ponteiro para o dispositivo 10,1 (se disponível) para evitar chamadas de QueryInterface frequentes quando a funcionalidade de 10,1 for desejada. Da mesma forma, em que 10,1 exibições de recursos e objetos de estado são associados a uma classe personalizada do aplicativo, é recomendável que o aplicativo rastreie se o objeto é um tipo 10,0 ou 10,1 para evitar chamadas de QueryInterface () redundantes. O D3DX10 inclui um conjunto de funções utilitárias para simplificar esse processo (consulte [**D3DX10CreateDevice**](d3dx10createdevice.md) e [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md)).

## <a name="accessing-101-features-on-vista-service-pack-1-exclusively"></a>Acessando os recursos do 10,1 no Vista Service Pack 1 exclusivamente

Alguns desenvolvedores podem optar por exigir o Vista Service Pack 1, que será distribuído amplamente aos usuários finais e inclui uma série de melhorias fora do Direct3D 10,1. Esses desenvolvedores podem usar exclusivamente os cabeçalhos e as bibliotecas do Direct3D 10,1, tomando uma dependência das DLLs do Direct3D 10,1 que dão suporte a hardware 10,0 e 10,1 (algumas chamadas podem falhar, no entanto, em dispositivos de 10,0 em que não há suporte para a nova funcionalidade).

Algumas observações adicionais:

-   As APIs expostas na D3DX10.dll aceitarão os dispositivos 10,0 e 10,1 e aproveitarão a funcionalidade 10,1 quando disponíveis.
-   D3D10SDKLayers.dll dá suporte a um dispositivo 10,1 e pode gerar o Spew de depuração apropriado para os recursos de 10,1.
-   D3D10Ref.dll implementa um dispositivo de software 10,0 e 10,1.
-   D3DX10 e FXC dão suporte ao modelo de sombreador 10,1 atualizado com os seguintes destinos: vs \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1 e FX \_ 4 \_ 1 que podem ser associados a um dispositivo 10,1. Um dispositivo 10,1 dá suporte A sombreadores de modelo 4,0 e 4,1 de sombreador.
-   No entanto, a estrutura de efeito do Direct3D 10,0 dá suporte a dispositivos 10,0 e 10,1. no entanto, qualquer técnica que inclua sombreadores do modelo do sombreador 4,1 ou os novos recursos do 10,1 deve usar um dispositivo 10,1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 




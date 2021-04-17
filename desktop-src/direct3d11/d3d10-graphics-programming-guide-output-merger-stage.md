---
title: Estágio de fusão de saída
description: O estágio de fusão de saída (OM) gera a cor de pixel renderizada final usando uma combinação de estado de pipeline, os dados de pixel gerados pelos sombreadores de pixel, o conteúdo dos destinos de renderização e o conteúdo dos buffers de profundidade/estêncil.
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- estágio de fusão de saída (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec77eaff506a0be87a3f0e98de691b50c27c0c3f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104366929"
---
# <a name="output-merger-stage"></a>Estágio de fusão de saída

O estágio de fusão de saída (OM) gera a cor de pixel renderizada final usando uma combinação de estado de pipeline, os dados de pixel gerados pelos sombreadores de pixel, o conteúdo dos destinos de renderização e o conteúdo dos buffers de profundidade/estêncil. O estágio OM é a etapa final para determinar quais pixels são visíveis (com o teste de estêncil de profundidade) e misturar as cores de pixel final.



|                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10: o Direct3D 9 implementa o teste alfa (usando o [estado de teste alfa](/windows/desktop/direct3d9/alpha-testing-state)) para controlar se um pixel é gravado em um destino de renderização de saída.<br/> O Direct3D 10 e superior não implementa um teste alfa (ou estado de teste alfa). Isso pode ser controlado usando um sombreador de pixel ou com funcionalidade de profundidade/estêncil.<br/> |



 

## <a name="depth-stencil-testing-overview"></a>Visão geral do teste de Depth-Stencil

Um buffer de estêncil de profundidade, que é criado como um recurso de textura, pode conter dados de profundidade e dados de estêncil. Os dados de profundidade são usados para determinar quais pixels ficam mais próximos da câmera e os dados de estêncil são usados para mascarar quais pixels podem ser atualizados. Por fim, tanto os dados de valores de profundidade e estêncil são usados pelo estágio de fusão de saída para determinar se um pixel deve ser desenhado ou não. O diagrama a seguir mostra conceitualmente como os testes de estêncil de profundidade são feitos.

![diagrama de como funciona o teste de estêncil de profundidade](images/d3d10-depth-stencil-test.png)

Para configurar o teste de estêncil de profundidade, consulte [Configuração da funcionalidade de estêncil de profundidade](d3d10-graphics-programming-guide-depth-stencil.md). Um objeto de estêncil de profundidade encapsula o estado de estêncil de profundidade. Um app pode especificar o estado de estêncil de profundidade, ou o estágio de OM usará valores padrão. Operações de mesclagem serão executadas de acordo com pixels se as várias amostras estiverem desabilitadas. Se as várias amostras estiverem habilitadas, a mesclagem ocorrerá de acordo com as várias amostragens.

O processo de usar o buffer de profundidade para determinar quais pixels devem ser desenhados é chamado de buffering de profundidade, também chamados de buffering z.

Depois que os valores de profundidade atingem o estágio de fusão de saída (seja vindo da interpolação ou de um sombreador de pixel), estarão sempre vinculados: z = min(Viewport.MaxDepth,max(Viewport.MinDepth,z)) de acordo com a formato/precisão do buffer de profundidade, usando as regras de ponto flutuante. Depois da vinculação, o valor de profundidade é comparado (usando DepthFunc) contra o valor existente do buffer de profundidade. Se nenhum buffer de profundidade estiver vinculado, o teste de profundidade sempre será aprovado.

Se não houver nenhum componente de estêncil em formato de buffer de profundidade, ou nenhum buffer de profundidade vinculado, então o teste de estêncil sempre será aprovado. Caso contrário, a funcionalidade não será alterada no Direct3D 9.

Somente um buffer de profundidade/estêncil pode estar ativo por vez; qualquer modo de exibição de recurso vinculado deve corresponder (mesmos tamanho e dimensões) ao modo de exibição de profundidade/estêncil. Isso não significa que o tamanho do recurso deve corresponder, basta que o tamanho da exibição corresponda.

Para obter mais informações sobre o teste de estêncil de profundidade, consulte o [tutorial 14](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="blending-overview"></a>Visão geral de mesclagem

A mesclagem combina um ou mais valores de pixel para criar uma cor de pixel final. O diagrama a seguir mostra o processo envolvido na mesclagem de dados de pixel.

![diagrama de como funciona a mesclagem de dados](images/d3d10-blend-state.png)

Conceitualmente, você pode visualizar esse gráfico de fluxo implementado duas vezes no estágio output-merger: o primeiro combina dados RGB, enquanto em paralelo, um segundo combina dados alfa. Para ver como usar a API para criar e definir o estado de mesclagem, consulte [Configurando a funcionalidade de mesclagem](d3d10-graphics-programming-guide-blend-state.md).

A mesclagem de função fixa pode ser habilitada independentemente para cada destino de renderização. No entanto, há apenas um conjunto de controles de mesclagem para que a mesma mesclagem seja aplicada a todos os RenderTargets com mesclagem habilitada. Valores de mesclagem (incluindo BlendFactor) sempre são vinculados ao intervalo do formato de destino de renderização antes da mesclagem. A vinculação é feita por destino de renderização, respeitando o tipo de destino de renderização. A única exceção é para os formatos float16, float11 ou float10, que não são vinculados para que as operações de mesclagem nesses formatos possam ser feitas com precisão/intervalo, no mínimo, igual ao formato de saída. NaNs e zeros assinados são propagados para todos os casos (incluindo pesos de mesclagem de 0,0).

Quando você usa destinos de renderização sRGB, o tempo de execução converte a cor do destino de renderização em espaço linear antes de realizar a mesclagem. O tempo de execução converte o valor mesclado final novamente em espaço de sRGB antes de salvar o valor de volta para o destino de renderização.



|                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10: no Direct3D 9, a mesclagem de funções fixas pode ser habilitada independentemente para cada destino de renderização.<br/> No Direct3D 10 e superior, há uma descrição de estado de mesclagem; Portanto, um valor de mesclagem pode ser definido para todos os destinos de renderização.<br/> |



 

### <a name="dual-source-color-blending"></a>Mesclagem de cores Dual-Source

Esse recurso permite que o estágio de mesclagem de saída use simultaneamente as saídas de sombreador de pixel (o0 e O1) como entradas para uma operação de mesclagem com o destino de renderização único no slot 0. As operações de mesclagem válidas incluem: adicionar, subtrair e revsubtract. As opções de Blend válidas para SrcBlend, DestBlend, SrcBlendAlpha ou DestBlendAlpha incluem: **D3D11 \_ Blend \_ SRC1 \_ Color**, **D3D11 \_ Blend \_ inv \_ SRC1 \_ Color**, **D3D11 \_ Blend \_ SRC1 \_ Alpha**, **D3D11 \_ Blend \_ inv \_ SRC1 \_ Alpha**. A equação de mesclagem e a máscara de gravação de saída especificam quais componentes são saída do sombreador de pixel. Componentes adicionais são ignorados.

A gravação para outras saídas de sombreador de pixel (o2, o3, etc.) são indefinidas; você não pode gravar em um destino de renderização não vinculado ao slot 0. Gravar oDepth é válido durante a mesclagem de cor de fonte dupla.

Para obter exemplos, consulte [mesclagem de saídas de sombreador de pixel](d3d10-graphics-programming-guide-blend-state.md).

## <a name="multiple-rendertargets-overview"></a>Visão geral de várias RenderTargets

Um sombreador de pixel pode ser usado para, no mínimo, 8 destinos de renderização diferentes, e todos devem ser do mesmo tipo (buffer, Texture1D, Texture1DArray e assim por diante). Além disso, todos os destinos de renderização devem ter o mesmo tamanho em todas as dimensões (largura, altura, profundidade, tamanho da matriz, contagens de amostra). Cada destino de renderização pode ter um formato de dados diferente.

Você pode usar qualquer combinação dos slots de destinos de renderização (até 8). No entanto, um modo de exibição de recurso não pode estar vinculado a vários slots de destino de renderização simultaneamente. Um modo de exibição poderá ser reutilizado, desde que os recursos não sejam usados simultaneamente.

## <a name="output-write-mask-overview"></a>Visão geral da máscara de Output-Write

Use uma máscara de gravação de saída para controlar (por componente) quais dados podem ser gravados em um destino de renderização.

## <a name="sample-mask-overview"></a>Visão geral da máscara de exemplo

Uma máscara de amostra é uma máscara de cobertura de várias amostras de 32 bits que determina quais amostras são atualizadas em destinos de renderização ativos. Apenas uma máscara de amostra é permitida. O mapeamento de bits em uma máscara de amostra para as amostras em um recurso é definido pelo usuário. Para renderização de n amostras, os primeiros n bits (de LSB) da máscara de amostra são usados (32 bits é o número máximo de bits).


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                    | Descrição                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configurando Depth-Stencil funcionalidade](d3d10-graphics-programming-guide-depth-stencil.md)<br/> | Esta seção abrange as etapas para configurar o buffer de estêncil de profundidade e o estado de estêncil de profundidade para o estágio de fusão de saída.<br/>                                                                                                                           |
| [Configurando a funcionalidade de mesclagem](d3d10-graphics-programming-guide-blend-state.md)<br/>        | As operações de mesclagem são executadas em cada saída de sombreador de pixel (valor RGBA) antes que o valor de saída seja gravado em um destino de renderização. Se a multiamostragem estiver habilitada, a mesclagem será feita em cada multiamostra; caso contrário, a mesclagem será executada em cada pixel.<br/> |
| [Tendência de profundidade](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | Polígonos que são coplanar no espaço 3D podem ser feitos para aparecer como se não fossem coplanar adicionando um Bias z (ou uma tendência de profundidade) a cada um.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 


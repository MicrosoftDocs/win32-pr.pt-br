---
title: Como indexar várias saídas Fluxos
description: No modelo de sombreador 5, um sombreador de geometria pode dar suporte a até 4 fluxos separados. Isso significa que um único sombreador pode ser produzido entre um e quatro fluxos de saída, dependendo do número de fluxos declarados.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37aefd8b7cdcab05515bda6f81fa6c679751dc95
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473392"
---
# <a name="how-to-index-multiple-output-streams"></a>Como indexar várias saídas Fluxos

No modelo de sombreador 5, um sombreador de geometria pode dar suporte a até 4 fluxos separados. Isso significa que um único sombreador pode ser produzido entre um e quatro fluxos de saída, dependendo do número de fluxos declarados.

Para indexar vários fluxos de saída

1.  Defina um fluxo de dados usando um tipo de modelo de fluxo.

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  Defina um segundo fluxo de dados usando um tipo de modelo de fluxo.

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  Dados de saída para fluxos (ou ambos) usando as funções intrínsecas do objeto de saída de fluxo (como Append ou RestartStrip).

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

Ao usar um único fluxo de saída, você pode emitir faixas de triângulo, faixas de linha ou listas de pontos. Quando você armazena as faixas de triângulo e linha no buffer de saída do fluxo, elas são expandidas para listas de triângulos e linhas, respectivamente. Você também pode rasterizar um fluxo e não enviá-lo para um buffer de memória.

Ao usar vários fluxos de saída, todos os fluxos devem conter pontos e até um fluxo de saída pode ser enviado para o rasterizador. Mais comumente, um aplicativo não rasterizará nenhum fluxo.

Depois de transmitir dados para um buffer, você pode usar esses dados para renderizar qualquer tipo primitivo, não apenas o tipo primitivo usado para preencher o buffer.

A saída total do sombreador de geometria é limitada a 1024 escalares. Quando existem vários fluxos, o número de escalares é calculado do maior tipo de fluxo multiplicado pela contagem máxima de vértices.




| | | Diferenças entre o modelo de sombreador 4 e o modelo de sombreador 5:<br /> Modelo de sombreador 4:<br /><ul><li>O número máximo de escalares para a saída de fluxo é 64.</li><li>A máscara de registro por componente deve corresponder ao intervalo de índice.</li></ul>Modelo de sombreador 5:<br /><ul><li>O número máximo de escalares para a saída de fluxo é 128.</li><li>A máscara de registro por componente não precisa corresponder no intervalo de índice.</li><li>A indexação dinâmica de saídas deve ser legal em todos os fluxos.</li><li>Os modos de interpolação não precisam corresponder aos fluxos.</li></ul> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de sombreador de geometria](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 






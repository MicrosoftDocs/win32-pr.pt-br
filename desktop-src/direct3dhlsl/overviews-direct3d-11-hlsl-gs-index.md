---
title: Como indexar vários fluxos de saída
description: No sombreador modelo 5, um sombreador Geometry pode dar suporte a até quatro fluxos separados. Isso significa que um único sombreador pode gerar uma saída entre um e quatro fluxos de saída, dependendo do número de fluxos declarados.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004991"
---
# <a name="how-to-index-multiple-output-streams"></a>Como: indexar vários fluxos de saída

No sombreador modelo 5, um sombreador Geometry pode dar suporte a até quatro fluxos separados. Isso significa que um único sombreador pode gerar uma saída entre um e quatro fluxos de saída, dependendo do número de fluxos declarados.

Para indexar vários fluxos de saída

1.  Defina um fluxo de dados usando um tipo de modelo de fluxo.

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  Defina um segundo fluxo de dados usando um tipo de modelo de fluxo.

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  Dados de saída para (ou ambos) fluxos usando as funções intrínsecas do objeto de saída de fluxo (como Append ou RestartStrip).

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

    

Ao usar um único fluxo de saída, você pode emitir faixas de triângulo, faixas de linha ou listas de pontos. Quando você armazena as faixas de triângulo e de linha no buffer de saída de fluxo, elas são expandidas para listas de linhas e triângulos, respectivamente. Você também pode rasterizar um fluxo e não enviá-lo para um buffer de memória.

Ao usar vários fluxos de saída, todos os fluxos devem conter pontos e até um fluxo de saída pode ser enviado para o rasterizador. Mais comumente, um aplicativo não rasterizará nenhum fluxo.

Depois de transmitir dados para um buffer, você pode usar esses dados para renderizar qualquer tipo primitivo, não apenas o tipo primitivo que você usou para preencher o buffer.

A saída total do sombreador Geometry é limitada a 1024 escalares. Quando há vários fluxos, o número de escalares é computado do maior tipo de fluxo multiplicado pela contagem máxima de vértices.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferenças entre o modelo de sombreador 4 e o modelo de sombreador 5:<br/> Modelo do sombreador 4:<br/>
<ul>
<li>O número máximo de escalares para a saída do fluxo é 64.</li>
<li>A máscara de registro por componente deve corresponder ao intervalo de índice.</li>
</ul>
Modelo do sombreador 5:<br/>
<ul>
<li>O número máximo de escalares para a saída do fluxo é 128.</li>
<li>A máscara de registro por componente não precisa corresponder ao intervalo de índice.</li>
<li>A indexação dinâmica de saídas deve ser válida em todos os fluxos.</li>
<li>Os modos de interpolação não precisam corresponder aos fluxos.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do sombreador de geometria](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 






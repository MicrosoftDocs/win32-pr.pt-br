---
title: Estágio de Stream-Output
description: A finalidade do estágio Stream-output é gerar continuamente (ou transmitir) dados de vértice do estágio Geometry-Shader (ou o estágio Vertex-Shader se o estágio Geometry-Shader estiver inativo) em um ou mais buffers na memória (consulte Introdução com o estágio Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- estágio de saída de fluxo (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f630208b60b107b211f8bb6f6ee0f1efac3ed736c96756dbe1e95e24032b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538570"
---
# <a name="stream-output-stage"></a>Estágio de Stream-Output

A finalidade do estágio Stream-output é gerar continuamente (ou transmitir) dados de vértice do estágio Geometry-Shader (ou o estágio Vertex-Shader se o estágio Geometry-Shader estiver inativo) em um ou mais buffers na memória (consulte [introdução com o estágio Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).

O estágio Stream-Output (por isso) está localizado no pipeline logo após o estágio Geometry-Shader e logo antes do estágio de rasterização, conforme mostrado no diagrama a seguir.

![diagrama da localização do estágio de saída de fluxo no pipeline](images/d3d10-pipeline-stages-so.png)

Os dados transmitidos para a memória podem ser lidos de volta no pipeline em uma passagem de renderização subsequente, ou podem ser copiados para um recurso de preparo (para que possam ser lidos pela CPU). A quantidade de dados transmitidos pode variar; a API [**ID3D11DeviceContext::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) foi projetada para lidar com os dados sem a necessidade de consultar (a GPU) sobre a quantidade de dados gravados.

Quando um triângulo ou uma faixa de linha está associado ao estágio de Assembler de entrada, cada faixa é convertida em uma lista antes de ser transmitida. Os vértices são sempre escritos como primitivos completos (por exemplo, três vértices por vez para triângulos); primitivos incompletos nunca são transmitidos. Tipos primitivos com adjacência descartam os dados de adjacência antes de transmitir os dados.

Há duas maneiras de fornecer dados de saída de fluxo para o pipeline:

-   Os dados de saída de fluxo podem ser devolvidos para o estágio de Assembler de entrada.
-   Os dados de saída de fluxo podem ser lidos por sombreadores programáveis usando funções de carga (como [carga](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).

Para usar um buffer como um recurso de saída de fluxo, crie o buffer com o sinalizador de [**\_ saída do \_ fluxo \_ de associação D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) . O estágio de saída de fluxo dá suporte a até 4 buffers simultaneamente.

-   Se você estiver transmitindo dados em vários buffers, cada buffer pode capturar apenas um único elemento (até 4 componentes) de dados por vértice, com uma distância de dados implícita igual à largura do elemento em cada buffer (compatível com a maneira como os buffers de elemento único podem ser vinculados para a entrada em estágios de sombreador). Além disso, se os buffers tiverem tamanhos diferentes, a escrita é interrompida assim que qualquer um dos buffers estiver cheio.
-   Se você estiver transmitindo dados em um único buffer, o buffer pode capturar até 64 componentes escalares de dados por vértice (256 bytes ou menos) ou a distância de vértice pode ser de até 2048 bytes.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                               | Descrição                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Introdução com o estágio de Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | Esta seção descreve como usar um sombreador de geometria com o estágio de saída de fluxo.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 


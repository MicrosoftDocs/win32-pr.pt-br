---
title: Exemplos de trabalhos
description: Os exemplos de trabalho estão disponíveis para download, mostrando o uso de vários recursos do Direct3D 12.
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6f8bad1d20729f4caa78952feda22378ad37526b33b668e79260ef9658da53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631876"
---
# <a name="working-samples"></a>Exemplos de trabalhos

Os exemplos de trabalho estão disponíveis para download, mostrando o uso de vários recursos do Direct3D 12.

## <a name="working-samples"></a>Exemplos de trabalho

os exemplos de trabalho (na forma de projetos Visual Studio 2015) podem ser baixados de [GitHub/Microsoft/DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples).

> [!Note]  
> A lista exata de exemplos disponíveis neste local varia conforme os exemplos são adicionados e atualizados.

 



<table>
<thead>
<tr class="header">
<th>Titulo do exemplo</th>
<th>Descrição</th>
<th>Desktop</th>
<th>UWP</th>
<th>Passo a passo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HelloWorld<dl> HelloWindow<br />
HelloTriangle<br />
HelloBundles<br />
HelloConstBuffers<br />
HelloTexture<br />
</dl></td>
<td>O conjunto de amostras HelloWorld contém os seguintes projetos simples para ajudá-lo a começar a usar o Direct3D 12.<dl> Cria uma janela na preparação da renderização do conteúdo do Direct3D 12.<br />
Renderiza um triângulo simples usando o Direct3D 12.<br />
Demonstra o uso de um pacote para renderização usando o Direct3D 12.<br />
Demonstra como usar buffers de constantes para passar dados para a GPU usada para renderização no Direct3D 12.<br />
Demonstra como aplicar uma textura a um triângulo usando o Direct3D 12.<br />
</dl></td>
<td>Y</td>
<td>Y</td>
<td><a href="creating-a-basic-direct3d-12-component.md">Criando um componente básico do Direct3D 12</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>Demonstra as práticas recomendadas de buffer e sincronização de quadros, bem como o processamento de uma malha simples usando pacotes.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>Um exemplo de como criar um aplicativo com capacidade para vários threads.</td>
<td>Y</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyGravity</td>
<td>Demonstra como o Multi-Engine pode ser usado para fazer o trabalho de computação assíncrona juntamente com o trabalho 3D na mesma GPU.</td>
<td>Y</td>
<td>Y</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">Simulação de gravidade de n-corpos de vários mecanismos</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>Demonstra a remoção de oclusão usando heaps de consulta e predicação.</td>
<td>Y</td>
<td>Y</td>
<td><a href="predication-queries.md">Consultas de predicação</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>Demonstra os recursos de indexação dinâmica do DirectX 12 e do HLSL.</td>
<td>Y</td>
<td>Y</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">Indexação dinâmica usando HLSL 5.1</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>Demonstra o uso básico da camada 11on12. Este exemplo renderiza o texto usando D2D usando a API do Direct3D 11 em um dispositivo 11on12 do Direct3D 12.</td>
<td>Y</td>
<td>Y</td>
<td><a href="d2d-using-d3d11on12.md">O D2D usando o D3D11on12</a></td>
</tr>
<tr class="even">
<td>D3D12ExecuteIndirect</td>
<td>Demonstra a remoção do mecanismo de computação em conjunto com o recurso de execução indireta para processar somente objetos que passam no teste de remoção.</td>
<td>Y</td>
<td>Y</td>
<td><a href="indirect-drawing-and-gpu-culling-.md">Seleção indireta de GPU e desenho</a></td>
</tr>
<tr class="odd">
<td>D3D12PipelineStateCache</td>
<td>Demonstra o cache do PSO (objeto de estado de pipeline).</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12Fullscreen</td>
<td>Demonstra como lidar com tela inteira para transições em janela e redimensionamento de janela no DirectX 12.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12HeterogeneousMultiadapter</td>
<td>Demonstra como compartilhar cargas de trabalho entre várias GPUs heterogêneas usando heaps compartilhados.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>Demonstra o uso de recursos reservados (com lado). Neste exemplo, um quádruplo é texturizado com um recurso reservado que contém uma cadeia MIP completa.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>Isso é destinado como uma solução de baixo custo de integração para gerenciar heaps e recursos confirmados do Direct3D 12, usando técnicas de gerenciamento de memória do Direct3D 11.</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>Demonstra o uso de recursos pequenos posicionados, mostrando as possíveis economias de memória obtidas com o uso de recursos inseridos (com um alinhamento de 4K) sobre os recursos confirmados e reservados (com um alinhamento de 64K).</td>
<td>Y</td>
<td>Y</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Guia detalhado do código D3D12](d3d12-code-walk-throughs.md)
</dt> </dl>

 

 





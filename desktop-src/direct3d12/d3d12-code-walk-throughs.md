---
title: Walk-Throughs de código D3D12
description: Esta seção fornece código para cenários de exemplo. Muitos dos passo-a-passo fornecem detalhes sobre qual codificação deve ser adicionada a um exemplo básico, para evitar a repetição do código de componente básico para cada cenário.
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdea9b519e2a0adac9dc346d6bee455af0018da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103942"
---
# <a name="d3d12-code-walk-throughs"></a>Walk-Throughs de código D3D12

Esta seção fornece código para cenários de exemplo. Muitos dos passo-a-passo fornecem detalhes sobre qual codificação deve ser adicionada a um exemplo básico, para evitar a repetição do código de componente básico para cada cenário.

Para o componente mais básico, consulte a seção [criando um componente básico do Direct3D 12](creating-a-basic-direct3d-12-component.md) . Os passo a passo a seguir descrevem cenários mais avançados.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [D2D usando D3D11on12](d2d-using-d3d11on12.md)<br/>                                       | O exemplo **D3D1211on12** demonstra como renderizar conteúdo D2D sobre conteúdo D3D12 compartilhando recursos entre um dispositivo baseado em 11 e um dispositivo baseado em 12. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Simulação de gravidade n-Body de vários mecanismos](multi-engine-n-body-gravity-simulation.md)<br/> | O exemplo **D3D12nBodyGravity** demonstra como fazer o trabalho de computação de forma assíncrona. O exemplo gira um número de threads cada um com uma fila de comando de computação e agenda o trabalho de computação na GPU que executa uma simulação de gravidade de n-corpo. Cada thread opera em dois buffers cheios de posição e dados de velocidade. Com cada iteração, o sombreador de computação lê a posição atual e os dados de velocidade de um buffer e grava a próxima iteração no outro buffer. Quando a iteração é concluída, o sombreador de computação troca qual buffer é o SRV para ler dados de posição/velocidade e que é o UAV para gravar atualizações de posição/velocidade alterando o estado do recurso em cada buffer.<br/> |
| [Consultas do predicação](predication-queries.md)<br/>                                       | O exemplo **D3D12PredicationQueries** demonstra a remoção de oclusão usando heaps de consulta do DirectX 12 e predicação. O passo a passos descreve o código adicional necessário para estender o exemplo de **HelloConstBuffer** para manipular consultas predicação. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Indexação dinâmica usando HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)<br/>               | O exemplo **D3D12DynamicIndexing** demonstra alguns dos novos recursos do HLSL disponíveis no Shader Model 5,1 – especialmente a indexação dinâmica e matrizes não associadas – para renderizar a mesma malha várias vezes, sempre processando-a com um material selecionado dinamicamente. Com a indexação dinâmica, os sombreadores agora podem ser indexados em uma matriz sem saber o valor do índice no momento da compilação. Quando combinado com matrizes não associadas, isso adiciona outro nível de indireção e flexibilidade para autores de sombreador e pipelines de arte.<br/>                                                                                                                                                                                  |
| [Remoção indireta de desenho e GPU](indirect-drawing-and-gpu-culling-.md)<br/>            | O exemplo D3D12ExecuteIndirect demonstra como usar comandos indiretos para desenhar conteúdo. Ele também demonstra como esses comandos podem ser manipulados na GPU em um sombreador de computação antes de serem emitidos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Tutoriais de vídeo do DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
</dt> <dt>

[Código de exemplo na referência de D3D12](notes-on-example-code.md)
</dt> <dt>

[Exemplos de trabalho](working-samples.md)
</dt> </dl>

 

 






---
title: Guia detalhado do código D3D12
description: Esta seção fornece código para cenários de exemplo. Muitos dos passo a passo fornecem detalhes sobre qual codificação é necessária para ser adicionada a um exemplo básico, para evitar repetir o código de componente básico para cada cenário.
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fc076657d8a9096d1206adc9c61b6dc16fc95792dc0c0da2fcd636377b7ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497196"
---
# <a name="d3d12-code-walk-throughs"></a>Guia detalhado do código D3D12

Esta seção fornece código para cenários de exemplo. Muitos dos passo a passo fornecem detalhes sobre qual codificação é necessária para ser adicionada a um exemplo básico, para evitar repetir o código de componente básico para cada cenário.

Para o componente mais básico, consulte [a seção Criando um componente Básico do Direct3D 12.](creating-a-basic-direct3d-12-component.md) Os passo a passo a seguir descrevem cenários mais avançados.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [O D2D usando o D3D11on12](d2d-using-d3d11on12.md)<br/>                                       | O exemplo **D3D1211on12** demonstra como renderizar conteúdo D2D em conteúdo D3D12 compartilhando recursos entre um dispositivo baseado em 11 e um dispositivo baseado em 12. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Simulação de gravidade de n-corpos de vários mecanismos](multi-engine-n-body-gravity-simulation.md)<br/> | O **exemplo D3D12nBodyGravity** demonstra como fazer computação funcionar de forma assíncrona. O exemplo gira um número de threads cada um com uma fila de comandos de computação e agenda o trabalho de computação na GPU que executa uma simulação de gravidade de n corpo. Cada thread opera em dois buffers cheio de dados de posição e velocidade. Com cada iteração, o sombreador de computação lê os dados de posição e velocidade atuais de um buffer e grava a próxima iteração no outro buffer. Quando a iteração é concluída, o sombreador de computação troca qual buffer é o SRV para leitura de dados de posição/velocidade e que é o UAV para escrever atualizações de posição/velocidade alterando o estado do recurso em cada buffer.<br/> |
| [Consultas de predicação](predication-queries.md)<br/>                                       | O **exemplo D3D12PredicationQueries** demonstra a eliminação de oclusão usando heaps de consulta e predicação do DirectX 12. O passo a passo descreve o código adicional necessário para estender o **exemplo HelloConstBuffer** para lidar com consultas de pré-sindicalidade. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Indexação dinâmica usando HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)<br/>               | O exemplo **D3D12DynamicIndexing** demonstra alguns dos novos recursos HLSL disponíveis no Modelo de Sombreador 5.1 – particularmente indexação dinâmica e matrizes não unidas – para renderizar a mesma malha várias vezes, cada vez renderizar com um material selecionado dinamicamente. Com a indexação dinâmica, os sombreadores agora podem indexar em uma matriz sem saber o valor do índice em tempo de compilação. Quando combinadas com matrizes não associados, isso adiciona outro nível de indcisão e flexibilidade para autores de sombreador e pipelines de arte.<br/>                                                                                                                                                                                  |
| [Seleção indireta de GPU e desenho](indirect-drawing-and-gpu-culling-.md)<br/>            | O exemplo D3D12ExecuteIndirect demonstra como usar comandos indiretos para desenhar conteúdo. Ele também demonstra como esses comandos podem ser manipulados na GPU em um sombreador de computação antes de serem emitidos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Tutoriais de vídeo de aprendizado avançado do DirectX](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
</dt> <dt>

[Código de exemplo na referência D3D12](notes-on-example-code.md)
</dt> <dt>

[Exemplos de trabalhos](working-samples.md)
</dt> </dl>

 

 






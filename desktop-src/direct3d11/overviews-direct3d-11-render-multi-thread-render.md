---
title: Renderização imediata e adiada
description: O Direct3D 11 dá suporte a dois tipos de renderização imediato e adiado. Ambos são implementados usando a interface ID3D11DeviceContext.
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef954a8e794755e1405c8e1e07505a5f39189b03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988518"
---
# <a name="immediate-and-deferred-rendering"></a>Renderização imediata e adiada

O Direct3D 11 dá suporte a dois tipos de renderização: Immediate e adiada. Ambos são implementados usando a interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

## <a name="immediate-rendering"></a>Renderização imediata

A renderização imediata refere-se à chamada de APIs de renderização ou comandos de um dispositivo, que enfileira os comandos em um buffer para execução na GPU. Use um contexto imediato para renderizar, definir o estado do pipeline e reproduzir uma lista de comandos.

Crie um contexto imediato usando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="deferred-rendering"></a>Renderização adiada

A renderização adiada registra comandos gráficos em um buffer de comando para que eles possam ser reproduzidos em algum outro momento. Use um contexto adiado para gravar comandos (renderização e configuração de estado) em uma lista de comandos. A renderização adiada é um novo conceito no Direct3D 11; a renderização adiada é projetada para dar suporte à renderização em um thread durante a gravação de comandos para renderização em threads adicionais. Essa estratégia de multithread paralela permite dividir cenas complexas em tarefas simultâneas. Para obter mais informações sobre como renderizar cenas complexas, consulte [renderização de várias passagens](overviews-direct3d-11-render-multipass.md).

Crie um contexto adiado usando [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

O Direct3D gera sobrecarga de renderização ao enfileirar comandos no buffer de comandos. Por outro lado, uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) é executada de forma muito mais eficiente durante a reprodução. Para usar uma lista de comandos, registre os comandos de renderização com um contexto adiado e reproduza-os novamente usando um contexto imediato.

Você pode gerar apenas uma única lista de comandos em um modo de thread único. No entanto, você pode criar e usar vários contextos adiados simultaneamente, cada um em um thread separado. Em seguida, você pode usar esses vários contextos adiados para criar simultaneamente várias listas de comandos.

Não é possível reproduzir duas ou mais listas de comandos simultaneamente no contexto imediato.

Para determinar se um contexto de dispositivo é um contexto imediato ou adiado, chame [**ID3D11DeviceContext:: GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype).

O método [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) só tem suporte em um contexto adiado para recursos dinâmicos ([**D3D11 \_ uso \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) em que a primeira chamada na lista de comandos é o [**\_ \_ \_ descarte de gravação do mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). **D3D11 \_ Gravação de mapa \_ \_ não \_** há suporte para substituição em chamadas subsequentes, se disponíveis para o tipo de recurso fornecido.

As consultas em um contexto adiado são limitadas à geração de dados e ao desenho com predicado. Você não pode chamar [**ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) em um contexto adiado para obter dados sobre uma consulta; Você só pode chamar **GetData** no contexto imediato para obter dados sobre uma consulta. Você pode definir um predicado de renderização (um tipo de consulta) chamando [**D3D11DeviceContext:: SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) para usar os resultados da consulta na GPU. Você pode gerar dados de consulta por meio de chamadas para [**ID3D11DeviceContext:: Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) e [**ID3D11DeviceContext:: End**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end). No entanto, os dados da consulta não estarão disponíveis até que você chame [**ID3D11DeviceContext:: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) no contexto imediato para enviar a lista de comandos de contexto adiado. Os dados da consulta são então processados pela GPU.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Multithread](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 





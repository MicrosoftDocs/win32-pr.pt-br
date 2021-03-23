---
title: Direct3D 11 on 12
description: D3D11On12 é um mecanismo pelo qual os desenvolvedores podem usar interfaces e objetos do D3D11 para direcionar a API D3D12.
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62816ea0d7d7969cd56e0a9f525b2c412c8da182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548211"
---
# <a name="direct3d-11-on-12"></a>Direct3D 11 on 12

D3D11On12 é um mecanismo pelo qual os desenvolvedores podem usar interfaces e objetos do D3D11 para direcionar a API D3D12. O D3D11on12 permite que os componentes escritos usando D3D11 (por exemplo, texto e interface do usuário D2D) trabalhem em conjunto com os componentes criados direcionando a API do D3D12. O D3D11on12 também permite portabilidade incremental de um aplicativo do D3D11 para o D3D12, permitindo que partes do aplicativo continuem direcionando para a D3D11 para simplificar enquanto outras voltam a D3D12 para desempenho, enquanto sempre têm renderização completa e correta. O D3D11On12 torna mais simples do que usar técnicas de interoperabilidade para compartilhar recursos e sincronizar o trabalho entre as duas APIs.

-   [Inicializando D3D11On12](#initializing-d3d11on12)
-   [Exemplo de uso](#example-usage)
-   [Tela de fundo](#background)
-   [Limpeza](#cleaning-up)
-   [Limitações](#limitations)
-   [APIs](#apis)
-   [Tópicos relacionados](#related-topics)

## <a name="initializing-d3d11on12"></a>Inicializando D3D11On12

Para começar a usar o D3D11On12, a primeira etapa é criar um dispositivo D3D12 e uma fila de comando. Esses objetos são fornecidos como entrada para o método de inicialização [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). Você pode considerar esse método como a criação de um dispositivo D3D11 com o tipo de driver imaginário 11ON12 tipo de driver D3D \_ \_ \_ , em que o driver D3D11 é responsável por criar objetos e enviar listas de comandos para a API D3D12.

Depois de ter um dispositivo D3D11 e um contexto imediato, você pode `QueryInterface` desativar o dispositivo para a interface [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) . Essa é a interface primária usada para interoperabilidade entre D3D11 e D3D12. Para que o contexto do dispositivo D3D11 e as listas de comandos D3D12 operem nos mesmos recursos, é necessário criar "recursos encapsulados" usando a API [**CreateWrappedResource**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) . Esse método "promove" um recurso D3D12 para ser compreensível no D3D11. Um recurso encapsulado começa no estado "adquirido", uma propriedade que é manipulada pelos métodos [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) e [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) .

## <a name="example-usage"></a>Exemplo de uso

O uso típico de D3D11On12 seria usar D2D para renderizar texto ou imagens na parte superior de um buffer de back D3D12. Consulte o exemplo de D3D11On12 para código de exemplo. Aqui está uma descrição preliminar das etapas a serem seguidas:

-   Crie um dispositivo D3D12 ([**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)) e uma cadeia de permuta D3D12 ([**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) com um [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) como uma entrada).
-   Crie um dispositivo D3D11On12 usando o dispositivo D3D12 e a mesma fila de comando como entrada.
-   Recupere os buffers de fundo da cadeia de permuta e crie recursos encapsulados D3D11 para cada um deles. O estado de entrada usado deve ser a última maneira que o D3D12 o utilizou (por exemplo, \_ destino de renderização) e o estado de saída deve ser o modo como o D3D12 o usará depois que D3D11 for concluído (por exemplo, presente).
-   Inicialize D2D e forneça os recursos empacotados D3D11 para D2D para se preparar para renderização.

Em seguida, em cada quadro, faça o seguinte:

-   Renderize no buffer de retorno da cadeia de permuta atual usando uma lista de comandos do D3D12 e execute-o.
-   Adquirir o recurso encapsulado do buffer de fundo atual ([**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)).
-   Emita comandos de renderização D2D.
-   Libere o recurso encapsulado ([**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)).
-   Libere o contexto imediato do D3D11.
-   Presente ([**IDXGISwapChain1::P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)).

## <a name="background"></a>Segundo plano

D3D11On12 funciona sistematicamente. Cada chamada à API do D3D11 passa pela validação de tempo de execução típica e faz seu caminho para o driver. Na camada de driver, o driver especial 11on12 registra as operações de renderização de estado e problemas para as listas de comandos do D3D12. Essas listas de comandos são enviadas conforme necessário (por exemplo, uma consulta `GetData` ou recurso `Map` pode exigir que os comandos sejam liberados) ou conforme solicitado por liberação. Criar um objeto D3D11 normalmente resulta no objeto D3D12 correspondente que está sendo criado. Algumas operações de renderização de função fixas em D3D11 como `GenerateMips` ou `DrawAuto` não têm suporte em D3D12 e, portanto, o D3D11On12 os emula usando sombreadores e recursos adicionais.

Para a interoperabilidade, é importante entender como o D3D11On12 interage com os objetos D3D12 que o aplicativo criou e forneceu. Para garantir que o trabalho ocorra na ordem correta, o contexto imediato do D3D11 deve ser liberado antes que o trabalho adicional do D3D12 possa ser enviado para essa fila. Também é importante garantir que a fila fornecida para D3D11On12 deve ser drenada o tempo todo. Isso significa que qualquer espera na fila deve, eventualmente, ser satisfeita, mesmo que o thread de processamento D3D11 seja bloqueado indefinidamente. Tenha cuidado para não assumir uma dependência quando o D3D11On12 insere liberações ou esperas, pois isso pode mudar com versões futuras. Além disso, o D3D11On12 rastreia e manipula os Estados de recursos por conta própria. A única maneira de garantir a coerência das transições de estado é usar as APIs de aquisição/liberação para manipular o rastreamento de estado para corresponder às necessidades do aplicativo.

## <a name="cleaning-up"></a>Limpeza

Para liberar um recurso encapsulado D3D11On12, duas coisas precisam acontecer nesta ordem:

-   Todas as referências ao recurso, incluindo quaisquer exibições do recurso, precisam ser liberadas.
-   O processamento de destruição adiado deve ocorrer. A maneira mais simples de garantir isso acontece é invocar a API de contexto imediata `Flush` .

Depois que essas duas etapas forem concluídas, todas as referências tomadas pelo recurso encapsulado deverão ser liberadas e o recurso D3D12 se tornará exclusivamente de Propriedade do componente D3D12. Lembre-se de que o D3D12 ainda exige a espera pela conclusão da GPU antes de liberar completamente um recurso, portanto, certifique-se de manter uma referência no recurso antes de executar as duas etapas acima, a menos que você já tenha confirmado que a GPU não está mais usando o recurso.

Todos os outros recursos ou objetos criados pelo D3D11On12 serão limpos no momento apropriado, quando a GPU terminar de usá-los, usando o mecanismo de destruição adiada do D3D11's. No entanto, se você tentar liberar o próprio dispositivo D3D11On12 enquanto a GPU ainda estiver em execução, a destruição poderá ser bloqueada até que a GPU seja concluída.

## <a name="limitations"></a>Limitações

A camada D3D11On12 implementa um subconjunto muito grande da API D3D11, mas há algumas lacunas conhecidas (além de bugs na implementação que podem causar renderização incorreta).

A partir do Windows 10, versão 1809 (10,0; Build 17763), desde que o D3D11On12 esteja em execução em um driver que dá suporte ao modelo de sombreador 6,0 ou posterior, ele pode executar sombreadores que usam interfaces. Nas versões anteriores do Windows, o recurso de interfaces de sombreador não é implementado no D3D11On12 e a tentativa de usar o recurso cautilizará erros e mensagens de depuração.

A partir do Windows 10, versão 1803 (10,0; Build 17134), há suporte para cadeias de permuta em dispositivos D3D11On12. Em versões anteriores do Windows, elas não são.

D3D11On12 não foi otimizado para desempenho. Provavelmente haverá sobrecarga de CPU moderada em comparação com um driver D3D11 padrão, sobrecarga de GPU mínima e que haja uma sobrecarga significativa na memória. Portanto, não é recomendável usar D3D11On12 para cenas 3D complicadas e, em vez disso, é recomendado para cenas simples ou renderização 2D.

## <a name="apis"></a>APIs

As APIs que compõem a camada 11on12 são descritas em [referência do 11on12](direct3d-11on12-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[D2D usando o passo a passo do D3D11on12](d2d-using-d3d11on12.md)
</dt> <dt>

[Entendendo o Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Trabalhando com o Direct3D 11, o Direct3D 10 e o Direct2D](direct3d-12-interop.md)
</dt> </dl>

 

 
---
title: Direct3D 11 on 12
description: D3D11On12 é um mecanismo pelo qual os desenvolvedores podem usar interfaces e objetos D3D11 para conduzir a API D3D12.
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a67c7e0cd3592d35af80f280fc9f1893f4741fcadcc73afd3753880bccda3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530224"
---
# <a name="direct3d-11-on-12"></a>Direct3D 11 on 12

D3D11On12 é um mecanismo pelo qual os desenvolvedores podem usar interfaces e objetos D3D11 para conduzir a API D3D12. D3D11on12 permite que componentes escritos usando D3D11 (por exemplo, texto D2D e interface do usuário) funcionem em conjunto com componentes gravados destinados à API D3D12. D3D11on12 também permite a portação incremental de um aplicativo de D3D11 para D3D12, permitindo que partes do aplicativo continuem direcionando D3D11 para simplificar, enquanto outros direcionam D3D12 para desempenho, sempre tendo renderização completa e correta. D3D11On12 simplifica o uso de técnicas de interop para compartilhar recursos e sincronizar o trabalho entre as duas APIs.

-   [Inicializando D3D11On12](#initializing-d3d11on12)
-   [Uso de exemplo](#example-usage)
-   [Tela de fundo](#background)
-   [Limpeza](#cleaning-up)
-   [Limitações](#limitations)
-   [APIs](#apis)
-   [Tópicos relacionados](#related-topics)

## <a name="initializing-d3d11on12"></a>Inicializando D3D11On12

Para começar a usar D3D11On12, a primeira etapa é criar um dispositivo D3D12 e uma fila de comandos. Esses objetos são fornecidos como entrada para o método de inicialização [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). Você pode pensar nesse método como criar um dispositivo D3D11 com o tipo de driver imaginário D3D \_ DRIVER \_ TYPE 11ON12, em que o driver D3D11 é responsável por criar objetos e enviar listas de comandos para a \_ API D3D12.

Depois de ter um dispositivo D3D11 e um contexto imediato, você pode sair do dispositivo para a `QueryInterface` interface [**ID3D11On12Device.**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) Essa é a interface primária usada para a interop entre D3D11 e D3D12. Para que o contexto do dispositivo D3D11 e as listas de comandos D3D12 operem nos mesmos recursos, é necessário criar "recursos empacotados" usando a API [**CreateWrappedResource.**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) Esse método "promove" um recurso D3D12 para ser compreensível em D3D11. Um recurso empacotado começa no estado "adquirido", uma propriedade que é manipulada pelos métodos [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) e [**ReleaseWrappedResources.**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)

## <a name="example-usage"></a>Exemplo de uso

O uso típico de D3D11On12 seria usar D2D para renderizar texto ou imagens sobre um buffer de back D3D12. Consulte o exemplo D3D11On12 para ver o código de exemplo. Aqui está um contorno aproximado das etapas a serem tomadas para fazer isso:

-   Crie um dispositivo D3D12 ([**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)) e uma cadeia de permuta D3D12 ([**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) com [**um ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) como entrada).
-   Crie um dispositivo D3D11On12 usando o dispositivo D3D12 e a mesma fila de comandos que a entrada.
-   Recupere os buffers de retorno da cadeia de permuta e crie recursos empacotados D3D11 para cada um deles. O estado de entrada usado deve ser a última maneira como D3D12 o usou (por exemplo, RENDER TARGET) e o estado de saída deve ser a maneira como D3D12 o usará depois que D3D11 tiver sido concluído (por exemplo, \_ PRESENT).
-   Inicialize D2D e forneça os recursos empacotados D3D11 ao D2D para se preparar para renderização.

Em seguida, em cada quadro, faça o seguinte:

-   Renderizar no buffer de retorno da cadeia de permuta atual usando uma lista de comandos D3D12 e executá-lo.
-   Adquirir o recurso empacotado do buffer de fundo atual ([**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)).
-   Emitir comandos de renderização D2D.
-   Libere o recurso empacotado ([**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)).
-   Liberar o contexto imediato D3D11.
-   Present ([**IDXGISwapChain1::P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)).

## <a name="background"></a>Segundo plano

D3D11On12 funciona sistematicamente. Cada chamada à API D3D11 passa pela validação típica de runtime e chega ao driver. Na camada de driver, o driver especial 11on12 registra o estado e emite operações de renderização para listas de comandos D3D12. Essas listas de comandos são enviadas conforme necessário (por exemplo, uma consulta ou recurso pode exigir que os comandos sejam liberados) ou conforme solicitado `GetData` `Map` por Flush. A criação de um objeto D3D11 normalmente resulta na criação do objeto D3D12 correspondente. Algumas operações de renderização de função fixas em D3D11, como ou não têm suporte em `GenerateMips` `DrawAuto` D3D12 e, portanto, D3D11On12 as emula usando sombreadores e recursos adicionais.

Para a interop, é importante entender como D3D11On12 interage com os objetos D3D12 que o aplicativo criou e forneceu. Para garantir que o trabalho ocorra na ordem correta, o contexto imediato D3D11 deve ser liberado antes que o trabalho adicional D3D12 possa ser enviado para essa fila. Também é importante garantir que a fila dada a D3D11On12 deve ser esvaziada o tempo todo. Isso significa que qualquer espera na fila deve ser eventualmente atendida, mesmo que o thread de renderização D3D11 seja bloco indefinidamente. Tenha cuidado para não assumir uma dependência quando D3D11On12 insere liberações ou esperas, pois isso pode mudar com versões futuras. Além disso, D3D11On12 rastreia e manipula os estados de recursos por conta própria. A única maneira de garantir a coerência das transições de estado é usar as APIs de aquisição/versão para manipular o acompanhamento de estado para corresponder às necessidades do aplicativo.

## <a name="cleaning-up"></a>Limpeza

Para liberar um recurso empacotado D3D11On12, duas coisas precisam acontecer nesta ordem:

-   Todas as referências ao recurso, incluindo quaisquer exibições do recurso, precisam ser liberadas.
-   O processamento de destruição adiada deve ocorrer. A maneira mais simples de garantir que isso aconteça é invocar a API de contexto `Flush` imediata.

Depois que ambas as etapas são concluídas, todas as referências feitas pelo recurso empacotado devem ser liberadas e o recurso D3D12 torna-se de propriedade exclusiva do componente D3D12. Esteja ciente de que D3D12 ainda requer aguardar a conclusão da GPU antes de liberar completamente um recurso, portanto, certifique-se de manter uma referência no recurso antes de realizar as duas etapas acima, a menos que você já tenha confirmado que a GPU não está mais usando o recurso.

Todos os outros recursos ou objetos criados por D3D11On12 serão limpos no momento apropriado, quando a GPU terminar de usá-los, usando o mecanismo de destruição adiada de D3D11. No entanto, se você tentar liberar o próprio dispositivo D3D11On12 enquanto a GPU ainda estiver em execução, a destruição poderá bloquear até que a GPU seja concluída.

## <a name="limitations"></a>Limitações

A camada D3D11On12 implementa um subconjunto muito grande da API D3D11, mas há algumas lacunas conhecidas (além de bugs na implementação que podem causar renderização incorreta).

A partir Windows 10, versão 1809 (10.0; Build 17763), desde que D3D11On12 seja executado em um driver que dá suporte ao Modelo de Sombreador 6.0 ou posterior, ele poderá executar sombreadores que usam interfaces. Em versões anteriores do Windows, o recurso de interfaces de sombreador não é implementado em D3D11On12 e tentar usar o recurso causará erros e mensagens de depuração.

A partir Windows 10, versão 1803 (10.0; Build 17134), há suporte para cadeias de permuta em dispositivos D3D11On12. Em versões anteriores Windows, elas não.

D3D11On12 não foi otimizado para desempenho. Provavelmente haverá sobrecarga moderada de CPU em comparação com um driver D3D11 padrão, sobrecarga mínima de GPU e é conhecido por haver sobrecarga de memória significativa. Portanto, não é recomendável usar D3D11On12 para cenas 3D complicadas e, em vez disso, é recomendado para cenas simples ou renderização 2D.

## <a name="apis"></a>APIs

AS APIs que comem a camada 11on12 são descritas em [Referência 11on12](direct3d-11on12-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[D2D usando o passo a passo D3D11on12](d2d-using-d3d11on12.md)
</dt> <dt>

[Introdução ao Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Como trabalhar com o Direct2D, o Direct3D 10 e o Direct3D 11](direct3d-12-interop.md)
</dt> </dl>

 

 
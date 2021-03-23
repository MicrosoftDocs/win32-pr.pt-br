---
title: Interoperabilidade do Direct3D 12
description: D3D12 pode ser usado para gravar aplicativos divididos em componentes.
ms.assetid: 51F7E715-82B6-48D8-A06A-CBBEDF6968F5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b5fcfe2adf756c12f034031675d0c3ac5571b44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548316"
---
# <a name="direct3d-12-interop"></a>Interoperabilidade do Direct3D 12

D3D12 pode ser usado para gravar aplicativos divididos em componentes.

-   [Visão geral da interoperabilidade](#interop-overview)
-   [Motivos para usar a interoperabilidade](#reasons-for-using-interop)
    -   [Compartilhando uma lista de comandos](#sharing-a-command-list)
    -   [Compartilhando uma fila de comandos](#sharing-a-command-queue)
    -   [Compartilhando primitivos de sincronização](#sharing-sync-primitives)
    -   [Compartilhando recursos](#sharing-resources)
    -   [Escolhendo um modelo de interoperabilidade](#choosing-an-interop-model)
-   [APIs de interoperabilidade](#interop-apis)
-   [Tópicos relacionados](#related-topics)

## <a name="interop-overview"></a>Visão geral da interoperabilidade

O D3D12 pode ser muito eficiente e permitir que os aplicativos escrevam código gráfico com eficiência semelhante ao console, mas nem todos os aplicativos precisam reinventarr a roda e escrever todo o seu mecanismo de renderização do zero. Em alguns casos, outro componente ou biblioteca já o fez melhor, ou em outros casos, o desempenho de uma parte do código não é tão crítico quanto sua exatidão e legibilidade.

Esta seção aborda as seguintes técnicas de interoperabilidade:

-   D3D12 e D3D12, no mesmo dispositivo
-   D3D12 e D3D12, em diferentes dispositivos
-   D3D12 e qualquer combinação de D3D11, D3D10 ou D2D, no mesmo dispositivo
-   D3D12 e qualquer combinação de D3D11, D3D10 ou D2D, em diferentes dispositivos
-   D3D12 e GDI, ou D3D12 e D3D11 e GDI

## <a name="reasons-for-using-interop"></a>Motivos para usar a interoperabilidade

Há vários motivos pelos quais um aplicativo desejaria D3D12 interoperabilidade com outras APIs. Alguns exemplos:

-   Portabilidade incremental: deseja portar um aplicativo inteiro de D3D10 ou D3D11 para D3D12, enquanto ele está funcionando em estágios intermediários do processo de portagem (para habilitar o teste e a depuração).
-   Código de caixa preta: deseja deixar uma parte específica de um aplicativo como está ao portar o restante do código. Por exemplo, pode não haver a necessidade de portar elementos de interface do usuário de um jogo.
-   Componentes inalteráveis: precisar usar componentes que não pertencem ao aplicativo, que não são gravados no D3D12 de destino.
-   Um novo componente: não quer portar todo o aplicativo, mas deseja usar um novo componente que é escrito usando D3D12.

Há quatro técnicas principais para a interoperabilidade no D3D12:

-   Um aplicativo pode optar por fornecer uma lista de comandos abertos a um componente, que registra alguns comandos de renderização adicionais para um destino de renderização já associado. Isso é equivalente a fornecer um contexto de dispositivo preparado para outro componente em D3D11 e é ótimo para coisas como adicionar interface do usuário/texto a um buffer de fundo já vinculado.
-   Um aplicativo pode optar por fornecer uma fila de comandos a um componente, juntamente com um recurso de destino desejado. Isso é equivalente a usar APIs [**clearstate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate) ou [**DeviceContextState**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate) no D3D11 para fornecer um contexto de dispositivo limpo para outro componente. É assim que componentes como D2D operam.
-   Um componente pode optar por um modelo em que ele produz uma lista de comandos, potencialmente em paralelo, que o aplicativo é responsável pelo envio posteriormente. Pelo menos um recurso deve ser fornecido entre limites de componentes. Essa mesma técnica está disponível em D3D11 usando contextos adiados, embora o desempenho em D3D12 seja mais desejável.
-   Cada componente tem suas próprias filas e/ou dispositivos, e o aplicativo e os componentes precisam compartilhar recursos e informações de sincronização entre limites de componentes. Isso é semelhante ao herdado `ISurfaceQueue` e ao [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex)mais moderno.

As diferenças entre esses cenários é o que é compartilhado exatamente entre os limites do componente. Presume-se que o dispositivo seja compartilhado, mas como ele é basicamente sem estado, ele não é realmente relevante. Os principais objetos são a lista de comandos, a fila de comandos, os objetos de sincronização e os recursos. Cada uma delas tem suas próprias complicações ao compartilhá-las.

### <a name="sharing-a-command-list"></a>Compartilhando uma lista de comandos

O método mais simples de interoperabilidade requer o compartilhamento de apenas uma lista de comandos com uma parte do mecanismo. Depois que as operações de renderização forem concluídas, a propriedade da lista de comandos voltará ao chamador. A propriedade da lista de comandos pode ser rastreada por meio da pilha. Como as listas de comandos são thread único, não há como fazer com que um aplicativo faça algo exclusivo ou inovador usando essa técnica.

### <a name="sharing-a-command-queue"></a>Compartilhando uma fila de comandos

Provavelmente, a técnica mais comum para vários componentes que compartilham um dispositivo no mesmo processo.

Quando a fila de comandos é a unidade de compartilhamento, precisa haver uma chamada para o componente para que ele saiba que todas as listas de comandos pendentes precisam ser enviadas à fila de comandos imediatamente (e todas as filas de comandos internas precisam ser sincronizadas). Isso é equivalente à API de [**liberação**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) D3D11 e é a única maneira que o aplicativo pode enviar suas próprias listas de comandos ou primitivos de sincronização.

### <a name="sharing-sync-primitives"></a>Compartilhando primitivos de sincronização

O padrão esperado para um componente que opera em seus próprios dispositivos e/ou filas de comando será aceitar um [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) ou um identificador compartilhado, e o par UInt64 ao iniciar seu trabalho, que ele aguardará e, em seguida, um segundo ID3D12Fence ou identificador compartilhado, e o par de UInt64, que será sinalizado quando todo o trabalho for concluído. Esse padrão corresponde à implementação atual de [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex) e do design de sincronização de modelo invertido DWM/dxgi.

### <a name="sharing-resources"></a>Compartilhando recursos

De longe, a parte mais complicada de escrever um aplicativo D3D12 que aproveita vários componentes é como lidar com os recursos que são compartilhados entre limites de componentes. Isso ocorre principalmente devido ao conceito de Estados de recursos. Embora alguns aspectos do design de estado do recurso sejam para lidar com a sincronização de lista de comandos, outros têm impacto entre as listas de comandos, afetando o layout de recursos e os conjuntos válidos de operações ou características de desempenho do acesso aos dados do recurso.

Há dois padrões de lidar com essa complicação, ambos envolvem, essencialmente, um contrato entre componentes.

-   O contrato pode ser definido pelo desenvolvedor do componente e documentado. Isso pode ser tão simples quanto "o recurso deve estar no estado padrão quando o trabalho é iniciado e será colocado de volta no estado padrão quando o trabalho é feito" ou pode ter regras mais complicadas para permitir coisas como o compartilhamento de um buffer de profundidade sem forçar a resolução de profundidade intermediária.
-   O contrato pode ser definido pelo aplicativo em tempo de execução, no momento em que o recurso é compartilhado entre limites de componentes. Ele consiste nas mesmas duas partes de informação: o estado em que o recurso estará quando o componente começar a usá-lo e o estado em que o componente deve deixá-lo quando for concluído.

### <a name="choosing-an-interop-model"></a>Escolhendo um modelo de interoperabilidade

Para a maioria dos aplicativos D3D12, o compartilhamento de uma fila de comandos provavelmente é o modelo ideal. Ele permite a propriedade completa da criação e do envio de trabalho, sem a sobrecarga de memória adicional de ter filas redundantes e sem o impacto de desempenho de lidar com os primitivos de sincronização de GPU.

O compartilhamento de primitivos de sincronização é necessário quando os componentes precisam lidar com propriedades de fila diferentes, como tipo ou prioridade, ou quando o compartilhamento precisa abranger limites de processo.

Compartilhar ou produzir listas de comandos não são amplamente usados externamente por componentes de terceiros, mas podem ser amplamente usados em componentes que são internos a um mecanismo de jogo.

## <a name="interop-apis"></a>APIs de interoperabilidade

O tópico do [Direct3D 11 no 12](./direct3d-11-on-12.md) orienta você pelo uso de grande parte da superfície da API relacionada aos tipos de interoperação descritos neste tópico.

Consulte também o método [ID3D12Device:: CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle) , que pode ser usado para compartilhar superfícies entre as APIs de gráficos do Windows.

## <a name="related-topics"></a>Tópicos relacionados

* [Entendendo o Direct3D 12](directx-12-getting-started.md)
* [Trabalhando com o Direct3D 11, o Direct3D 10 e o Direct2D](direct3d-12-interop.md)
* [Direct3D 11 on 12](./direct3d-11-on-12.md)
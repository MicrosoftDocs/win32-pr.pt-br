---
title: Gerenciador
description: O stub, como o proxy, é composto de uma ou mais partes de interface e um gerente.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "105763465"
---
# <a name="stub"></a>Gerenciador

O stub, como o proxy, é composto de uma ou mais partes de interface e um gerente. Cada stub de interface fornece código para desempacotar os parâmetros e o código que chama uma das interfaces com suporte do objeto. Cada stub também fornece uma interface para comunicação interna. O Gerenciador de stub controla os stubs de interface disponíveis.

No entanto, há as seguintes diferenças entre o stub e o proxy:

-   A diferença mais importante é que o stub representa o cliente no espaço de endereço do objeto.
-   O stub não é implementado como um objeto de agregação porque não há nenhum requisito de que o cliente seja exibido como uma única unidade; cada parte no stub é um componente separado.
-   Os stubs de interface são privados em vez de públicos.
-   Os stubs de interface implementam [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), não [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).
-   Em vez dos parâmetros de empacotamento a serem empacotados, o stub os empacota depois que eles foram empacotados e, em seguida, empacota a resposta.

## <a name="structure-of-the-stub"></a>Estrutura do stub

O diagrama a seguir mostra a estrutura do stub. Cada stub de interface é conectado a uma interface no objeto. O canal despacha as mensagens de entrada para o stub de interface apropriado. Todos os componentes falam com o canal por meio do [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), a interface que fornece acesso à biblioteca de tempo de execução RPC.

![Captura de tela que mostra a estrutura do stub.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Comunicação entre objetos](inter-object-communication.md)
</dt> <dt>

[Detalhes de marshaling](marshaling-details.md)
</dt> <dt>

[RPC da Microsoft](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> </dl>

 

 
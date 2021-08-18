---
title: Proxy
description: Um proxy reside no espaço de endereço do processo de chamada e atua como um substituto para o objeto remoto.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0478ce9ad1e08d343f1536fcd4bba63e59ae0fd229390be31c978bd20f737b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129998"
---
# <a name="proxy"></a>Proxy

Um proxy reside no espaço de endereço do processo de chamada e atua como um substituto para o objeto remoto. Da perspectiva do objeto de chamada, o proxy é o objeto. Normalmente, a função do proxy é empacotar os parâmetros da interface para chamadas para métodos em suas interfaces de objeto. O proxy empacota os parâmetros em um buffer de mensagens e passa o buffer para o canal, que manipula o transporte entre os processos. O proxy é implementado como um objeto agregado, ou composto. Ele contém uma peça do gerente, fornecida pelo sistema, chamada Gerenciador de proxy e um ou mais componentes específicos de interface chamados de proxies de interface. O número de proxies de interface é igual ao número de interfaces de objeto que foram expostas a esse cliente específico. Para o cliente estar de conformidade com o modelo de objeto de componente, o proxy parece ser o objeto real.

> [!Note]  
> Com o marshaling personalizado, o proxy pode ser implementado da mesma forma ou pode se comunicar diretamente com o objeto sem usar um stub.

 

Cada proxy de interface é um objeto de componente que implementa o código de marshaling para uma das interfaces do objeto. O proxy representa o objeto para o qual ele fornece o código de marshaling. Cada proxy também implementa a interface [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) . Embora a interface de objeto representada pelo proxy seja pública, a implementação de **IRpcProxyBuffer** é privada e usada internamente no proxy. O Gerenciador de proxy controla os proxies de interface e também contém a implementação pública da interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de controle para a agregação. Cada proxy de interface pode existir em uma DLL separada que é carregada quando a interface à qual ele dá suporte é materializada para o cliente.

## <a name="structure-of-the-proxy"></a>Estrutura do proxy

O diagrama a seguir mostra a estrutura de um proxy que dá suporte ao empacotamento padrão de parâmetros que pertencem a duas interfaces: IA1 e IA2. Cada proxy de interface implementa [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) para comunicação interna entre as partes agregadas. Quando o proxy está pronto para passar seus parâmetros de marshaling pelo limite do processo, ele chama os métodos na interface [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) , que é implementada pelo canal. O canal, por sua vez, encaminha a chamada para a biblioteca de tempo de execução RPC para que possa acessar seu destino no objeto.

![Diagrama que mostra a estrutura do proxy.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

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

[Gerenciador](stub.md)
</dt> </dl>

 

 
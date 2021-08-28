---
title: Detalhes de marshaling
description: Se você usar o marshaling padrão, o COM tratará todos os detalhes descritos aqui para você.
ms.assetid: bf3fe212-648e-4d00-ad1d-43d2e5e6a7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f821d06ce452b9492a6b2c5953c5c0d20cd55e653ab471380987dc91566636da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859336"
---
# <a name="marshaling-details"></a>Detalhes de marshaling

Se você usar o marshaling padrão, o COM tratará todos os detalhes descritos aqui para você. No entanto, existem poucos programadores que precisam desses detalhes e para aqueles interessados nas informações subjacentes. O marshaling é o processo de empacotamento e desempacotamento de parâmetros para que uma chamada de procedimento remota possa ocorrer.

Tipos de parâmetros diferentes são empacotados de maneiras diferentes. Por exemplo, o marshaling de um parâmetro inteiro envolve simplesmente copiar o valor para o buffer de mensagens. (Embora mesmo nesse caso simples, há problemas como a ordenação de bytes para lidar em chamadas entre computadores.) O marshaling de uma matriz, no entanto, é um processo mais complexo. Os membros da matriz são copiados em uma ordem específica para que o outro lado possa reconstruir a matriz exatamente. Quando um ponteiro é empacotado, os dados aos quais o ponteiro está apontando são copiados seguindo regras e convenções para lidar com ponteiros aninhados em estruturas. Existem funções exclusivas para lidar com o marshaling de cada tipo de parâmetro.

Com o marshaling padrão, os proxies e os stubs são recursos de todo o recurso para a interface e interagem com o canal por meio de um protocolo padrão. O empacotamento padrão pode ser usado por interfaces padrão definidas COM e por interfaces personalizadas, da seguinte maneira:

-   No caso da maioria das interfaces COM, os proxies e os stubs para marshaling padrão são objetos de componente em processo que são carregados de uma DLL de todo o setor fornecida pelo COM no Ole32.dll.
-   No caso de interfaces personalizadas, os proxies e os stubs para marshaling padrão são gerados pelo designer de interface, normalmente com MIDL. Esses proxies e stubs são configurados estaticamente no registro, de modo que qualquer cliente potencial pode usar a interface personalizada entre limites de processo. Esses proxies e stubs são carregados de uma DLL localizada por meio do registro do sistema, usando a IID (ID de interface) para a interface personalizada que eles realizam marshaling.
-   Uma alternativa ao uso de MIDL para gerar proxies e stubs para interfaces personalizadas, uma biblioteca de tipos pode ser gerada em vez disso e o sistema fornecido, o "mecanismo de marshaling controlado pelo tipo libraryâ €" realizará marshaling da interface.

Como uma alternativa ao empacotamento padrão, uma interface (padrão ou personalizada) pode usar o marshaling personalizado. Com o marshaling personalizado, um objeto implementa dinamicamente os proxies em tempo de execução para cada interface que ele suporta. Para qualquer interface especificada, o objeto pode selecionar marshaling padrão fornecido COM ou marshaling personalizado. Essa opção é feita pelo objeto em uma base interface por interface. Depois que a escolha é feita para uma determinada interface, ela permanece em vigor durante o tempo de vida do objeto. No entanto, uma interface em um objeto pode usar marshaling personalizado enquanto outro usa marshaling padrão.

O marshaling personalizado é inerentemente exclusivo ao objeto que o implementa. Ele usa proxies implementados pelo objeto e fornecido ao sistema na solicitação em tempo de execução. Os objetos que implementam o marshaling personalizado devem implementar a interface [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , enquanto os objetos que dão suporte ao marshaling padrão não.

Se você decidir escrever uma interface personalizada, deverá fornecer suporte de marshaling para ela. Normalmente, você fornecerá uma DLL de marshaling padrão para a interface que você projeta. Você pode criar o código de proxy/stub e o proxy/DLL de stub, ou pode criar uma biblioteca de tipos que o COM usará para realizar o marshaling controlado por dados (usando os dados na biblioteca de tipos).

Para que um cliente faça uma chamada para um método de interface em um objeto em outro processo envolve a cooperação de vários componentes. O proxy padrão é uma parte do código específico de interface que reside no espaço de processo do cliente e prepara os parâmetros de interface para transmissão. Pacotes de ti, ou Marshals, de forma que eles possam ser recriados e compreendidos no processo de recebimento. O stub padrão, também uma parte do código específico da interface, reside no espaço do processo do servidor e reverte o trabalho do proxy. O stub desempacota ou desempacota os parâmetros enviados e os encaminha para o aplicativo de objeto. Ele também empacota informações de resposta para enviar de volta para o cliente.

> [!Note]  
> Os leitores mais familiarizados com RPC do que COM podem ser usados para ver os termos stub de cliente e stub de servidor. Esses termos são análogos ao proxy e ao stub.

 

## <a name="components-of-interprocess-communications"></a>Componentes de comunicações entre processos

O diagrama a seguir mostra o fluxo de comunicação entre os componentes envolvidos. No lado do cliente do limite do processo, a chamada do método do cliente passa pelo proxy e, em seguida, para o canal, que faz parte da biblioteca COM. O canal envia o buffer que contém os parâmetros de marshaling para a biblioteca de tempo de execução RPC, que o transmite ao longo do limite do processo. O tempo de execução RPC e as bibliotecas COM existem em ambos os lados do processo. A distinção entre o canal e o tempo de execução de RPC é uma característica dessa implementação e não faz parte do modelo de programação ou do modelo conceitual para objetos cliente/servidor COM. Os servidores COM só veem o proxy ou o stub e, indiretamente, o canal. Implementações futuras podem usar camadas diferentes abaixo do canal ou nenhuma camada.

![Diagrama que mostra o Client.exe e Server.exe flui em cada lado do limite do processo.](images/457036c1-98b8-4f35-aebe-70de38112b83.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Comunicação entre objetos](inter-object-communication.md)
</dt> <dt>

[RPC da Microsoft](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Gerenciador](stub.md)
</dt> </dl>

 

 
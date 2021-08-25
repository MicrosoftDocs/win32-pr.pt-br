---
title: Arquitetura de objetos conectáveis
description: Arquitetura de objetos conectáveis
ms.assetid: 69949a3b-3ab8-4054-84d8-9256fbf39c7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1215b013c3db751e90b07ed21d5f897ef0332000ce2cd2b3b167cbe86798927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993947"
---
# <a name="architecture-of-connectable-objects"></a>Arquitetura de objetos conectáveis

O objeto conectável é apenas uma parte da arquitetura geral de objetos conectáveis. Essa tecnologia inclui os seguintes elementos:

-   **Objeto conectável.** Implementa a interface [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) ; cria pelo menos um objeto de ponto de conexão; define uma interface de saída para o cliente.
-   **Cliente.** Consulta o objeto para [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) para determinar se o objeto é conectável; Cria um objeto de coletor para implementar a interface de saída definida pelo objeto que pôde ser conectado.
-   **Objeto Sink.** Implementa a interface de saída; usado para estabelecer uma conexão com o objeto conectável.
-   **Objeto de ponto de conexão.** Implementa a interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) e gerencia a conexão com o coletor do cliente.

As relações entre o cliente, o objeto connectável, um ponto de conexão e um coletor são ilustradas no diagrama a seguir:

![Diagrama que mostra os pontos de conexão entre o cliente e o objeto conectável.](images/1cd44fec-5d2c-4427-846b-ccab7ec0b08a.png)

Antes que o objeto de ponto de conexão Chame métodos na interface do coletor na etapa 3 no diagrama anterior, ele deve ser [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para a interface específica necessária, mesmo que o ponteiro já tenha passado na chamada Step 2 para o método [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) .

Dois objetos enumeradores também estão envolvidos nessa arquitetura, embora não sejam mostrados na ilustração. Um é criado por um método em [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) para enumerar os pontos de conexão dentro do objeto conectável. O outro é criado por um método em [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) para enumerar as conexões estabelecidas atualmente com esse ponto de conexão. Um ponto de conexão pode dar suporte a várias interfaces de coletor conectadas e deve iterar na lista de conexões toda vez que faz uma chamada de método nessa interface. Esse processo é conhecido como multicast.

Ao trabalhar com objetos conectáveis, é importante entender que o objeto conectável, cada ponto de conexão, cada coletor e todos os enumeradores são objetos separados com implementações [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) separadas, contagens de referência separadas e tempos de vida separados. Um cliente que usa esses objetos é sempre responsável por liberar todas as contagens de referência que ele possui.

> [!Note]  
> Um objeto conectável pode dar suporte a mais de um cliente e pode dar suporte a vários coletores dentro de um cliente. Da mesma forma, um coletor pode ser conectado a mais de um objeto conectável.

 

As etapas para estabelecer uma conexão entre um cliente e um objeto conectável são as seguintes:

1.  O cliente consulta o [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) no objeto para determinar se o objeto é conectável. Se essa chamada for bem-sucedida, o cliente mantém um ponteiro para a interface **IConnectionPointContainer** no objeto que pôde ser conectado e o contador de referência de objeto conectável foi incrementado. Caso contrário, o objeto não será conectável e não dará suporte a interfaces de saída.
2.  Se o objeto for conectável, o cliente tentará, em seguida, obter um ponteiro para a interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) em um ponto de conexão dentro do objeto conectável. Há dois métodos para obter esse ponteiro, em [**IConnectionPointContainer:: FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) e em [**IConnectionPointContainer:: EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Há algumas etapas adicionais necessárias se **EnumConnectionPoints** for usado. (Consulte [usando IConnectionPointContainer](using-iconnectionpointcontainer.md) para obter mais informações.) Se for bem-sucedido, o objeto conectável e o cliente terão suporte para a mesma interface de saída. O objeto conectável o define e o chama, e o cliente o implementa. Em seguida, o cliente pode se comunicar por meio do ponto de conexão dentro do objeto que pode ser conectado.
3.  Em seguida, o cliente chama [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) no ponto de conexão para estabelecer uma conexão entre sua interface de coletor e o ponto de conexão do objeto. Após essa chamada, o ponto de conexão do objeto mantém um ponteiro para a interface de saída no coletor.
4.  O código dentro de [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) chama [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro de interface que é passado, solicitando o identificador de interface específico ao qual ele se conecta.
5.  O objeto chama métodos na interface do coletor, conforme necessário, usando o ponteiro mantido por seu ponto de conexão.
6.  O cliente chama [**Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise) para encerrar a conexão. Em seguida, o cliente chama **IConnectionPoint:: Release** para liberar sua espera no ponto de conexão e, portanto, o principal objeto conectável também. O cliente também deve chamar **IConnectionPointContainer:: Release** para liberar sua espera no objeto principal que pode ser conectado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de objeto conectáveis](connectable-object-interfaces.md)
</dt> </dl>

 

 





---
title: Eventos em objetos COM e conectáveis
description: Quando um programa detecta algo que aconteceu, ele pode notificar seus clientes.
ms.assetid: f6ffbd1d-4bc1-4dc2-b3ed-ee12359e3d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5115cfd08d57658eec879d44b4361e88965b3c
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "104007032"
---
# <a name="events-in-com-and-connectable-objects"></a>Eventos em objetos COM e conectáveis

Quando um programa detecta algo que aconteceu, ele pode notificar seus clientes. Por exemplo, se um programa de cotação de ações detectar uma alteração no preço de uma ação, ele poderá notificar todos os clientes da alteração. Esse processo de notificação é conhecido como *acionando um evento*.

Com o COM, os objetos de servidor podem usar eventos COM para acionar eventos sem nenhuma informação sobre quais objetos serão notificados. Os objetos também podem usar *objetos conectáveis* para manter informações detalhadas sobre os clientes que solicitaram notificações.

Os objetos de conexão COM fornecem interfaces de saída para seus clientes, além de suas interfaces de entrada. Como resultado, os objetos e seus clientes podem se envolver na comunicação bidirecional. As interfaces de entrada são implementadas em um objeto e recebem chamadas de clientes externos de um objeto, enquanto as interfaces de saída são implementadas no coletor do cliente e recebem chamadas do objeto. O objeto define uma interface que gostaria de usar e o cliente a implementa.

Um objeto define suas interfaces de entrada e fornece implementações dessas interfaces. As interfaces de entrada estão disponíveis para clientes por meio do método [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) do objeto. Os clientes chamam os métodos de uma interface de entrada no objeto e o objeto executa as ações desejadas em nome do cliente.

As interfaces de saída também são definidas por um objeto, mas o cliente fornece as implementações das interfaces de saída em um objeto de coletor que o cliente cria. Em seguida, o objeto chama métodos da interface de saída no objeto do coletor para notificar o cliente sobre as alterações no objeto, disparar eventos no cliente, solicitar algo do cliente, ou, na verdade, para qualquer finalidade com a qual o criador de objeto é fornecido.

Um exemplo de uma interface de saída é uma interface IButtonSink definida por um controle de botão de ação para notificar seus clientes sobre seus eventos. Por exemplo, o objeto Button chama IButtonSink:: OnClick no objeto Sink do cliente quando o usuário clica no botão na tela. O controle de botão define a interface de saída. Para um cliente do botão manipular o evento, o cliente deve implementar essa interface de saída em um objeto de coletor e, em seguida, conectar esse coletor ao controle de botão. Em seguida, quando os eventos ocorrerem no botão, o botão chamará o coletor, no momento em que o cliente pode executar qualquer ação que desejar atribuir a esse botão.

Os objetos conectáveis fornecem um mecanismo geral para comunicação entre objetos e clientes. Qualquer objeto que queira expor eventos ou notificações de qualquer tipo pode usar essa tecnologia. Além da tecnologia de objeto de conexão geral, o COM fornece muitas interfaces de site e coletor de propósito especial usadas por objetos para notificar os clientes sobre eventos específicos de interesse do cliente. Por exemplo, [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) pode ser usado por objetos para notificar clientes de dados e exibir alterações no objeto.

Para mais informações, consulte os seguintes tópicos:

-   [Arquitetura de objetos conectáveis](architecture-of-connectable-objects.md)
-   [Interfaces de objeto conectáveis](connectable-object-interfaces.md)

 

 





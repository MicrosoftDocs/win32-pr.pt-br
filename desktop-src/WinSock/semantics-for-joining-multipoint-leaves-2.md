---
description: A seguir, um soquete do MultiPoint é frequentemente descrito definindo sua função em um dos dois planos (controle ou dados).
ms.assetid: 34f639e2-9363-4f3f-a8de-b7c5d12618c9
title: Semântica para unir as folhas do MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df12683838fbad89f717b08d7a19802f24556761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811587"
---
# <a name="semantics-for-joining-multipoint-leaves"></a>Semântica para unir as folhas do MultiPoint

A seguir, um soquete do MultiPoint é frequentemente descrito definindo sua função em um dos dois planos (controle ou dados). Deve-se entender que esse mesmo soquete tem uma função no outro plano, mas isso não é mencionado para manter as referências curtas. Por exemplo, quando uma referência é feita a um " \_ soquete raiz c", ela pode ser uma \_ raiz c/d \_ ou um soquete de \_ folha c raiz/d \_ .

Em esquemas de plano de controle com raiz, novos nós folha são adicionados a uma sessão do MultiPoint em uma ou ambas as duas maneiras diferentes. No primeiro método, a raiz usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para iniciar uma conexão com um nó folha e convidá-la para se tornar um participante. No nó folha, o aplicativo par deve ter criado um \_ soquete folha c e usado [**escutar**](/windows/desktop/api/Winsock2/nf-winsock2-listen) para defini-lo no modo de escuta. O nó folha recebe uma \_ indicação FD Accept quando convidado para ingressar na sessão e sinaliza sua disposição para ingressar chamando [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept). Em seguida, o aplicativo raiz recebe uma \_ indicação FD Connect quando a operação de **junção** é concluída.

No segundo método, as funções são essencialmente invertidas. O aplicativo raiz cria um \_ soquete raiz c e o define no modo de escuta. Um nó folha que deseja ingressar na sessão cria um \_ soquete folha c e usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para iniciar a conexão e solicitar Admittance. O aplicativo raiz recebe \_ o FD Accept quando chega uma solicitação Admittance de entrada e admite o nó folha chamando [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept). O nó folha recebe o FD \_ Connect quando ele foi admitido.

Em um plano de controle não raiz, em que todos os nós são \_ folhas c, o [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) é usado para iniciar a inclusão de um nó em uma sessão de MultiPoint existente. Uma indicação do FD \_ Connect é fornecida quando a junção é concluída e o descritor de soquete retornado é utilizável na sessão do MultiPoint. No caso do multicast de IP, isso corresponderia à \_ opção IP adicionar \_ soquete de associação.

(Os leitores familiarizados com o uso de multicast IP do protocolo UDP sem conexão podem estar preocupados com a semântica orientada por conexão apresentada aqui. Em particular, a noção de usar [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) em um soquete UDP e aguardar uma \_ indicação FD Connect pode ser preocupantes. No entanto, há uma ampla preprecedente para aplicar a semântica orientada a conexão a protocolos sem conexão. Ele é permitido e, às vezes, útil, por exemplo, para invocar a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) padrão em um soquete UDP. O resultado geral da aplicação de semântica orientada a conexão a soquetes sem conexão é uma restrição de como esses soquetes podem ser usados, e esse também é o caso aqui. Um soquete UDP usado em **WSAJoinLeaf** terá certas restrições e aguardando uma \_ indicação FD Connect (que, nesse caso, simplesmente indica que a mensagem IGMP correspondente foi enviada) é uma dessas limitações.)

Portanto, há três instâncias em que um aplicativo usaria [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) atuando como:

-   Raiz do MultiPoint e convidando uma nova folha para ingressar na sessão
-   Folha fazendo uma solicitação de Admittance para uma sessão do MultiPoint com raiz
-   Folha buscando Admittance a uma sessão do MultiPoint não enraizada (por exemplo, multicast de IP)

 

 




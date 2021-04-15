---
description: A seguir, um soquete do MultiPoint é geralmente caracterizado com a descrição de sua função em um dos dois planos (controle ou dados).
ms.assetid: 35e4a8c9-d943-44b8-be61-605b60a6cf5d
title: Semântica SPI para unir folhas do MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0e77203e5405f6cb820baba5d545de03e3a8ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768275"
---
# <a name="spi-semantics-for-joining-multipoint-leaves"></a>Semântica SPI para unir folhas do MultiPoint

A seguir, um soquete do MultiPoint é geralmente caracterizado com a descrição de sua função em um dos dois planos (controle ou dados). Deve-se entender que esse mesmo soquete tem uma função no outro plano, mas isso não é mencionado para manter as referências curtas. Por exemplo, uma referência a um \_ soquete raiz c poderia se referir a uma \_ raiz c raiz/d \_ ou a um \_ soquete folha c raiz/d \_ .

Em esquemas de plano de controle com raiz, novos nós folha são adicionados a uma sessão do MultiPoint em uma ou ambas as duas maneiras diferentes. No primeiro método, a raiz usa [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para iniciar uma conexão com um nó folha e convidá-la para se tornar um participante. No nó folha, o aplicativo par deve ter criado um \_ soquete folha c e usado [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) para defini-lo no modo de escuta. O nó folha receberá uma \_ indicação FD Accept quando convidado para ingressar na sessão e sinalizará sua disposição para ingressar chamando [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). O aplicativo raiz receberá uma \_ indicação FD Connect quando a operação de junção for concluída.

No segundo método, as funções são essencialmente invertidas. O cliente raiz cria um \_ soquete raiz c e o define no modo de escuta. Um nó folha que deseja ingressar na sessão cria um \_ soquete folha c e usa [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para iniciar a conexão e solicitar Admittance. O cliente raiz recebe \_ o FD Accept quando chega uma solicitação Admittance de entrada e admite o nó folha chamando [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). O nó folha recebe o FD \_ Connect quando ele foi admitido.

Em um plano de controle não raiz, em que todos os nós são \_ folhas c, a função [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) é usada para iniciar a inclusão de um nó em uma sessão de MultiPoint existente. Uma indicação do FD \_ Connect é fornecida quando a junção é concluída e o descritor de soquete retornado é utilizável na sessão do MultiPoint. No caso do multicast de IP, isso corresponderia à \_ opção IP adicionar \_ soquete de associação.

Há, portanto, três instâncias em que um cliente usaria [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf):

-   Atuando como uma raiz do MultiPoint e convidando uma nova folha para ingressar na sessão.
-   Atuar como uma folha fazendo uma solicitação Admittance para uma sessão do MultiPoint com raiz.
-   Atuando como uma folha que procura Admittance a uma sessão multiponto não-enraizada (por exemplo, multicast de IP).

 

 

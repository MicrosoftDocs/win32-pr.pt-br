---
description: Este tópico discute considerações de programação específicas ao usar a infraestrutura par.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Considerações sobre programação (ponto a ponto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d5af967503c216422e3a12572aeeaf91d751473f88d8589c2e125894721b41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518056"
---
# <a name="programming-considerations-peer-to-peer"></a>Considerações sobre programação (ponto a ponto)

Este tópico discute considerações de programação específicas ao usar a infraestrutura par.

Ao usar a Infraestrutura par para desenvolver aplicativos pares, você deve levar em conta as seguintes considerações de programação:

-   IPv6

    A Infraestrutura par exige que o IPv6 seja instalado e iniciado para permitir que os aplicativos de rede par funcionem.

-   Portas de firewall

    Quando um firewall está sendo usado em uma rede (como o firewall da Conexão com a Internet IPv6), portas específicas devem ser abertas para permitir que a Infraestrutura par funcione. As seguintes portas devem estar abertas:

    Porta TCP 3587 para a infraestrutura de grupo de pares.

    Porta UDP 3540 para a infraestrutura de grafo de pares.

    > [!Note]  
    > Os aplicativos que usam a infraestrutura de grafo de pares em vez do TCP escolhem sua própria porta TCP ao chamar [**PeerGraphListen.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)

     

-   Opção socket

    Ao tentar se conectar a outros nós de par IPv6 diretamente (sem usar a Infraestrutura par), verifique se a opção de soquete IPV6 PROTECTION LEVEL está definida como NÍVEL DE PROTEÇÃO \_ \_ **\_ \_ IRRESTRITO.**

-   Largura de banda

    Ao usar o PNRP, um aplicativo pode publicar um ou mais [nomes de pares](peer-names.md) que podem ser resolvidos. Para cada nome de par registrado com PNRP, há um aumento na largura de banda de rede que o PNRP usa para publicar o nome do par e mantê-lo disponível para ser resolvido por outros nós.

    Para evitar o uso de muita largura de banda, os aplicativos devem evitar o registro de grandes números de nomes de pares em um computador. Por exemplo, um aplicativo que publica imagens não deve criar um nome par para cada imagem, mas deve criar um nome par para o serviço que publica imagens e usar um protocolo diferente para que os clientes consultem o serviço para imagens específicas.

-   Registro de nome de par

    Alguns aplicativos podem ser necessários para registrar o mesmo [nome de par](peer-names.md) em mais de um computador. Normalmente, isso acontece se um nome de par estiver associado a uma pessoa que usa mais de um computador. Um método que você pode usar para registrar o mesmo nome de par em vários computadores é criar um grupo par para a pessoa e conectar-se a esse grupo de todos os computadores. Outro método é criar uma identidade de par e um nome de par em um computador, exportar a identidade de par desse computador e importá-la em outros computadores. Isso permite que o mesmo nome de par seguro seja criado em todos os computadores que importaram a identidade de par.

 

 




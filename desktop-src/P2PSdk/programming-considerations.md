---
description: Este tópico discute considerações de programação específicas ao usar a infraestrutura de pares.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Considerações sobre programação (ponto a ponto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755971"
---
# <a name="programming-considerations-peer-to-peer"></a>Considerações sobre programação (ponto a ponto)

Este tópico discute considerações de programação específicas ao usar a infraestrutura de pares.

Ao usar a infraestrutura de pares para desenvolver aplicativos de mesmo nível, você deve levar em conta as seguintes considerações de programação:

-   IPv6

    A infraestrutura de pares requer que o IPv6 seja instalado e iniciado para permitir que os aplicativos de rede de mesmo nível funcionem.

-   Portas de firewall

    Quando um firewall está sendo usado em uma rede (como o firewall de conexão com a Internet IPv6), as portas específicas devem ser abertas para permitir que a infraestrutura de mesmo nível funcione. As seguintes portas devem estar abertas:

    Porta TCP 3587 para a infraestrutura de agrupamento de pares.

    Porta UDP 3540 para a infraestrutura de grafo de pares.

    > [!Note]  
    > Os aplicativos que usam a infraestrutura de grafo de pares sobre TCP escolhem sua própria porta TCP ao chamar [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Opção de soquete

    Ao tentar se conectar a outros nós de mesmo nível IPv6 diretamente (sem usar a infraestrutura de mesmo nível), verifique se a opção de soquete \_ nível de proteção IPv6 \_ está definida como **nível de proteção \_ \_ irrestrito**.

-   Largura de banda

    Ao usar o PNRP, um aplicativo pode publicar um ou mais [nomes de pares](peer-names.md) que podem ser resolvidos. Para cada nome de par registrado com o PNRP, há um aumento na largura de banda de rede que o PNRP usa para publicar o nome do par e mantê-lo disponível para ser resolvido por outros nós.

    Para evitar o uso de muita largura de banda, os aplicativos devem evitar o registro de grandes números de nomes de pares em um computador. Por exemplo, um aplicativo que publica imagens não deve criar um nome de par para cada imagem, mas deve criar um nome de par para o serviço que publica imagens e usar um protocolo diferente para os clientes consultarem o serviço em busca de imagens específicas.

-   Registro de nome de par

    Alguns aplicativos podem ser necessários para registrar o mesmo [nome de par](peer-names.md) em mais de um computador. Normalmente, isso acontece se um nome de par estiver associado a uma pessoa que usa mais de um computador. Um método que você pode usar para registrar o mesmo nome de par em vários computadores é criar um grupo de pares para a pessoa e conectar-se a esse grupo de todos os computadores. Outro método é criar uma identidade de mesmo nível e um nome de par em um computador, exportar a identidade do par desse computador e importá-la em outros computadores. Isso permite que o mesmo nome de par seguro seja criado em todos os computadores que importaram a identidade de par.

 

 




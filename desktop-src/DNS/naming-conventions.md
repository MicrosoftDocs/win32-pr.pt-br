---
title: Convenções de nomenclatura
description: As convenções de nomenclatura compartilham uma meta comum para resolver de forma não ambígua um nome para um endereço de rede, geralmente um endereço IP. A diferença entre as convenções de nomenclatura está na abordagem distinta de cada Convenção para resolver nomes.
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2091123ed2bf1022910231cd08cb0e6cccae51a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005803"
---
# <a name="naming-conventions"></a>Convenções de nomenclatura

As convenções de nomenclatura compartilham uma meta comum: para resolver inequivocamente um nome para um endereço de rede, geralmente um endereço IP. A diferença entre as convenções de nomenclatura está na abordagem distinta de cada Convenção para resolver nomes.

As seguintes convenções de nomenclatura são usadas para identificar computadores em vários métodos de resolução de nomes de sistema, incluindo o método do Windows 2000:

-   [Nome do computador](#computer-name)
-   [Nome do host](#host-name)
-   [FQDN (nome de domínio totalmente qualificado)](#fully-qualified-domain-name)
-   [Nome distinto relativo](#relative-distinguished-name)

## <a name="computer-name"></a>Nome do Computador

No espaço de nome NetBIOS simples, um único nome resolve de forma inequívoca um nome de computador para um endereço de rede. Esse é o nome que as versões anteriores do Windows armazenaram nas listas navegador e navegador mestre, permitindo que redes Windows de mesmo nível procurem recursos em computadores com Windows em rede. Nesse cenário, o termo associado ao computador era nome do *computador*. O registro do nome do computador depende de difusões de rede (e de um navegador mestre, determinado pelas eleições ganhas por números de versão posteriores do Windows ou pelo uso do Windows NT ou uma combinação). Isso era útil para redes pequenas e baseadas em pares do Windows, mas redes em breve cresceram além do que o uso de difusões e listas simples de navegadores de arquivos simples podem ser atendidos.

## <a name="host-name"></a>Nome de host

Em seguida, vieram o Windows Internet Serviço de Nomenclatura (WINS), que permitia um repositório dinâmico e centralizado de nomes de computadores baseados em NetBIOS armazenados em servidores WINS. Esses repositórios podem atender a uma rede maior. Com esse desenvolvimento, as consultas de resolução de nomes podem ser direcionadas para um servidor WINS (em vez de serem transmitidas) e os conflitos poderiam ser centralizados centralmente. Com o WINS, o termo nome do computador foi retido, mas o termo *nome do host* também apareceu e foi usado de forma intercambiável com o nome do computador. No momento, o WINS era o resolvedor de nome padrão para plataformas Windows, mas o DNS estava ganhando a popularidade e proliferação de redes maiores e maiores.

As redes cresceram e o WINS tornou-se menos capaz de lidar com o crescente volume de nomes. A capacidade de redução do WINS para lidar com a carga de resolução de nomes não foi devido à capacidade de processamento necessária para a resolução, mas, em vez disso, o fato de gerar nomes exclusivos para muitos computadores se tornou uma sobrecarga de gerenciamento cada vez maior.

## <a name="fully-qualified-domain-name"></a>Nome do Domínio Totalmente Qualificado

O DNS é uma solução melhor; com seu espaço de nome hierárquico, a necessidade de nomes de computador exclusivos é isolada para um determinado domínio, permitindo que um nome de computador, como *Server1* , exista em diferentes locais de domínio na mesma hierarquia. Com a capacidade de ter o mesmo nome de host em domínios diferentes, a necessidade surgiu para um nome que resolveu corretamente a hierarquia de DNS. O nome tinha que incluir não apenas o nome do computador ou o nome do host, mas também um nome que poderia identificar, ou qualificar totalmente, esse computador dentro de toda a hierarquia DNS. Esse nome é o FQDN ( [*nome de domínio totalmente qualificado*](f-gly.md) ) — por exemplo, server1.widgets.Microsoft.com.

No entanto, em determinadas situações, a parte da hierarquia de domínio do FQDN é complicada e um nome local para um determinado computador (ou qualquer outro host DNS) relativo ao domínio DNS no qual o host reside é necessário. Esse nome é o [*nome distinto relativo*](r-gly.md). O nome distinto relativo é simplesmente o nome de host único à esquerda do ponto mais à direita no FQDN, de modo que um FQDN de server1.widgets.microsoft.com tenha Server1 como seu nome diferenciado relativo.

## <a name="relative-distinguished-name"></a>Nome distinto relativo

Em vez de impor novos nomes ou novas convenções de nomenclatura aos usuários de nomes NetBIOS, o DNS simplesmente usa o nome do computador (nome do host) como o nome distinto relativo e acrescenta a hierarquia de domínio DNS a esse nome para criar o FQDN. A figura a seguir ilustra como identificar a parte do nome do computador (ou nome do host ou nome distinto relativo) do FQDN:

![o RDN e a hierarquia de domínio DNS se combinam para criar um FQDN](images/fqdn.png)

 

 





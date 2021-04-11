---
title: Priorização de destino do servidor DFS
description: A priorização de destino do servidor DFS é um recurso disponível no Microsoft Windows Server 2003 com Service Pack 1 (SP1) e sistemas operacionais posteriores.
ms.assetid: 0aacebf7-49cc-4287-a5c4-0d25a416d227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e784a540a67f624ca5b8075009cd862c6063427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164155"
---
# <a name="dfs-server-target-prioritization"></a>Priorização de destino do servidor DFS

A priorização de destino do servidor DFS é um recurso disponível no Microsoft Windows Server 2003 com Service Pack 1 (SP1) e sistemas operacionais posteriores. Esse recurso permite que os servidores DFS tirem proveito do Active Directory informações de custo de site disponíveis para priorizar os destinos nas referências do cliente.

Antes do Windows Server 2003 com SP1, os destinos foram agrupados em dois conjuntos: um grupo para conter todos os destinos no mesmo site que o cliente; e outro grupo para todos os outros destinos. Esses destinos que compartilham o mesmo site que o cliente são chamados "no local" e, se o custo do site estiver habilitado, eles receberão um valor de custo específico relativo ao site em geral, com custos de site mais baixos preferenciais mais altos.

Com a disponibilidade desses dados de custo de site, os destinos de servidor podem ser priorizados para estratégias de failover de servidor DFS mais eficazes. No passado, esse nível granular de detalhes não estava disponível, e os administradores tinham que recorrer a meios artificiais (como sites fictícios no AD) para dar suporte a requisitos ainda simples, como a designação de servidores específicos como um servidor de "backup" ou "secundário" no caso em que um servidor DFS "primário" falha. Agora, com os detalhes adicionais fornecidos pelas estratégias de failover de vários níveis e de custo de site, é possível.

A discussão a seguir pressupõe que o custo do site está habilitado.

## <a name="target-prioritization"></a>Priorização de destino

A prioridade de destino é uma ordem específica de uma perspectiva administrativa, classificando e classificando servidores no site em termos de preferência explícita com base no custo do site de um cliente DFS. A prioridade global é independente do custo do site. Observe que as classes de prioridade global não indicam necessariamente os destinos mais ideais da perspectiva de um cliente de DFS, mas sim a importância, ou a falta de importância, de destinos específicos da perspectiva de um administrador de site.

A prioridade de destino do servidor é dividida em duas categorias de valor: classe de prioridade e classificação de prioridade. As classes de prioridade são divididas em dois níveis: local e global. Nessas classes, há uma ordem aproximada dos destinos com base no custo do site, agrupados como alta, normal e baixa prioridade. O resultado é cinco classes de prioridade, de acordo com a prioridade mais alta para a mais baixa, como a seguir:

- Alta prioridade global
- Prioridade alta de custo de site
- Prioridade normal de custo do site
- Prioridade baixa de custo de site
- Prioridade baixa global

As classes de custo de site podem ser consideradas como subdivisãos de "prioridade normal global". A classificação de prioridade é uma classificação de inteiro simples com base em valores ordinais: 0, 1, 2 e em diante, sendo que 0 é o valor mais alto e todos os valores subsequentes que indicam a classificação decrescente.

As prioridades globais alta e baixa não consideram os valores de custo de site. Destinos com uma preferência de recebimento de alta prioridade global em todos os outros destinos e destinos com uma prioridade baixa global recebem a preferência menos.

Ao ordenar uma referência, o processo completo tem as seguintes etapas:

1. Os conjuntos de destinos global alto e baixo são identificados, juntamente com os destinos "globais normais" restantes.
2. Se a opção "Insite" for definida, todos os destinos fora do site do cliente serão removidos. A opção "Insite" não é aplicada aos conjuntos de prioridade global alta e baixa.
3. Em cada um desses três conjuntos, os destinos são ordenados usando o mecanismo de custo de site do AD, usando o custo local ou de site completo. O resultado são conjuntos de destinos de custo de site igual.
4. Dentro dos conjuntos de destinos "globais normais" de custo de site igual, os destinos são atribuídos a uma classe de prioridade das classificações de prioridade alta, normal e baixa de custo do site.
5. Dentro dos conjuntos de destinos de classe de prioridade e custo de site igual, os destinos agora são ordenados por classificação de prioridade, sendo que 0 é a classificação mais alta.
6. Dentro dos conjuntos de destinos de custo de site igual, classe de prioridade e classificação de prioridade, os destinos são aleatoriamente aleatórios para balanceamento de carga.

Graficamente, um conjunto de destinos é ordenado como mostrado abaixo:

- destinos de classe de alta prioridade global 
- destinos de classe de alta prioridade de custo de site com custo do site = 0
- normal com custo do site = 0
- baixo com custo do site = 0
- destinos de classe de alta prioridade de custo de site com custo de site = 1
- normal com custo do site = 1
- baixo com custo do site = 1
- e assim por diante
- destinos de classe de baixa prioridade global

Dentro de cada um desses conjuntos, os destinos são classificados de acordo com a classificação de prioridade. A classificação mais alta é zero, com cada valor inteiro subsequente (1, 2 e assim por diante) indicando uma classificação cada vez mais baixa.

A prioridade de destino é definida em um destino específico de um link (ou raiz) em um namespace do DFS. A prioridade de um destino para um link não influenciará a ordenação de outros links se o mesmo caminho de destino for usado várias vezes. Por exemplo, se dois links tiverem \\ \\ \\ o servidor share1 como um destino, a prioridade do \\ \\ servidor \\ share1 será definida separadamente para ambos os links.

A prioridade padrão para todos os links é a prioridade normal de custo de site com uma classificação de 0. A prioridade de destino não afeta a ordenação de referências, a menos que seja usada, e todos os links existentes são ordenados à medida que são recebidos.

A resposta de referência de um servidor DFS consiste em conjuntos de destino ordenados conforme indicado acima, com cada conjunto de destino não global que contém destinos do mesmo custo do site, classe de prioridade e classificação de prioridade. Os destinos dentro de cada conjunto são ordenados aleatoriamente. Clientes DFS que recebem a referência começam com o primeiro destino do primeiro conjunto e continuam na lista até que um destino disponível para uma determinada raiz ou link do DFS seja encontrado.

Para a implementação de API específica desse recurso, consulte os seguintes tópicos de referência:

[**DFS_INFO_6**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6) 
 [**DFS_INFO_104**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104) 
 [**DFS_INFO_106**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106) 
 [**DFS_TARGET_PRIORITY**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority) 
 [**DFS_TARGET_PRIORITY_CLASS**](/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1)

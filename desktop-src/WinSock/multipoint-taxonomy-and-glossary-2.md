---
description: A taxonomia descrita abaixo primeiro distingue o plano de controle que se preocupa com a maneira como uma sessão do MultiPoint é estabelecida, do plano de dados que lida com a transferência de dados entre os participantes da sessão.
ms.assetid: d138347a-826a-4615-afbd-ffa7726a47eb
title: Glossário e taxonomia do MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ecdfe59640ec58b592aace4e46c66faf752281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810207"
---
# <a name="multipoint-taxonomy-and-glossary"></a>Glossário e taxonomia do MultiPoint

A taxonomia descrita abaixo primeiro distingue o plano de controle que se preocupa com a maneira como uma sessão do MultiPoint é estabelecida, do plano de dados que lida com a transferência de dados entre os participantes da sessão.

No plano de controle, há dois tipos distintos de estabelecimento de sessão:

-   com raiz
-   não raiz

Para um plano de controle com raiz, existe um participante especial, chamado c \_ root, que é diferente do restante dos membros dessa sessão do MultiPoint, sendo que cada um é chamado de folha c \_ . A \_ raiz c deve permanecer presente por toda a duração da sessão do MultiPoint, pois a sessão será dividida na ausência da \_ raiz c. A \_ raiz c geralmente inicia a sessão do MultiPoint Configurando a conexão com uma \_ folha c ou um número de folhas c \_ . A \_ raiz c pode adicionar mais \_ folhas c ou (em alguns casos) uma folha c \_ pode unir a raiz c \_ em um momento posterior. Exemplos do plano de controle com raiz podem ser encontrados em ATM e ST-II.

Para um plano de controle não raiz, todos os membros que pertencem a uma sessão do MultiPoint são folhas, ou seja, nenhum participante especial atuando como uma \_ raiz c existe. Cada \_ folha c precisa se adicionar a uma sessão do MultiPoint pré-existente que está sempre disponível (como no caso de um endereço IP multicast) ou foi configurada por meio de um mecanismo OOB que está fora do escopo desta discussão (e, portanto, não resolvida nas extensões propostas do Windows Sockets). Outra maneira de examinar isso é que uma raiz c \_ ainda existe, mas pode ser considerada na nuvem de rede, em oposição a um dos participantes. Como uma raiz de controle ainda existe, um plano de controle não-raiz também poderia ser considerado implicitamente enraizada. Exemplos desse tipo de esquemas MultiPoint com raiz implícita são: uma ponte de teleconferência, o sistema multicast IP, uma MCU (unidade de controle do MultiPoint) em uma conferência de vídeo H. 320 etc.

No plano de dados, há também dois tipos de estilos de transferência de dados:

-   com raiz
-   não raiz

Em um plano de dados com raiz, existe um participante especial chamado d \_ root. A transferência de dados ocorre apenas entre a \_ raiz d e o restante dos membros dessa sessão do MultiPoint, sendo que cada uma delas é conhecida como \_ folha d. O tráfego pode ser unidirecional ou bidirecional. Os dados enviados da \_ raiz d serão duplicados (se necessário) e entregues a cada \_ folha d, enquanto os dados de \_ folhas d só vão para a \_ raiz d. No caso de um plano de dados com raiz, não há nenhum tráfego permitido entre \_ folhas d. Um exemplo de um protocolo que usa um plano de dados com raiz é ST-II.

Em um plano de dados não-raiz, todos os participantes são iguais no sentido de que todos os dados enviados serão entregues a todos os outros participantes na mesma sessão do MultiPoint. Da mesma forma \_ , cada nó de folha d poderá receber dados de todas as outras folhas de d \_ e, em alguns casos, de outros nós que não estão participando da sessão do MultiPoint também. Não existe nenhum \_ nó raiz d especial. IP-multicast é um exemplo de um protocolo que usa um plano de dados não-raiz.

Observe que a pergunta de onde ocorre a duplicação da unidade de dados ou se uma única árvore compartilhada ou várias árvores de caminho mais curto são usadas para a distribuição do MultiPoint são problemas de protocolo. Assim, eles são irrelevantes para a interface que o cliente usaria para executar comunicações do MultiPoint. Portanto, esses problemas não são tratados pela interface do Windows Sockets.

A tabela a seguir descreve a taxonomia descrita acima e indica como os esquemas existentes se encaixam em cada uma das categorias de controle e de plano de dados. Observe que não parece haver nenhum esquema do MultiPoint que empregue um plano de controle sem raiz junto com um plano de dados com raiz.

| Plano de dados           | Exemplos de plano de controle com raiz | Exemplos de plano de controle não raiz (com raiz implícita) |
|----------------------|-------------------------------|----------------------------------------------------|
| Plano de dados com raiz    | ATM, ST-II                    | Nenhum exemplo conhecido                                  |
| Plano de dados não raiz | T. 120                         | IP-multicast, H. 320 (MCU)                          |



 

 

 




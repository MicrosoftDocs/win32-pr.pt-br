---
description: A taxonomia descrita nesta seção primeiro distingue o plano de controle que se preocupa com a maneira como uma sessão do MultiPoint é estabelecida, do plano de dados que lida com a transferência de dados entre os participantes da sessão.
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Taxonomia do MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97159312a2e431cb82b73336a13904c6b5ab021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827109"
---
# <a name="multipoint-taxonomy"></a>Taxonomia do MultiPoint

A taxonomia descrita nesta seção primeiro distingue o plano de controle que se preocupa com a maneira como uma sessão do MultiPoint é estabelecida, do plano de dados que lida com a transferência de dados entre os participantes da sessão.

## <a name="session-establishment-in-the-control-plane"></a>Estabelecimento de sessão no plano de controle

No plano de controle, há dois tipos distintos de estabelecimento de sessão:

-   com raiz
-   não raiz

No caso do controle com raiz, um participante especial, a \_ raiz c, que é diferente do restante dos membros dessa sessão do MultiPoint, cada um deles é chamado de \_ folha c. A \_ raiz c deve permanecer presente por toda a duração da sessão do MultiPoint, pois a sessão é dividida na ausência da \_ raiz c. A \_ raiz c geralmente inicia a sessão do MultiPoint Configurando a conexão com uma \_ folha c ou um número de folhas c \_ . A \_ raiz c pode adicionar mais \_ folhas c ou (em alguns casos) uma folha c \_ pode unir a raiz c \_ em um momento posterior. Exemplos do plano de controle com raiz podem ser encontrados em ATM e ST-II.

Para um plano de controle não raiz, todos os membros que pertencem a uma sessão do MultiPoint são folhas, ou seja, nenhum participante especial agindo como uma \_ raiz c existe. Cada \_ folha c deve se adicionar a uma sessão do MultiPoint pré-existente que está sempre disponível (como no caso de um endereço IP multicast) ou foi configurada por meio de um mecanismo OOB (fora de banda) que está fora do escopo da especificação do Windows Sockets.

Outra maneira de examinar isso é que uma raiz c \_ ainda existe, mas pode ser considerada na nuvem de rede, em oposição a um dos participantes. Como uma raiz de controle ainda existe, um plano de controle não-raiz também poderia ser considerado implicitamente enraizada. Exemplos para esse tipo de esquemas MultiPoint com raiz implícita são:

-   Uma ponte de teleconferência.
-   O sistema multicast IP.
-   Uma MCU (unidade de controle do MultiPoint) em uma conferência de vídeo H. 320.

## <a name="data-transfer-in-the-data-plane"></a>Transferência de Dados no plano de dados

No plano de dados, há dois tipos de estilos de transferência de dados:

-   com raiz
-   não raiz

Em um plano de dados com raiz, existe um participante especial chamado d \_ root. A transferência de dados ocorre apenas entre a \_ raiz d e o restante dos membros dessa sessão do MultiPoint, sendo que cada uma delas é conhecida como \_ folha d. O tráfego pode ser unidirecional ou bidirecional. Os dados enviados da \_ raiz d são duplicados (se necessário) e entregues a cada \_ folha d, enquanto os dados de folhas d \_ vão apenas para a raiz d \_ . No caso de um plano de dados com raiz, nenhum tráfego é permitido entre \_ folhas d. Um exemplo de um protocolo com raiz no plano de dados é ST-II.

Em um plano de dados não raiz, todos os participantes são iguais, ou seja, todos os dados que eles enviam são entregues a todos os outros participantes na mesma sessão do MultiPoint. Da mesma forma \_ , cada nó de folha d pode receber dados de todas as outras folhas de d \_ e, em alguns casos, de outros nós que não estão participando da sessão do MultiPoint. Não existe nenhum \_ nó raiz d especial. IP-multicast não tem raiz no plano de dados.

Observe que a pergunta de onde ocorre a duplicação da unidade de dados ou se uma única árvore compartilhada ou várias árvores de caminho mais curto são usadas para a distribuição do MultiPoint são problemas de protocolo e é irrelevante para a interface que o aplicativo usaria para executar comunicações do MultiPoint. Portanto, esses problemas não são abordados neste apêndice ou na interface do Windows Sockets.

A tabela a seguir descreve a taxonomia descrita acima e indica como os esquemas existentes se encaixam em cada uma das categorias. Observe que não parece haver nenhum esquema existente que empregue um plano de controle sem raiz junto com um plano de dados com raiz.

|                      | Plano de controle com raiz | Plano de controle não raiz (com raiz implícita) |
|----------------------|----------------------|-------------------------------------------|
| Plano de dados com raiz    | ATM, ST-II           | Nenhum exemplo conhecido.                        |
| Plano de dados não raiz | T. 120                | IP-multicast, H. 320 (MCU)                 |



 

 

 




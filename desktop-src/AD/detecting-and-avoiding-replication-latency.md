---
title: Detectando e evitando a latência de replicação
description: A latência de replicação é um fato da vida em um sistema distribuído menos rígido.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634975"
---
# <a name="detecting-and-avoiding-replication-latency"></a>Detectando e evitando a latência de replicação

A latência de replicação é um fato da vida em um sistema distribuído menos rígido. Os aplicativos devem acomodar isso. A melhor maneira de acomodar a latência de replicação é projetar aplicativos para minimizar os efeitos. O aplicativo habilitado para diretório ideal:

-   Não é sensível à distorção de versão.
-   Não depende de relações entre vários objetos.
-   Não tem requisitos de consistência dentro ou entre objetos.

Os aplicativos e serviços que se ajustam a esse perfil não precisam se preocupar com a latência de replicação. Outros aplicativos devem ser projetados com a latência de replicação em mente. A chave para o sucesso na criação de um aplicativo desse tipo é a percepção do processo de replicação. Etapas executadas em tempo de design para reduzir dependências entre objetos e minimizar as janelas de atualização parciais pagarão grandes dividendos em tempo de execução. As abordagens para lidar com a latência de replicação são divididas em duas classes — evitam estratégias que reduzem o impacto da latência e das estratégias de detecção que permitem que um aplicativo detecte Estados induzidos por latência.

 

 





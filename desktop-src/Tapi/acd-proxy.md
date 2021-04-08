---
description: Um servidor AD (distribuição de chamada automática) é uma combinação de hardware e software que classifica, enfileira e distribui chamadas de entrada para agentes ou chamadas de saída para linhas.
ms.assetid: 29fb0bd7-0ca9-4490-82d2-39550f00a97b
title: Proxy AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c345fbcac3ac3471098e964336a0c3135fd1f582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922220"
---
# <a name="acd-proxy"></a>Proxy AD

Um servidor AD (distribuição de chamada automática) é uma combinação de hardware e software que classifica, enfileira e distribui chamadas de entrada para agentes ou chamadas de saída para linhas.

O aplicativo servidor AD é um aplicativo de proxy TAPI, que para eficiência máxima deve ser executado no mesmo servidor que o TSP (provedor de serviços de telefonia). Com uma opção AD tradicional, o aplicativo proxy faria a interface com o AD interno do comutador e Expose sua operação. Um aplicativo de proxy AD "virtual" ou baseado em software seria totalmente responsável pelo acompanhamento de chamadas, filas, grupos e agentes e usaria as interfaces TAPI padrão para controlar o hardware de alternância. Os aplicativos cliente do Agent normalmente serão executados nas estações de trabalho do agente individual e usarão o provedor de serviço TAPI remoto para se comunicar com o TAPISRV no computador do servidor e, portanto, o aplicativo proxy.

A classificação de chamadas de entrada foi projetada para obter uma chamada para um agente que poderá tratá-lo com eficiência. A classificação pode ser baseada no número discado, em um sistema IVR (reconhecimento de voz interativo) ou em outros critérios. A TAPI usa o conceito de um [grupo de AD](about-call-center-controls.md) para representar essa operação.

As filas são uma maneira normal e esperada para que os centros de chamadas lidem com períodos de carga pesadas. Uma fila é normalmente associada a um grupo ad, mas pode ser criada para lidar com linhas de saída ou chamadas de entrada aguardando um aplicativo de IVR. Consulte [filas](about-call-center-controls.md) para obter mais informações.

A distribuição de chamadas para agentes ou grupos de agentes pode ser uniforme, mas normalmente se baseia em dados como informações de chamada, disponibilidade do agente e capacidade. O [manipulador de agentes](about-call-center-controls.md) da TAPI fornece acesso a informações como a disponibilidade do agente e endereços para a transferência de chamadas para agentes.

Além da distribuição básica de chamadas, um sistema ad fornece o gerenciamento e a emissão de relatórios sobre o desempenho do sistema. As estatísticas coletadas em filas de chamadas, grupos e agentes são usadas para refinar e aprimorar o desempenho do sistema e normalmente são usadas como base para o Remuneration do agente.

 

 




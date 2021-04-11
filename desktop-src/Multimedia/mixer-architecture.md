---
title: Arquitetura do mixer
description: Arquitetura do mixer
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- áudio multimídia, arquitetura do mixer
- áudio, arquitetura do mixer
- mixers de áudio, arquitetura
- mixers de áudio, linhas de áudio
- linhas de áudio
- mixers de áudio, controles
- áudio de multimídia, controles de mixer
- áudio, controles de mixer
- mixers, linhas de áudio
- mixers, arquitetura
- mixers, controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292135"
---
# <a name="mixer-architecture"></a>Arquitetura do mixer

O elemento básico da arquitetura do mixer é uma *linha de áudio*. Uma linha de áudio consiste em um ou mais canais de dados provenientes de uma única fonte ou um recurso do sistema. Por exemplo, uma linha de áudio estéreo tem dois canais de dados, mas é considerada uma única linha de áudio porque ela se origina de uma única fonte.

A arquitetura do mixer fornece serviços de roteamento para gerenciar linhas de áudio em um computador. Você pode usar os serviços de roteamento se tiver dispositivos de hardware e drivers de software adequados instalados. A arquitetura do mixer permite que várias linhas de origem de áudio sejam mapeadas para uma única linha de áudio de destino.

Cada linha de áudio pode ter controles de mixer associados a ela. Um controle de mixer pode executar qualquer número de funções (como o volume de controle), dependendo das características da linha de áudio associada.

 

 





---
title: Mixer Arquitectura
description: Mixer Arquitectura
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
ms.openlocfilehash: c3f435396dd2a8d5983f596628711dfd01afe7111e75af1dc2060f5c6c4ef0a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065606"
---
# <a name="mixer-architecture"></a>Mixer Arquitectura

O elemento básico da arquitetura do mixer é uma *linha de áudio*. Uma linha de áudio consiste em um ou mais canais de dados provenientes de uma única fonte ou um recurso do sistema. Por exemplo, uma linha de áudio estéreo tem dois canais de dados, mas é considerada uma única linha de áudio porque ela se origina de uma única fonte.

A arquitetura do mixer fornece serviços de roteamento para gerenciar linhas de áudio em um computador. Você pode usar os serviços de roteamento se tiver dispositivos de hardware e drivers de software adequados instalados. A arquitetura do mixer permite que várias linhas de origem de áudio sejam mapeadas para uma única linha de áudio de destino.

Cada linha de áudio pode ter controles de mixer associados a ela. Um controle de mixer pode executar qualquer número de funções (como o volume de controle), dependendo das características da linha de áudio associada.

 

 





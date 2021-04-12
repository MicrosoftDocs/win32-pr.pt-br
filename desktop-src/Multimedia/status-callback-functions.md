---
title: Funções de retorno de chamada de status
description: Funções de retorno de chamada de status
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Funções de retorno de chamada AVICap, status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364000"
---
# <a name="status-callback-functions"></a>Funções de retorno de chamada de status

Uma janela de captura pode enviar mensagens para a função de retorno de chamada de status durante a captura de vídeo em disco ou durante outras operações demoradas para notificar seu aplicativo sobre o progresso de uma operação. As informações de status incluem um identificador de mensagem e uma cadeia de texto formatada pronta para exibição. Seu aplicativo pode usar o identificador de mensagem para filtrar as notificações e limitar as mensagens a apresentar ao usuário. Durante as operações de captura, a primeira mensagem enviada para a função de retorno de chamada é sempre IDS \_ \_ de início e a última é sempre IDs \_ \_ end. Um identificador de mensagem igual a zero indica que uma nova operação está sendo iniciada e a função de retorno de chamada deve limpar o status atual.

 

 





---
title: Funções de retorno de chamada de status
description: Funções de retorno de chamada de status
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Funções de retorno de chamada AVICap, status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07539b016ea344f2a38d54a7274d01006532ed040ea3fa96990bff09e22d470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037156"
---
# <a name="status-callback-functions"></a>Funções de retorno de chamada de status

Uma janela de captura pode enviar mensagens para a função de retorno de chamada de status durante a captura de vídeo no disco ou durante outras operações demoradas para notificar seu aplicativo sobre o progresso de uma operação. As informações de status incluem um identificador de mensagem e uma cadeia de caracteres de texto formatada pronta para exibição. Seu aplicativo pode usar o identificador de mensagem para filtrar as notificações e limitar as mensagens a apresentar ao usuário. Durante as operações de captura, a primeira mensagem enviada para a função de retorno de chamada é sempre IDS CAP BEGIN e a última \_ \_ é sempre IDS \_ CAP \_ END. Um identificador de mensagem zero indica que uma nova operação está iniciando e a função de retorno de chamada deve limpar o status atual.

 

 





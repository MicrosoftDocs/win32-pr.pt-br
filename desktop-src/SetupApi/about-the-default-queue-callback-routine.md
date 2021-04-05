---
description: A rotina de retorno de chamada de fila padrão manipula as notificações enviadas pelo SetupCommitFileQueue de maneira genérica.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: Sobre a rotina de retorno de chamada de fila padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827019"
---
# <a name="about-the-default-queue-callback-routine"></a>Sobre a rotina de retorno de chamada de fila padrão

A rotina de retorno de chamada de fila padrão manipula as notificações enviadas pelo [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) de maneira genérica. Usando a rotina padrão, você obtém uma interface do usuário pronta para criar caixas de diálogo de instalação comuns. É recomendável que você use a rotina de retorno de chamada de fila padrão, tanto para facilitar o uso quanto para garantir uma aparência e comportamento consistentes das caixas de diálogo geradas durante a instalação.

A rotina de retorno de chamada padrão requer uma estrutura de contexto para manter o registro interno. Além disso, a fila passa informações adicionais relevantes para a notificação atual em um conjunto de parâmetros, *param1* e *param2*.

Por exemplo, se a fila enviar uma \_ notificação SPFILENOTIFY NEEDMEDIA para a rotina de retorno de chamada padrão, o *param1* apontará para uma estrutura de [**\_ mídia de origem**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) que contém informações sobre a mídia necessária e *param2* aponta para uma matriz de caracteres que pode receber novas informações de caminho do usuário.

A rotina de retorno de chamada padrão usa essas informações para solicitar que o usuário insira a mídia de origem necessária, especifique um novo caminho, ignore a cópia do arquivo atual ou cancele a operação atual. A rotina de retorno de chamada de fila padrão retorna FILEOP \_ NEWPATH, FILEOP \_ doit, FILEOP \_ Skip ou FILEOP \_ Abort para a fila, dependendo de qual ação o usuário realizou.

Para obter informações sobre como a rotina de retorno de chamada de fila padrão manipula cada notificação de fila, consulte [notificações de fila de arquivos](file-queue-notifications.md).

Para obter informações sobre rotinas de retorno de chamada de fila personalizada, consulte [criando uma rotina de retorno de chamada de fila personalizada](creating-a-custom-queue-callback-routine.md).

 

 




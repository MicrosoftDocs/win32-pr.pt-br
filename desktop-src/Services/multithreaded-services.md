---
description: O SCM (Gerenciador de controle de serviço) controla um serviço enviando eventos de controle de serviço para a rotina do manipulador de controle de serviços.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Serviços multithread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5795a170f912050d115537407fcb491305a35ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748387"
---
# <a name="multithreaded-services"></a>Serviços multithread

O SCM (Gerenciador de controle de serviço) controla um serviço enviando eventos de controle de serviço para a rotina do manipulador de controle do serviço. O serviço deve responder a eventos de controle em tempo hábil para que o SCM possa acompanhar o estado do serviço. Além disso, o estado do serviço deve corresponder à descrição de seu estado que o SCM recebe.

Devido a esse mecanismo de comunicação entre um serviço e o SCM, você deve ter cuidado ao usar vários threads em um serviço. Quando um serviço é instruído a parar pelo SCM, ele deve aguardar a saída de todos os threads antes de reportar para o SCM que o serviço está parado. Caso contrário, o SCM pode ficar confuso sobre o estado do serviço e pode falhar ao desligar corretamente.

O SCM precisa ser notificado de que o serviço está respondendo ao evento de controle de parada e que o progresso está sendo feito na interrupção do serviço. O SCM assumirá que o serviço está progredindo se o serviço responder (por meio de [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) no tempo (dica de espera) especificado na chamada anterior para **falha em SetServiceStatus**, e o ponto de verificação será atualizado para ser maior que o ponto de verificação especificado na chamada anterior para **falha em SetServiceStatus**.

Se o serviço se reportar ao SCM que o serviço parou antes de todos os threads serem encerrados, é possível que o SCM interprete isso como uma contradição. Isso pode resultar em um estado em que o serviço não pode ser interrompido ou reiniciado.

 

 




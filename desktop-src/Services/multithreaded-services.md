---
description: O SCM (gerenciador de controle de serviço) controla um serviço enviando eventos de controle de serviço para a rotina do manipulador de controle de serviços.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Serviços multithread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32b4b51f740e0a3773115b9048ec34619910936f1531fba1260740df28873b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003724"
---
# <a name="multithreaded-services"></a>Serviços multithread

O SCM (gerenciador de controle de serviço) controla um serviço enviando eventos de controle de serviço para a rotina do manipulador de controle do serviço. O serviço deve responder aos eventos de controle em tempo hábil para que o SCM possa controlar o estado do serviço. Além disso, o estado do serviço deve corresponder à descrição de seu estado que o SCM recebe.

Devido a esse mecanismo de comunicação entre um serviço e o SCM, você deve ter cuidado ao usar vários threads em um serviço. Quando um serviço é instruído a parar pelo SCM, ele deve aguardar a saída de todos os threads antes de relatar ao SCM que o serviço está parado. Caso contrário, o SCM pode ficar confuso sobre o estado do serviço e pode não conseguir desligar corretamente.

O SCM precisa ser notificado de que o serviço está respondendo ao evento de controle de parada e que o progresso está sendo feito na interrupção do serviço. O SCM assumirá que o serviço está progredindo se o serviço responder (por meio de [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) dentro do tempo (dica de espera) especificado na chamada anterior para **SetServiceStatus** e o ponto de verificação for atualizado para ser maior que o ponto de verificação especificado na chamada anterior para **SetServiceStatus**.

Se o serviço relata ao SCM que o serviço foi interrompido antes de todos os threads sairem, é possível que o SCM interprete isso como um problema. Isso pode resultar em um estado em que o serviço não pode ser interrompido ou reiniciado.

 

 




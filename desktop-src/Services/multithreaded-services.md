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
# <a name="multithreaded-services"></a><span data-ttu-id="089fa-103">Serviços multithread</span><span class="sxs-lookup"><span data-stu-id="089fa-103">Multithreaded Services</span></span>

<span data-ttu-id="089fa-104">O SCM (Gerenciador de controle de serviço) controla um serviço enviando eventos de controle de serviço para a rotina do manipulador de controle do serviço.</span><span class="sxs-lookup"><span data-stu-id="089fa-104">The service control manager (SCM) controls a service by sending service control events to the service's control handler routine.</span></span> <span data-ttu-id="089fa-105">O serviço deve responder a eventos de controle em tempo hábil para que o SCM possa acompanhar o estado do serviço.</span><span class="sxs-lookup"><span data-stu-id="089fa-105">The service must respond to control events in a timely manner so that the SCM can keep track of the state of the service.</span></span> <span data-ttu-id="089fa-106">Além disso, o estado do serviço deve corresponder à descrição de seu estado que o SCM recebe.</span><span class="sxs-lookup"><span data-stu-id="089fa-106">Also, the state of the service must match the description of its state that the SCM receives.</span></span>

<span data-ttu-id="089fa-107">Devido a esse mecanismo de comunicação entre um serviço e o SCM, você deve ter cuidado ao usar vários threads em um serviço.</span><span class="sxs-lookup"><span data-stu-id="089fa-107">Due to this communication mechanism between a service and the SCM, you must be careful when using multiple threads in a service.</span></span> <span data-ttu-id="089fa-108">Quando um serviço é instruído a parar pelo SCM, ele deve aguardar a saída de todos os threads antes de reportar para o SCM que o serviço está parado.</span><span class="sxs-lookup"><span data-stu-id="089fa-108">When a service is instructed to stop by the SCM, it must wait for all the threads to exit before reporting to the SCM that the service is stopped.</span></span> <span data-ttu-id="089fa-109">Caso contrário, o SCM pode ficar confuso sobre o estado do serviço e pode falhar ao desligar corretamente.</span><span class="sxs-lookup"><span data-stu-id="089fa-109">Otherwise, the SCM can become confused about the state of the service and might fail to shut down correctly.</span></span>

<span data-ttu-id="089fa-110">O SCM precisa ser notificado de que o serviço está respondendo ao evento de controle de parada e que o progresso está sendo feito na interrupção do serviço.</span><span class="sxs-lookup"><span data-stu-id="089fa-110">The SCM needs to be notified that the service is responding to the stop control event and that progress is being made in stopping the service.</span></span> <span data-ttu-id="089fa-111">O SCM assumirá que o serviço está progredindo se o serviço responder (por meio de [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) no tempo (dica de espera) especificado na chamada anterior para **falha em SetServiceStatus**, e o ponto de verificação será atualizado para ser maior que o ponto de verificação especificado na chamada anterior para **falha em SetServiceStatus**.</span><span class="sxs-lookup"><span data-stu-id="089fa-111">The SCM will assume the service is making progress if the service responds (through [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) within the time (wait hint) specified in the previous call to **SetServiceStatus**, and the check point is updated to be greater than the checkpoint specified in the previous call to **SetServiceStatus**.</span></span>

<span data-ttu-id="089fa-112">Se o serviço se reportar ao SCM que o serviço parou antes de todos os threads serem encerrados, é possível que o SCM interprete isso como uma contradição.</span><span class="sxs-lookup"><span data-stu-id="089fa-112">If the service reports to the SCM that the service has stopped before all threads have exited, it is possible that the SCM will interpret this as a contradiction.</span></span> <span data-ttu-id="089fa-113">Isso pode resultar em um estado em que o serviço não pode ser interrompido ou reiniciado.</span><span class="sxs-lookup"><span data-stu-id="089fa-113">This might result in a state where the service cannot be stopped or restarted.</span></span>

 

 




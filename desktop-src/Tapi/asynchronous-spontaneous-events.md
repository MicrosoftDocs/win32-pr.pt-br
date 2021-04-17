---
description: Há outra classe de eventos assíncronos além daquelas descritas acima.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Eventos ESPONTANEOS assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780127"
---
# <a name="asynchronous-spontaneous-events"></a><span data-ttu-id="c2645-103">Eventos ESPONTANEOS assíncronos</span><span class="sxs-lookup"><span data-stu-id="c2645-103">Asynchronous Spontaneous Events</span></span>

<span data-ttu-id="c2645-104">Há outra classe de eventos assíncronos além daquelas descritas acima.</span><span class="sxs-lookup"><span data-stu-id="c2645-104">There is another class of asynchronous events besides those described above.</span></span> <span data-ttu-id="c2645-105">Esses eventos são "ESPONTANEOS", no sentido de que não são resultados diretos de solicitações correspondentes.</span><span class="sxs-lookup"><span data-stu-id="c2645-105">These events are "spontaneous" in the sense that they are not direct results of corresponding requests.</span></span> <span data-ttu-id="c2645-106">Esses eventos são detectados nesses casos como quando uma chamada de entrada chega ou quando uma chamada de saída passa de um "toque" para um estado de "resposta".</span><span class="sxs-lookup"><span data-stu-id="c2645-106">These events are detected in such cases as when an incoming call arrives, or when an outbound call goes from a "ringing" to an "answering" state.</span></span> <span data-ttu-id="c2645-107">Quando a TAPI Inicializa pela primeira vez as interações com o TSPI para um dispositivo específico, ele passa um ponteiro para um procedimento de retorno de chamada a ser chamado para relatar esses eventos ESPONTANEOS.</span><span class="sxs-lookup"><span data-stu-id="c2645-107">When TAPI first initializes interactions with the TSPI for a particular device, it passes a pointer to a callback procedure to be called for reporting such spontaneous events.</span></span> <span data-ttu-id="c2645-108">Juntamente com este ponteiro de procedimento há um identificador de dispositivo que o provedor de serviços inclui como um dos parâmetros reais para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c2645-108">Along with this procedure pointer is a device handle that the service provider includes as one of the actual parameters to the callback.</span></span>

 

 




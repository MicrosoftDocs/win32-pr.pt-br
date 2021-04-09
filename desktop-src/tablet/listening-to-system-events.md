---
description: Os aplicativos podem escutar eventos do sistema usando o objeto InkCollector e ouvindo o evento SystemGesture nele.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Ouvindo eventos do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011772"
---
# <a name="listening-to-system-events"></a><span data-ttu-id="70a2e-103">Ouvindo eventos do sistema</span><span class="sxs-lookup"><span data-stu-id="70a2e-103">Listening to System Events</span></span>

<span data-ttu-id="70a2e-104">Os aplicativos podem escutar eventos do sistema usando o objeto [**InkCollector**](inkcollector-class.md) e ouvindo o evento [**SystemGesture**](inkcollector-systemgesture.md) nele.</span><span class="sxs-lookup"><span data-stu-id="70a2e-104">Applications can listen to system events by using the [**InkCollector**](inkcollector-class.md) object and listening for the [**SystemGesture**](inkcollector-systemgesture.md) event on it.</span></span> <span data-ttu-id="70a2e-105">Você pode definir quais eventos um aplicativo ouve.</span><span class="sxs-lookup"><span data-stu-id="70a2e-105">You can set which events an application listens to.</span></span> <span data-ttu-id="70a2e-106">Quando ocorre uma ação da caneta do Tablet, o evento **SystemGesture** correspondente é enviado para o aplicativo em seu objeto **InkCollector** .</span><span class="sxs-lookup"><span data-stu-id="70a2e-106">When a tablet pen action occurs, the corresponding **SystemGesture** event is sent to the application on its **InkCollector** object.</span></span> <span data-ttu-id="70a2e-107">Um aplicativo pode cancelar a mensagem do mouse que corresponde a um determinado evento **SystemGesture** quando recebe o evento.</span><span class="sxs-lookup"><span data-stu-id="70a2e-107">An application can cancel the mouse message that corresponds to a given **SystemGesture** event when it receives the event.</span></span> <span data-ttu-id="70a2e-108">Para obter detalhes sobre como cancelar mensagens do mouse, consulte evento **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="70a2e-108">For details about canceling mouse messages, see **SystemGesture** event.</span></span>

 

 




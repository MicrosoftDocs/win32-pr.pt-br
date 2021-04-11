---
description: Usando WPUCloseEvent para destruir um objeto de evento (aplicativo ou provedor de serviços) quando o objeto de evento não é mais necessário.
ms.assetid: ad6f7018-3647-4ab8-9a77-d833d18cd4b6
title: Destruindo objetos de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f0a17f623d0dd9ebceaf76b963ce72306000b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296357"
---
# <a name="destroying-event-objects"></a><span data-ttu-id="4e0d8-103">Destruindo objetos de evento</span><span class="sxs-lookup"><span data-stu-id="4e0d8-103">Destroying Event Objects</span></span>

<span data-ttu-id="4e0d8-104">A entidade que cria um objeto de evento (aplicativo ou provedor de serviços) é responsável por destruí-lo quando ele não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="4e0d8-104">The entity that creates an event object (application or service provider) is responsible for destroying it when it is no longer required.</span></span> <span data-ttu-id="4e0d8-105">Os provedores de serviço fazem isso por meio de **WPUCloseEvent**.</span><span class="sxs-lookup"><span data-stu-id="4e0d8-105">Service providers do this through **WPUCloseEvent**.</span></span>

 

 




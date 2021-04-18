---
description: Os exemplos de aplicativo WMI nesta seção são escritos em C++.
ms.assetid: 5c4c4c4c-adbc-4702-a6fe-5f98a6db3ba1
ms.tgt_platform: multiple
title: Exemplos de aplicativos WMI C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883b51bd00de5e3938fef8467c68d299ac60683a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811462"
---
# <a name="wmi-c-application-examples"></a><span data-ttu-id="62eac-103">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="62eac-103">WMI C++ Application Examples</span></span>

<span data-ttu-id="62eac-104">Os exemplos de aplicativo WMI nesta seção são escritos em C++.</span><span class="sxs-lookup"><span data-stu-id="62eac-104">The WMI application examples in this section are written in C++.</span></span> <span data-ttu-id="62eac-105">Eles demonstram uma variedade de tarefas que podem ser concluídas usando componentes WMI e oferecem uma alternativa em relação ao uso de scripts Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="62eac-105">They demonstrate a range of tasks that can be completed using WMI components and offer an alternative over using Visual Basic scripts.</span></span> <span data-ttu-id="62eac-106">Cada aplicativo é separado em uma série de etapas de forma semelhante, para que as seções de código de exemplos diferentes possam ser facilmente combinadas para formar aplicativos personalizados.</span><span class="sxs-lookup"><span data-stu-id="62eac-106">Each application is separated into a series of steps in a similar way so that code sections from different examples can easily be combined to form customized applications.</span></span>

<span data-ttu-id="62eac-107">A tabela a seguir lista os exemplos de C++ nesta seção.</span><span class="sxs-lookup"><span data-stu-id="62eac-107">The following table lists the C++ examples in this section.</span></span>



| <span data-ttu-id="62eac-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="62eac-108">Example</span></span>                                                                                                                                  | <span data-ttu-id="62eac-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="62eac-109">Description</span></span>                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62eac-110">Exemplo: obtendo dados WMI do computador local</span><span class="sxs-lookup"><span data-stu-id="62eac-110">Example: Getting WMI Data from the Local Computer</span></span>](example--getting-wmi-data-from-the-local-computer.md)                               | <span data-ttu-id="62eac-111">Este exemplo conecta-se ao namespace WMI no computador local e obtém dados de uma consulta no computador local.</span><span class="sxs-lookup"><span data-stu-id="62eac-111">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="62eac-112">Os dados são coletados semisynchronously.</span><span class="sxs-lookup"><span data-stu-id="62eac-112">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="62eac-113">Exemplo: obtendo dados do WMI do computador local de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="62eac-113">Example: Getting WMI Data from the Local Computer Asynchronously</span></span>](example--getting-wmi-data-from-the-local-computer-asynchronously.md) | <span data-ttu-id="62eac-114">Este exemplo conecta-se ao namespace WMI no computador local e obtém dados de uma consulta no computador local.</span><span class="sxs-lookup"><span data-stu-id="62eac-114">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="62eac-115">Os dados são coletados de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="62eac-115">The data is gathered asynchronously.</span></span>    |
| [<span data-ttu-id="62eac-116">Exemplo: obtendo dados WMI de um computador remoto</span><span class="sxs-lookup"><span data-stu-id="62eac-116">Example: Getting WMI Data from a Remote Computer</span></span>](example--getting-wmi-data-from-a-remote-computer.md)                                 | <span data-ttu-id="62eac-117">Este exemplo conecta-se ao namespace do WMI em um computador remoto e obtém dados de uma consulta no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="62eac-117">This example connects to the WMI namespace on a remote computer and gets data from a query on the remote computer.</span></span> <span data-ttu-id="62eac-118">Os dados são coletados semisynchronously.</span><span class="sxs-lookup"><span data-stu-id="62eac-118">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="62eac-119">Exemplo: chamando um método de provedor</span><span class="sxs-lookup"><span data-stu-id="62eac-119">Example: Calling a Provider Method</span></span>](example--calling-a-provider-method.md)                                                             | <span data-ttu-id="62eac-120">Este exemplo conecta-se ao namespace WMI no computador local e chama um método no WMI.</span><span class="sxs-lookup"><span data-stu-id="62eac-120">This example connects to the WMI namespace on the local computer and calls a method in WMI.</span></span> <span data-ttu-id="62eac-121">O método é executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="62eac-121">The method is executed synchronously.</span></span>                          |
| [<span data-ttu-id="62eac-122">Exemplo: recebendo notificações de eventos por meio do WMI</span><span class="sxs-lookup"><span data-stu-id="62eac-122">Example: Receiving Event Notifications Through WMI</span></span>](example--receiving-event-notifications-through-wmi-.md)                            | <span data-ttu-id="62eac-123">Este exemplo conecta-se ao namespace WMI no computador local e recebe um evento do computador local.</span><span class="sxs-lookup"><span data-stu-id="62eac-123">This example connects to the WMI namespace on the local computer and receives an event from the local computer.</span></span> <span data-ttu-id="62eac-124">O evento é recebido semisynchronously.</span><span class="sxs-lookup"><span data-stu-id="62eac-124">The event is received semisynchronously.</span></span>   |



 

 

 




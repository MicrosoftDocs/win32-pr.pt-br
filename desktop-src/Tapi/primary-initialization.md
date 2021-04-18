---
description: Um aplicativo TAPI deve chamar uma operação de inicialização, que solicita uma série de ações da TAPI e os provedores de serviço que configuram o ambiente de comunicação para o aplicativo.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Inicialização primária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757955"
---
# <a name="primary-initialization"></a><span data-ttu-id="62373-103">Inicialização primária</span><span class="sxs-lookup"><span data-stu-id="62373-103">Primary Initialization</span></span>

<span data-ttu-id="62373-104">Um aplicativo TAPI deve chamar uma operação de inicialização, que solicita uma série de ações da TAPI e os provedores de serviço que configuram o ambiente de comunicação para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="62373-104">A TAPI application must call an initialization operation, which prompts a series of actions from TAPI and the service providers that set up the communication environment for the application.</span></span>

-   <span data-ttu-id="62373-105">A inicialização é síncrona e não retorna até que a operação seja concluída ou tenha falhado.</span><span class="sxs-lookup"><span data-stu-id="62373-105">Initialization is synchronous and does not return until the operation is complete or has failed.</span></span>
-   <span data-ttu-id="62373-106">Se o TAPISRV ainda não estiver em execução, a TAPI o iniciará.</span><span class="sxs-lookup"><span data-stu-id="62373-106">If TAPISRV is not already running, TAPI starts it.</span></span>
-   <span data-ttu-id="62373-107">A TAPI configura uma conexão com o processo TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="62373-107">TAPI sets up a connection to the TAPISRV process.</span></span>
-   <span data-ttu-id="62373-108">O TAPISVR carrega os provedores de serviço especificados no registro e solicita que eles inicializem os dispositivos para os quais dão suporte.</span><span class="sxs-lookup"><span data-stu-id="62373-108">TAPISVR loads the service providers specified in the registry and prompts them to initialize the devices they support.</span></span>

<span data-ttu-id="62373-109">**TAPI 2. x:** Os aplicativos executam a inicialização chamando [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="62373-109">**TAPI 2.x:** Applications perform initialization by calling [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="62373-110">**TAPI 3. x:** Os aplicativos chamam [**ITTAPI:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span><span class="sxs-lookup"><span data-stu-id="62373-110">**TAPI 3.x:** Applications call [**ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span></span>

 

 

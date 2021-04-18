---
description: Um provedor de tempo é implementado como uma DLL. Cada DLL pode dar suporte a vários provedores de tempo. Cada provedor é responsável por sua própria configuração e sincronização.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Criando um provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749436"
---
# <a name="creating-a-time-provider"></a><span data-ttu-id="5b15f-105">Criando um provedor de tempo</span><span class="sxs-lookup"><span data-stu-id="5b15f-105">Creating a Time Provider</span></span>

<span data-ttu-id="5b15f-106">Um provedor de tempo é implementado como uma DLL.</span><span class="sxs-lookup"><span data-stu-id="5b15f-106">A time provider is implemented as a DLL.</span></span> <span data-ttu-id="5b15f-107">Cada DLL pode dar suporte a vários provedores de tempo.</span><span class="sxs-lookup"><span data-stu-id="5b15f-107">Each DLL can support multiple time providers.</span></span> <span data-ttu-id="5b15f-108">Cada provedor é responsável por sua própria configuração e sincronização.</span><span class="sxs-lookup"><span data-stu-id="5b15f-108">Each provider is responsible for its own configuration and synchronization.</span></span>

<span data-ttu-id="5b15f-109">Os provedores de tempo devem implementar as seguintes funções de retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="5b15f-109">Time providers must implement the following callback functions:</span></span>

-   [<span data-ttu-id="5b15f-110">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="5b15f-110">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [<span data-ttu-id="5b15f-111">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="5b15f-111">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [<span data-ttu-id="5b15f-112">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="5b15f-112">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

<span data-ttu-id="5b15f-113">Depois de carregar a DLL do provedor, o Gerenciador de provedores de tempo chama [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passando o nome do provedor e os ponteiros para as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="5b15f-113">After it has loaded the provider DLL, the time provider manager calls [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passing the name of the provider and pointers to the following functions:</span></span>

-   [<span data-ttu-id="5b15f-114">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="5b15f-114">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [<span data-ttu-id="5b15f-115">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="5b15f-115">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [<span data-ttu-id="5b15f-116">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="5b15f-116">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

<span data-ttu-id="5b15f-117">Essas funções são para uso pelo provedor de tempo.</span><span class="sxs-lookup"><span data-stu-id="5b15f-117">These functions are for use by the time provider.</span></span> <span data-ttu-id="5b15f-118">O provedor de tempo usa [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) para retornar um identificador de provedor que o Gerenciador de provedores de tempo usa ao enviar comandos para o provedor de tempo.</span><span class="sxs-lookup"><span data-stu-id="5b15f-118">The time provider uses [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) to return a provider handle that the time provider manager uses when sending commands to the time provider.</span></span> <span data-ttu-id="5b15f-119">O valor do identificador é definido pelo provedor de tempo e é usado principalmente para distinguir entre diferentes provedores implementados na mesma DLL.</span><span class="sxs-lookup"><span data-stu-id="5b15f-119">The handle value is defined by the time provider and is used primarily to distinguish between different providers implemented in the same DLL.</span></span> <span data-ttu-id="5b15f-120">O provedor de tempo pode registrar eventos significativos usando [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span><span class="sxs-lookup"><span data-stu-id="5b15f-120">The time provider can log significant events using [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span></span>

<span data-ttu-id="5b15f-121">O Gerenciador de provedores de tempo usa [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) para enviar comandos para o provedor de tempo.</span><span class="sxs-lookup"><span data-stu-id="5b15f-121">The time provider manager uses [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) to send commands to the time provider.</span></span> <span data-ttu-id="5b15f-122">Quando o provedor de tempo precisa notificar o Gerenciador de provedores de tempo de que ele tem exemplos de tempo disponíveis, ele chama [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span><span class="sxs-lookup"><span data-stu-id="5b15f-122">When the time provider needs to notify the time provider manager that it has time samples available, it calls [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span></span> <span data-ttu-id="5b15f-123">Em seguida, o Gerenciador de provedores de tempo chama **TimeProvCommand** com o \_ comando TPC getsamples para recuperar os exemplos de tempo.</span><span class="sxs-lookup"><span data-stu-id="5b15f-123">The time provider manager then calls **TimeProvCommand** with the TPC\_GetSamples command to retrieve the time samples.</span></span> <span data-ttu-id="5b15f-124">Pode levar até 16 segundos para que o Gerenciador do provedor de tempo solicite o exemplo.</span><span class="sxs-lookup"><span data-stu-id="5b15f-124">It can take up to 16 seconds for the time provider manager to request the sample.</span></span> <span data-ttu-id="5b15f-125">Portanto, o aplicativo não deve aguardar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b15f-125">Therefore, the application should not wait for the request.</span></span>

<span data-ttu-id="5b15f-126">Para garantir a exatidão, o provedor de tempo deve recuperar todas as informações relacionadas ao tempo usando [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span><span class="sxs-lookup"><span data-stu-id="5b15f-126">To ensure accuracy, the time provider should retrieve all time-related information using [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span></span>

<span data-ttu-id="5b15f-127">Quando é hora de desligar o provedor de tempo, o Gerenciador de provedores de tempo chama [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span><span class="sxs-lookup"><span data-stu-id="5b15f-127">When it is time to shut down the time provider, the time provider manager calls [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span></span>

 

 




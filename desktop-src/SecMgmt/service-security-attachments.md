---
description: O conjunto de ferramentas de configuração de segurança da Microsoft é um conjunto do MMC (console de gerenciamento Microsoft) que simplifica a configuração e a análise da segurança do sistema.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Anexos de segurança de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296267"
---
# <a name="service-security-attachments"></a><span data-ttu-id="2300f-103">Anexos de segurança de serviço</span><span class="sxs-lookup"><span data-stu-id="2300f-103">Service Security Attachments</span></span>

<span data-ttu-id="2300f-104">O conjunto de ferramentas de configuração de segurança da Microsoft é um conjunto do MMC (console de gerenciamento Microsoft) que simplifica a configuração e a análise da segurança do sistema.</span><span class="sxs-lookup"><span data-stu-id="2300f-104">The Microsoft Security Configuration tool set is a set of Microsoft Management Console (MMC) tools that simplify configuration and analysis of system security.</span></span> <span data-ttu-id="2300f-105">Alguns serviços, no entanto, têm necessidades de configuração especializadas que vão além das configurações de segurança fornecidas pelo conjunto de ferramentas padrão.</span><span class="sxs-lookup"><span data-stu-id="2300f-105">Some services, however, have specialized configuration needs that go beyond the security settings provided by the standard tool set.</span></span> <span data-ttu-id="2300f-106">Para lidar com essas necessidades, você pode estender a funcionalidade do conjunto de ferramentas escrevendo um anexo que manipula as tarefas de segurança específicas do serviço.</span><span class="sxs-lookup"><span data-stu-id="2300f-106">To handle those needs, you can extend the functionality of the tool set by writing an attachment that handles the service-specific security tasks.</span></span>

<span data-ttu-id="2300f-107">Por exemplo, o spooler é um serviço do Windows NT que define objetos privados, que precisam ser protegidos, por exemplo, impressoras.</span><span class="sxs-lookup"><span data-stu-id="2300f-107">For example, Spooler is a Windows NT service that defines private objects, which need to be secured, for example, printers.</span></span> <span data-ttu-id="2300f-108">Essa funcionalidade não é tratada pelo conjunto de ferramentas padrão e, portanto, requer um anexo para lidar com a configuração e a análise de objetos de impressora.</span><span class="sxs-lookup"><span data-stu-id="2300f-108">This functionality is not handled by the standard tool set and thus requires an attachment to handle configuration and analysis of printer objects.</span></span> <span data-ttu-id="2300f-109">A configuração de parâmetros de segurança geral, como a política de invocação de serviço, ainda é manipulada pelo conjunto de ferramentas de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="2300f-109">Configuration of general security parameters, such as the service invocation policy, is still handled by the Security Configuration tool set.</span></span>

<span data-ttu-id="2300f-110">Os anexos do serviço de segurança estendem a funcionalidade da ferramenta configuração de segurança definida para dar suporte a configurações específicas do serviço.</span><span class="sxs-lookup"><span data-stu-id="2300f-110">Security service attachments extend the functionality of the Security Configuration tool set to support service-specific configurations.</span></span>

<span data-ttu-id="2300f-111">Um anexo tem dois componentes:</span><span class="sxs-lookup"><span data-stu-id="2300f-111">An attachment has two components:</span></span>

-   <span data-ttu-id="2300f-112">Uma extensão de snap-in do MMC que implementa a interface do usuário do anexo.</span><span class="sxs-lookup"><span data-stu-id="2300f-112">An MMC snap-in extension that implements the attachment user interface.</span></span>
-   <span data-ttu-id="2300f-113">Um mecanismo de anexo que processa tarefas de análise e configuração de segurança específicas de serviço.</span><span class="sxs-lookup"><span data-stu-id="2300f-113">An attachment engine that processes service-specific security configuration and analysis tasks.</span></span>

<span data-ttu-id="2300f-114">A extensão do snap-in de anexos é hospedada pelos snap-ins de configuração de segurança. Esses são snap-ins do MMC que fornecem ao usuário interfaces para configurar e analisar as configurações de segurança gerais de um serviço.</span><span class="sxs-lookup"><span data-stu-id="2300f-114">The attachment snap-in extension is hosted by the Security Configuration snap-ins. These are MMC snap-ins that provide the user with interfaces to configure and analyze the general security settings for a service.</span></span> <span data-ttu-id="2300f-115">As configurações específicas do serviço são configuradas usando a extensão de snap-in de anexo.</span><span class="sxs-lookup"><span data-stu-id="2300f-115">Service-specific settings are configured using the attachment snap-in extension.</span></span>

<span data-ttu-id="2300f-116">Quando o usuário altera uma definição de configuração, os snap-ins de configuração de segurança armazenam as novas informações e, em seguida, passam a solicitação para o mecanismo de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="2300f-116">When the user changes a configuration setting, the Security Configuration snap-ins store the new information and then pass the request to the Security Configuration Engine.</span></span> <span data-ttu-id="2300f-117">O mecanismo processa a solicitação e define o serviço para a nova configuração.</span><span class="sxs-lookup"><span data-stu-id="2300f-117">The Engine processes the request and sets the service to the new configuration.</span></span> <span data-ttu-id="2300f-118">Se a solicitação afetar uma configuração de segurança padrão, ela será manipulada pelo mecanismo.</span><span class="sxs-lookup"><span data-stu-id="2300f-118">If the request affects a standard security setting, it is handled by the Engine.</span></span> <span data-ttu-id="2300f-119">Se a solicitação for específica do serviço, o mecanismo chamará o mecanismo de anexo apropriado para manipular a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2300f-119">If the request is service-specific, the Engine calls the appropriate attachment engine to handle the request.</span></span>

<span data-ttu-id="2300f-120">A ilustração a seguir mostra como o mecanismo de anexo e a extensão do snap-in funcionam dentro da estrutura do conjunto de ferramentas de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="2300f-120">The following illustration shows how the attachment engine and snap-in extension work within the framework of the Security Configuration tool set.</span></span>

![mecanismo de anexo e snap-ins](images/model1a.png)

<span data-ttu-id="2300f-122">Para obter mais informações sobre como usar o conjunto de ferramentas de configuração de segurança da Microsoft, pesquise configuração de segurança usando seu mecanismo de pesquisa preferido.</span><span class="sxs-lookup"><span data-stu-id="2300f-122">For more information about using the Microsoft Security Configuration tool set, search for Security Configuration using your preferred search engine.</span></span>

 

 




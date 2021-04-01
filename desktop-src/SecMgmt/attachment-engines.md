---
description: Um mecanismo de anexo é uma DLL que manipula solicitações de análise e configuração específicas do serviço.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Mecanismos de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829311"
---
# <a name="attachment-engines"></a><span data-ttu-id="98eec-103">Mecanismos de anexo</span><span class="sxs-lookup"><span data-stu-id="98eec-103">Attachment Engines</span></span>

<span data-ttu-id="98eec-104">Um mecanismo de anexo é uma DLL que manipula solicitações de análise e configuração específicas do serviço.</span><span class="sxs-lookup"><span data-stu-id="98eec-104">An attachment engine is a DLL that handles service-specific configuration and analysis requests.</span></span>

<span data-ttu-id="98eec-105">O usuário faz uma solicitação de configuração e análise específica do serviço usando a extensão de snap-in de anexo.</span><span class="sxs-lookup"><span data-stu-id="98eec-105">The user makes a service-specific configuration and analysis request using the attachment snap-in extension.</span></span> <span data-ttu-id="98eec-106">Essa solicitação é passada por meio dos snap-ins de configuração de segurança para o mecanismo de configuração de segurança geral que, por sua vez, passa o processamento específico do serviço para o mecanismo de anexo apropriado.</span><span class="sxs-lookup"><span data-stu-id="98eec-106">This request is then passed through the Security Configuration snap-ins to the general Security Configuration Engine, which in turn passes the service-specific processing to the appropriate attachment engine.</span></span> <span data-ttu-id="98eec-107">Em seguida, o mecanismo de anexo se conecta ao serviço e altera sua configuração.</span><span class="sxs-lookup"><span data-stu-id="98eec-107">The attachment engine then connects to the service and changes its configuration.</span></span> <span data-ttu-id="98eec-108">Em outras palavras, o mecanismo de anexo fornece o processamento de back-end que dá suporte à extensão de snap-in de anexo.</span><span class="sxs-lookup"><span data-stu-id="98eec-108">In other words, the attachment engine provides the back-end processing that supports the attachment snap-in extension.</span></span>

<span data-ttu-id="98eec-109">Um mecanismo de anexo deve implementar as três funções a seguir:</span><span class="sxs-lookup"><span data-stu-id="98eec-109">An attachment engine must implement the following three functions:</span></span>

-   <span data-ttu-id="98eec-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), que computa a diferença entre a configuração do serviço e a configuração armazenada no banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="98eec-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), which computes the difference between the service's configuration and the configuration stored in the security database.</span></span> <span data-ttu-id="98eec-111">As diferenças são gravadas no banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="98eec-111">The differences are written to the security database.</span></span>
-   <span data-ttu-id="98eec-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), que configura o serviço conforme especificado na interface do usuário do snap-in.</span><span class="sxs-lookup"><span data-stu-id="98eec-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), which configures the service as specified in the snap-in user interface.</span></span>
-   <span data-ttu-id="98eec-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), que atualiza a configuração de base e a análise de configuração para o serviço no banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="98eec-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), which updates the base configuration and configuration analysis for the service in the security database.</span></span>

<span data-ttu-id="98eec-114">Para simplificar a implementação das funções anteriores, o conjunto de ferramentas de configuração de segurança oferece suporte a funções e estruturas que seu aplicativo pode usar para consultar e definir informações no banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="98eec-114">To simplify implementation of the preceding functions, the Security Configuration tool set provides support functions and structures that your application can use to query and set information in the security database.</span></span> <span data-ttu-id="98eec-115">Para obter mais informações, consulte [funções de retorno de chamada de anexo](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="98eec-115">For more information, see [Attachment Callback Functions](management-functions.md).</span></span>

<span data-ttu-id="98eec-116">Ao criar uma DLL do mecanismo de anexo, você deve instalá-la e registrá-la no mecanismo de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="98eec-116">When you create an attachment engine DLL, you must install it and then register it with the Security Configuration Engine.</span></span> <span data-ttu-id="98eec-117">Para registrar a DLL, você adiciona uma chave específica ao registro.</span><span class="sxs-lookup"><span data-stu-id="98eec-117">To register the DLL, you add a specific key to the registry.</span></span> <span data-ttu-id="98eec-118">Quando o mecanismo de configuração de segurança é iniciado, ele verifica o registro e carrega todas as DLLs do mecanismo de anexo registrado.</span><span class="sxs-lookup"><span data-stu-id="98eec-118">When the Security Configuration Engine starts, it checks the registry and loads all registered attachment engine DLLs.</span></span> <span data-ttu-id="98eec-119">Em seguida, ele passa as solicitações de análise e configuração específicas do serviço para o mecanismo de anexo apropriado.</span><span class="sxs-lookup"><span data-stu-id="98eec-119">It then passes service-specific configuration and analysis requests to the appropriate attachment engine.</span></span> <span data-ttu-id="98eec-120">As solicitações de análise e configuração padrão, aquelas que não são específicas do serviço, são tratadas pelo mecanismo de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="98eec-120">Standard configuration and analysis requests, those that are not service-specific, are handled by the Security Configuration Engine.</span></span>

 

 




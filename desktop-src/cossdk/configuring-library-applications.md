---
description: Configurando aplicativos de biblioteca
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configurando aplicativos de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010143"
---
# <a name="configuring-library-applications"></a><span data-ttu-id="bc3d6-103">Configurando aplicativos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc3d6-103">Configuring Library Applications</span></span>

<span data-ttu-id="bc3d6-104">Como os aplicativos de biblioteca COM+ são executados no processo do cliente, os elementos configuráveis para aplicativos de biblioteca são consideravelmente diferentes dos aplicativos de servidor.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-104">Because COM+ library applications run in the client's process, the configurable elements for library applications are considerably different than for server applications.</span></span> <span data-ttu-id="bc3d6-105">Você não pode configurar qualquer aspecto do aplicativo que é determinado pelo processo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-105">You cannot configure any aspect of the application that is determined by the hosting process.</span></span>

<span data-ttu-id="bc3d6-106">No nível do aplicativo, várias configurações são limitadas ou não disponíveis para aplicativos de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-106">At the application level, several settings are either limited or unavailable for library applications.</span></span> <span data-ttu-id="bc3d6-107">Essas restrições são descritas na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="bc3d6-107">These constraints are described in the following table:</span></span>



| <span data-ttu-id="bc3d6-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="bc3d6-108">Attribute</span></span>                                       | <span data-ttu-id="bc3d6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc3d6-109">Description</span></span>                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3d6-110">Nível de segurança</span><span class="sxs-lookup"><span data-stu-id="bc3d6-110">Security level</span></span><br/>                       | <span data-ttu-id="bc3d6-111">Você deve escolher as verificações de acesso no nível do componente.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-111">You must choose component-level access checks.</span></span> <span data-ttu-id="bc3d6-112">O aplicativo de biblioteca não pode influenciar as verificações de acesso no nível do processo.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-112">The library application cannot influence process-level access checks.</span></span> <span data-ttu-id="bc3d6-113">Consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="bc3d6-113">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span><br/>             |
| <span data-ttu-id="bc3d6-114">Habilitando ou desabilitando a autenticação</span><span class="sxs-lookup"><span data-stu-id="bc3d6-114">Enabling or disabling authentication</span></span><br/> | <span data-ttu-id="bc3d6-115">Você pode indicar se o aplicativo de biblioteca participará da autenticação executada pelo processo de host.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-115">You can indicate whether the library application will participate in authentication performed by the host process.</span></span> <span data-ttu-id="bc3d6-116">Consulte [habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="bc3d6-116">See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span><br/> |
| <span data-ttu-id="bc3d6-117">Nível de representação</span><span class="sxs-lookup"><span data-stu-id="bc3d6-117">Impersonation level</span></span><br/>                  | <span data-ttu-id="bc3d6-118">Indisponível.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-118">Unavailable.</span></span> <span data-ttu-id="bc3d6-119">A configuração do processo de host é usada.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-119">The setting of the host process is used.</span></span> <br/>                                                                                                                                                                             |
| <span data-ttu-id="bc3d6-120">Identidade de segurança</span><span class="sxs-lookup"><span data-stu-id="bc3d6-120">Security identity</span></span><br/>                    | <span data-ttu-id="bc3d6-121">Indisponível.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-121">Unavailable.</span></span> <span data-ttu-id="bc3d6-122">O aplicativo é executado sob a identidade do processo do host.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-122">The application runs under the identity of the host process.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="bc3d6-123">Desligamento de processo do servidor</span><span class="sxs-lookup"><span data-stu-id="bc3d6-123">Server process shutdown</span></span><br/>              | <span data-ttu-id="bc3d6-124">Indisponível.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-124">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="bc3d6-125">Habilitar suporte a 3 GB</span><span class="sxs-lookup"><span data-stu-id="bc3d6-125">Enable 3-GB support</span></span><br/>                  | <span data-ttu-id="bc3d6-126">Indisponível.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-126">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="bc3d6-127">Iniciar no depurador</span><span class="sxs-lookup"><span data-stu-id="bc3d6-127">Launch in debugger</span></span><br/>                   | <span data-ttu-id="bc3d6-128">Indisponível.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-128">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="bc3d6-129">Habilitar CRM</span><span class="sxs-lookup"><span data-stu-id="bc3d6-129">Enable CRM</span></span><br/>                           | <span data-ttu-id="bc3d6-130">Indisponível.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-130">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="bc3d6-131">Serviço</span><span class="sxs-lookup"><span data-stu-id="bc3d6-131">Queuing</span></span><br/>                              | <span data-ttu-id="bc3d6-132">Indisponível.</span><span class="sxs-lookup"><span data-stu-id="bc3d6-132">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="bc3d6-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc3d6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc3d6-134">Visão geral do aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="bc3d6-134">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> </dl>

 

 





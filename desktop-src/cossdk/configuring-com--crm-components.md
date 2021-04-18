---
description: Os componentes do CRM podem ser instalados em um aplicativo de servidor COM+ ou em um aplicativo de biblioteca COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configurando componentes de CRM do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765681"
---
# <a name="configuring-com-crm-components"></a><span data-ttu-id="811a2-103">Configurando componentes de CRM do COM+</span><span class="sxs-lookup"><span data-stu-id="811a2-103">Configuring COM+ CRM Components</span></span>

<span data-ttu-id="811a2-104">Os componentes do CRM podem ser instalados em um aplicativo de servidor COM+ ou em um aplicativo de biblioteca COM+.</span><span class="sxs-lookup"><span data-stu-id="811a2-104">CRM components can be installed into either a COM+ server application or a COM+ library application.</span></span> <span data-ttu-id="811a2-105">No entanto, eles devem sempre ser executados em um aplicativo de servidor do COM+.</span><span class="sxs-lookup"><span data-stu-id="811a2-105">However, they must always run in a COM+ server application.</span></span> <span data-ttu-id="811a2-106">Se eles estiverem instalados em um aplicativo de biblioteca COM+, eles não estarão disponíveis para uso em processos de cliente.</span><span class="sxs-lookup"><span data-stu-id="811a2-106">If they are installed in a COM+ library application, they are not available for use in client processes.</span></span>

<span data-ttu-id="811a2-107">Se os componentes do CRM estiverem instalados em um aplicativo de biblioteca, eles estarão disponíveis para mais de um aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="811a2-107">If the CRM components they are installed in a library application, they are available to more than one server application.</span></span> <span data-ttu-id="811a2-108">Se instalado em um aplicativo de servidor específico, ele estará disponível somente para esse aplicativo de servidor específico.</span><span class="sxs-lookup"><span data-stu-id="811a2-108">If installed in a specific server application, they are available only to that specific server application.</span></span>

<span data-ttu-id="811a2-109">Para habilitar o uso de um CRM em um aplicativo de servidor, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="811a2-109">To enable use of a CRM in a server application, use the following steps:</span></span>

1.  <span data-ttu-id="811a2-110">Em serviços de componentes, na página Propriedades do aplicativo de servidor, clique na guia **avançado** .</span><span class="sxs-lookup"><span data-stu-id="811a2-110">From Component Services, under the server application properties page, click the **Advanced** tab.</span></span>

2.  <span data-ttu-id="811a2-111">Selecione a opção **habilitar gerenciadores de recursos de compensação** para esse aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="811a2-111">Select the **Enable compensating Resource Managers** option for that server application.</span></span> <span data-ttu-id="811a2-112">Se essa opção não estiver selecionada, as tentativas de usar um CRM dentro desse aplicativo de servidor falharão.</span><span class="sxs-lookup"><span data-stu-id="811a2-112">If this option is not selected, attempts to use a CRM within this server application will fail.</span></span>

    > [!Note]  
    > <span data-ttu-id="811a2-113">Se instalado em um aplicativo de biblioteca, não é necessário selecionar a opção **habilitar gerenciadores de recursos de compensação** para esse aplicativo de biblioteca, mas essa opção deve ser selecionada para o aplicativo de servidor no qual o CRM deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="811a2-113">If installed in a library application, it is not necessary to select the **Enable compensating Resource Managers** option for that library application, but this option must be selected for the server application in which the CRM is intended to run.</span></span>

     

<span data-ttu-id="811a2-114">É recomendável que os componentes de trabalho CRM e compensador CRM para um CRM específico sejam instalados no mesmo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="811a2-114">It is recommended that the CRM Worker and CRM Compensator components for a specific CRM be installed in the same application.</span></span>

<span data-ttu-id="811a2-115">As configurações recomendadas para os componentes do CRM são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="811a2-115">The recommended settings for CRM components are as follows.</span></span>



| <span data-ttu-id="811a2-116">Componente</span><span class="sxs-lookup"><span data-stu-id="811a2-116">Component</span></span>           | <span data-ttu-id="811a2-117">Configurações</span><span class="sxs-lookup"><span data-stu-id="811a2-117">Settings</span></span>                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="811a2-118">**Trabalhador do CRM**</span><span class="sxs-lookup"><span data-stu-id="811a2-118">**CRM Worker**</span></span>      | <span data-ttu-id="811a2-119">transação = requiredsync = yesJIT = modelo de yesthreading = (ou modelo de Threading = Apartment)</span><span class="sxs-lookup"><span data-stu-id="811a2-119">transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)</span></span>     |
| <span data-ttu-id="811a2-120">**Compensador de CRM**</span><span class="sxs-lookup"><span data-stu-id="811a2-120">**CRM Compensator**</span></span> | <span data-ttu-id="811a2-121">transação = disabledsync = disabledJIT = modelo nothreading = (ou modelo de Threading = Apartment)</span><span class="sxs-lookup"><span data-stu-id="811a2-121">transaction = disabledsync = disabledJIT = nothreading model = Both (or threading model = Apartment)</span></span> |



 

> [!Note]  
> <span data-ttu-id="811a2-122">Os componentes que usam o CRM devem especificar explicitamente um modelo de Threading quando eles são registrados.</span><span class="sxs-lookup"><span data-stu-id="811a2-122">Components that use the CRM must explicitly specify a threading model when they are registered.</span></span> <span data-ttu-id="811a2-123">Não há suporte para o padrão ' Main thread apartment '.</span><span class="sxs-lookup"><span data-stu-id="811a2-123">The default, 'Main Thread Apartment,' is not supported.</span></span> <span data-ttu-id="811a2-124">Os únicos dois modelos de Threading com suporte são Apartment e both.</span><span class="sxs-lookup"><span data-stu-id="811a2-124">The only two threading models supported are Apartment and Both.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="811a2-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="811a2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="811a2-126">Conceitos do Gerenciador de recursos de compensação COM+</span><span class="sxs-lookup"><span data-stu-id="811a2-126">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 




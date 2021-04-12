---
description: O COM+ fornece um modelo de objeto de administração que expõe toda a funcionalidade da ferramenta administrativa serviços de componentes, em si, um front-end gráfico escrito sobre os objetos administrativos.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatizando a administração do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089378"
---
# <a name="automating-com-administration"></a><span data-ttu-id="43887-103">Automatizando a administração do COM+</span><span class="sxs-lookup"><span data-stu-id="43887-103">Automating COM+ Administration</span></span>

<span data-ttu-id="43887-104">O COM+ fornece um modelo de objeto de administração que expõe toda a funcionalidade da ferramenta administrativa serviços de componentes, em si, um front-end gráfico escrito sobre os objetos administrativos.</span><span class="sxs-lookup"><span data-stu-id="43887-104">COM+ provides an administration object model that exposes all of the functionality of the Component Services administrative tool, itself a graphical front end written on top of the administrative objects.</span></span> <span data-ttu-id="43887-105">Você pode usar esses objetos, fornecidos pela biblioteca de administração de serviços de componentes (COMAdmin), para automatizar todas as tarefas na administração de aplicativos e serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="43887-105">You can use these objects, supplied by the Component Services Administration (COMAdmin) Library, to automate all tasks in the administration of COM+ applications and services.</span></span>

<span data-ttu-id="43887-106">Os objetos COMAdmin permitem que você leia e grave informações armazenadas no catálogo COM+, o armazenamento de dados subjacente que contém todos os dados de configuração do COM+.</span><span class="sxs-lookup"><span data-stu-id="43887-106">The COMAdmin objects enable you to read and write information that is stored on the COM+ catalog, the underlying data store that holds all COM+ configuration data.</span></span>

<span data-ttu-id="43887-107">Você pode usar esses objetos para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="43887-107">You can use these objects to do the following:</span></span>

-   <span data-ttu-id="43887-108">Criar e configurar aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="43887-108">Create and configure COM+ applications.</span></span>
-   <span data-ttu-id="43887-109">Instalar e exportar aplicativos COM+ existentes.</span><span class="sxs-lookup"><span data-stu-id="43887-109">Install and export existing COM+ applications.</span></span>
-   <span data-ttu-id="43887-110">Gerenciar aplicativos COM+ instalados.</span><span class="sxs-lookup"><span data-stu-id="43887-110">Manage installed COM+ applications.</span></span>
-   <span data-ttu-id="43887-111">Gerenciar e configurar serviços.</span><span class="sxs-lookup"><span data-stu-id="43887-111">Manage and configure services.</span></span>
-   <span data-ttu-id="43887-112">Administre remotamente os serviços de componentes em um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="43887-112">Remotely administer Component Services on a different machine.</span></span>

<span data-ttu-id="43887-113">Você pode usar os objetos COMAdmin programáveis com qualquer linguagem compatível com a automação, como o Microsoft Visual Basic e Visual Basic Script.</span><span class="sxs-lookup"><span data-stu-id="43887-113">You can use the scriptable COMAdmin objects with any Automation-compatible language, such as Microsoft Visual Basic and Visual Basic Script.</span></span> <span data-ttu-id="43887-114">Você pode desenvolver scripts leves ou ferramentas de administração de uso geral.</span><span class="sxs-lookup"><span data-stu-id="43887-114">You can develop either lightweight scripts or general-purpose administration tools.</span></span> <span data-ttu-id="43887-115">Por exemplo, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="43887-115">For example, you can do the following:</span></span>

-   <span data-ttu-id="43887-116">Gravar scripts para executar tarefas administrativas rotineiras.</span><span class="sxs-lookup"><span data-stu-id="43887-116">Write scripts to perform routine administrative tasks.</span></span>
-   <span data-ttu-id="43887-117">Grave scripts para automatizar processos no desenvolvimento de aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="43887-117">Write scripts to automate processes in the development of COM+ applications.</span></span>
-   <span data-ttu-id="43887-118">Desenvolva ferramentas de finalidade geral para administrar e monitorar serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="43887-118">Develop general-purpose tools for administering and monitoring Component Services.</span></span>
-   <span data-ttu-id="43887-119">Desenvolva executáveis de instalação para instalar e implantar seu aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="43887-119">Develop setup executables to install and deploy your COM+ application.</span></span>

<span data-ttu-id="43887-120">A biblioteca COMAdmin fornece compatibilidade com versões anteriores da biblioteca de administração do MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="43887-120">The COMAdmin Library provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="43887-121">A maioria dos códigos de administração do MTS 2,0 ainda funcionará, embora com algumas exceções.</span><span class="sxs-lookup"><span data-stu-id="43887-121">Most existing MTS 2.0 administration code will still work, although with some exceptions.</span></span> <span data-ttu-id="43887-122">(Consulte [biblioteca de administração do MTS](mts-administration-library.md).)</span><span class="sxs-lookup"><span data-stu-id="43887-122">(See [MTS Administration Library](mts-administration-library.md).)</span></span>

<span data-ttu-id="43887-123">Para automatizar a administração com eficiência, você deve estar familiarizado com as tarefas de Administração realizadas com a ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="43887-123">To automate administration effectively, you should be familiar with administration tasks as performed with the Component Services administrative tool.</span></span>

<span data-ttu-id="43887-124">Para obter descrições completas dos objetos COMAdmin e das interfaces correspondentes, consulte a documentação de referência do COM+ para as seguintes classes e interfaces:</span><span class="sxs-lookup"><span data-stu-id="43887-124">For full descriptions of the COMAdmin objects and the corresponding interfaces, see the COM+ Reference documentation for the following classes and interfaces:</span></span>

-   [<span data-ttu-id="43887-125">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="43887-125">**COMAdminCatalog**</span></span>](comadmincatalog.md)
-   [<span data-ttu-id="43887-126">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="43887-126">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
-   [<span data-ttu-id="43887-127">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="43887-127">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
-   [<span data-ttu-id="43887-128">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="43887-128">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [<span data-ttu-id="43887-129">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="43887-129">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [<span data-ttu-id="43887-130">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="43887-130">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [<span data-ttu-id="43887-131">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="43887-131">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

<span data-ttu-id="43887-132">Os tópicos a seguir nesta seção fornecem uma visão geral para automatizar a administração usando os objetos COMAdmin:</span><span class="sxs-lookup"><span data-stu-id="43887-132">The following topics in this section provide an overview for automating administration using the COMAdmin objects:</span></span>

-   [<span data-ttu-id="43887-133">Visão geral dos objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="43887-133">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
-   [<span data-ttu-id="43887-134">Recuperando coleções no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="43887-134">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
-   [<span data-ttu-id="43887-135">Definindo propriedades e salvando alterações no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="43887-135">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [<span data-ttu-id="43887-136">Manipulando erros de administração COM+</span><span class="sxs-lookup"><span data-stu-id="43887-136">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
-   [<span data-ttu-id="43887-137">Operações de administração COM+ em transações</span><span class="sxs-lookup"><span data-stu-id="43887-137">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
-   [<span data-ttu-id="43887-138">Exemplo introdutório usando o catálogo de administração do COM+</span><span class="sxs-lookup"><span data-stu-id="43887-138">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)

 

 




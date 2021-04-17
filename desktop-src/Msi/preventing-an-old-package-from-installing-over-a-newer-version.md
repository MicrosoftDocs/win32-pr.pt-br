---
description: Windows Installer pacotes de atualização podem ser criados para que as principais atualizações não sejam instaladas se um usuário já tiver uma versão mais recente instalada.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Impedir que um pacote antigo seja instalado em uma versão mais recente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748975"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a><span data-ttu-id="9931f-103">Impedindo que um pacote antigo seja instalado em uma versão mais recente</span><span class="sxs-lookup"><span data-stu-id="9931f-103">Preventing an Old Package from Installing Over a Newer Version</span></span>

<span data-ttu-id="9931f-104">Windows Installer pacotes de atualização podem ser criados para que as principais atualizações não sejam instaladas se um usuário já tiver uma versão mais recente instalada.</span><span class="sxs-lookup"><span data-stu-id="9931f-104">Windows Installer upgrade packages can be authored to have major upgrades not install if a user already has a newer version installed.</span></span> <span data-ttu-id="9931f-105">O procedimento neste tópico só pode impedir downgrades que podem ser causados pela execução de um pacote de atualização principal.</span><span class="sxs-lookup"><span data-stu-id="9931f-105">The procedure in this topic can only prevent downgrades that might be caused by running a major upgrade package.</span></span> <span data-ttu-id="9931f-106">Esse procedimento depende da [ação FindRelatedProducts](findrelatedproducts-action.md), que é executada apenas durante uma instalação inicial e não é executada no modo de manutenção (reinstalação).</span><span class="sxs-lookup"><span data-stu-id="9931f-106">This procedure relies on the [FindRelatedProducts Action](findrelatedproducts-action.md), which only runs during a first-time installation and does not run in maintenance mode (reinstallation).</span></span> <span data-ttu-id="9931f-107">Como as atualizações secundárias são executadas usando a reinstalação, esse procedimento não pode ser usado para determinar se um pacote de atualização secundário está tentando fazer downgrade de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9931f-107">Because minor upgrades are performed using reinstallation, this procedure cannot be used to determine whether a minor upgrade package is attempting to downgrade an application.</span></span> <span data-ttu-id="9931f-108">Para obter mais informações, consulte [preparando um aplicativo para futuras atualizações importantes](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="9931f-108">For more information, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

<span data-ttu-id="9931f-109">**Para impedir que um pacote antigo seja instalado em uma versão mais recente**</span><span class="sxs-lookup"><span data-stu-id="9931f-109">**To prevent an old package from installing over a newer version**</span></span>

1.  <span data-ttu-id="9931f-110">Insira a propriedade [**UpgradeCode**](upgradecode.md) para o grupo de produtos relacionados que podem estar qualificados para receber essa atualização na coluna UpgradeCode da tabela de [atualização](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="9931f-110">Enter the [**UpgradeCode**](upgradecode.md) Property for the group of related products that may be eligible to receive this upgrade into the UpgradeCode column of the [Upgrade Table](upgrade-table.md).</span></span>
2.  <span data-ttu-id="9931f-111">Insira o sinalizador de bit **msidbUpgradeAttributesOnlyDetect** na coluna atributos da [tabela de atualização](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="9931f-111">Enter the **msidbUpgradeAttributesOnlyDetect** bit flag in the Attributes column of the [Upgrade Table](upgrade-table.md).</span></span>
3.  <span data-ttu-id="9931f-112">Insira a versão da atualização fornecida por esse pacote na coluna VersionMin da [tabela de atualização](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="9931f-112">Enter the version of the upgrade provided by this package into the VersionMin column of the [Upgrade Table](upgrade-table.md).</span></span> <span data-ttu-id="9931f-113">Deixe a coluna VersionMax em branco.</span><span class="sxs-lookup"><span data-stu-id="9931f-113">Leave the VersionMax column blank.</span></span>
4.  <span data-ttu-id="9931f-114">Insira o nome da propriedade que deve ser definida pela [ação FindRelatedProducts](findrelatedproducts-action.md) na coluna actionproperty da [tabela de atualização](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="9931f-114">Enter the name of the property that is to be set by the [FindRelatedProducts Action](findrelatedproducts-action.md) into the ActionProperty column of the [Upgrade Table](upgrade-table.md).</span></span>
5.  <span data-ttu-id="9931f-115">Adicione a propriedade [**SecureCustomProperties**](securecustomproperties.md) e a propriedade chamada na coluna actionproperty da tabela de [atualização](upgrade-table.md) à tabela de [Propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="9931f-115">Add the [**SecureCustomProperties**](securecustomproperties.md) property and the property named in the ActionProperty column of the [Upgrade Table](upgrade-table.md) to the [Property Table](property-table.md).</span></span>
6.  <span data-ttu-id="9931f-116">Adicione um [tipo de ação personalizada 19](custom-action-type-19.md) após a ação FindRelatedProducts na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9931f-116">Add a [Custom Action Type 19](custom-action-type-19.md) after the FindRelatedProducts action in the [InstallExecuteSequence Table](installexecutesequence-table.md).</span></span> <span data-ttu-id="9931f-117">Inclua um registro na [tabela CustomAction](customaction-table.md) para esta ação e insira o texto a ser exibido na coluna de destino.</span><span class="sxs-lookup"><span data-stu-id="9931f-117">Include a record in the [CustomAction Table](customaction-table.md) for this action and enter the text to be displayed in the Target column.</span></span> <span data-ttu-id="9931f-118">A ação personalizada Type 19 é criada no instalador, portanto, não há nenhum código a ser escrito.</span><span class="sxs-lookup"><span data-stu-id="9931f-118">The type 19 custom action is built into the installer, so there is no code to write.</span></span>
7.  <span data-ttu-id="9931f-119">Insira o nome da Actionproperty na coluna Condition do registro na [tabela InstallExecuteSequence](installexecutesequence-table.md) que contém o [tipo de ação personalizada 19](custom-action-type-19.md).</span><span class="sxs-lookup"><span data-stu-id="9931f-119">Enter the name of the ActionProperty into the Condition column of the record in [InstallExecuteSequence Table](installexecutesequence-table.md) that contains the [Custom Action Type 19](custom-action-type-19.md).</span></span> <span data-ttu-id="9931f-120">Isso faz com que a ação personalizada seja executada somente quando a [tabela de atualização](upgrade-table.md) detectar que uma versão mais recente já está instalada.</span><span class="sxs-lookup"><span data-stu-id="9931f-120">This conditions the custom action to only be executed when the [Upgrade Table](upgrade-table.md) detects that a newer version is already installed.</span></span>

    <span data-ttu-id="9931f-121">Por exemplo, um pacote Windows Installer que atualiza um grupo de produtos relacionados à versão 3,0 pode incluir os seguintes registros em suas tabelas de [Propriedade](property-table.md) , [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e de [atualização](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="9931f-121">For example, a Windows Installer package that upgrades a group of related products to version 3.0 may include the following records in its [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [Property](property-table.md) tables.</span></span> <span data-ttu-id="9931f-122">Todos os produtos relacionados no grupo têm o mesmo UpgradeCode, mas o instalador não instala esse pacote de atualização se uma versão posterior à 3,0 já estiver instalada no computador.</span><span class="sxs-lookup"><span data-stu-id="9931f-122">All the related products in the group have the same UpgradeCode, but the installer does not install this upgrade package if a version later than 3.0 is already installed on the computer.</span></span> <span data-ttu-id="9931f-123">Nesse caso, o instalador apresenta uma mensagem de erro e a instalação falha.</span><span class="sxs-lookup"><span data-stu-id="9931f-123">In this case, the Installer presents an error message and the installation fails.</span></span> <span data-ttu-id="9931f-124">O pacote de atualização da versão 3,0 é instalado nas versões 1,0 e 2,0.</span><span class="sxs-lookup"><span data-stu-id="9931f-124">The version 3.0 upgrade package installs over versions 1.0 and 2.0.</span></span>

    [<span data-ttu-id="9931f-125">Atualizar tabela</span><span class="sxs-lookup"><span data-stu-id="9931f-125">Upgrade Table</span></span>](upgrade-table.md)

    

    | <span data-ttu-id="9931f-126">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="9931f-126">UpgradeCode</span></span>                            | <span data-ttu-id="9931f-127">VersionMin</span><span class="sxs-lookup"><span data-stu-id="9931f-127">VersionMin</span></span> | <span data-ttu-id="9931f-128">VersionMax</span><span class="sxs-lookup"><span data-stu-id="9931f-128">VersionMax</span></span> | <span data-ttu-id="9931f-129">Idioma</span><span class="sxs-lookup"><span data-stu-id="9931f-129">Language</span></span> | <span data-ttu-id="9931f-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="9931f-130">Attributes</span></span>                                | <span data-ttu-id="9931f-131">Remover</span><span class="sxs-lookup"><span data-stu-id="9931f-131">Remove</span></span> | <span data-ttu-id="9931f-132">Açãoproperty</span><span class="sxs-lookup"><span data-stu-id="9931f-132">ActionProperty</span></span>  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | <span data-ttu-id="9931f-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="9931f-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="9931f-134">3.0</span><span class="sxs-lookup"><span data-stu-id="9931f-134">3.0</span></span>        |            |          | <span data-ttu-id="9931f-135">msidbUpgradeAttributesOnlyDetect</span><span class="sxs-lookup"><span data-stu-id="9931f-135">msidbUpgradeAttributesOnlyDetect</span></span>          |        | <span data-ttu-id="9931f-136">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="9931f-136">NEWPRODUCTFOUND</span></span> |
    | <span data-ttu-id="9931f-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="9931f-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="9931f-138">1.0</span><span class="sxs-lookup"><span data-stu-id="9931f-138">1.0</span></span>        | <span data-ttu-id="9931f-139">3.0</span><span class="sxs-lookup"><span data-stu-id="9931f-139">3.0</span></span>        |          | <span data-ttu-id="9931f-140">msidbUpgradeAttributesVersionMinInclusive</span><span class="sxs-lookup"><span data-stu-id="9931f-140">msidbUpgradeAttributesVersionMinInclusive</span></span> |        | <span data-ttu-id="9931f-141">UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="9931f-141">UPGRADEFOUND</span></span>    |

    

     

    [<span data-ttu-id="9931f-142">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="9931f-142">CustomAction Table</span></span>](customaction-table.md)

    

    | <span data-ttu-id="9931f-143">Ação</span><span class="sxs-lookup"><span data-stu-id="9931f-143">Action</span></span> | <span data-ttu-id="9931f-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="9931f-144">Type</span></span> | <span data-ttu-id="9931f-145">Fonte</span><span class="sxs-lookup"><span data-stu-id="9931f-145">Source</span></span> | <span data-ttu-id="9931f-146">Destino</span><span class="sxs-lookup"><span data-stu-id="9931f-146">Target</span></span>                                 |
    |--------|------|--------|----------------------------------------|
    | <span data-ttu-id="9931f-147">CA1</span><span class="sxs-lookup"><span data-stu-id="9931f-147">CA1</span></span>    | <span data-ttu-id="9931f-148">19</span><span class="sxs-lookup"><span data-stu-id="9931f-148">19</span></span>   |        | <span data-ttu-id="9931f-149">Uma atualização mais alta já está instalada.</span><span class="sxs-lookup"><span data-stu-id="9931f-149">A higher upgrade is already installed.</span></span> |

    

     

    [<span data-ttu-id="9931f-150">Tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="9931f-150">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)

    

    | <span data-ttu-id="9931f-151">Ação</span><span class="sxs-lookup"><span data-stu-id="9931f-151">Action</span></span>              | <span data-ttu-id="9931f-152">Condição</span><span class="sxs-lookup"><span data-stu-id="9931f-152">Condition</span></span>       | <span data-ttu-id="9931f-153">Sequência</span><span class="sxs-lookup"><span data-stu-id="9931f-153">Sequence</span></span> |
    |---------------------|-----------------|----------|
    | <span data-ttu-id="9931f-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="9931f-154">FindRelatedProducts</span></span> |                 | <span data-ttu-id="9931f-155">200</span><span class="sxs-lookup"><span data-stu-id="9931f-155">200</span></span>      |
    | <span data-ttu-id="9931f-156">CA1</span><span class="sxs-lookup"><span data-stu-id="9931f-156">CA1</span></span>                 | <span data-ttu-id="9931f-157">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="9931f-157">NEWPRODUCTFOUND</span></span> | <span data-ttu-id="9931f-158">201</span><span class="sxs-lookup"><span data-stu-id="9931f-158">201</span></span>      |

    

     

    [<span data-ttu-id="9931f-159">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="9931f-159">Property Table</span></span>](property-table.md)

    

    | <span data-ttu-id="9931f-160">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9931f-160">Property</span></span>                                                 | <span data-ttu-id="9931f-161">Valor</span><span class="sxs-lookup"><span data-stu-id="9931f-161">Value</span></span>                        |
    |----------------------------------------------------------|------------------------------|
    | [<span data-ttu-id="9931f-162">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="9931f-162">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="9931f-163">NEWPRODUCTFOUND; UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="9931f-163">NEWPRODUCTFOUND;UPGRADEFOUND</span></span> |

    

     

 

 




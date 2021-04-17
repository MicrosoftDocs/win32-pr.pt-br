---
description: A ação MigrateFeatureStates é usada durante a atualização e ao instalar um novo aplicativo em um aplicativo relacionado.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: Ação MigrateFeatureStates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e76edb5fa13506291cc85ebcf8c8824e4ee28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775709"
---
# <a name="migratefeaturestates-action"></a><span data-ttu-id="9e60b-103">Ação MigrateFeatureStates</span><span class="sxs-lookup"><span data-stu-id="9e60b-103">MigrateFeatureStates Action</span></span>

<span data-ttu-id="9e60b-104">A ação MigrateFeatureStates é usada durante a atualização e ao instalar um novo aplicativo em um aplicativo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9e60b-104">The MigrateFeatureStates action is used during upgrading and when installing a new application over a related application.</span></span> <span data-ttu-id="9e60b-105">MigrateFeatureStates lê os Estados de recursos no aplicativo existente e define esses Estados de recursos na instalação pendente.</span><span class="sxs-lookup"><span data-stu-id="9e60b-105">MigrateFeatureStates reads the feature states in the existing application and then sets these feature states in the pending installation.</span></span> <span data-ttu-id="9e60b-106">O método só é útil quando a nova árvore de recursos não mudou muito do original.</span><span class="sxs-lookup"><span data-stu-id="9e60b-106">The method is only useful when the new feature tree has not greatly changed from the original.</span></span>

<span data-ttu-id="9e60b-107">A ação MigrateFeatureStates é executada apenas na primeira vez em que o produto é instalado.</span><span class="sxs-lookup"><span data-stu-id="9e60b-107">The MigrateFeatureStates action only runs the first time the product is installed.</span></span> <span data-ttu-id="9e60b-108">A ação MigrateFeatureStates não é executada durante o modo de manutenção ou a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="9e60b-108">The MigrateFeatureStates action does not run during maintenance mode or uninstallation.</span></span>

<span data-ttu-id="9e60b-109">A ação MigrateFeatureStates é executada por meio de cada registro da [tabela de atualização](upgrade-table.md) em sequência e compara o código de atualização, a versão do produto e o idioma em cada linha para todos os produtos instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="9e60b-109">MigrateFeatureStates action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to all products installed on the system.</span></span> <span data-ttu-id="9e60b-110">Se a ação MigrateFeatureStates detectar uma correspondência e se o sinalizador de bit msidbUpgradeAttributesMigrateFeatures estiver definido na coluna atributos da tabela de atualização, o instalador consultará os Estados de recurso existentes para o produto e definirá esses Estados para os mesmos recursos no novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9e60b-110">If MigrateFeatureStates action detects a correspondence, and if the msidbUpgradeAttributesMigrateFeatures bit flag is set in the Attributes column of the Upgrade table, the installer queries the existing feature states for the product and sets these states for the same features in the new application.</span></span> <span data-ttu-id="9e60b-111">A ação migrará apenas os Estados do recurso se a propriedade [**preselecionada**](preselected.md) não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="9e60b-111">The action only migrates the feature states if the [**Preselected**](preselected.md) property is not set.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9e60b-112">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="9e60b-112">Sequence Restrictions</span></span>

<span data-ttu-id="9e60b-113">A ação MigrateFeatureStates deve vir imediatamente após a [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9e60b-113">The MigrateFeatureStates action should come immediately after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="9e60b-114">MigrateFeatureStates deve ser sequenciado na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e60b-114">MigrateFeatureStates must be sequenced in both the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="9e60b-115">O instalador impede que o MigrateFeatureStates seja executado em InstallExecuteSequence se a ação já tiver sido executada no InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="9e60b-115">The installer prevents MigrateFeatureStates from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9e60b-116">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="9e60b-116">ActionData Messages</span></span>

<span data-ttu-id="9e60b-117">MigrateFeatureSettings envia uma mensagem de dados de ação para cada produto.</span><span class="sxs-lookup"><span data-stu-id="9e60b-117">MigrateFeatureSettings sends an action data message for each product.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e60b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e60b-118">Remarks</span></span>

<span data-ttu-id="9e60b-119">Se mais de um produto instalado compartilhar um recurso, o estado de instalação desse recurso poderá ser diferente entre os produtos.</span><span class="sxs-lookup"><span data-stu-id="9e60b-119">If more than one installed product shares a feature, the installation state for that feature may differ between products.</span></span> <span data-ttu-id="9e60b-120">A ação MigrateFeatureState usa a seguinte ordem de precedência ao migrar Estados de instalação de recursos: executar local, executar da origem, anunciado e desinstalado.</span><span class="sxs-lookup"><span data-stu-id="9e60b-120">MigrateFeatureState action uses the following order of precedence when migrating feature installation states: run local, run from source, advertised, and uninstalled.</span></span> <span data-ttu-id="9e60b-121">Por exemplo, o produto instalado A pode ter o recurso Y como INSTALLstate \_ local e o produto B instalado pode ter o recurso y como InstallState \_ ausente.</span><span class="sxs-lookup"><span data-stu-id="9e60b-121">For example, installed product A may have feature Y as INSTALLSTATE\_LOCAL and installed product B may have feature Y as INSTALLSTATE\_ABSENT.</span></span> <span data-ttu-id="9e60b-122">Se uma atualização instalar o produto C e migrar o estado de instalação do recurso Y, o MigrateFeatureState definirá o estado de instalação do recurso Y no produto C para INSTALLstate \_ local.</span><span class="sxs-lookup"><span data-stu-id="9e60b-122">If an upgrade installs product C and migrates the installation state of feature Y, MigrateFeatureState sets the installation state of feature Y in product C to INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="9e60b-123">Para obter mais informações sobre como usar a ação MigrateFeatureStates para atualizações de produto, consulte [preparando um aplicativo para atualizações principais futuras](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="9e60b-123">For more information about how to use the MigrateFeatureStates action for product upgrades, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

 

 




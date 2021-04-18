---
description: As seções a seguir apresentam um exemplo de criação de um pacote de atualização para o aplicativo descrito em um exemplo de instalação.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Um exemplo de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768487"
---
# <a name="an-upgrade-example"></a><span data-ttu-id="3a45d-103">Um exemplo de atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-103">An Upgrade Example</span></span>

<span data-ttu-id="3a45d-104">As seções a seguir apresentam um exemplo de criação de um pacote de atualização para o aplicativo descrito em [um exemplo de instalação](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="3a45d-104">The following sections present an example of authoring an upgrade package for the application described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="3a45d-105">Um exemplo de uma interface de usuário mínima para esse exemplo é fornecido nos [componentes SDK do Windows para Windows Installer desenvolvedores](platform-sdk-components-for-windows-installer-developers.md) como o arquivo Uisample.msi.</span><span class="sxs-lookup"><span data-stu-id="3a45d-105">An example of a minimal user interface for this sample is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) as the file Uisample.msi.</span></span> <span data-ttu-id="3a45d-106">Se você tiver o SDK, terá acesso a todas as ferramentas e dados necessários para reproduzir o pacote de instalação de exemplo, a interface do usuário e o pacote de atualização de exemplo.</span><span class="sxs-lookup"><span data-stu-id="3a45d-106">If you have the SDK, you have access to all the tools and data necessary to reproduce the sample installation package, user interface, and sample upgrade package.</span></span>

<span data-ttu-id="3a45d-107">Este exemplo ilustra como criar um pacote de Windows Installer que atualiza o produto hipotético MNP2000 para um novo produto chamado MNP2001.</span><span class="sxs-lookup"><span data-stu-id="3a45d-107">This example illustrates how to create a Windows Installer package that upgrades the hypothetical product MNP2000 to a new product called MNP2001.</span></span> <span data-ttu-id="3a45d-108">O pacote de atualização de exemplo aplica uma atualização importante para o produto que requer a alteração do código do produto.</span><span class="sxs-lookup"><span data-stu-id="3a45d-108">The example upgrade package applies a major upgrade to the product which requires changing the product code.</span></span> <span data-ttu-id="3a45d-109">Para obter mais informações sobre atualizações principais, consulte o tópico sobre [atualizações importantes](major-upgrades.md) na seção [patches e atualizações](patching-and-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="3a45d-109">For more information about major upgrades, see the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section.</span></span>

<span data-ttu-id="3a45d-110">O pacote de atualização de exemplo tem as seguintes especificações:</span><span class="sxs-lookup"><span data-stu-id="3a45d-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="3a45d-111">Para se qualificar para receber essa atualização para o MNP2001, um usuário deve ter instalado anteriormente as versões 1,0 para 1,4 (inclusivas) do idioma inglês MNP2000 usando Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3a45d-111">To qualify to receive this upgrade to MNP2001, a user must have previously installed the 1.0 to 1.4 (inclusive) versions of English language MNP2000 using Windows Installer.</span></span>
-   <span data-ttu-id="3a45d-112">Quando um usuário tenta instalar o pacote de atualização, a funcionalidade de atualização do Windows Installer pesquisa o computador do usuário em busca de todos os produtos que se qualificam para a atualização.</span><span class="sxs-lookup"><span data-stu-id="3a45d-112">When a user attempts to install the upgrade package, the upgrade functionality of Windows Installer searches the user's computer for any products that qualify for the upgrade.</span></span>
-   <span data-ttu-id="3a45d-113">Windows Installer migra todas as configurações de recurso do produto original para o produto atualizado.</span><span class="sxs-lookup"><span data-stu-id="3a45d-113">Windows Installer migrates all the of the original product's feature settings to the upgraded product.</span></span>
-   <span data-ttu-id="3a45d-114">O instalador remove todos os recursos obsoletos do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a45d-114">The installer removes all obsolete features from the user's computer.</span></span>
-   <span data-ttu-id="3a45d-115">O instalador instala todos os novos recursos que pertencem à atualização.</span><span class="sxs-lookup"><span data-stu-id="3a45d-115">The installer installs all new features belonging to the upgrade.</span></span>
-   <span data-ttu-id="3a45d-116">Uma desinstalação do pacote de atualização remove o produto do computador do usuário e não restaura a versão anterior do produto.</span><span class="sxs-lookup"><span data-stu-id="3a45d-116">An uninstall of the upgrade package removes the product from the user's computer, and does not restore the earlier version of the product.</span></span>
-   <span data-ttu-id="3a45d-117">A atualização de exemplo atualiza atalhos para novos arquivos e recursos.</span><span class="sxs-lookup"><span data-stu-id="3a45d-117">The sample upgrade updates shortcuts to new files and features.</span></span>

    [<span data-ttu-id="3a45d-118">Planejando uma atualização principal</span><span class="sxs-lookup"><span data-stu-id="3a45d-118">Planning a Major Upgrade</span></span>](planning-a-major-upgrade.md)

    [<span data-ttu-id="3a45d-119">Importando banco de dados de instalação original</span><span class="sxs-lookup"><span data-stu-id="3a45d-119">Importing Original Installation Database</span></span>](importing-original-installation-database.md)

    [<span data-ttu-id="3a45d-120">Atualizando a estrutura de diretório para uma atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-120">Updating Directory Structure for an Upgrade</span></span>](updating-directory-structure-for-an-upgrade.md)

    [<span data-ttu-id="3a45d-121">Atualizando arquivos e atributos de arquivo para uma atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-121">Updating Files and File Attributes for an Upgrade</span></span>](updating-files-and-file-attributes-for-an-upgrade.md)

    [<span data-ttu-id="3a45d-122">Atualizando componentes para uma atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-122">Updating Components for an Upgrade</span></span>](updating-components-for-an-upgrade.md)

    [<span data-ttu-id="3a45d-123">Atualizando recursos para uma atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-123">Updating Features for an Upgrade</span></span>](updating-features-for-an-upgrade.md)

    [<span data-ttu-id="3a45d-124">Atualizando atalhos para uma atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-124">Updating Shortcuts for an Upgrade</span></span>](updating-shortcuts-for-an-upgrade.md)

    [<span data-ttu-id="3a45d-125">Atualizando a tabela de atualização para uma atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-125">Updating Upgrade Table for an Upgrade</span></span>](updating-upgrade-table-for-an-upgrade.md)

    [<span data-ttu-id="3a45d-126">Atualizando Propriedades para uma atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-126">Updating Properties for an Upgrade</span></span>](updating-properties-for-an-upgrade.md)

    [<span data-ttu-id="3a45d-127">Atualizando tabelas de sequência para uma atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-127">Updating Sequence Tables for an Upgrade</span></span>](updating-sequence-tables-for-an-upgrade.md)

    [<span data-ttu-id="3a45d-128">Atualizando informações de resumo para uma atualização</span><span class="sxs-lookup"><span data-stu-id="3a45d-128">Updating Summary Information for an Upgrade</span></span>](updating-summary-information-for-an-upgrade.md)

    [<span data-ttu-id="3a45d-129">Validando uma atualização de instalação</span><span class="sxs-lookup"><span data-stu-id="3a45d-129">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)

 

 




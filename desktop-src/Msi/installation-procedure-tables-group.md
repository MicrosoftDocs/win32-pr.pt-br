---
description: As tabelas no grupo de procedimentos de instalação controlam tarefas executadas durante a instalação por ações padrão e ações personalizadas.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Grupo de tabelas de procedimento de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297600"
---
# <a name="installation-procedure-tables-group"></a><span data-ttu-id="3c4b0-103">Grupo de tabelas de procedimento de instalação</span><span class="sxs-lookup"><span data-stu-id="3c4b0-103">Installation Procedure Tables Group</span></span>

<span data-ttu-id="3c4b0-104">As tabelas no grupo de procedimentos de instalação controlam tarefas executadas durante a instalação por [ações padrão](standard-actions.md) e [ações personalizadas](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3c4b0-104">The tables in the Installation Procedure group control tasks performed during the installation by [standard actions](standard-actions.md) and [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="3c4b0-105">Algumas das tabelas nesse grupo controlam uma ação de alto nível, fornecendo uma sequência de ações.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-105">Some of the tables in this group control a high level action by providing a sequence of actions.</span></span> <span data-ttu-id="3c4b0-106">Cada uma das tabelas de sequência a seguir controla uma parte de uma ação de alto nível.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-106">Each of the following sequence tables controls a portion of a high level action.</span></span>

-   [<span data-ttu-id="3c4b0-107">Tabela InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="3c4b0-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="3c4b0-108">Tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="3c4b0-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="3c4b0-109">Tabela AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="3c4b0-109">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="3c4b0-110">Tabela AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="3c4b0-110">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="3c4b0-111">Tabela AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="3c4b0-111">AdvtUISequence table</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="3c4b0-112">Tabela AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="3c4b0-112">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)

<span data-ttu-id="3c4b0-113">Pode haver situações em que uma instalação precisa fazer algo que não é possível usando apenas [ações padrão](standard-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3c4b0-113">There may be situations in which an installation needs to do something that is not possible using only [standard actions](standard-actions.md).</span></span> <span data-ttu-id="3c4b0-114">Para fornecer o maior grau de flexibilidade, o instalador fornece aos autores da instalação a capacidade de criar suas próprias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-114">To provide the greatest degree of flexibility, the installer provides setup authors the ability to create their own custom actions.</span></span> <span data-ttu-id="3c4b0-115">Se você tiver ações personalizadas, deverá registrá-las com o instalador preenchendo a tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-115">If you have any custom actions, you should register them with the installer by populating the CustomAction Table.</span></span>

<span data-ttu-id="3c4b0-116">A [tabela CustomAction](customaction-table.md) fornece os meios de integrar código e dados personalizados ao processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-116">The [CustomAction table](customaction-table.md) provides the means of integrating custom code and data into the installation process.</span></span> <span data-ttu-id="3c4b0-117">O código executado pode ser um fluxo contido no banco de dados, um arquivo recentemente instalado ou um executável existente.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-117">The code that is executed can be a stream contained within the database, a recently installed file, or an existing executable.</span></span>

<span data-ttu-id="3c4b0-118">As tabelas a seguir estendem os recursos do instalador para manipular arquivos e pastas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-118">The following tables extend the installer's capabilities to manipulate files and folders during the installation.</span></span>

-   <span data-ttu-id="3c4b0-119">A [tabela RemoveFile](removefile-table.md) contém uma lista de arquivos que são removidos durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-119">The [RemoveFile table](removefile-table.md) contains a list of files that are removed during the installation.</span></span>
-   <span data-ttu-id="3c4b0-120">A [tabela RemoveIniFile](removeinifile-table.md) contém as informações que um aplicativo precisa remover dos arquivos. ini.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-120">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to remove from .ini files.</span></span>
-   <span data-ttu-id="3c4b0-121">A [tabela RemoveRegistry](removeregistry-table.md) contém as informações que são excluídas do registro do sistema quando o componente correspondente é selecionado para ser instalado.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-121">The [RemoveRegistry table](removeregistry-table.md) contains the information which is deleted from the system registry when the corresponding component is selected to be installed.</span></span>
-   <span data-ttu-id="3c4b0-122">A [tabela CreateFolder](createfolder-table.md) lista as pastas que devem ser criadas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-122">The [CreateFolder table](createfolder-table.md) lists the folders that must be created during the installation.</span></span> <span data-ttu-id="3c4b0-123">Embora o instalador Crie pastas conforme necessário, elas são removidas assim que estiverem vazias.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-123">Although the installer creates folders as they are needed, these are removed as soon as they are empty.</span></span> <span data-ttu-id="3c4b0-124">A lista de pastas na tabela CreateFolder não é excluída até que o componente seja desinstalado.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-124">Folders list in the CreateFolder table are not deleted until the component is uninstalled.</span></span>
-   <span data-ttu-id="3c4b0-125">A [tabela MoveFile](movefile-table.md) contém uma lista de arquivos a serem movidos ou copiados de um diretório de origem especificado no computador do usuário para um diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-125">The [MoveFile table](movefile-table.md) contains a list of files to be moved or copied from a specified source directory on the user's computer to a destination directory.</span></span> <span data-ttu-id="3c4b0-126">Não é necessário usar a tabela MoveFile para descrever os arquivos associados aos componentes que você está instalando.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-126">It is not necessary to use the MoveFile table to describe the files associated with the components you are installing.</span></span>

<span data-ttu-id="3c4b0-127">Para configurar as condições necessárias que devem ser atendidas para iniciar a instalação, preencha a tabela LaunchCondition.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-127">To set up necessary conditions that must be met to initiate the installation, populate the LaunchCondition table.</span></span>

<span data-ttu-id="3c4b0-128">A [tabela LaunchCondition](launchcondition-table.md) contém uma lista de condições, que devem ser satisfeitas para que a ação seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3c4b0-128">The [LaunchCondition table](launchcondition-table.md) contains a list of conditions, all of which must be satisfied for the action to succeed.</span></span>

 

 




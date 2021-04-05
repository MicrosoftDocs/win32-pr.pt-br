---
description: Este exemplo ilustra como criar um pacote Windows Installer simples que instala um aplicativo.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Um exemplo de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828076"
---
# <a name="an-installation-example"></a><span data-ttu-id="ac92f-103">Um exemplo de instalação</span><span class="sxs-lookup"><span data-stu-id="ac92f-103">An Installation Example</span></span>

<span data-ttu-id="ac92f-104">Este exemplo ilustra como criar um pacote Windows Installer simples que instala um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac92f-104">This example illustrates how to create a simple Windows Installer package that installs an application.</span></span> <span data-ttu-id="ac92f-105">O exemplo instala o bloco de notas, um editor de texto incluído no Windows e vários arquivos de texto que descrevem eventos e admissões na arena de parque vermelho imaginário.</span><span class="sxs-lookup"><span data-stu-id="ac92f-105">The sample installs Notepad, a text editor included with Windows, and several text files describing events and admissions at the imaginary Red Park Arena.</span></span>

<span data-ttu-id="ac92f-106">O exemplo tem as seguintes especificações:</span><span class="sxs-lookup"><span data-stu-id="ac92f-106">The sample has the following specifications:</span></span>

-   <span data-ttu-id="ac92f-107">O aplicativo é fornecido aos usuários como um pacote de Windows Installer de instalação automática que instala todos os arquivos, atalhos e informações de registro necessários.</span><span class="sxs-lookup"><span data-stu-id="ac92f-107">The application is provided to users as a self-installing Windows Installer package that installs all the required files, shortcuts, and registry information.</span></span>
-   <span data-ttu-id="ac92f-108">O pacote de instalação pode apresentar um assistente de interface de usuário ao usuário durante a instalação para coletar informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="ac92f-108">The installation package may present a UI wizard to the user during setup to collect user information.</span></span>
-   <span data-ttu-id="ac92f-109">Durante a instalação, os usuários têm a opção de selecionar recursos individuais a serem instalados para execução local, para execução a partir de origem ou para não ser instalado.</span><span class="sxs-lookup"><span data-stu-id="ac92f-109">During setup, users have the option of selecting individual features to be installed to run-locally, to run-from-source, or to not be installed.</span></span>
-   <span data-ttu-id="ac92f-110">Um dos recursos pode ser apresentado aos usuários como um recurso de instalação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="ac92f-110">One of the features can be presented to users as an install-on-demand feature.</span></span>
-   <span data-ttu-id="ac92f-111">O mesmo pacote desinstala o aplicativo e remove todos os arquivos de aplicativo e informações de registro do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="ac92f-111">The same package uninstalls the application and removes all the application files and registry information from the user's computer.</span></span>
-   <span data-ttu-id="ac92f-112">O pacote está preparado para receber uma atualização importante que inclui a alteração do código do produto.</span><span class="sxs-lookup"><span data-stu-id="ac92f-112">The package is prepared to receive a major upgrade that includes changing its product code.</span></span>

<span data-ttu-id="ac92f-113">Para reproduzir o exemplo, você precisa de uma ferramenta de software capaz de criar e editar um banco de dados Windows Installer em branco.</span><span class="sxs-lookup"><span data-stu-id="ac92f-113">To reproduce the example, you need a software tool capable of creating and editing a blank Windows Installer database.</span></span> <span data-ttu-id="ac92f-114">Várias ferramentas de criação de pacote estão disponíveis de fornecedores de software independentes.</span><span class="sxs-lookup"><span data-stu-id="ac92f-114">Several package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="ac92f-115">Um editor de banco de dados Windows Installer chamado Orca é fornecido no [SDK do Windows components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="ac92f-115">A Windows Installer database editor called Orca is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="ac92f-116">Para concluir o exemplo, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="ac92f-116">To complete the example, follow these steps:</span></span>

[<span data-ttu-id="ac92f-117">Planejando a instalação</span><span class="sxs-lookup"><span data-stu-id="ac92f-117">Planning the Installation</span></span>](planning-the-installation.md)

[<span data-ttu-id="ac92f-118">Importando um banco de dados em branco</span><span class="sxs-lookup"><span data-stu-id="ac92f-118">Importing a Blank Database</span></span>](importing-a-blank-database.md)

[<span data-ttu-id="ac92f-119">Especificando a estrutura do diretório</span><span class="sxs-lookup"><span data-stu-id="ac92f-119">Specifying Directory Structure</span></span>](specifying-directory-structure.md)

[<span data-ttu-id="ac92f-120">Especificando componentes</span><span class="sxs-lookup"><span data-stu-id="ac92f-120">Specifying Components</span></span>](specifying-components.md)

[<span data-ttu-id="ac92f-121">Especificando arquivos e atributos de arquivo</span><span class="sxs-lookup"><span data-stu-id="ac92f-121">Specifying Files and File Attributes</span></span>](specifying-files-and-file-attributes.md)

[<span data-ttu-id="ac92f-122">Especificando a mídia de origem</span><span class="sxs-lookup"><span data-stu-id="ac92f-122">Specifying Source Media</span></span>](specifying-source-media.md)

[<span data-ttu-id="ac92f-123">Especificando recursos</span><span class="sxs-lookup"><span data-stu-id="ac92f-123">Specifying Features</span></span>](specifying-features.md)

[<span data-ttu-id="ac92f-124">Especificando relações de Feature-Component</span><span class="sxs-lookup"><span data-stu-id="ac92f-124">Specifying Feature-Component Relationships</span></span>](specifying-feature-component-relationships.md)

[<span data-ttu-id="ac92f-125">Adicionando informações do registro</span><span class="sxs-lookup"><span data-stu-id="ac92f-125">Adding Registry Information</span></span>](adding-registry-information.md)

[<span data-ttu-id="ac92f-126">Especificando atalhos</span><span class="sxs-lookup"><span data-stu-id="ac92f-126">Specifying Shortcuts</span></span>](specifying-shortcuts.md)

[<span data-ttu-id="ac92f-127">Especificando propriedades</span><span class="sxs-lookup"><span data-stu-id="ac92f-127">Specifying Properties</span></span>](specifying-properties.md)

[<span data-ttu-id="ac92f-128">Importando o InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ac92f-128">Importing the InstallExecuteSequence</span></span>](importing-the-installexecutesequence.md)

[<span data-ttu-id="ac92f-129">Importando o InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="ac92f-129">Importing the InstallUISequence</span></span>](importing-the-installuisequence.md)

[<span data-ttu-id="ac92f-130">Importando o AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ac92f-130">Importing the AdminExecuteSequence</span></span>](importing-the-adminexecutesequence.md)

[<span data-ttu-id="ac92f-131">Importando o AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="ac92f-131">Importing the AdminUISequence</span></span>](importing-the-adminuisequence.md)

[<span data-ttu-id="ac92f-132">Importando o AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ac92f-132">Importing the AdvtExecuteSequence</span></span>](importing-the-advtexecutesequence.md)

[<span data-ttu-id="ac92f-133">Adicionando informações de resumo</span><span class="sxs-lookup"><span data-stu-id="ac92f-133">Adding Summary Information</span></span>](adding-summary-information.md)

[<span data-ttu-id="ac92f-134">Importando a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="ac92f-134">Importing the User Interface</span></span>](importing-the-user-interface.md)

[<span data-ttu-id="ac92f-135">Validando um banco de dados de instalação</span><span class="sxs-lookup"><span data-stu-id="ac92f-135">Validating an Installation Database</span></span>](validating-an-installation-database.md)

 

 




---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca95a473f648ca9e1a08773d93f47bd198df11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828983"
---
# <a name="i-windows-installer"></a><span data-ttu-id="935f5-103">I (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="935f5-103">I (Windows Installer)</span></span>

<span data-ttu-id="935f5-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H i J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="935f5-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="935f5-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**arquivo. IDT**</span><span class="sxs-lookup"><span data-stu-id="935f5-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-106">Tabela de banco de dados do instalador exportada.</span><span class="sxs-lookup"><span data-stu-id="935f5-106">Exported installer database table.</span></span> <span data-ttu-id="935f5-107">Para obter mais informações, consulte [importando e exportando](importing-and-exporting.md) e [Windows Installer extensões de arquivo](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="935f5-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Importar tabela de endereços (IAT)**</span><span class="sxs-lookup"><span data-stu-id="935f5-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-109">Onde o endereço virtual computado é salvo de cada função importada de todas as DLLs.</span><span class="sxs-lookup"><span data-stu-id="935f5-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="935f5-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interface do usuário interna**</span><span class="sxs-lookup"><span data-stu-id="935f5-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-111">Recursos internos do instalador que podem ser usados para criar uma interface gráfica do usuário para instalação.</span><span class="sxs-lookup"><span data-stu-id="935f5-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="935f5-112">Um autor pode escolher uma [*interface de usuário externa*](e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="935f5-113">Para obter mais informações, consulte [sobre a interface do usuário](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="935f5-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**nível de instalação**</span><span class="sxs-lookup"><span data-stu-id="935f5-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-115">Valor de instalação especificado.</span><span class="sxs-lookup"><span data-stu-id="935f5-115">Specified installation value.</span></span> <span data-ttu-id="935f5-116">Um aplicativo será instalado somente se seu próprio nível for menor ou igual ao nível de instalação.</span><span class="sxs-lookup"><span data-stu-id="935f5-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="935f5-117">O conjunto de aplicativos escolhido para instalação pode, portanto, ser alterado alterando o nível de instalação.</span><span class="sxs-lookup"><span data-stu-id="935f5-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="935f5-118">Para obter mais informações, consulte [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="935f5-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**instalação sob demanda**</span><span class="sxs-lookup"><span data-stu-id="935f5-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-120">Serviço que instala aplicativos ou recursos conforme solicitado pelo usuário ou outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="935f5-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="935f5-121">O [*anúncio*](a-gly.md) disponibiliza um recurso ou aplicativo para instalação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="935f5-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="935f5-122">Para obter mais informações, consulte: [instalação sob demanda](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="935f5-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contexto de instalação**</span><span class="sxs-lookup"><span data-stu-id="935f5-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-124">A combinação de direitos de instalação e tipos de instalação produz três contextos de instalação diferentes: por usuário, gerenciado por usuário e gerenciado por computador.</span><span class="sxs-lookup"><span data-stu-id="935f5-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="935f5-125">Não há tal coisa como não gerenciado por computador.</span><span class="sxs-lookup"><span data-stu-id="935f5-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="935f5-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**instalador**</span><span class="sxs-lookup"><span data-stu-id="935f5-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-127">O [*Windows Installer*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="935f5-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**banco de dados do instalador**</span><span class="sxs-lookup"><span data-stu-id="935f5-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-129">Banco de dados relacional que contém instruções de instalação para uma instalação do.</span><span class="sxs-lookup"><span data-stu-id="935f5-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="935f5-130">O banco de dados do instalador é armazenado no [*arquivo. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="935f5-131">Para obter mais informações, consulte [instalador Database](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="935f5-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**função do instalador**</span><span class="sxs-lookup"><span data-stu-id="935f5-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-133">Chamado por um usuário ou aplicativo para obter os serviços e a funcionalidade do instalador.</span><span class="sxs-lookup"><span data-stu-id="935f5-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="935f5-134">Esta é a interface de programação de aplicativo do instalador.</span><span class="sxs-lookup"><span data-stu-id="935f5-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="935f5-135">Para obter informações, consulte [referência da função do instalador](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="935f5-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**ferramenta de criação de pacote do instalador**</span><span class="sxs-lookup"><span data-stu-id="935f5-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-137">Software que permite que um desenvolvedor crie e edite um [*arquivo. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="935f5-138">Isso junto com qualquer [*arquivo de origem externo*](e-gly.md) , composto por um [*pacote*](p-gly.md) contendo todas as informações necessárias para uma instalação.</span><span class="sxs-lookup"><span data-stu-id="935f5-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="935f5-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**arquivos de origem internos**</span><span class="sxs-lookup"><span data-stu-id="935f5-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="935f5-140">Armazenado no [*arquivo. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="935f5-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="935f5-141">Vários arquivos de origem internos podem ser compactados e armazenados juntos em um [*arquivo de gabinete*](c-gly.md) que é armazenado em um arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="935f5-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 




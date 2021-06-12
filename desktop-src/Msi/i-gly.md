---
description: Saiba mais Windows Installer conceitos que começam com a letra I, como a tabela Importar Endereço e o nível de instalação.
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33b5cfb9c4545a5482b214e0413ab3e3d981109
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010649"
---
# <a name="i-windows-installer"></a><span data-ttu-id="adf8f-103">I (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="adf8f-103">I (Windows Installer)</span></span>

<span data-ttu-id="adf8f-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](f-gly.md) [](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="adf8f-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="adf8f-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**Arquivo .idt**</span><span class="sxs-lookup"><span data-stu-id="adf8f-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-106">Tabela de banco de dados do instalador exportado.</span><span class="sxs-lookup"><span data-stu-id="adf8f-106">Exported installer database table.</span></span> <span data-ttu-id="adf8f-107">Para obter mais informações, [consulte Importando e exportando e](importing-and-exporting.md) Windows Installer [extensões de arquivo](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="adf8f-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Tabela Importar Endereço (IAT)**</span><span class="sxs-lookup"><span data-stu-id="adf8f-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-109">Onde o endereço virtual computado é salvo de cada função importada de todas as DLLs.</span><span class="sxs-lookup"><span data-stu-id="adf8f-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interface do usuário interna**</span><span class="sxs-lookup"><span data-stu-id="adf8f-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-111">Recursos integrados do instalador que podem ser usados para a autor de uma interface do usuário gráfica para instalação.</span><span class="sxs-lookup"><span data-stu-id="adf8f-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="adf8f-112">Um autor pode escolher uma [*interface do usuário externa*](e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="adf8f-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="adf8f-113">Para obter mais informações, [consulte Sobre o Interface do Usuário](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="adf8f-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**nível de instalação**</span><span class="sxs-lookup"><span data-stu-id="adf8f-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-115">Valor de instalação especificado.</span><span class="sxs-lookup"><span data-stu-id="adf8f-115">Specified installation value.</span></span> <span data-ttu-id="adf8f-116">Um aplicativo será instalado somente se seu próprio nível for menor ou igual ao nível de instalação.</span><span class="sxs-lookup"><span data-stu-id="adf8f-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="adf8f-117">Portanto, o conjunto de aplicativos escolhido para instalação pode ser alterado alterando o nível de instalação.</span><span class="sxs-lookup"><span data-stu-id="adf8f-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="adf8f-118">Para obter mais informações, consulte [Tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="adf8f-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**instalação sob demanda**</span><span class="sxs-lookup"><span data-stu-id="adf8f-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-120">Serviço que instala aplicativos ou recursos conforme solicitado pelo usuário ou outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="adf8f-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="adf8f-121">[*A publicidade*](a-gly.md) disponibiliza um recurso ou aplicativo para instalação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="adf8f-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="adf8f-122">Para obter mais informações, consulte: [Instalação sob demanda.](installation-on-demand.md)</span><span class="sxs-lookup"><span data-stu-id="adf8f-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contexto de instalação**</span><span class="sxs-lookup"><span data-stu-id="adf8f-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-124">A combinação de direitos de instalação e tipos de instalação produz três contextos de instalação diferentes: por usuário não gerenciado, gerenciado por usuário e gerenciado por computador.</span><span class="sxs-lookup"><span data-stu-id="adf8f-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="adf8f-125">Não há essa coisa de não gerenciado por computador.</span><span class="sxs-lookup"><span data-stu-id="adf8f-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**Instalador**</span><span class="sxs-lookup"><span data-stu-id="adf8f-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-127">O [*Windows Installer*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="adf8f-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**banco de dados do instalador**</span><span class="sxs-lookup"><span data-stu-id="adf8f-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-129">Banco de dados relacional que contém instruções de instalação para uma instalação.</span><span class="sxs-lookup"><span data-stu-id="adf8f-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="adf8f-130">O banco de dados do instalador é armazenado [*no arquivo.msi .*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="adf8f-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="adf8f-131">Para obter mais informações, consulte [Installer Database](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="adf8f-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**função do instalador**</span><span class="sxs-lookup"><span data-stu-id="adf8f-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-133">Chamado por um usuário ou aplicativo para obter serviços e funcionalidades do instalador.</span><span class="sxs-lookup"><span data-stu-id="adf8f-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="adf8f-134">Essa é a interface de programação de aplicativo do instalador.</span><span class="sxs-lookup"><span data-stu-id="adf8f-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="adf8f-135">Para obter informações, consulte [Referência de função do instalador](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="adf8f-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**ferramenta de autor de pacote do instalador**</span><span class="sxs-lookup"><span data-stu-id="adf8f-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-137">Software que permite que um desenvolvedor crie e edite um [*arquivo.msi .*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="adf8f-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="adf8f-138">Isso junto com os [*arquivos de origem externos*](e-gly.md) compõem [*um*](p-gly.md) pacote que contém todas as informações necessárias para uma instalação.</span><span class="sxs-lookup"><span data-stu-id="adf8f-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="adf8f-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**arquivos de origem internos**</span><span class="sxs-lookup"><span data-stu-id="adf8f-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="adf8f-140">Armazenado no arquivo [*.msi .*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="adf8f-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="adf8f-141">Vários arquivos de origem internos podem ser compactados e armazenados juntos em um arquivo [*de gabinete*](c-gly.md) armazenado em um .msi arquivo.</span><span class="sxs-lookup"><span data-stu-id="adf8f-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 




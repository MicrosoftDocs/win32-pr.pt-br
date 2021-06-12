---
description: Saiba mais Windows Installer conceitos que começam com a letra C, como arquivo de gabinete e checksum.
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e7af99ad32d8dff7f4e8509976b0004045477b
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010919"
---
# <a name="c-windows-installer"></a><span data-ttu-id="dbc8b-103">C (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="dbc8b-103">C (Windows Installer)</span></span>

<span data-ttu-id="dbc8b-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="dbc8b-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="dbc8b-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**arquivo de gabinete**</span><span class="sxs-lookup"><span data-stu-id="dbc8b-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**cabinet file**</span></span>
</dt> <dd>

<span data-ttu-id="dbc8b-106">Arquivo único, geralmente com uma .cab, que armazena arquivos compactados em uma biblioteca de arquivos.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-106">Single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="dbc8b-107">O formato de gabinete é uma maneira eficiente de empacotar vários arquivos porque a compactação é executada entre limites de arquivo, melhorando significativamente a taxa de compactação.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-107">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, significantly improving compression ratio.</span></span> <span data-ttu-id="dbc8b-108">Para obter informações sobre como criar gabinetes, consulte [Arquivos de gabinete](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="dbc8b-108">For information about creating cabinets, see [Cabinet Files](cabinet-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbc8b-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**Soma**</span><span class="sxs-lookup"><span data-stu-id="dbc8b-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span></span>
</dt> <dd>

<span data-ttu-id="dbc8b-110">Valor computado que depende do conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-110">Computed value that depends on the contents of a file.</span></span> <span data-ttu-id="dbc8b-111">Ele é armazenado com dados para detectar corrupção de arquivo.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-111">It is stored with data to detect file corruption.</span></span> <span data-ttu-id="dbc8b-112">O sistema verifica esse valor para garantir que os dados não são interrompidos.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-112">The system checks this value to ensure that the data is uncorrupted.</span></span>

</dd> <dt>

<span data-ttu-id="dbc8b-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**Componente**</span><span class="sxs-lookup"><span data-stu-id="dbc8b-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="dbc8b-114">A menor parte de uma instalação manipulada pelo instalador, também um bloco de construção de um aplicativo ou recurso da perspectiva do programador.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-114">Smallest piece of an installation handled by the installer, also a building-block of an application or feature from the programmer's perspective.</span></span> <span data-ttu-id="dbc8b-115">Exemplos de componentes são um grupo de arquivos relacionados, um objeto COM ou uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-115">Examples of components are a group of related files, a COM object, or a library.</span></span> <span data-ttu-id="dbc8b-116">Para obter mais informações, consulte [Componentes e recursos](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="dbc8b-116">For more information, see [Components and Features](components-and-features.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbc8b-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**commitindo bancos de dados**</span><span class="sxs-lookup"><span data-stu-id="dbc8b-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**committing databases**</span></span>
</dt> <dd>

<span data-ttu-id="dbc8b-118">Alterações acumuladas feitas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-118">Accumulated changes made in a database.</span></span> <span data-ttu-id="dbc8b-119">As alterações não são refletidas no banco de dados real até que o banco de dados seja confirmado.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-119">The changes are not reflected in the actual database until the database is committed.</span></span> <span data-ttu-id="dbc8b-120">Para obter mais informações, consulte [Committing Databases](committing-databases.md).</span><span class="sxs-lookup"><span data-stu-id="dbc8b-120">For more information, see [Committing Databases](committing-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbc8b-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span><span class="sxs-lookup"><span data-stu-id="dbc8b-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span></span>
</dt> <dd>

<span data-ttu-id="dbc8b-122">Aspecto da funcionalidade da interface do usuário do instalador.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-122">Aspect of functionality of the installer's user interface.</span></span> <span data-ttu-id="dbc8b-123">Um ControlEvent típico dispara alguma ação do instalador após a ativação de um controle de caixa de diálogo ou outro evento.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-123">A typical ControlEvent triggers some action by the installer upon the activation of a dialog box control or other event.</span></span> <span data-ttu-id="dbc8b-124">Para obter mais informações, consulte [Visão geral do ControlEvent.](controlevent-overview.md)</span><span class="sxs-lookup"><span data-stu-id="dbc8b-124">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbc8b-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**Custando**</span><span class="sxs-lookup"><span data-stu-id="dbc8b-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costing**</span></span>
</dt> <dd>

<span data-ttu-id="dbc8b-126">Método usado pelo instalador para determinar os requisitos de espaço em disco para instalação.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-126">Method used by the installer to determine disk space requirements for installation.</span></span> <span data-ttu-id="dbc8b-127">O custo leva em conta fatores como se os arquivos existentes precisam ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-127">Costing takes into account factors such as whether existing files need to be overwritten.</span></span> <span data-ttu-id="dbc8b-128">Para obter mais informações, consulte [Custo do arquivo](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="dbc8b-128">For more information, see [File Costing](file-costing.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbc8b-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**Arquivo .file**</span><span class="sxs-lookup"><span data-stu-id="dbc8b-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub file**</span></span>
</dt> <dd>

<span data-ttu-id="dbc8b-130">Módulo de validação que armazena e fornece acesso a ações personalizadas do ICE.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-130">Validation module that stores and provides access to ICE custom actions.</span></span> <span data-ttu-id="dbc8b-131">Para obter mais informações, consulte [Arquivo .cú de exemplo](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="dbc8b-131">For more information, see [Sample .cub File](sample--cub-file.md).</span></span> <span data-ttu-id="dbc8b-132">Para obter mais informações, consulte [também Windows Installer extensões de arquivo](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="dbc8b-132">For more information, see also [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbc8b-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**ação personalizada**</span><span class="sxs-lookup"><span data-stu-id="dbc8b-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**custom action**</span></span>
</dt> <dd>

<span data-ttu-id="dbc8b-134">Escrito pelo autor do [*pacote, mas*](p-gly.md) não integrado ao instalador como uma ação padrão.</span><span class="sxs-lookup"><span data-stu-id="dbc8b-134">Written by the author of the [*package*](p-gly.md) but not built into the installer as a standard action.</span></span> <span data-ttu-id="dbc8b-135">Para obter mais informações, consulte [Ações personalizadas.](custom-actions.md)</span><span class="sxs-lookup"><span data-stu-id="dbc8b-135">For more information, see [Custom Actions](custom-actions.md).</span></span>

</dd> </dl>

 

 




---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091534"
---
# <a name="p-windows-installer"></a><span data-ttu-id="b8b1a-103">P (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="b8b1a-103">P (Windows Installer)</span></span>

<span data-ttu-id="b8b1a-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="b8b1a-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="b8b1a-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**agrupa**</span><span class="sxs-lookup"><span data-stu-id="b8b1a-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="b8b1a-106">[*arquivo. msi*](m-gly.md) e quaisquer [*arquivos de origem externos*](e-gly.md) que possam ser apontados por esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="b8b1a-107">Portanto, um pacote contém todas as informações que o Windows Installer precisa para executar a interface do usuário e instalar ou desinstalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="b8b1a-108">Para obter mais informações, consulte também [*banco de dados do instalador*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b8b1a-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b1a-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**código do pacote**</span><span class="sxs-lookup"><span data-stu-id="b8b1a-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="b8b1a-110">GUID que identifica um pacote específico.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="b8b1a-111">Um código de pacote exclusivo é necessário porque algumas transformações ou pacotes de patch podem ser aplicados a mais de um aplicativo ou podem atualizar um aplicativo para outro aplicativo ou versão.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="b8b1a-112">Para obter mais informações, consulte [Package codes](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b8b1a-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b1a-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patch**</span><span class="sxs-lookup"><span data-stu-id="b8b1a-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="b8b1a-114">Método de atualização de um arquivo que substitui somente os bits que estão sendo alterados, em vez de todo o arquivo.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="b8b1a-115">Isso significa que os usuários podem baixar um patch de atualização para um produto que seja muito menor do que o produto inteiro.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="b8b1a-116">Para obter mais informações, consulte [pacotes de patch](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="b8b1a-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b1a-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**arquivo de patch**</span><span class="sxs-lookup"><span data-stu-id="b8b1a-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="b8b1a-118">[Pacote P corresponder](patch-packages.md) usado para aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="b8b1a-119">Para obter mais informações, consulte [patches e atualizações](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="b8b1a-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b1a-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modo de visualização**</span><span class="sxs-lookup"><span data-stu-id="b8b1a-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="b8b1a-121">Modo para exibir o design da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="b8b1a-122">Para obter mais informações, consulte [visualizando a interface do usuário](previewing-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b8b1a-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b1a-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**barra de progresso**</span><span class="sxs-lookup"><span data-stu-id="b8b1a-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="b8b1a-124">O controle do instalador pode ser exibido durante o tempo de execução do script que representa o progresso da instalação.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="b8b1a-125">Para obter mais informações, consulte [criando um controle ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="b8b1a-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b1a-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="b8b1a-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="b8b1a-127">Variáveis globais usadas durante uma instalação.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-127">Global variables used during an installation.</span></span> <span data-ttu-id="b8b1a-128">(Consulte [sobre propriedades](about-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="b8b1a-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="b8b1a-129">O termo "Propriedade" também se refere a um atributo de um objeto de automação.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="b8b1a-130">(Consulte [interface de automação](automation-interface.md).)</span><span class="sxs-lookup"><span data-stu-id="b8b1a-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="b8b1a-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**editor**</span><span class="sxs-lookup"><span data-stu-id="b8b1a-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="b8b1a-132">Método de [*anunciar*](a-gly.md) um recurso ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="b8b1a-133">A publicação não preenche a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="b8b1a-134">No entanto, se outro aplicativo tentar abrir um aplicativo publicado, há informações suficientes presentes para o instalador atribuir o aplicativo publicado.</span><span class="sxs-lookup"><span data-stu-id="b8b1a-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="b8b1a-135">Para obter mais informações, consulte [*atribuindo*](a-gly.md) e [componentes e recursos](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="b8b1a-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 




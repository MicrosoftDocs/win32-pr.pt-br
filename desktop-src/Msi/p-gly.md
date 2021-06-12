---
description: Saiba mais sobre os conceitos de Windows Installer que começam com a letra P, como código de pacote e aplicação de patches.
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8923359197916a1186fe28ab0d12e4118b989bc
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011092"
---
# <a name="p-windows-installer"></a><span data-ttu-id="1303f-103">P (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="1303f-103">P (Windows Installer)</span></span>

<span data-ttu-id="1303f-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="1303f-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="1303f-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**agrupa**</span><span class="sxs-lookup"><span data-stu-id="1303f-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="1303f-106">[*.msi arquivo*](m-gly.md) e quaisquer [*arquivos de origem externos*](e-gly.md) que possam ser apontados por esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="1303f-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="1303f-107">Portanto, um pacote contém todas as informações que o Windows Installer precisa para executar a interface do usuário e instalar ou desinstalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1303f-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="1303f-108">Para obter mais informações, consulte também [*banco de dados do instalador*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1303f-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1303f-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**código do pacote**</span><span class="sxs-lookup"><span data-stu-id="1303f-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="1303f-110">GUID que identifica um pacote específico.</span><span class="sxs-lookup"><span data-stu-id="1303f-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="1303f-111">Um código de pacote exclusivo é necessário porque algumas transformações ou pacotes de patch podem ser aplicados a mais de um aplicativo ou podem atualizar um aplicativo para outro aplicativo ou versão.</span><span class="sxs-lookup"><span data-stu-id="1303f-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="1303f-112">Para obter mais informações, consulte [Package codes](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1303f-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="1303f-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patch**</span><span class="sxs-lookup"><span data-stu-id="1303f-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="1303f-114">Método de atualização de um arquivo que substitui somente os bits que estão sendo alterados, em vez de todo o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1303f-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="1303f-115">Isso significa que os usuários podem baixar um patch de atualização para um produto que seja muito menor do que o produto inteiro.</span><span class="sxs-lookup"><span data-stu-id="1303f-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="1303f-116">Para obter mais informações, consulte [pacotes de patch](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="1303f-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="1303f-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**arquivo de patch**</span><span class="sxs-lookup"><span data-stu-id="1303f-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="1303f-118">[Pacote P corresponder](patch-packages.md) usado para aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="1303f-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="1303f-119">Para obter mais informações, consulte [patches e atualizações](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="1303f-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="1303f-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modo de visualização**</span><span class="sxs-lookup"><span data-stu-id="1303f-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="1303f-121">Modo para exibir o design da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1303f-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="1303f-122">Para obter mais informações, consulte [visualizando a interface do usuário](previewing-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="1303f-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="1303f-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**barra de progresso**</span><span class="sxs-lookup"><span data-stu-id="1303f-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="1303f-124">O controle do instalador pode ser exibido durante o tempo de execução do script que representa o progresso da instalação.</span><span class="sxs-lookup"><span data-stu-id="1303f-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="1303f-125">Para obter mais informações, consulte [criando um controle ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="1303f-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="1303f-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="1303f-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="1303f-127">Variáveis globais usadas durante uma instalação.</span><span class="sxs-lookup"><span data-stu-id="1303f-127">Global variables used during an installation.</span></span> <span data-ttu-id="1303f-128">(Consulte [sobre propriedades](about-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="1303f-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="1303f-129">O termo "Propriedade" também se refere a um atributo de um objeto de automação.</span><span class="sxs-lookup"><span data-stu-id="1303f-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="1303f-130">(Consulte [interface de automação](automation-interface.md).)</span><span class="sxs-lookup"><span data-stu-id="1303f-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="1303f-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**editor**</span><span class="sxs-lookup"><span data-stu-id="1303f-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="1303f-132">Método de [*anunciar*](a-gly.md) um recurso ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1303f-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="1303f-133">A publicação não preenche a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1303f-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="1303f-134">No entanto, se outro aplicativo tentar abrir um aplicativo publicado, há informações suficientes presentes para o instalador atribuir o aplicativo publicado.</span><span class="sxs-lookup"><span data-stu-id="1303f-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="1303f-135">Para obter mais informações, consulte [*atribuindo*](a-gly.md) e [componentes e recursos](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="1303f-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 




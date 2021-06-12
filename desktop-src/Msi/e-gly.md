---
description: Saiba mais sobre os conceitos de Windows Installer que começam com a letra E, como um arquivo de origem com privilégios elevados e externos.
ms.assetid: 8f180e2c-06f4-41d5-b167-52525f4a9985
title: E (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2c65c50427b1f8271be838971a387388ea53db
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011089"
---
# <a name="e-windows-installer"></a><span data-ttu-id="017b7-103">E (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="017b7-103">E (Windows Installer)</span></span>

<span data-ttu-id="017b7-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="017b7-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="017b7-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**com privilégios elevados**</span><span class="sxs-lookup"><span data-stu-id="017b7-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**elevated**</span></span>
</dt> <dd>

<span data-ttu-id="017b7-106">As ações executadas com privilégios de sistema são chamadas elevadas.</span><span class="sxs-lookup"><span data-stu-id="017b7-106">Actions performed with system privileges are called elevated.</span></span>

</dd> <dt>

<span data-ttu-id="017b7-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**fase de execução**</span><span class="sxs-lookup"><span data-stu-id="017b7-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**execution phase**</span></span>
</dt> <dd>

<span data-ttu-id="017b7-108">Quando o instalador executa um script de ações do instalador.</span><span class="sxs-lookup"><span data-stu-id="017b7-108">When the installer executes a script of installer actions.</span></span> <span data-ttu-id="017b7-109">No Microsoft Windows 2000, esse processo é executado pelo serviço do instalador.</span><span class="sxs-lookup"><span data-stu-id="017b7-109">In Microsoft Windows 2000, this process is performed by the installer service.</span></span> <span data-ttu-id="017b7-110">Em um aplicativo gerenciado, o script é executado com privilégios de sistema.</span><span class="sxs-lookup"><span data-stu-id="017b7-110">In a managed application, the script is executed with system privileges.</span></span> <span data-ttu-id="017b7-111">Para obter mais informações, consulte [mecanismo de instalação](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="017b7-111">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="017b7-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**script de execução**</span><span class="sxs-lookup"><span data-stu-id="017b7-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**execution script**</span></span>
</dt> <dd>

<span data-ttu-id="017b7-113">Ações do instalador para uma instalação.</span><span class="sxs-lookup"><span data-stu-id="017b7-113">Installer actions for an installation.</span></span> <span data-ttu-id="017b7-114">O script de execução é gerado durante a [*fase de aquisição*](a-gly.md) da instalação e executado durante a fase de [*execução*](/windows).</span><span class="sxs-lookup"><span data-stu-id="017b7-114">The execution script is generated during the [*acquisition phase*](a-gly.md) of installation and executed during the [*execution phase*](/windows).</span></span> <span data-ttu-id="017b7-115">Para obter mais informações, consulte [mecanismo de instalação](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="017b7-115">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="017b7-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**arquivos de origem externos**</span><span class="sxs-lookup"><span data-stu-id="017b7-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**external source files**</span></span>
</dt> <dd>

<span data-ttu-id="017b7-117">Arquivos de origem do aplicativo que está sendo instalado que são armazenados fora do [*arquivo de.msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="017b7-117">Source files of the application being installed that are stored outside of the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="017b7-118">Vários arquivos de origem externos podem ser compactados e armazenados juntos dentro de um [*arquivo de gabinete*](c-gly.md) incluído no [*pacote*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="017b7-118">Multiple external source files can be compressed and stored together inside of a [*cabinet file*](c-gly.md) included in the [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="017b7-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**interface do usuário externa**</span><span class="sxs-lookup"><span data-stu-id="017b7-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**external user interface**</span></span>
</dt> <dd>

<span data-ttu-id="017b7-120">Interface do usuário fornecida pelo autor de um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="017b7-120">UI provided by the author of an installation package.</span></span> <span data-ttu-id="017b7-121">Ele não usa os recursos internos de interface do usuário do instalador.</span><span class="sxs-lookup"><span data-stu-id="017b7-121">It does not use the internal UI capabilities of the installer.</span></span> <span data-ttu-id="017b7-122">Para obter mais informações, consulte [sobre a interface do usuário](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="017b7-122">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> </dl>

 

 

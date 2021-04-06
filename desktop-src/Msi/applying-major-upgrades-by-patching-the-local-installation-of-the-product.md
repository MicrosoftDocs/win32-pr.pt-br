---
description: Uma atualização importante pode ser aplicada a um aplicativo por meio da aplicação de patch na instalação local do aplicativo a partir da linha de comando ou usando um executável.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Aplicando as principais atualizações por meio da aplicação de patch na instalação local do produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828071"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="f68bb-103">Aplicando as principais atualizações por meio da aplicação de patch na instalação local do produto</span><span class="sxs-lookup"><span data-stu-id="f68bb-103">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="f68bb-104">Uma atualização importante pode ser aplicada a um aplicativo por meio da aplicação de patch na instalação local do aplicativo a partir da linha de comando ou usando um executável.</span><span class="sxs-lookup"><span data-stu-id="f68bb-104">A major upgrade can be applied to an application by patching the local installation of the application from the command line or by using an executable.</span></span>

> [!Note]  
> <span data-ttu-id="f68bb-105">Não é recomendável fornecer uma atualização importante como um pacote de patch porque um pacote de patch de atualização importante não pode ser sequenciado com outras atualizações e porque o patch não é um [patch desinstalável](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="f68bb-105">Providing a major upgrade as a patch package is not recommended because a major upgrade patch package cannot be sequenced with other updates and because the patch is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="f68bb-106">O utilitário de [Msimsp.exe](msimsp-exe.md) não pode ser usado para gerar um pacote de patch que aplica uma atualização importante.</span><span class="sxs-lookup"><span data-stu-id="f68bb-106">The [Msimsp.exe](msimsp-exe.md) utility cannot be used to generate a patch package that applies a major upgrade.</span></span> <span data-ttu-id="f68bb-107">Em vez disso, aplique atualizações importantes, conforme descrito em [aplicando as principais atualizações instalando o produto](applying-major-upgrades-by-installing-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="f68bb-107">Instead, apply major upgrades as described in [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).</span></span>

 

<span data-ttu-id="f68bb-108">**Para aplicar um patch de atualização importante a uma instalação local do produto**</span><span class="sxs-lookup"><span data-stu-id="f68bb-108">**To apply a major upgrade patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="f68bb-109">Inicie a instalação do patch na linha de comando ou usando um executável.</span><span class="sxs-lookup"><span data-stu-id="f68bb-109">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="f68bb-110">Para iniciar a partir da linha de comando, use msiexec/p patch. msp.</span><span class="sxs-lookup"><span data-stu-id="f68bb-110">To launch from the command line, use msiexec /p patch.msp.</span></span> <span data-ttu-id="f68bb-111">Para iniciar a partir de um executável, chame [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou o [**método ApplyPatch**](installer-applypatch.md) e forneça os mesmos argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f68bb-111">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="f68bb-112">Ao aplicar patch na instalação de um cliente, o instalador ignora a origem da instalação e prossegue para corrigir os arquivos que já estão instalados no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="f68bb-112">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="f68bb-113">O instalador altera todos os componentes com patches marcados como executar da origem para execução local.</span><span class="sxs-lookup"><span data-stu-id="f68bb-113">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="f68bb-114">Os usuários não poderão executar esses componentes da origem desde que o patch permaneça no computador.</span><span class="sxs-lookup"><span data-stu-id="f68bb-114">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="f68bb-115">O instalador adiciona todas as transformações usadas para atualizar o arquivo. msi ou adiciona informações específicas do patch ao perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="f68bb-115">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="f68bb-116">O instalador armazena em cache o arquivo. msi no computador do usuário para que ele possa executar a instalação sob demanda, reinstalar e reparar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f68bb-116">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="f68bb-117">Depois que um patch é aplicado a uma instalação autônoma, o instalador faz referência a duas ou mais listas de origem a arquivos externos: uma para a fonte original e outra para cada patch que foi aplicado.</span><span class="sxs-lookup"><span data-stu-id="f68bb-117">After a patch is applied to a stand alone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 




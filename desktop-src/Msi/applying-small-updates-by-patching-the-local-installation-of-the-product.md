---
description: Uma pequena atualização pode ser aplicada a um aplicativo por meio da aplicação de patch na instalação local do aplicativo.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921514"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="b306b-103">Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto</span><span class="sxs-lookup"><span data-stu-id="b306b-103">Applying Small Updates by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="b306b-104">Uma pequena atualização pode ser aplicada a um aplicativo por meio da aplicação de patch na instalação local do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b306b-104">A small update can be applied to an application by patching the local installation of the application.</span></span>

<span data-ttu-id="b306b-105">**Para aplicar um patch de atualização pequeno a uma instalação local do produto**</span><span class="sxs-lookup"><span data-stu-id="b306b-105">**To apply a small update patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="b306b-106">Inicie a instalação do patch na linha de comando ou usando um executável.</span><span class="sxs-lookup"><span data-stu-id="b306b-106">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="b306b-107">Para iniciar a partir da linha de comando, use \**msiexec/p patch. msp \[ reinstalar =\*\*\*_\] REINSTALLMODE_* da _lista de recursos_ = omus.</span><span class="sxs-lookup"><span data-stu-id="b306b-107">To launch from the command line, use **msiexec /p patch.msp REINSTALL=\[**_Feature list_*_\] REINSTALLMODE=omus_*.</span></span> <span data-ttu-id="b306b-108">Para iniciar a partir de um executável, chame [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou o [**método ApplyPatch**](installer-applypatch.md) e forneça os mesmos argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b306b-108">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="b306b-109">Ao aplicar patch na instalação de um cliente, o instalador ignora a origem da instalação e prossegue para corrigir os arquivos que já estão instalados no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="b306b-109">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="b306b-110">O instalador altera todos os componentes com patches marcados como executar da origem para execução local.</span><span class="sxs-lookup"><span data-stu-id="b306b-110">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="b306b-111">Os usuários não poderão executar esses componentes da origem desde que o patch permaneça no computador.</span><span class="sxs-lookup"><span data-stu-id="b306b-111">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="b306b-112">O instalador adiciona todas as transformações usadas para atualizar o arquivo. msi ou adiciona informações específicas do patch ao perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="b306b-112">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="b306b-113">O instalador armazena em cache o arquivo. msi no computador do usuário para que ele possa executar a instalação sob demanda, reinstalar e reparar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b306b-113">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="b306b-114">Depois que um patch é aplicado a uma instalação autônoma, o instalador faz referência a duas ou mais listas de origem a arquivos externos: uma para a fonte original e outra para cada patch que foi aplicado.</span><span class="sxs-lookup"><span data-stu-id="b306b-114">After a patch is applied to a standalone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 




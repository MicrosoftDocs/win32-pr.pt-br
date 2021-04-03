---
description: Para remover um aplicativo que foi instalado no estado anunciado, basta desinstalá-lo usando MsiInstallProduct ou MsiConfigureProduct. Você também pode remover um aplicativo anunciado da linha de comando. Consulte Opções de linha de comando.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Removendo um aplicativo anunciado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828868"
---
# <a name="removing-an-advertised-application"></a><span data-ttu-id="aa848-105">Removendo um aplicativo anunciado</span><span class="sxs-lookup"><span data-stu-id="aa848-105">Removing an Advertised Application</span></span>

<span data-ttu-id="aa848-106">Para remover um aplicativo que foi instalado no estado anunciado, basta desinstalá-lo usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span><span class="sxs-lookup"><span data-stu-id="aa848-106">To remove an application that has been installed in the advertised state, simply uninstall it using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span></span> <span data-ttu-id="aa848-107">Você também pode remover um aplicativo anunciado da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="aa848-107">You can also remove an advertised application from the command line.</span></span> <span data-ttu-id="aa848-108">Consulte [Opções de linha de comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="aa848-108">See [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="aa848-109">Observe que talvez você não consiga remover um aplicativo anunciado se tiver criado o pacote de forma que a execução de uma instalação seja condicional na instrução **não instalada**.</span><span class="sxs-lookup"><span data-stu-id="aa848-109">Note that you may be unable to remove an advertised application if you have authored the package in such a way that running an installation is conditional upon the statement **NOT Installed**.</span></span> <span data-ttu-id="aa848-110">Um aplicativo anunciado não está instalado no computador do usuário e o instalador não define a propriedade [**instalada**](installed.md) .</span><span class="sxs-lookup"><span data-stu-id="aa848-110">An advertised application is not installed on the user's computer and the installer does not set the [**Installed**](installed.md) Property.</span></span> <span data-ttu-id="aa848-111">O pacote deve ser criado para que os aplicativos anunciados possam ser desinstalados.</span><span class="sxs-lookup"><span data-stu-id="aa848-111">The package must be authored so that advertised applications can be uninstalled.</span></span>

 

 




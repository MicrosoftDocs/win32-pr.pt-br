---
description: Você pode instalar produtos inteiros com o Windows Installer functions. As etapas a seguir descrevem como instalar um produto.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Instalando um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755082"
---
# <a name="installing-an-application"></a><span data-ttu-id="01d0c-104">Instalando um aplicativo</span><span class="sxs-lookup"><span data-stu-id="01d0c-104">Installing an Application</span></span>

<span data-ttu-id="01d0c-105">Você pode instalar produtos inteiros com o Windows Installer functions.</span><span class="sxs-lookup"><span data-stu-id="01d0c-105">You can install entire products with Windows Installer functions.</span></span> <span data-ttu-id="01d0c-106">As etapas a seguir descrevem como instalar um produto.</span><span class="sxs-lookup"><span data-stu-id="01d0c-106">The following steps describe how to install a product.</span></span>

<span data-ttu-id="01d0c-107">**Para instalar um produto**</span><span class="sxs-lookup"><span data-stu-id="01d0c-107">**To install a product**</span></span>

1.  <span data-ttu-id="01d0c-108">Execute um produto por meio de sua sequência de instalação ou desinstalação chamando a função [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) .</span><span class="sxs-lookup"><span data-stu-id="01d0c-108">Run a product through its installation or uninstallation sequence by calling the [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) function.</span></span>
2.  <span data-ttu-id="01d0c-109">Especifique o nível de instalação chamando a função [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .</span><span class="sxs-lookup"><span data-stu-id="01d0c-109">Specify the installation level by calling the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function.</span></span>

    <span data-ttu-id="01d0c-110">Você pode usar os parâmetros da função [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) para definir o estado da instalação.</span><span class="sxs-lookup"><span data-stu-id="01d0c-110">You can use the parameters of the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function to set the installation state.</span></span> <span data-ttu-id="01d0c-111">Por exemplo, você pode definir o estado para instalar localmente ou instalar a partir da origem.</span><span class="sxs-lookup"><span data-stu-id="01d0c-111">For example, you can set the state to install locally or to install from the source.</span></span> <span data-ttu-id="01d0c-112">Você pode definir o intervalo de recursos do produto a ser incluído definindo o nível.</span><span class="sxs-lookup"><span data-stu-id="01d0c-112">You can set the range of product features to be included by setting the level.</span></span>

<span data-ttu-id="01d0c-113">Para obter mais informações sobre a instalação de um aplicativo, consulte [mecanismo](installation-mechanism.md)de [resiliência](resiliency.md) e instalação.</span><span class="sxs-lookup"><span data-stu-id="01d0c-113">For more information about installing an application, see [Resiliency](resiliency.md) and [Installation Mechanism](installation-mechanism.md).</span></span>

 

 




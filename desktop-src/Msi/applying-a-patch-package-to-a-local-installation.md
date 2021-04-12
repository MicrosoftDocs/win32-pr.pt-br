---
description: Você pode aplicar a atualização pequena a uma instalação local do MNP2000 com o patch de exemplo MNPpatch. msp criado na geração de um pacote de patch.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Aplicando um pacote de patch a uma instalação local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169209"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a><span data-ttu-id="dfa28-103">Aplicando um pacote de patch a uma instalação local</span><span class="sxs-lookup"><span data-stu-id="dfa28-103">Applying a Patch Package to a Local Installation</span></span>

<span data-ttu-id="dfa28-104">Você pode aplicar a atualização pequena a uma instalação local do MNP2000 com o patch de exemplo MNPpatch. msp criado na [geração de um pacote de patch](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="dfa28-104">You may apply the small update to a local installation of MNP2000 with the sample patch MNPpatch.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="dfa28-105">O procedimento geral é abordado na seção [aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="dfa28-105">The general procedure is discussed in the section [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span></span>

<span data-ttu-id="dfa28-106">Instale o produto MNP2000 original localmente no seu computador.</span><span class="sxs-lookup"><span data-stu-id="dfa28-106">Install the original MNP2000 product locally on your computer.</span></span> <span data-ttu-id="dfa28-107">Verifique se isso tem o erro Concert.txt que a pequena atualização deve ser corrigida.</span><span class="sxs-lookup"><span data-stu-id="dfa28-107">Verify that this has the error Concert.txt that the small update is to fix.</span></span> <span data-ttu-id="dfa28-108">Em seguida, inicie a instalação inserindo a seguinte linha de comando.</span><span class="sxs-lookup"><span data-stu-id="dfa28-108">Next launch the installation by entering the following command line.</span></span>

<span data-ttu-id="dfa28-109">**msiexec/p MNP2000. msp reinstalar = todos os REINSTALLMODE = omus**</span><span class="sxs-lookup"><span data-stu-id="dfa28-109">**msiexec /p MNP2000.msp REINSTALL=ALL REINSTALLMODE=omus**</span></span>

<span data-ttu-id="dfa28-110">Examine novamente as Concert.txt pertencentes a MNP2000 para verificar se o instalador aplicou a pequena atualização para corrigir esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="dfa28-110">Reexamine the Concert.txt belonging to MNP2000 to verify that the installer has applied the small update to fix this file.</span></span>

<span data-ttu-id="dfa28-111">Para aplicar a pequena atualização a uma imagem administrativa, consulte [aplicando um pacote de patch a uma instalação administrativa](applying-a-patch-package-to-an-administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="dfa28-111">To apply the small update to an administrative image, see [Applying a Patch Package to an Administrative Installation](applying-a-patch-package-to-an-administrative-installation.md).</span></span>

[<span data-ttu-id="dfa28-112">Continuar</span><span class="sxs-lookup"><span data-stu-id="dfa28-112">Continue</span></span>](applying-a-patch-package-to-an-administrative-installation.md)

 

 




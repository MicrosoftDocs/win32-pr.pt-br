---
description: Este tópico fornece diretrizes para instalar ou reinstalar uma instalação de várias instâncias que usa transformações de instância.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Instalando várias instâncias com transformações de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010651"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a><span data-ttu-id="4f485-103">Instalando várias instâncias com transformações de instância</span><span class="sxs-lookup"><span data-stu-id="4f485-103">Installing Multiple Instances with Instance Transforms</span></span>

<span data-ttu-id="4f485-104">Este tópico fornece diretrizes para instalar ou reinstalar uma instalação de várias instâncias que usa transformações de instância.</span><span class="sxs-lookup"><span data-stu-id="4f485-104">This topic provides guidelines for installing or reinstalling a multiple instance installation that uses instance transforms.</span></span>

-   <span data-ttu-id="4f485-105">Ao instalar uma nova instância com uma transformação de instância, inclua a propriedade **MSINEWINSTANCE** e defina **MSINEWINSTANCE**= 1.</span><span class="sxs-lookup"><span data-stu-id="4f485-105">When installing a new instance with an instance transform, include the **MSINEWINSTANCE** property and set **MSINEWINSTANCE**=1.</span></span>
-   <span data-ttu-id="4f485-106">Ao instalar uma nova instância com uma transformação de instância, inclua a propriedade Transforms e defina a primeira transformação na lista de transformações para a transformação instância que altera o código do produto.</span><span class="sxs-lookup"><span data-stu-id="4f485-106">When installing a new instance with an instance transform, include the TRANSFORMS property and set the first transform in the list of transforms to the instance transform that changes the product code.</span></span> <span data-ttu-id="4f485-107">Todas as transformações de personalização devem seguir a transformação de instância no início desta lista.</span><span class="sxs-lookup"><span data-stu-id="4f485-107">Any customization transforms should follow the instance transform at the beginning of this list.</span></span>
-   <span data-ttu-id="4f485-108">A maneira mais fácil de iniciar uma instalação de manutenção e reinstalar uma instância do é fazer referência ao código do produto da instância do.</span><span class="sxs-lookup"><span data-stu-id="4f485-108">The easiest way to initiate a maintenance installation, and reinstall an instance, is to reference the product code of the instance.</span></span> <span data-ttu-id="4f485-109">Se você iniciar a instalação de manutenção usando o caminho do pacote, também deverá especificar o código do produto da instância.</span><span class="sxs-lookup"><span data-stu-id="4f485-109">If you initiate the maintenance installation by using the package path, you must also specify the product code of the instance.</span></span> <span data-ttu-id="4f485-110">Na linha de comando, use a opção/n {código do produto}.</span><span class="sxs-lookup"><span data-stu-id="4f485-110">From the command line, use the /n {Product Code} option.</span></span> <span data-ttu-id="4f485-111">No código ou script, use a propriedade **MSIINSTANCEGUID** .</span><span class="sxs-lookup"><span data-stu-id="4f485-111">From code or script, use the **MSIINSTANCEGUID** property.</span></span>

<span data-ttu-id="4f485-112">O exemplo a seguir mostra a instalação de uma nova instância de uma linha de comando na qual a transformação da instância é prefixada por dois-pontos, o que especifica que a transformação é inserida no pacote.</span><span class="sxs-lookup"><span data-stu-id="4f485-112">The following example shows installing a new instance from a command line where the instance transform is prefixed by a colon which specifies that the transform is embedded in the package.</span></span>

<span data-ttu-id="4f485-113">**msiexec/I mypackage.msi transformações =: instância. MST MSINEWINSTANCE = 1/QB**</span><span class="sxs-lookup"><span data-stu-id="4f485-113">**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**</span></span>

<span data-ttu-id="4f485-114">O exemplo a seguir mostra a instalação de uma nova instância usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span><span class="sxs-lookup"><span data-stu-id="4f485-114">The following example shows installing a new instance using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

<span data-ttu-id="4f485-115">O exemplo a seguir mostra a instalação da nova instância do script.</span><span class="sxs-lookup"><span data-stu-id="4f485-115">The following example shows installing the new instance from script.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

<span data-ttu-id="4f485-116">O exemplo a seguir reinstala uma instância sem armazenar em cache novamente o pacote.</span><span class="sxs-lookup"><span data-stu-id="4f485-116">The following example reinstalls an instance without re-caching the package.</span></span> <span data-ttu-id="4f485-117">A instância é referenciada por seu código de produto {00000001-0002-0000-0000-624474736554} .</span><span class="sxs-lookup"><span data-stu-id="4f485-117">The instance is referred to by its product code {00000001-0002-0000-0000-624474736554}.</span></span>

<span data-ttu-id="4f485-118">**msiexec/I {00000001-0002-0000-0000-624474736554} reinstalar = todas as REinstalaçãomode = omus/QB**</span><span class="sxs-lookup"><span data-stu-id="4f485-118">**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**</span></span>

<span data-ttu-id="4f485-119">O exemplo a seguir reinstala uma instância e armazena novamente em cache o pacote da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4f485-119">The following example reinstalls an instance and re-caches the package from the command line.</span></span> <span data-ttu-id="4f485-120">A instância é referenciada pelo caminho do pacote.</span><span class="sxs-lookup"><span data-stu-id="4f485-120">The instance is referred to by the package path.</span></span> <span data-ttu-id="4f485-121">Você só precisa incluir a opção/n {código do produto} se o produto for instalado originalmente com uma transformação de instância.</span><span class="sxs-lookup"><span data-stu-id="4f485-121">You are only required to include the /n {Product Code} option if the product is originally installed with an instance transform.</span></span>

<span data-ttu-id="4f485-122">**msiexec/I c: \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} reinstalar = todos os REINSTALLMODE = vomus/qb**</span><span class="sxs-lookup"><span data-stu-id="4f485-122">**msiexec /I c:\\newpath\\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**</span></span>

<span data-ttu-id="4f485-123">O exemplo a seguir reinstala uma instância e armazena o pacote em cache usando **MsiInstallProduct**.</span><span class="sxs-lookup"><span data-stu-id="4f485-123">The following example reinstalls an instance and caches the package using **MsiInstallProduct**.</span></span> <span data-ttu-id="4f485-124">A instância é referenciada pelo caminho do pacote.</span><span class="sxs-lookup"><span data-stu-id="4f485-124">The instance is referred to by the package path.</span></span> <span data-ttu-id="4f485-125">Use a propriedade **MSIINSTANCEGUID** para fornecer o código do produto da instância.</span><span class="sxs-lookup"><span data-stu-id="4f485-125">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

<span data-ttu-id="4f485-126">O exemplo a seguir reinstala uma instância e armazena o pacote em cache usando o script.</span><span class="sxs-lookup"><span data-stu-id="4f485-126">The following example reinstalls an instance and caches the package using script.</span></span> <span data-ttu-id="4f485-127">Use a propriedade **MSIINSTANCEGUID** para fornecer o código do produto da instância.</span><span class="sxs-lookup"><span data-stu-id="4f485-127">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

<span data-ttu-id="4f485-128">O exemplo a seguir mostra como anunciar uma instância usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4f485-128">The following example shows how to advertise an instance using the command line.</span></span>

<span data-ttu-id="4f485-129">**msiexec/JM mypackage.msi/t: instance. MST/c/QB**</span><span class="sxs-lookup"><span data-stu-id="4f485-129">**msiexec /jm mypackage.msi /t :instance.mst /c /qb**</span></span>

<span data-ttu-id="4f485-130">O exemplo a seguir mostra como instalar o para anunciar uma instância usando o **MsiAdvertiseProductEx**.</span><span class="sxs-lookup"><span data-stu-id="4f485-130">The following example shows how to install to advertise an instance using **MsiAdvertiseProductEx**.</span></span>

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

<span data-ttu-id="4f485-131">O exemplo a seguir mostra como aplicar um patch a uma instância de uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4f485-131">The following example shows how to apply a patch to an instance from a command line.</span></span> <span data-ttu-id="4f485-132">Você só precisa incluir a opção/n {código do produto} se o produto tiver sido originalmente instalado com uma transformação de instância.</span><span class="sxs-lookup"><span data-stu-id="4f485-132">You are only required to include the /n {Product Code} option if the product was originally installed with an instance transform.</span></span>

<span data-ttu-id="4f485-133">**msiexec/p mypatch. msp/n {00000001-0002-0000-0000-624474736554} /QB**</span><span class="sxs-lookup"><span data-stu-id="4f485-133">**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**</span></span>

<span data-ttu-id="4f485-134">O exemplo a seguir mostra como aplicar um patch a uma instalação de instância usando o [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span><span class="sxs-lookup"><span data-stu-id="4f485-134">The following example shows how to apply a patch to an instance installation using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span></span>

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

<span data-ttu-id="4f485-135">Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md) e [criando várias instâncias com transformações de instância](authoring-multiple-instances-with-instance-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="4f485-135">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md) and [Authoring Multiple Instances with Instance Transforms](authoring-multiple-instances-with-instance-transforms.md).</span></span>

 

 




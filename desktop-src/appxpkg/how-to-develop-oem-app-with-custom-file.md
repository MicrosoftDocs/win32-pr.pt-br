---
title: Como desenvolver um aplicativo OEM que usa um arquivo personalizado
description: Saiba como desenvolver um aplicativo que usa um arquivo personalizado para passar informações do OEM para o aplicativo.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105763318"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a><span data-ttu-id="6ed17-103">Como desenvolver um aplicativo OEM que usa um arquivo personalizado</span><span class="sxs-lookup"><span data-stu-id="6ed17-103">How to develop an OEM app that uses a custom file</span></span>

<span data-ttu-id="6ed17-104">Para obter mais informações sobre como criar e usar arquivos de dados personalizados, consulte [Opções de manutenção do pacote do aplicativo do DISM (. Appx ou. appxbundle) Command-Line](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span><span class="sxs-lookup"><span data-stu-id="6ed17-104">For more information on creating and using custom data files, see [DISM App Package (.appx or .appxbundle) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span></span>

<span data-ttu-id="6ed17-105">Saiba como desenvolver um aplicativo que usa um arquivo personalizado para passar informações do OEM para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ed17-105">Learn how to develop an app that uses a custom file to pass info from the OEM to the app.</span></span>

<span data-ttu-id="6ed17-106">Para aplicativos que você cria para a implantação do OEM, você pode usar um arquivo personalizado para passar informações do OEM para os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6ed17-106">For apps that you create for OEM deployment, you can use a custom file to pass info from the OEM to the apps.</span></span> <span data-ttu-id="6ed17-107">Para passar informações de OEM para um aplicativo, você cria um arquivo. Data personalizado na pasta microsoft.system. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="6ed17-107">To pass OEM info to an app, you create a Custom.data file in the microsoft.system.package.metadata folder.</span></span> <span data-ttu-id="6ed17-108">Esse nome de arquivo é especial para o sistema operacional e é executado automaticamente durante as atualizações do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6ed17-108">This file name is special to the operating system and is automatically carried forward during operating system updates.</span></span> <span data-ttu-id="6ed17-109">Os OEMs podem usar esse arquivo para passar identificadores personalizados, para que os aplicativos saibam quando os OEMs o implantaram.</span><span class="sxs-lookup"><span data-stu-id="6ed17-109">OEMs can use this file to pass in custom identifiers, so that apps know when OEMs have deployed them.</span></span> <span data-ttu-id="6ed17-110">Você pode ter apenas um arquivo. Data personalizado por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ed17-110">You can have only one Custom.data file per app.</span></span> <span data-ttu-id="6ed17-111">Os aplicativos devem ser capazes de procurar e ler esse arquivo corretamente.</span><span class="sxs-lookup"><span data-stu-id="6ed17-111">Apps must be able to look for and read this file correctly.</span></span> <span data-ttu-id="6ed17-112">Os desenvolvedores tratam o arquivo como dados não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="6ed17-112">Developers treat the file as untrusted data.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6ed17-113">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="6ed17-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6ed17-114">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="6ed17-114">Technologies</span></span>

-   [<span data-ttu-id="6ed17-115">Início rápido: consultar informações de manifesto do pacote de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ed17-115">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a><span data-ttu-id="6ed17-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="6ed17-116">Prerequisites</span></span>

-   <span data-ttu-id="6ed17-117">Você precisa da ferramenta [DISM (gerenciamento e manutenção de imagens de implantação)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) para adicionar o pacote do aplicativo com o arquivo de dados personalizado.</span><span class="sxs-lookup"><span data-stu-id="6ed17-117">You need the [Deployment Image Servicing and Management (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool to add the app package with the custom data file.</span></span>

## <a name="instructions"></a><span data-ttu-id="6ed17-118">Instruções</span><span class="sxs-lookup"><span data-stu-id="6ed17-118">Instructions</span></span>

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a><span data-ttu-id="6ed17-119">Etapa 1: criar um arquivo personalizado e adicioná-lo à pasta de metadados do pacote</span><span class="sxs-lookup"><span data-stu-id="6ed17-119">Step 1: Create custom file and add it to the package metadata folder</span></span>

<span data-ttu-id="6ed17-120">Você pode criar seu aplicativo para usar qualquer formato escolhido para os dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="6ed17-120">You can design your app to use any format you choose for the custom data.</span></span> <span data-ttu-id="6ed17-121">Por exemplo, você pode usar XML, um arquivo de texto ou outro tipo de arquivo para organizar seus dados.</span><span class="sxs-lookup"><span data-stu-id="6ed17-121">For example, you can use XML, a text file, or another file type to organize your data.</span></span> <span data-ttu-id="6ed17-122">Recomendamos que você considere como você pode testar e validar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ed17-122">We recommend that you consider how you can test and validate the file.</span></span> <span data-ttu-id="6ed17-123">Por exemplo, você pode criar um esquema XML para validar um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="6ed17-123">For example, you can create an XML schema to validate an XML file.</span></span>

<span data-ttu-id="6ed17-124">Você pode especificar qualquer tipo de arquivo com qualquer nome de arquivo para os dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="6ed17-124">You can specify any type of file with any file name for the custom data.</span></span> <span data-ttu-id="6ed17-125">Quando você adiciona o pacote do aplicativo com o arquivo de dados personalizado usando a ferramenta [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , o DISM renomeia o arquivo personalizado para Custom. Data e salva o arquivo na pasta microsoft.system. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="6ed17-125">When you add the app package with the custom data file by using the [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool, DISM renames the custom file to Custom.data and saves the file to the microsoft.system.package.metadata folder.</span></span>

> [!Note]  
> <span data-ttu-id="6ed17-126">O arquivo de dados personalizado não pode ser modificado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ed17-126">The custom data file can't be modified by the app.</span></span> <span data-ttu-id="6ed17-127">É um recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6ed17-127">It's a read-only resource.</span></span>

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a><span data-ttu-id="6ed17-128">Etapa 2: acessar o arquivo de dados personalizado para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ed17-128">Step 2: Access the custom data file for an app</span></span>

<span data-ttu-id="6ed17-129">Você pode acessar o arquivo. Data personalizado para um aplicativo do seu código usando as APIs do Windows para obter informações para o pacote atual.</span><span class="sxs-lookup"><span data-stu-id="6ed17-129">You can access the Custom.data file for an app from your code by using Windows APIs to get information for the current package.</span></span> <span data-ttu-id="6ed17-130">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6ed17-130">For example:</span></span>

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

<span data-ttu-id="6ed17-131">Para obter mais informações sobre como desenvolver com a propriedade [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) , consulte [início rápido: consultar informações de manifesto do pacote de aplicativo](how-to-query-package-identity-information.md).</span><span class="sxs-lookup"><span data-stu-id="6ed17-131">For more info about developing with the [**Package.Current**](/uwp/api/windows.applicationmodel.package.current) property, see [Quickstart: Query app package manifest info](how-to-query-package-identity-information.md).</span></span>

<span data-ttu-id="6ed17-132">Para obter mais informações sobre como acessar o arquivo Custom. Data por meio de [**IStorageFolder. GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) e usando objetos [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) , consulte [acessando dados e arquivos](/previous-versions/windows/apps/hh464959(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="6ed17-132">For more info about accessing the custom.data file via [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) and by using [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) objects, see [Accessing data and files](/previous-versions/windows/apps/hh464959(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ed17-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ed17-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed17-134">Início rápido: consultar informações de manifesto do pacote de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ed17-134">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)
</dt> </dl>

 

 
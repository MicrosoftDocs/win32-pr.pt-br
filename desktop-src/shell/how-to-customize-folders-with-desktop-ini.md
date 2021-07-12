---
description: Personalização da aparência e do comportamento de uma pasta individual com Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Como personalizar pastas com Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a671b169c4b025683cdd220ee3a920b4d592488
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581744"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="862e6-103">Como personalizar pastas com Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="862e6-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="862e6-104">As pastas do sistema de arquivos normalmente são exibidas com um ícone padrão e um conjunto de propriedades, que especificam, por exemplo, se a pasta é compartilhada.</span><span class="sxs-lookup"><span data-stu-id="862e6-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="862e6-105">Você pode personalizar a aparência e o comportamento de uma pasta individual criando um arquivo Desktop.ini para essa pasta.</span><span class="sxs-lookup"><span data-stu-id="862e6-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="862e6-106">Instruções</span><span class="sxs-lookup"><span data-stu-id="862e6-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="862e6-107">Usando Desktop.ini arquivos</span><span class="sxs-lookup"><span data-stu-id="862e6-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="862e6-108">As pastas normalmente são exibidas com o ícone de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="862e6-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="862e6-109">Um uso comum do arquivo Desktop.ini é atribuir um ícone personalizado ou uma imagem em miniatura a uma pasta.</span><span class="sxs-lookup"><span data-stu-id="862e6-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="862e6-110">Você também pode usar Desktop.ini para criar uma *infotip* que exibe informações sobre a pasta e controla alguns aspectos do comportamento da pasta, como especificar nomes localizados para a pasta ou itens na pasta.</span><span class="sxs-lookup"><span data-stu-id="862e6-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="862e6-111">**Use o procedimento a seguir para personalizar o estilo de uma pasta com Desktop.ini:**</span><span class="sxs-lookup"><span data-stu-id="862e6-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="862e6-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) para tornar a pasta uma pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="862e6-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="862e6-113">Isso define o bit somente leitura na pasta para indicar que o comportamento especial reservado para Desktop.ini deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="862e6-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="862e6-114">Você também pode tornar uma pasta do sistema uma pasta do sistema na linha de comando usando **atrib +s** *FolderName.*</span><span class="sxs-lookup"><span data-stu-id="862e6-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="862e6-115">Crie um Desktop.ini para a pasta.</span><span class="sxs-lookup"><span data-stu-id="862e6-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="862e6-116">Você deve marcá-lo *como oculto* *e sistema* para garantir que ele seja oculto dos usuários normais.</span><span class="sxs-lookup"><span data-stu-id="862e6-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="862e6-117">Certifique-se de Desktop.ini arquivo que você cria está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="862e6-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="862e6-118">Isso é necessário para armazenar as cadeias de caracteres localizadas que podem ser exibidas aos usuários.</span><span class="sxs-lookup"><span data-stu-id="862e6-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="862e6-119">Criando um arquivo Desktop.ini dados</span><span class="sxs-lookup"><span data-stu-id="862e6-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="862e6-120">O Desktop.ini arquivo é um arquivo de texto que permite que você especifique como uma pasta do sistema de arquivos é exibida.</span><span class="sxs-lookup"><span data-stu-id="862e6-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="862e6-121">O \[ . A seção ShellClassInfo permite personalizar a exibição da pasta \] atribuindo valores a várias entradas:</span><span class="sxs-lookup"><span data-stu-id="862e6-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

| <span data-ttu-id="862e6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="862e6-122">Value</span></span>             | <span data-ttu-id="862e6-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="862e6-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="862e6-124">**ConfirmFileOp**</span><span class="sxs-lookup"><span data-stu-id="862e6-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="862e6-125">De definir essa entrada como 0 para evitar um aviso "Você está excluindo uma pasta do sistema" ao excluir ou mover a pasta.</span><span class="sxs-lookup"><span data-stu-id="862e6-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="862e6-126">**NoSharing**</span><span class="sxs-lookup"><span data-stu-id="862e6-126">**NoSharing**</span></span>     | <span data-ttu-id="862e6-127">Não há suporte no Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="862e6-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="862e6-128">De definir essa entrada como 1 para impedir que a pasta seja compartilhada.</span><span class="sxs-lookup"><span data-stu-id="862e6-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="862e6-129">**Iconfile**</span><span class="sxs-lookup"><span data-stu-id="862e6-129">**IconFile**</span></span>      | <span data-ttu-id="862e6-130">Se você quiser especificar um ícone personalizado para a pasta, de definir essa entrada como o nome de arquivo do ícone.</span><span class="sxs-lookup"><span data-stu-id="862e6-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="862e6-131">A extensão de nome de arquivo .ico é preferencial, mas também é possível especificar arquivos .bmp ou arquivos .exe e .dll que contêm ícones.</span><span class="sxs-lookup"><span data-stu-id="862e6-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="862e6-132">Se você usar um caminho relativo, o ícone estará disponível para as pessoas que visualizam a pasta pela rede.</span><span class="sxs-lookup"><span data-stu-id="862e6-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="862e6-133">Você também deve definir a **entrada IconIndex.**</span><span class="sxs-lookup"><span data-stu-id="862e6-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="862e6-134">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="862e6-134">**IconIndex**</span></span>     | <span data-ttu-id="862e6-135">De definir essa entrada para especificar o índice de um ícone personalizado.</span><span class="sxs-lookup"><span data-stu-id="862e6-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="862e6-136">Se o arquivo atribuído a **IconFile** contiver apenas um único ícone, de definir **IconIndex** como 0.</span><span class="sxs-lookup"><span data-stu-id="862e6-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="862e6-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="862e6-137">**InfoTip**</span></span>       | <span data-ttu-id="862e6-138">De definir essa entrada como uma cadeia de caracteres de texto informacional.</span><span class="sxs-lookup"><span data-stu-id="862e6-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="862e6-139">Ele é exibido como uma infotip quando o cursor fica sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="862e6-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="862e6-140">Se o usuário clicar na pasta, o texto de informações será exibido no bloco de informações da pasta, abaixo das informações padrão.</span><span class="sxs-lookup"><span data-stu-id="862e6-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="862e6-141">As ilustrações a seguir são da pasta Música com um arquivo Desktop.ini personalizado.</span><span class="sxs-lookup"><span data-stu-id="862e6-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="862e6-142">A pasta agora:</span><span class="sxs-lookup"><span data-stu-id="862e6-142">The folder now:</span></span>

-   <span data-ttu-id="862e6-143">Tem um ícone personalizado.</span><span class="sxs-lookup"><span data-stu-id="862e6-143">Has a custom icon.</span></span>
-   <span data-ttu-id="862e6-144">Não exibirá um aviso "Você está excluindo uma pasta do sistema" se a pasta for movida ou excluída.</span><span class="sxs-lookup"><span data-stu-id="862e6-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="862e6-145">Não pode ser compartilhada.</span><span class="sxs-lookup"><span data-stu-id="862e6-145">Cannot be shared.</span></span>
-   <span data-ttu-id="862e6-146">Exibe texto informacional quando o cursor fica sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="862e6-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="862e6-147">As opções de pasta nas ilustrações a seguir são definidas para mostrar arquivos ocultos para que Desktop.ini seja visível.</span><span class="sxs-lookup"><span data-stu-id="862e6-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="862e6-148">A pasta tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="862e6-148">The folder looks like this:</span></span>

![captura de tela da pasta com o ícone personalizado](images/webview4.jpg)

<span data-ttu-id="862e6-150">Quando o cursor passar o mouse sobre a pasta, a infotip será exibida.</span><span class="sxs-lookup"><span data-stu-id="862e6-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![captura de tela da pasta com uma infotip](images/webview6.jpg)

<span data-ttu-id="862e6-152">O ícone personalizado substitui o ícone de pasta em todos os lugares em que o nome da pasta é exibido.</span><span class="sxs-lookup"><span data-stu-id="862e6-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![captura de tela do ícone personalizado substituindo o ícone de pasta](images/webview5.jpg)

<span data-ttu-id="862e6-154">O arquivo desktop.ini a seguir foi usado para personalizar a pasta Música, conforme visto nas ilustrações anteriores.</span><span class="sxs-lookup"><span data-stu-id="862e6-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 




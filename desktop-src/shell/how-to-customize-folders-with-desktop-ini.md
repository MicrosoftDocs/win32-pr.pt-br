---
description: Personalizando a aparência e o comportamento de uma pasta individual com Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Como Personalizar pastas com Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571163"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="9c9d0-103">Como Personalizar pastas com Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="9c9d0-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="9c9d0-104">As pastas do sistema de arquivos são normalmente exibidas com um ícone padrão e um conjunto de propriedades, que especificam, por exemplo, se a pasta é compartilhada.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="9c9d0-105">Você pode personalizar a aparência e o comportamento de uma pasta individual criando um arquivo de Desktop.ini para essa pasta.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="9c9d0-106">Instruções</span><span class="sxs-lookup"><span data-stu-id="9c9d0-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="9c9d0-107">Usando arquivos Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="9c9d0-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="9c9d0-108">Normalmente, as pastas são exibidas com o ícone de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="9c9d0-109">Um uso comum do arquivo de Desktop.ini é atribuir um ícone personalizado ou uma imagem em miniatura a uma pasta.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="9c9d0-110">Você também pode usar Desktop.ini para criar um *InfoTip* que exibe informações sobre a pasta e controla alguns aspectos do comportamento da pasta, como especificar nomes localizados para a pasta ou os itens na pasta.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="9c9d0-111">**Use o procedimento a seguir para personalizar o estilo de uma pasta com Desktop.ini:**</span><span class="sxs-lookup"><span data-stu-id="9c9d0-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="9c9d0-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) para tornar a pasta uma pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="9c9d0-113">Isso define o bit somente leitura na pasta para indicar que o comportamento especial reservado para Desktop.ini deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="9c9d0-114">Você também pode tornar uma pasta de uma pasta do sistema a partir da linha de comando usando **attrib + s** *nome_da_pasta*.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="9c9d0-115">Crie um arquivo de Desktop.ini para a pasta.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="9c9d0-116">Você deve marcá-lo como *oculto* e *sistema* para garantir que ele fique oculto dos usuários normais.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="9c9d0-117">Verifique se o arquivo de Desktop.ini que você cria está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="9c9d0-118">Isso é necessário para armazenar as cadeias de caracteres localizadas que podem ser exibidas aos usuários.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="9c9d0-119">Criando um arquivo de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="9c9d0-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="9c9d0-120">O arquivo de Desktop.ini é um arquivo de texto que permite especificar como uma pasta do sistema de arquivos é exibida.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="9c9d0-121">O \[ . ShellClassInfo \] seção, permite que você personalize a exibição da pasta atribuindo valores a várias entradas:</span><span class="sxs-lookup"><span data-stu-id="9c9d0-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9d0-122">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="9c9d0-122">**Entry**</span></span>         | <span data-ttu-id="9c9d0-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9c9d0-123">**Value**</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="9c9d0-124">**ConfirmFileOp**</span><span class="sxs-lookup"><span data-stu-id="9c9d0-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="9c9d0-125">Defina essa entrada como 0 para evitar um aviso "você está excluindo uma pasta do sistema" ao excluir ou mover a pasta.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9c9d0-126">**Nosharing**</span><span class="sxs-lookup"><span data-stu-id="9c9d0-126">**NoSharing**</span></span>     | <span data-ttu-id="9c9d0-127">Sem suporte no Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="9c9d0-128">Defina essa entrada como 1 para impedir que a pasta seja compartilhada.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9c9d0-129">**Ícone**</span><span class="sxs-lookup"><span data-stu-id="9c9d0-129">**IconFile**</span></span>      | <span data-ttu-id="9c9d0-130">Se você quiser especificar um ícone personalizado para a pasta, defina essa entrada como o nome do arquivo do ícone.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="9c9d0-131">A extensão de nome de arquivo. ico é preferida, mas também é possível especificar arquivos. bmp ou. exe e. dll que contêm ícones.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="9c9d0-132">Se você usar um caminho relativo, o ícone estará disponível para as pessoas que exibirem a pasta pela rede.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="9c9d0-133">Você também deve definir a entrada **IconIndex** .</span><span class="sxs-lookup"><span data-stu-id="9c9d0-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="9c9d0-134">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="9c9d0-134">**IconIndex**</span></span>     | <span data-ttu-id="9c9d0-135">Defina essa entrada para especificar o índice para um ícone personalizado.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="9c9d0-136">Se o arquivo atribuído a **IconFile** contiver apenas um único ícone, defina **IconIndex** como 0.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9c9d0-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="9c9d0-137">**InfoTip**</span></span>       | <span data-ttu-id="9c9d0-138">Defina essa entrada como uma cadeia de caracteres de texto informativa.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="9c9d0-139">Ele é exibido como um InfoTip quando o cursor passa sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="9c9d0-140">Se o usuário clicar na pasta, o texto das informações será exibido no bloco de informações da pasta, abaixo das informações padrão.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="9c9d0-141">As ilustrações a seguir são da pasta música com um arquivo de Desktop.ini personalizado.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="9c9d0-142">A pasta agora:</span><span class="sxs-lookup"><span data-stu-id="9c9d0-142">The folder now:</span></span>

-   <span data-ttu-id="9c9d0-143">Tem um ícone personalizado.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-143">Has a custom icon.</span></span>
-   <span data-ttu-id="9c9d0-144">Não exibirá um aviso "você está excluindo uma pasta do sistema" se a pasta for movida ou excluída.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="9c9d0-145">Não pode ser compartilhada.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-145">Cannot be shared.</span></span>
-   <span data-ttu-id="9c9d0-146">Exibe o texto informativo quando o cursor passa sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="9c9d0-147">As opções de pasta nas ilustrações a seguir são definidas para mostrar arquivos ocultos para que Desktop.ini seja visível.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="9c9d0-148">A pasta tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="9c9d0-148">The folder looks like this:</span></span>

![captura de tela da pasta com o ícone personalizado](images/webview4.jpg)

<span data-ttu-id="9c9d0-150">Quando o cursor passa sobre a pasta, o InfoTip é exibido.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![captura de tela da pasta com um InfoTip](images/webview6.jpg)

<span data-ttu-id="9c9d0-152">O ícone personalizado substitui o ícone de pasta em todos os lugares em que o nome da pasta é exibido.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![captura de tela do ícone personalizado substituindo ícone de pasta](images/webview5.jpg)

<span data-ttu-id="9c9d0-154">O arquivo de desktop.ini a seguir foi usado para personalizar a pasta música, como visto nas ilustrações anteriores.</span><span class="sxs-lookup"><span data-stu-id="9c9d0-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 




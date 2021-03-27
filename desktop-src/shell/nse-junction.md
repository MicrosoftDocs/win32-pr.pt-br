---
description: A raiz de uma extensão de namespace é normalmente exibida pelo Windows Explorer como uma pasta nos modos de exibição de árvore e de pasta.
title: Especificando o local de uma extensão de namespace
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828910"
---
# <a name="specifying-a-namespace-extensions-location"></a><span data-ttu-id="0ed03-103">Especificando o local de uma extensão de namespace</span><span class="sxs-lookup"><span data-stu-id="0ed03-103">Specifying a Namespace Extension's Location</span></span>

<span data-ttu-id="0ed03-104">A raiz de uma extensão de namespace é normalmente exibida pelo Windows Explorer como uma pasta nos modos de exibição de árvore e de pasta.</span><span class="sxs-lookup"><span data-stu-id="0ed03-104">The root of a namespace extension is normally displayed by Windows Explorer as a folder in both tree and folder views.</span></span> <span data-ttu-id="0ed03-105">Para que o Windows Explorer exiba os arquivos e as subpastas da extensão, você deve especificar onde a pasta raiz está localizada na hierarquia de namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="0ed03-105">For Windows Explorer to display your extension's files and subfolders, you must specify where the root folder is located in the Shell namespace hierarchy.</span></span> <span data-ttu-id="0ed03-106">Esse local é conhecido como ponto de *junção*.</span><span class="sxs-lookup"><span data-stu-id="0ed03-106">This location is referred to as a *junction point*.</span></span>

-   [<span data-ttu-id="0ed03-107">Usando pastas virtuais como pontos de junção</span><span class="sxs-lookup"><span data-stu-id="0ed03-107">Using Virtual Folders as Junction Points</span></span>](#using-virtual-folders-as-junction-points)
-   [<span data-ttu-id="0ed03-108">Usando pastas do sistema de arquivos como pontos de junção</span><span class="sxs-lookup"><span data-stu-id="0ed03-108">Using File System Folders as Junction Points</span></span>](#using-file-system-folders-as-junction-points)
-   [<span data-ttu-id="0ed03-109">Abrindo uma exibição de uma extensão de namespace</span><span class="sxs-lookup"><span data-stu-id="0ed03-109">Opening a View of a Namespace Extension</span></span>](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a><span data-ttu-id="0ed03-110">Usando pastas virtuais como pontos de junção</span><span class="sxs-lookup"><span data-stu-id="0ed03-110">Using Virtual Folders as Junction Points</span></span>

<span data-ttu-id="0ed03-111">A maneira mais simples de definir o ponto de junção de uma extensão é tornar a pasta raiz uma subpasta de uma pasta virtual do sistema.</span><span class="sxs-lookup"><span data-stu-id="0ed03-111">The simplest way to define an extension's junction point is to make the root folder a subfolder of a system virtual folder.</span></span> <span data-ttu-id="0ed03-112">Esse tipo de ponto de junção é chamado de *ponto de junção virtual*.</span><span class="sxs-lookup"><span data-stu-id="0ed03-112">This type of junction point is referred to as a *virtual junction point*.</span></span> <span data-ttu-id="0ed03-113">As pastas **Desktop** e **meu computador** são os locais típicos para pontos de junção virtuais, mas você também pode definir um ponto de junção virtual em um computador remoto ou nas pastas **meus locais de rede**, **Internet Explorer** e **painel de controle** .</span><span class="sxs-lookup"><span data-stu-id="0ed03-113">The **Desktop** and **My Computer** folders are the typical locations for virtual junction points, but you can also define a virtual junction point on a remote computer or under the **My Network Places**, **Internet Explorer**, and **Control Panel** folders.</span></span>

<span data-ttu-id="0ed03-114">Para definir um ponto de junção virtual, crie uma subchave da chave que representa a pasta virtual apropriada e nomeie-a com a forma de cadeia de caracteres do identificador de classe da extensão (CLSID).</span><span class="sxs-lookup"><span data-stu-id="0ed03-114">To define a virtual junction point, create a subkey of the key that represents the appropriate virtual folder and name it with the string form of your extension's class identifier (CLSID).</span></span> <span data-ttu-id="0ed03-115">O CLSID registrado seria exibido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="0ed03-115">The registered CLSID would appear as follows.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

<span data-ttu-id="0ed03-116">O *nome da pasta virtual* é uma das subchaves na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ed03-116">*Virtual Folder Name* is one of the subkeys in the following table.</span></span>



| <span data-ttu-id="0ed03-117">Localização</span><span class="sxs-lookup"><span data-stu-id="0ed03-117">Location</span></span>          | <span data-ttu-id="0ed03-118">Nome da pasta virtual</span><span class="sxs-lookup"><span data-stu-id="0ed03-118">Virtual Folder Name</span></span>                        |
|-------------------|--------------------------------------------|
| <span data-ttu-id="0ed03-119">Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="0ed03-119">Control Panel</span></span>     | <span data-ttu-id="0ed03-120">**ControlPanel**</span><span class="sxs-lookup"><span data-stu-id="0ed03-120">**ControlPanel**</span></span>                           |
| <span data-ttu-id="0ed03-121">Área de trabalho</span><span class="sxs-lookup"><span data-stu-id="0ed03-121">Desktop</span></span>           | <span data-ttu-id="0ed03-122">**Área de trabalho**</span><span class="sxs-lookup"><span data-stu-id="0ed03-122">**Desktop**</span></span>                                |
| <span data-ttu-id="0ed03-123">Rede inteira</span><span class="sxs-lookup"><span data-stu-id="0ed03-123">Entire Network</span></span>    | <span data-ttu-id="0ed03-124">**NetworkNeighborhood** \\ **EntireNetwork**</span><span class="sxs-lookup"><span data-stu-id="0ed03-124">**NetworkNeighborhood**\\**EntireNetwork**</span></span> |
| <span data-ttu-id="0ed03-125">Meu Computador</span><span class="sxs-lookup"><span data-stu-id="0ed03-125">My Computer</span></span>       | <span data-ttu-id="0ed03-126">**Meu**</span><span class="sxs-lookup"><span data-stu-id="0ed03-126">**MyComputer**</span></span>                             |
| <span data-ttu-id="0ed03-127">Meus locais de rede</span><span class="sxs-lookup"><span data-stu-id="0ed03-127">My Network Places</span></span> | <span data-ttu-id="0ed03-128">**NetworkNeighborhood**</span><span class="sxs-lookup"><span data-stu-id="0ed03-128">**NetworkNeighborhood**</span></span>                    |
| <span data-ttu-id="0ed03-129">Computador remoto</span><span class="sxs-lookup"><span data-stu-id="0ed03-129">Remote Computer</span></span>   | <span data-ttu-id="0ed03-130">**Computador_remoto**</span><span class="sxs-lookup"><span data-stu-id="0ed03-130">**RemoteComputer**</span></span>                         |
| <span data-ttu-id="0ed03-131">Arquivos de usuários</span><span class="sxs-lookup"><span data-stu-id="0ed03-131">Users Files</span></span>       | <span data-ttu-id="0ed03-132">**UsersFiles**</span><span class="sxs-lookup"><span data-stu-id="0ed03-132">**UsersFiles**</span></span>                             |



 

<span data-ttu-id="0ed03-133">Extensões remotas devem ser inicializadas com [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span><span class="sxs-lookup"><span data-stu-id="0ed03-133">Remote extensions must be initialized with [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span></span>

## <a name="using-file-system-folders-as-junction-points"></a><span data-ttu-id="0ed03-134">Usando pastas do sistema de arquivos como pontos de junção</span><span class="sxs-lookup"><span data-stu-id="0ed03-134">Using File System Folders as Junction Points</span></span>

<span data-ttu-id="0ed03-135">Há duas maneiras de definir pastas do sistema de arquivos como pontos de junção.</span><span class="sxs-lookup"><span data-stu-id="0ed03-135">There are two ways to define file system folders as junction points.</span></span> <span data-ttu-id="0ed03-136">A abordagem mais simples é criar uma pasta no local apropriado e acrescentar um ponto ao nome da pasta, seguido pelo formato da cadeia de caracteres do CLSID de sua extensão.</span><span class="sxs-lookup"><span data-stu-id="0ed03-136">The simplest approach is to create a folder in the appropriate location and append a period to the folder's name, followed by the string form of the CLSID of your extension.</span></span> <span data-ttu-id="0ed03-137">Somente o nome da pasta ficará visível no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="0ed03-137">Only the folder name will be visible in Windows Explorer.</span></span> <span data-ttu-id="0ed03-138">O exemplo a seguir cria um ponto de junção com um nome de exibição de MyFolder.</span><span class="sxs-lookup"><span data-stu-id="0ed03-138">The following example creates a junction point with a display name of MyFolder.</span></span>


```
MyFolder.{Extension CLSID}
```



<span data-ttu-id="0ed03-139">Como alternativa, você pode definir uma pasta nomeada de forma convencional como um ponto de junção:</span><span class="sxs-lookup"><span data-stu-id="0ed03-139">Alternatively, you can define a conventionally named folder as a junction point by:</span></span>

-   <span data-ttu-id="0ed03-140">Tornando a pasta somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0ed03-140">Making the folder read-only.</span></span>
-   <span data-ttu-id="0ed03-141">Tornando a pasta uma pasta do sistema chamando [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span><span class="sxs-lookup"><span data-stu-id="0ed03-141">Making the folder a system folder by calling [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span></span>
-   <span data-ttu-id="0ed03-142">Colocar um arquivo de Desktop.ini oculto na pasta que inclui o CLSID da extensão.</span><span class="sxs-lookup"><span data-stu-id="0ed03-142">Placing a hidden Desktop.ini file in the folder that includes the extension's CLSID.</span></span>

<span data-ttu-id="0ed03-143">Desktop.ini é um arquivo de texto padrão que pode ser adicionado a qualquer pasta para personalizar determinados aspectos do comportamento da pasta.</span><span class="sxs-lookup"><span data-stu-id="0ed03-143">Desktop.ini is a standard text file that can be added to any folder to customize certain aspects of the folder's behavior.</span></span> <span data-ttu-id="0ed03-144">Para obter uma discussão geral sobre como usar esse arquivo, consulte [como personalizar pastas com Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="0ed03-144">For a general discussion of how to use this file, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span> <span data-ttu-id="0ed03-145">Para definir uma pasta como um ponto de junção, o \[ . \] A seção ShellClassInfo de Desktop.ini deve conter o CLSID da extensão da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0ed03-145">To define a folder as a junction point, the \[.ShellClassInfo\] section of Desktop.ini must contain the extension's CLSID as follows:</span></span>


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a><span data-ttu-id="0ed03-146">Abrindo uma exibição de uma extensão de namespace</span><span class="sxs-lookup"><span data-stu-id="0ed03-146">Opening a View of a Namespace Extension</span></span>

<span data-ttu-id="0ed03-147">Quando um usuário navega em um ponto de junção, o Windows Explorer cria automaticamente uma exibição da pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="0ed03-147">When a user browses into a junction point, Windows Explorer automatically creates a view of the root folder.</span></span> <span data-ttu-id="0ed03-148">Você também pode criar uma exibição iniciando explicitamente Explorer.exe com o CLSID da extensão como um argumento.</span><span class="sxs-lookup"><span data-stu-id="0ed03-148">You can also create a view by explicitly launching Explorer.exe with the extension's CLSID as an argument.</span></span> <span data-ttu-id="0ed03-149">Você pode, por exemplo, usar essa abordagem para iniciar uma exibição de uma extensão de um menu de atalho ou atalho.</span><span class="sxs-lookup"><span data-stu-id="0ed03-149">You can, for instance, use this approach to launch a view of an extension from a shortcut menu or shortcut.</span></span> <span data-ttu-id="0ed03-150">Por exemplo, para iniciar uma exibição de MyExtension que inclui um modo de exibição de árvore, você pode usar a seguinte cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="0ed03-150">For example, to launch a view of MyExtension that includes a tree view, you can use the following command string.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



<span data-ttu-id="0ed03-151">Uma cadeia de caracteres de comando alternativa pode ser usada para iniciar uma exibição de um objeto dentro da extensão.</span><span class="sxs-lookup"><span data-stu-id="0ed03-151">An alternative command string can be used to launch a view of an object within the extension.</span></span> <span data-ttu-id="0ed03-152">Esse recurso seria útil, por exemplo, para uma extensão que usa uma exibição de pasta para permitir que os usuários exibam o conteúdo de um dos vários arquivos compactados.</span><span class="sxs-lookup"><span data-stu-id="0ed03-152">This feature would be useful, for instance, for an extension that uses a folder view to allow users to view the contents of one of a number of compressed files.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



<span data-ttu-id="0ed03-153">O parâmetro *objectname* é o nome do objeto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="0ed03-153">The *objectname* parameter is the name of the object that is to be viewed.</span></span> <span data-ttu-id="0ed03-154">O Windows Explorer converte o nome para seu PIDL correspondente e passa o PIDL para o método [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) do novo objeto de pasta.</span><span class="sxs-lookup"><span data-stu-id="0ed03-154">Windows Explorer converts the name to its corresponding PIDL and passes the PIDL to the new folder object's [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) method.</span></span>

> [!Note]  
> <span data-ttu-id="0ed03-155">A cadeia de caracteres CLSID deve ser precedida por um par de dois-pontos (::) ou o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="0ed03-155">The CLSID string must be preceded by a pair of colons (::) or the command will fail.</span></span> <span data-ttu-id="0ed03-156">O sinalizador de barra e (/e) usado nas duas linhas de comando de exemplo mostradas anteriormente instrui o Windows Explorer a exibir um modo de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="0ed03-156">The slash-e (/e) flag used in the two sample command lines shown previously instructs Windows Explorer to display a tree view.</span></span> <span data-ttu-id="0ed03-157">O sinalizador deve ser separado dos dois dois-pontos por uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="0ed03-157">The flag must be separated from the two colons by a comma.</span></span> <span data-ttu-id="0ed03-158">Se você não quiser um modo de exibição de árvore, omita o sinalizador/e e a vírgula.</span><span class="sxs-lookup"><span data-stu-id="0ed03-158">If you do not want a tree view, omit the /e flag and the comma.</span></span>

 

 

 




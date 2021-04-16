---
description: Este tópico descreve quais bibliotecas são e como elas podem beneficiar usuários e desenvolvedores.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Sobre bibliotecas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550124"
---
# <a name="about-libraries"></a><span data-ttu-id="0c2ad-103">Sobre bibliotecas</span><span class="sxs-lookup"><span data-stu-id="0c2ad-103">About Libraries</span></span>

<span data-ttu-id="0c2ad-104">Este tópico descreve quais bibliotecas são e como elas podem beneficiar usuários e desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-104">This topic describes what libraries are and how they can benefit users and developers.</span></span>

<span data-ttu-id="0c2ad-105">As bibliotecas são coleções de pastas definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-105">Libraries are user-defined collections of folders.</span></span> <span data-ttu-id="0c2ad-106">Uma biblioteca controla o local de armazenamento físico de cada pasta, o que alivia o usuário e o software dessa tarefa.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-106">A library keeps track of each folder's physical storage location, which relieves the user and the software of that task.</span></span> <span data-ttu-id="0c2ad-107">Os usuários podem agrupar pastas relacionadas em uma biblioteca, mesmo se essas pastas estiverem armazenadas em diferentes discos rígidos ou em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-107">Users can group related folders together in a library even if those folders are stored on different hard drives or different computers.</span></span>

<span data-ttu-id="0c2ad-108">Em uma biblioteca, as pastas e os arquivos aparecem para o usuário como uma única coleção e, usando a API da biblioteca do Shell, o conteúdo da biblioteca também pode parecer estar em um único local para um programa.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-108">In a library, the folders and files appear to the user as a single collection and, using the Shell Library API, the library's contents can also appear to be in a single location to a program.</span></span>

<span data-ttu-id="0c2ad-109">Em uma biblioteca, o conteúdo, como documentos, fotos, vídeos ou músicas de um usuário, pode ser classificado e exibido conforme o usuário desejar e não simplesmente como o sistema de arquivos exige.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-109">In a library, the contents, such as a user's documents, photos, videos, or music, can be sorted and displayed as the user wants and not simply as how the file system requires.</span></span> <span data-ttu-id="0c2ad-110">Por exemplo, os usuários podem organizar o conteúdo de uma biblioteca usando as propriedades dos itens na biblioteca para que os itens relacionados sejam classificados juntos mesmo se estiverem armazenados em pastas diferentes.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-110">For example, users can organize the contents of a library using the properties of the items in the library so that related items will sort together even if they are stored in different folders.</span></span>

![captura de tela da interface do usuário das bibliotecas](images/libraries-whatare.png)

<span data-ttu-id="0c2ad-112">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="0c2ad-112">In this topic:</span></span>

-   [<span data-ttu-id="0c2ad-113">Benefícios da biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c2ad-113">Library Benefits</span></span>](#library-benefits)
    -   [<span data-ttu-id="0c2ad-114">Benefícios do usuário</span><span class="sxs-lookup"><span data-stu-id="0c2ad-114">User Benefits</span></span>](#user-benefits)
    -   [<span data-ttu-id="0c2ad-115">Benefícios para o desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="0c2ad-115">Developer Benefits</span></span>](#developer-benefits)
-   [<span data-ttu-id="0c2ad-116">Gerenciando pastas em bibliotecas</span><span class="sxs-lookup"><span data-stu-id="0c2ad-116">Managing Folders in Libraries</span></span>](#managing-folders-in-libraries)
-   [<span data-ttu-id="0c2ad-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c2ad-117">Related topics</span></span>](#related-topics)

## <a name="library-benefits"></a><span data-ttu-id="0c2ad-118">Benefícios da biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c2ad-118">Library Benefits</span></span>

<span data-ttu-id="0c2ad-119">Esta seção descreve alguns dos benefícios das bibliotecas da perspectiva do usuário final e da perspectiva do desenvolvedor do programa.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-119">This section describes some of the benefits of libraries from the end-user's perspective and the program developer's perspective.</span></span>

### <a name="user-benefits"></a><span data-ttu-id="0c2ad-120">Benefícios do usuário</span><span class="sxs-lookup"><span data-stu-id="0c2ad-120">User Benefits</span></span>

<span data-ttu-id="0c2ad-121">A adição de suporte de biblioteca ao seu programa fornece os seguintes benefícios para o usuário:</span><span class="sxs-lookup"><span data-stu-id="0c2ad-121">Adding library support to your program provides the following benefits to the user:</span></span>

-   <span data-ttu-id="0c2ad-122">**As bibliotecas fornecem uma interface de usuário consistente no Windows 7**</span><span class="sxs-lookup"><span data-stu-id="0c2ad-122">**Libraries provide a consistent user interface in Windows 7**</span></span>

    <span data-ttu-id="0c2ad-123">As caixas de diálogo arquivo comum oferecem suporte a bibliotecas e fornecem a mesma experiência de usuário que o Windows Explorer no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-123">The common file dialog boxes support libraries and provide the same user experience as the Windows Explorer in Windows 7.</span></span> <span data-ttu-id="0c2ad-124">O suporte a bibliotecas em seu programa ajudará a fornecer uma interação mais direta para o usuário ao usar seu programa no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-124">Supporting libraries in your program will help provide a more seamless interaction for the user when using your program in Windows 7.</span></span>

-   <span data-ttu-id="0c2ad-125">**Os usuários decidem onde armazenar o conteúdo**</span><span class="sxs-lookup"><span data-stu-id="0c2ad-125">**Users decide where to store content**</span></span>

    <span data-ttu-id="0c2ad-126">As bibliotecas possibilitam que os usuários controlem onde o conteúdo é armazenado.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-126">Libraries make it possible for users to control where their content is stored.</span></span> <span data-ttu-id="0c2ad-127">Ao mesmo tempo, as bibliotecas fornecem padrões razoáveis para os usuários que não desejam gerenciar esse nível de detalhe em seu computador.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-127">At the same time, libraries provide reasonable defaults for users who do not want to manage that level of detail in their computer.</span></span> <span data-ttu-id="0c2ad-128">Os usuários decidem quanto, ou quanto pouco, o controle desejam exercitar onde e como o conteúdo é armazenado e a biblioteca funciona bem de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-128">Users decide how much, or how little, control they want to exercise over where and how their content is stored and the library works fine either way.</span></span>

### <a name="developer-benefits"></a><span data-ttu-id="0c2ad-129">Benefícios para o desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="0c2ad-129">Developer Benefits</span></span>

<span data-ttu-id="0c2ad-130">Você pode usar bibliotecas em seu programa para fornecer uma interface do usuário mais flexível e conveniente sem precisar adicionar muito código de programa complexo.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-130">You can use libraries in your program to provide a more flexible and convenient user interface without having to add a lot of complex program code.</span></span> <span data-ttu-id="0c2ad-131">Algumas das vantagens de adicionar suporte à biblioteca incluem:</span><span class="sxs-lookup"><span data-stu-id="0c2ad-131">Some of the advantages of adding library support include:</span></span>

-   <span data-ttu-id="0c2ad-132">**Bibliotecas dão suporte ao acesso à biblioteca e ao sistema de arquivos**</span><span class="sxs-lookup"><span data-stu-id="0c2ad-132">**Libraries support library and file-system access**</span></span>

    <span data-ttu-id="0c2ad-133">Usando a [**API da biblioteca do Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), os programas podem fornecer suporte à biblioteca para o usuário, ao mesmo tempo que reduz a complexidade de seu código de gerenciamento de arquivos e pastas.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-133">Using the [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), programs can provide library support for the user while reducing the complexity of their file and folder management code.</span></span> <span data-ttu-id="0c2ad-134">Se o seu programa já usa a API do sistema de arquivos, você pode preservar tanto desse código existente quanto desejar e ainda fornecer suporte de biblioteca ao usuário obtendo as informações necessárias do sistema de arquivos da API da **biblioteca do Shell**.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-134">If your program already uses the file-system API, you can preserve as much of that existing code as you want and still provide library support to the user by getting the necessary file-system information from the **Shell Library API**.</span></span>

-   <span data-ttu-id="0c2ad-135">**Notificação de alteração mais simples**</span><span class="sxs-lookup"><span data-stu-id="0c2ad-135">**Simpler change notification**</span></span>

    <span data-ttu-id="0c2ad-136">Tanto o sistema de arquivos quanto a API do Shell podem notificar seu programa quando o conteúdo de uma pasta ou biblioteca monitorada for alterada.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-136">Both the file-system and the Shell API can notify your program when the contents of a monitored folder or library change.</span></span> <span data-ttu-id="0c2ad-137">No entanto, usando a API do Shell, você pode monitorar todas as pastas na biblioteca com uma única notificação, mesmo que a pasta na biblioteca possa ser armazenada em diferentes unidades ou até mesmo em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-137">Using the Shell API, however, you can monitor all the folders in the library with a single notification, even though the folder in the library may be stored on different drives or even different computers.</span></span>

-   <span data-ttu-id="0c2ad-138">**Bibliotecas usam Propriedades de arquivo**</span><span class="sxs-lookup"><span data-stu-id="0c2ad-138">**Libraries use file properties**</span></span>

    <span data-ttu-id="0c2ad-139">Os programas podem usar as propriedades do arquivo para controlar quais arquivos são exibidos durante as operações de abrir e salvar que usam as caixas de diálogo de arquivo comum.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-139">Programs can use the file properties to control which files are displayed during open and save operations that use the common file dialog boxes.</span></span> <span data-ttu-id="0c2ad-140">Os programas também podem ter acesso às propriedades do arquivo usando as interfaces [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="0c2ad-140">Programs can also have access to file properties by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces.</span></span> <span data-ttu-id="0c2ad-141">As caixas de diálogo de arquivo comum também podem ser configuradas para permitir que os usuários atualizem as propriedades associadas ao seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-141">The common file dialog boxes can also be configured allow users to update the properties that are associated with their content.</span></span>

-   <span data-ttu-id="0c2ad-142">**Os programas podem criar bibliotecas dedicadas**</span><span class="sxs-lookup"><span data-stu-id="0c2ad-142">**Programs can create dedicated libraries**</span></span>

    <span data-ttu-id="0c2ad-143">Uma nova biblioteca pode ser criada quando as bibliotecas de usuários existentes não atendem às necessidades do programa — por exemplo, se um programa criar um novo tipo de conteúdo de usuário.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-143">A new library can be created when an existing user libraries does not meet the program's needs—for example, if a program creates a new type of user content.</span></span> <span data-ttu-id="0c2ad-144">A nova biblioteca pode ser configurada com um ícone exclusivo que representa seu conteúdo e torna a biblioteca fácil de identificar no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-144">The new library can be configured with a unique icon that represents their content and makes the library easy to identify in the Windows Explorer.</span></span>

## <a name="managing-folders-in-libraries"></a><span data-ttu-id="0c2ad-145">Gerenciando pastas em bibliotecas</span><span class="sxs-lookup"><span data-stu-id="0c2ad-145">Managing Folders in Libraries</span></span>

<span data-ttu-id="0c2ad-146">Os usuários podem organizar suas bibliotecas adicionando, movendo ou removendo pastas na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-146">Users can organize their libraries by adding, moving, or removing folders in the library.</span></span> <span data-ttu-id="0c2ad-147">Nem todas as pastas, no entanto, dão suporte a toda a funcionalidade que uma biblioteca pode fornecer.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-147">Not all folders, however, support all the functionality that a library can provide.</span></span> <span data-ttu-id="0c2ad-148">Muitos recursos de biblioteca exigem acesso rápido às diferentes propriedades da pasta e de seu conteúdo que só estão disponíveis por meio do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-148">Many library features require quick access to the different properties of the folder and its contents that are only available through Windows Search.</span></span> <span data-ttu-id="0c2ad-149">Para fornecer a funcionalidade completa da biblioteca, uma pasta deve ser capaz de ser indexada pelo Windows Search.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-149">To provide full library functionality, a folder must be able to be indexed by Windows Search.</span></span>

<span data-ttu-id="0c2ad-150">Uma biblioteca não permite que um usuário adicione pastas que não fornecem funcionalidade completa de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-150">A library does not allow a user to add folders that do not provide full library functionality.</span></span> <span data-ttu-id="0c2ad-151">No entanto, a [**API da biblioteca do Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) pode adicionar essas pastas.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-151">The [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) can, however, add such folders.</span></span> <span data-ttu-id="0c2ad-152">Se uma biblioteca contiver uma pasta que não oferece suporte à funcionalidade de biblioteca completa, a biblioteca funcionará em um modo de segurança e fornecerá uma funcionalidade limitada.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-152">If a library contains a folder that does not support full library functionality, the library will operate in a safe mode and provide a limited functionality.</span></span> <span data-ttu-id="0c2ad-153">A tabela a seguir descreve as pastas que oferecem suporte à funcionalidade de biblioteca completa e as que não fazem isso.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-153">The following table describes the folders that support full library functionality and those that do not.</span></span>



| <span data-ttu-id="0c2ad-154">Tipos de pasta que dão suporte à funcionalidade de biblioteca completa</span><span class="sxs-lookup"><span data-stu-id="0c2ad-154">Folder types that support full library functionality</span></span>                                                               | <span data-ttu-id="0c2ad-155">Tipos de pasta que não dão suporte à funcionalidade de biblioteca completa</span><span class="sxs-lookup"><span data-stu-id="0c2ad-155">Folder types that do not support full library functionality</span></span>                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c2ad-156">Discos rígidos NTFS e FAT32 fixos e externos.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-156">Fixed and external NTFS and FAT32 hard drives.</span></span>                                                                     | <span data-ttu-id="0c2ad-157">Unidades removíveis, como unidades flash USB ou cartões de memória Secure Digital (SD).</span><span class="sxs-lookup"><span data-stu-id="0c2ad-157">Removable drives such as USB flash drives or Secure Digital (SD) memory cards.</span></span>               |
| <span data-ttu-id="0c2ad-158">Compartilhamentos de arquivos que são indexados pelo Windows Search, como servidores departamentais, Windows 7 ou Windows Vista Home PCs.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-158">File shares that are indexed by Windows Search such as departmental servers, Windows 7, or Windows Vista home PCs.</span></span> | <span data-ttu-id="0c2ad-159">Mídia removível, como mídia de CD-ROM ou DVD.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-159">Removable media such as CD-ROM or DVD media.</span></span>                                                 |
| <span data-ttu-id="0c2ad-160">Compartilhamentos de arquivos que estão disponíveis offline, como uma pasta **meus documentos** redirecionada ou um cache Client-Side.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-160">File shares that are available offline such as a redirected **My Documents** folder or a Client-Side Cache.</span></span>        | <span data-ttu-id="0c2ad-161">Compartilhamentos de rede que não estão disponíveis offline nem remotamente indexados, como unidades NAS.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-161">Network shares that are neither available offline nor remotely indexed such as NAS drives.</span></span>   |
|                                                                                                                    | <span data-ttu-id="0c2ad-162">Outras fontes de dados, como o Microsoft SharePoint, o Microsoft Exchange e o Microsoft OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-162">Other data sources such as Microsoft SharePoint, Microsoft Exchange, and Microsoft OneDrive.</span></span> |



 

<span data-ttu-id="0c2ad-163">A imagem a seguir mostra a exibição limitada de conteúdo da biblioteca no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="0c2ad-163">The following image shows the limited display of library contents while in safe mode.</span></span>

![abrir caixa de diálogo quando as bibliotecas estiverem no modo de segurança](images/libraries-supportedfolders.png)

## <a name="related-topics"></a><span data-ttu-id="0c2ad-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c2ad-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c2ad-166">Sobre bibliotecas</span><span class="sxs-lookup"><span data-stu-id="0c2ad-166">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="0c2ad-167">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="0c2ad-167">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="0c2ad-168">Links do Shell</span><span class="sxs-lookup"><span data-stu-id="0c2ad-168">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="0c2ad-169">Pastas conhecidas</span><span class="sxs-lookup"><span data-stu-id="0c2ad-169">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="0c2ad-170">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c2ad-170">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 

---
description: Um link do Shell é um objeto de dados que contém informações usadas para acessar outro objeto no namespace do Shell&\# 8212; ou seja, qualquer objeto visível por meio do Windows Explorer.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Links do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327bcb425f998bcc2a4c0714118d4461ded253ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170098"
---
# <a name="shell-links"></a><span data-ttu-id="d21a1-103">Links do Shell</span><span class="sxs-lookup"><span data-stu-id="d21a1-103">Shell Links</span></span>

<span data-ttu-id="d21a1-104">Um *link do Shell* é um objeto de dados que contém informações usadas para acessar outro objeto no namespace do Shell, ou seja, qualquer objeto visível por meio do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d21a1-104">A *Shell link* is a data object that contains information used to access another object in the Shell's namespace—that is, any object visible through Windows Explorer.</span></span> <span data-ttu-id="d21a1-105">Os tipos de objetos que podem ser acessados por meio de links do Shell incluem arquivos, pastas, unidades de disco e impressoras.</span><span class="sxs-lookup"><span data-stu-id="d21a1-105">The types of objects that can be accessed through Shell links include files, folders, disk drives, and printers.</span></span> <span data-ttu-id="d21a1-106">Um link do Shell permite que um usuário ou um aplicativo acesse um objeto de qualquer lugar no namespace.</span><span class="sxs-lookup"><span data-stu-id="d21a1-106">A Shell link allows a user or an application to access an object from anywhere in the namespace.</span></span> <span data-ttu-id="d21a1-107">O usuário ou o aplicativo não precisa saber o nome atual e o local do objeto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-107">The user or application does not need to know the current name and location of the object.</span></span>

-   [<span data-ttu-id="d21a1-108">Sobre links do Shell</span><span class="sxs-lookup"><span data-stu-id="d21a1-108">About Shell Links</span></span>](#about-shell-links)
    -   [<span data-ttu-id="d21a1-109">Resolução de link</span><span class="sxs-lookup"><span data-stu-id="d21a1-109">Link Resolution</span></span>](#link-resolution)
    -   [<span data-ttu-id="d21a1-110">Vincular arquivos</span><span class="sxs-lookup"><span data-stu-id="d21a1-110">Link Files</span></span>](#link-files)
    -   [<span data-ttu-id="d21a1-111">Identificadores de item e listas de identificadores</span><span class="sxs-lookup"><span data-stu-id="d21a1-111">Item Identifiers and Identifier Lists</span></span>](#item-identifiers-and-identifier-lists)
-   [<span data-ttu-id="d21a1-112">Usando links do Shell</span><span class="sxs-lookup"><span data-stu-id="d21a1-112">Using Shell Links</span></span>](#using-shell-links)
    -   [<span data-ttu-id="d21a1-113">Criação de um atalho e um atalho de pasta para um arquivo</span><span class="sxs-lookup"><span data-stu-id="d21a1-113">Creating a Shortcut and a Folder Shortcut to a File</span></span>](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [<span data-ttu-id="d21a1-114">Resolvendo um atalho</span><span class="sxs-lookup"><span data-stu-id="d21a1-114">Resolving a Shortcut</span></span>](#resolving-a-shortcut)
    -   [<span data-ttu-id="d21a1-115">Criando um atalho para um objeto não arquivo</span><span class="sxs-lookup"><span data-stu-id="d21a1-115">Creating a Shortcut to a Nonfile Object</span></span>](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a><span data-ttu-id="d21a1-116">Sobre links do Shell</span><span class="sxs-lookup"><span data-stu-id="d21a1-116">About Shell Links</span></span>

<span data-ttu-id="d21a1-117">O usuário cria um link do Shell escolhendo o comando **criar atalho** no menu de atalho de um objeto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-117">The user creates a Shell link by choosing the **Create Shortcut** command from an object's shortcut menu.</span></span> <span data-ttu-id="d21a1-118">O sistema cria automaticamente um ícone para o link do Shell combinando o ícone do objeto com uma pequena seta (conhecida como ícone de sobreposição de link definido pelo sistema) que aparece no canto inferior esquerdo do ícone.</span><span class="sxs-lookup"><span data-stu-id="d21a1-118">The system automatically creates an icon for the Shell link by combining the object's icon with a small arrow (known as the system-defined link overlay icon) that appears in the lower left corner of the icon.</span></span> <span data-ttu-id="d21a1-119">Um link do shell que tem um ícone é chamado de atalho; no entanto, os termos link e atalho do shell são frequentemente usados de maneira intercambiável.</span><span class="sxs-lookup"><span data-stu-id="d21a1-119">A Shell link that has an icon is called a shortcut; however, the terms Shell link and shortcut are often used interchangeably.</span></span> <span data-ttu-id="d21a1-120">Normalmente, o usuário cria atalhos para obter acesso rápido a objetos armazenados em subpastas ou em pastas compartilhadas em outros computadores.</span><span class="sxs-lookup"><span data-stu-id="d21a1-120">Typically, the user creates shortcuts to gain quick access to objects stored in subfolders or in shared folders on other computers.</span></span> <span data-ttu-id="d21a1-121">Por exemplo, um usuário pode criar um atalho para um documento do Microsoft Word que está localizado em uma subpasta e posicionar o ícone de atalho na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-121">For example, a user can create a shortcut to a Microsoft Word document that is located in a subfolder and place the shortcut icon on the desktop.</span></span> <span data-ttu-id="d21a1-122">Em seguida, o usuário pode abrir o documento clicando duas vezes no ícone de atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-122">The user can then open the document by double-clicking the shortcut icon.</span></span> <span data-ttu-id="d21a1-123">Se o documento for movido ou renomeado depois que o atalho for criado, o sistema tentará atualizar o atalho na próxima vez que o usuário o selecionar.</span><span class="sxs-lookup"><span data-stu-id="d21a1-123">If the document is moved or renamed after the shortcut is created, the system will attempt to update the shortcut the next time the user selects it.</span></span>

<span data-ttu-id="d21a1-124">Os aplicativos também podem criar e usar links e atalhos do Shell.</span><span class="sxs-lookup"><span data-stu-id="d21a1-124">Applications can also create and use Shell links and shortcuts.</span></span> <span data-ttu-id="d21a1-125">Por exemplo, um aplicativo de processamento de texto pode criar um link do Shell para implementar uma lista dos documentos usados mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="d21a1-125">For example, a word processing application might create a Shell link to implement a list of the most recently used documents.</span></span> <span data-ttu-id="d21a1-126">Um aplicativo cria um link do shell usando a interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para criar um objeto de link do Shell.</span><span class="sxs-lookup"><span data-stu-id="d21a1-126">An application creates a Shell link by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface to create a Shell link object.</span></span> <span data-ttu-id="d21a1-127">O aplicativo usa a interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ou [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) para armazenar o objeto em um arquivo ou fluxo.</span><span class="sxs-lookup"><span data-stu-id="d21a1-127">The application uses the [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to store the object in a file or stream.</span></span>

> [!Note]  
> <span data-ttu-id="d21a1-128">Você não pode usar [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para criar um link para uma URL.</span><span class="sxs-lookup"><span data-stu-id="d21a1-128">You cannot use [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) to create a link to a URL.</span></span>

 

<span data-ttu-id="d21a1-129">Esta visão geral descreve a interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) e explica como usá-la para criar e resolver links de Shell de dentro de um aplicativo baseado no Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="d21a1-129">This overview describes the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface and explains how to use it to create and resolve Shell links from within a Microsoft Win32-based application.</span></span> <span data-ttu-id="d21a1-130">Como o design de links do Shell se baseia no COM (Component Object Model OLE), você deve estar familiarizado com os conceitos básicos da programação COM e OLE antes de ler essa visão geral.</span><span class="sxs-lookup"><span data-stu-id="d21a1-130">Because the design of Shell links is based on the OLE Component Object Model (COM), you should be familiar with the basic concepts of COM and OLE programming before reading this overview.</span></span>

### <a name="link-resolution"></a><span data-ttu-id="d21a1-131">Resolução de link</span><span class="sxs-lookup"><span data-stu-id="d21a1-131">Link Resolution</span></span>

<span data-ttu-id="d21a1-132">Se um usuário criar um atalho para um objeto e o nome ou o local do objeto for alterado posteriormente, o sistema executará automaticamente as etapas para atualizar ou resolver o atalho na próxima vez que o usuário o selecionar.</span><span class="sxs-lookup"><span data-stu-id="d21a1-132">If a user creates a shortcut to an object and the name or location of the object is later changed, the system automatically takes steps to update, or resolve, the shortcut the next time the user selects it.</span></span> <span data-ttu-id="d21a1-133">No entanto, se um aplicativo criar um link do Shell e o armazenar em um fluxo, o sistema não tentará resolver automaticamente o link.</span><span class="sxs-lookup"><span data-stu-id="d21a1-133">However, if an application creates a Shell link and stores it in a stream, the system does not automatically attempt to resolve the link.</span></span> <span data-ttu-id="d21a1-134">O aplicativo deve resolver o link chamando o método [**IShellLink:: resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-134">The application must resolve the link by calling the [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) method.</span></span>

<span data-ttu-id="d21a1-135">Quando um link do Shell é criado, o sistema salva as informações sobre o link.</span><span class="sxs-lookup"><span data-stu-id="d21a1-135">When a Shell link is created, the system saves information about the link.</span></span> <span data-ttu-id="d21a1-136">Ao resolver um link, seja automaticamente ou com uma chamada [**IShellLink:: resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) — o sistema primeiro recupera o caminho associado ao link do shell usando um ponteiro para a lista de identificadores do link do Shell.</span><span class="sxs-lookup"><span data-stu-id="d21a1-136">When resolving a link—either automatically or with an [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) call—the system first retrieves the path associated with the Shell link by using a pointer to the Shell link's identifier list.</span></span> <span data-ttu-id="d21a1-137">Para obter mais informações sobre a lista de identificadores, consulte [identificadores de item e listas de identificadores](#item-identifiers-and-identifier-lists).</span><span class="sxs-lookup"><span data-stu-id="d21a1-137">For more information about the identifier list, see [Item Identifiers and Identifier Lists](#item-identifiers-and-identifier-lists).</span></span> <span data-ttu-id="d21a1-138">O sistema pesquisa o objeto associado nesse caminho e, se encontrar o objeto, resolve o link.</span><span class="sxs-lookup"><span data-stu-id="d21a1-138">The system searches for the associated object in that path and, if it finds the object, resolves the link.</span></span> <span data-ttu-id="d21a1-139">Se o sistema não conseguir localizar o objeto, ele chamará o serviço de [rastreamento de link distribuído e](../fileio/distributed-link-tracking-and-object-identifiers.md) de DLT (identificadores de objeto), se disponível, para localizar o objeto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-139">If the system cannot find the object, it calls on the [Distributed Link Tracking and Object Identifiers](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT) service, if available, to locate the object.</span></span> <span data-ttu-id="d21a1-140">Se o serviço DLT não estiver disponível ou não puder localizar o objeto, o sistema examinará o mesmo diretório em busca de um objeto com o mesmo tempo e atributos de criação de arquivo, mas com um nome diferente.</span><span class="sxs-lookup"><span data-stu-id="d21a1-140">If the DLT service is not available or cannot find the object, the system looks in the same directory for an object with the same file creation time and attributes but with a different name.</span></span> <span data-ttu-id="d21a1-141">Esse tipo de pesquisa resolve um link para um objeto que foi renomeado.</span><span class="sxs-lookup"><span data-stu-id="d21a1-141">This type of search resolves a link to an object that has been renamed.</span></span>

<span data-ttu-id="d21a1-142">Se o sistema ainda não conseguir localizar o objeto, ele pesquisará os diretórios, a área de trabalho e os volumes locais, olhando recursivamente, embora a árvore de diretórios de um objeto com o mesmo nome ou hora de criação.</span><span class="sxs-lookup"><span data-stu-id="d21a1-142">If the system still cannot find the object, it searches the directories, the desktop, and local volumes, looking recursively though the directory tree for an object with either the same name or creation time.</span></span> <span data-ttu-id="d21a1-143">Se o sistema ainda não encontrar uma correspondência, ele exibirá uma caixa de diálogo solicitando ao usuário um local.</span><span class="sxs-lookup"><span data-stu-id="d21a1-143">If the system still does not find a match, it displays a dialog box prompting the user for a location.</span></span> <span data-ttu-id="d21a1-144">Um aplicativo pode suprimir a caixa de diálogo especificando o **SLR nenhum valor de \_ interface do \_ usuário** em uma chamada para [**IShellLink:: resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span><span class="sxs-lookup"><span data-stu-id="d21a1-144">An application can suppress the dialog box by specifying the **SLR\_NO\_UI** value in a call to [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span>

### <a name="initialization-of-the-component-object-library"></a><span data-ttu-id="d21a1-145">Inicialização da biblioteca de objetos de componente</span><span class="sxs-lookup"><span data-stu-id="d21a1-145">Initialization of the Component Object Library</span></span>

<span data-ttu-id="d21a1-146">Antes que um aplicativo possa criar e resolver atalhos, ele deve inicializar a biblioteca de objetos de componente chamando a função [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-146">Before an application can create and resolve shortcuts, it must initialize the component object library by calling the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function.</span></span> <span data-ttu-id="d21a1-147">Cada chamada para **CoInitialize** requer uma chamada correspondente para a função [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , que um aplicativo deve chamar quando termina.</span><span class="sxs-lookup"><span data-stu-id="d21a1-147">Each call to **CoInitialize** requires a corresponding call to the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function, which an application should call when it terminates.</span></span> <span data-ttu-id="d21a1-148">A chamada para **CoUninitialize** garante que o aplicativo não seja encerrado até que tenha recebido todas as suas mensagens pendentes.</span><span class="sxs-lookup"><span data-stu-id="d21a1-148">The call to **CoUninitialize** ensures that the application does not terminate until it has received all of its pending messages.</span></span>

### <a name="location-independent-names"></a><span data-ttu-id="d21a1-149">Nomes de Location-Independent</span><span class="sxs-lookup"><span data-stu-id="d21a1-149">Location-Independent Names</span></span>

<span data-ttu-id="d21a1-150">O sistema fornece nomes independentes de local para links de Shell para objetos armazenados em pastas compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="d21a1-150">The system provides location-independent names for Shell links to objects stored in shared folders.</span></span> <span data-ttu-id="d21a1-151">Se o objeto for armazenado localmente, o sistema fornecerá o caminho local e o nome do arquivo para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-151">If the object is stored locally, the system provides the local path and file name for the object.</span></span> <span data-ttu-id="d21a1-152">Se o objeto for armazenado remotamente, o sistema fornecerá um nome de recurso de rede UNC (Convenção de nomenclatura universal) para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-152">If the object is stored remotely, the system provides a Universal Naming Convention (UNC) network resource name for the object.</span></span> <span data-ttu-id="d21a1-153">Como o sistema fornece nomes independentes de local, um link de shell pode servir como um nome universal para um arquivo que pode ser transferido para outros computadores.</span><span class="sxs-lookup"><span data-stu-id="d21a1-153">Because the system provides location-independent names, a Shell link can serve as a universal name for a file that can be transferred to other computers.</span></span>

### <a name="link-files"></a><span data-ttu-id="d21a1-154">Vincular arquivos</span><span class="sxs-lookup"><span data-stu-id="d21a1-154">Link Files</span></span>

<span data-ttu-id="d21a1-155">Quando o usuário cria um atalho para um objeto escolhendo o comando **criar atalho** no menu de atalho do objeto, o Windows armazena as informações necessárias para acessar o objeto em um arquivo de link — um arquivo binário que tem a extensão de nome de arquivo. lnk.</span><span class="sxs-lookup"><span data-stu-id="d21a1-155">When the user creates a shortcut to an object by choosing the **Create Shortcut** command from the object's shortcut menu, Windows stores the information it needs to access the object in a link file—a binary file that has the .lnk file name extension.</span></span> <span data-ttu-id="d21a1-156">Um arquivo de link contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="d21a1-156">A link file contains the following information:</span></span>

-   <span data-ttu-id="d21a1-157">O local (caminho) do objeto referenciado pelo atalho (chamado de objeto correspondente).</span><span class="sxs-lookup"><span data-stu-id="d21a1-157">The location (path) of the object referenced by the shortcut (called the corresponding object).</span></span>
-   <span data-ttu-id="d21a1-158">O diretório de trabalho do objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="d21a1-158">The working directory of the corresponding object.</span></span>
-   <span data-ttu-id="d21a1-159">A lista de argumentos que o sistema passa para o objeto correspondente quando o método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) é ativado para o atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-159">The list of arguments that the system passes to the corresponding object when the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method is activated for the shortcut.</span></span>
-   <span data-ttu-id="d21a1-160">O comando show usado para definir o estado de exibição inicial do objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="d21a1-160">The show command used to set the initial show state of the corresponding object.</span></span> <span data-ttu-id="d21a1-161">Esse é um dos valores de SW \_ descritos em [**conwindow**](/windows/win32/api/winuser/nf-winuser-showwindow).</span><span class="sxs-lookup"><span data-stu-id="d21a1-161">This is one of the SW\_ values described in [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).</span></span>
-   <span data-ttu-id="d21a1-162">O local (caminho e índice) do ícone do atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-162">The location (path and index) of the shortcut's icon.</span></span>
-   <span data-ttu-id="d21a1-163">A cadeia de caracteres de descrição do atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-163">The shortcut's description string.</span></span>
-   <span data-ttu-id="d21a1-164">O atalho de teclado para o atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-164">The keyboard shortcut for the shortcut.</span></span>

<span data-ttu-id="d21a1-165">Quando um arquivo de link é excluído, o objeto correspondente não é afetado.</span><span class="sxs-lookup"><span data-stu-id="d21a1-165">When a link file is deleted, the corresponding object is not affected.</span></span>

<span data-ttu-id="d21a1-166">Se você criar um atalho para outro atalho, o sistema simplesmente copiará o arquivo de link em vez de criar um novo arquivo de link.</span><span class="sxs-lookup"><span data-stu-id="d21a1-166">If you create a shortcut to another shortcut, the system simply copies the link file rather than creating a new link file.</span></span> <span data-ttu-id="d21a1-167">Nesse caso, os atalhos não serão independentes um do outro.</span><span class="sxs-lookup"><span data-stu-id="d21a1-167">In this case, the shortcuts will not be independent of each other.</span></span>

<span data-ttu-id="d21a1-168">Um aplicativo pode registrar uma extensão de nome de arquivo como um tipo de arquivo de atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-168">An application can register a file name extension as a shortcut file type.</span></span> <span data-ttu-id="d21a1-169">Se um arquivo tiver uma extensão de nome de arquivo que tenha sido registrada como um tipo de arquivo de atalho, o sistema adicionará automaticamente o ícone de sobreposição de link definido pelo sistema (uma pequena seta) ao ícone do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d21a1-169">If a file has a file name extension that has been registered as a shortcut file type, the system automatically adds the system-defined link overlay icon (a small arrow) to the file's icon.</span></span> <span data-ttu-id="d21a1-170">Para registrar uma extensão de nome de arquivo como um tipo de arquivo de atalho, você deve adicionar o valor IsShortcut à descrição do registro da extensão de nome de arquivo, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="d21a1-170">To register a file name extension as a shortcut file type, you must add the IsShortcut value to the registry description of the file name extension, as shown in the example below.</span></span> <span data-ttu-id="d21a1-171">Observe que o Shell deve ser reiniciado para que o ícone de sobreposição entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="d21a1-171">Note that the Shell must be restarted for the overlay icon to take effect.</span></span> <span data-ttu-id="d21a1-172">IsShortcut não tem valor de dados.</span><span class="sxs-lookup"><span data-stu-id="d21a1-172">IsShortcut has no data value.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a><span data-ttu-id="d21a1-173">Nomes de atalho</span><span class="sxs-lookup"><span data-stu-id="d21a1-173">Shortcut names</span></span>

<span data-ttu-id="d21a1-174">O nome do atalho, que é uma cadeia de caracteres que aparece abaixo do ícone de link do Shell, é, na verdade, o nome do arquivo do próprio atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-174">The shortcut's name, which is a string that appears below the Shell link icon, is actually the file name of the shortcut itself.</span></span> <span data-ttu-id="d21a1-175">O usuário pode editar a cadeia de caracteres de descrição selecionando-a e inserindo uma nova cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d21a1-175">The user can edit the description string by selecting it and entering a new string.</span></span>

### <a name="location-of-shortcuts-in-the-namespace"></a><span data-ttu-id="d21a1-176">Local dos atalhos no namespace</span><span class="sxs-lookup"><span data-stu-id="d21a1-176">Location of shortcuts in the namespace</span></span>

<span data-ttu-id="d21a1-177">Um atalho pode existir na área de trabalho ou em qualquer lugar no namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="d21a1-177">A shortcut can exist on the desktop or anywhere in the Shell's namespace.</span></span> <span data-ttu-id="d21a1-178">Da mesma forma, o objeto que está associado ao atalho também pode existir em qualquer lugar no namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="d21a1-178">Similarly, the object that is associated with the shortcut can also exist anywhere in the Shell's namespace.</span></span> <span data-ttu-id="d21a1-179">Um aplicativo pode usar o método [**IShellLink:: SetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) para definir o caminho e o nome de arquivo para o objeto associado e o método [**IShellLink:: GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) para recuperar o caminho atual e o nome do arquivo para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-179">An application can use the [**IShellLink::SetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) method to set the path and file name for the associated object, and the [**IShellLink::GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) method to retrieve the current path and file name for the object.</span></span>

### <a name="shortcut-working-directory"></a><span data-ttu-id="d21a1-180">Diretório de trabalho de atalho</span><span class="sxs-lookup"><span data-stu-id="d21a1-180">Shortcut working directory</span></span>

<span data-ttu-id="d21a1-181">O diretório de trabalho é o diretório em que o objeto correspondente de um atalho carrega ou armazena arquivos quando o usuário não identifica um diretório específico.</span><span class="sxs-lookup"><span data-stu-id="d21a1-181">The working directory is the directory where the corresponding object of a shortcut loads or stores files when the user does not identify a specific directory.</span></span> <span data-ttu-id="d21a1-182">Um arquivo de link contém o nome do diretório de trabalho para o objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="d21a1-182">A link file contains the name of the working directory for the corresponding object.</span></span> <span data-ttu-id="d21a1-183">Um aplicativo pode definir o nome do diretório de trabalho para o objeto correspondente usando o método [**IShellLink:: SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) e pode recuperar o nome do diretório de trabalho atual para o objeto correspondente usando o método [**IShellLink:: GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-183">An application can set the name of the working directory for the corresponding object by using the [**IShellLink::SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) method and can retrieve the name of the current working directory for the corresponding object by using the [**IShellLink::GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) method.</span></span>

### <a name="shortcut-command-line-arguments"></a><span data-ttu-id="d21a1-184">Argumentos de linha de comando de atalho</span><span class="sxs-lookup"><span data-stu-id="d21a1-184">Shortcut command-line arguments</span></span>

<span data-ttu-id="d21a1-185">Um arquivo de link contém argumentos de linha de comando que o Shell passa para o objeto correspondente quando o usuário seleciona o link.</span><span class="sxs-lookup"><span data-stu-id="d21a1-185">A link file contains command-line arguments that the Shell passes to the corresponding object when the user selects the link.</span></span> <span data-ttu-id="d21a1-186">Um aplicativo pode definir os argumentos de linha de comando para um atalho usando o método [**IShellLink:: SetArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-186">An application can set the command-line arguments for a shortcut by using the [**IShellLink::SetArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) method.</span></span> <span data-ttu-id="d21a1-187">É útil definir argumentos de linha de comando quando o aplicativo correspondente, como um vinculador ou compilador, usa sinalizadores especiais como argumentos.</span><span class="sxs-lookup"><span data-stu-id="d21a1-187">It is useful to set command-line arguments when the corresponding application, such as a linker or compiler, takes special flags as arguments.</span></span> <span data-ttu-id="d21a1-188">Um aplicativo pode recuperar os argumentos de linha de comando de um atalho usando o método [**IShellLink:: Getarguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-188">An application can retrieve the command-line arguments from a shortcut by using the [**IShellLink::GetArguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) method.</span></span>

### <a name="shortcut-show-commands"></a><span data-ttu-id="d21a1-189">Comandos show de atalho</span><span class="sxs-lookup"><span data-stu-id="d21a1-189">Shortcut show commands</span></span>

<span data-ttu-id="d21a1-190">Quando o usuário clica duas vezes em um atalho, o sistema inicia o aplicativo associado ao objeto correspondente e define o estado de exibição inicial do aplicativo com base no comando show especificado pelo atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-190">When the user double-clicks a shortcut, the system starts the application associated with the corresponding object and sets the initial show state of the application based on the show command specified by the shortcut.</span></span> <span data-ttu-id="d21a1-191">O comando show pode ser qualquer um dos valores de SW \_ incluídos na descrição da função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-191">The show command can be any of the SW\_ values included in the description of the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span> <span data-ttu-id="d21a1-192">Um aplicativo pode definir o comando show para um atalho usando o método [**IShellLink:: SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) e pode recuperar o comando show atual usando o método [**IShellLink:: GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-192">An application can set the show command for a shortcut by using the [**IShellLink::SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) method and can retrieve the current show command by using the [**IShellLink::GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) method.</span></span>

### <a name="shortcut-icons"></a><span data-ttu-id="d21a1-193">Ícones de atalho</span><span class="sxs-lookup"><span data-stu-id="d21a1-193">Shortcut icons</span></span>

<span data-ttu-id="d21a1-194">Assim como outros objetos do Shell, um atalho tem um ícone.</span><span class="sxs-lookup"><span data-stu-id="d21a1-194">Like other Shell objects, a shortcut has an icon.</span></span> <span data-ttu-id="d21a1-195">O usuário acessa o objeto associado a um atalho clicando duas vezes no ícone do atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-195">The user accesses the object associated with a shortcut by double-clicking the shortcut's icon.</span></span> <span data-ttu-id="d21a1-196">Quando o sistema cria um ícone para um atalho, ele usa o bitmap do objeto correspondente e adiciona o ícone de sobreposição de link definido pelo sistema (uma seta pequena) no canto inferior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="d21a1-196">When the system creates an icon for a shortcut, it uses the bitmap of the corresponding object and adds the system-defined link overlay icon (a small arrow) to the lower left corner.</span></span> <span data-ttu-id="d21a1-197">Um aplicativo pode definir o local (caminho e índice) do ícone de um atalho usando o método [**IShellLink:: SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-197">An application can set the location (path and index) of a shortcut's icon by using the [**IShellLink::SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) method.</span></span> <span data-ttu-id="d21a1-198">Um aplicativo pode recuperar esse local usando o método [**IShellLink:: GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-198">An application can retrieve this location by using the [**IShellLink::GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) method.</span></span>

### <a name="shortcut-descriptions"></a><span data-ttu-id="d21a1-199">Descrições de atalho</span><span class="sxs-lookup"><span data-stu-id="d21a1-199">Shortcut descriptions</span></span>

<span data-ttu-id="d21a1-200">Os atalhos têm descrições, mas o usuário nunca as vê.</span><span class="sxs-lookup"><span data-stu-id="d21a1-200">Shortcuts have descriptions, but the user never sees them.</span></span> <span data-ttu-id="d21a1-201">Um aplicativo pode usar uma descrição para armazenar qualquer informação de texto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-201">An application can use a description to store any text information.</span></span> <span data-ttu-id="d21a1-202">As descrições são definidas usando o método [**IShellLink:: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) e recuperadas usando o método [**IShellLink:: GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-202">Descriptions are set using the [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) method and retrieved using the [**IShellLink::GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) method.</span></span>

### <a name="shortcut-keyboard-shortcuts"></a><span data-ttu-id="d21a1-203">Atalhos de teclado de atalho</span><span class="sxs-lookup"><span data-stu-id="d21a1-203">Shortcut Keyboard Shortcuts</span></span>

<span data-ttu-id="d21a1-204">Um objeto de atalho pode ter um atalho de teclado associado a ele.</span><span class="sxs-lookup"><span data-stu-id="d21a1-204">A shortcut object can have a keyboard shortcut associated with it.</span></span> <span data-ttu-id="d21a1-205">Os atalhos de teclado permitem que um usuário pressione uma combinação de teclas para ativar um atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-205">Keyboard shortcuts allow a user to press a combination of keys to activate a shortcut.</span></span> <span data-ttu-id="d21a1-206">Um aplicativo pode definir o atalho de teclado para um atalho usando o método [**IShellLink::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) AutoFormat e pode recuperar o atalho de teclado atual usando o método [**IShellLink::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) keyshortcut.</span><span class="sxs-lookup"><span data-stu-id="d21a1-206">An application can set the keyboard shortcut for a shortcut by using the [**IShellLink::SetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) method and can retrieve the current keyboard shortcut by using the [**IShellLink::GetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) method.</span></span>

### <a name="item-identifiers-and-identifier-lists"></a><span data-ttu-id="d21a1-207">Identificadores de item e listas de identificadores</span><span class="sxs-lookup"><span data-stu-id="d21a1-207">Item Identifiers and Identifier Lists</span></span>

<span data-ttu-id="d21a1-208">O Shell usa identificadores de objeto dentro do namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="d21a1-208">The Shell uses object identifiers within the Shell's namespace.</span></span> <span data-ttu-id="d21a1-209">Todos os objetos visíveis no Shell (arquivos, diretórios, servidores, grupos de pastas e assim por diante) têm identificadores exclusivos entre os objetos dentro de sua pasta pai.</span><span class="sxs-lookup"><span data-stu-id="d21a1-209">All objects visible in the Shell (files, directories, servers, workgroups, and so on) have unique identifiers among the objects within their parent folder.</span></span> <span data-ttu-id="d21a1-210">Esses identificadores são chamados de identificadores de item e têm o tipo de dados [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , conforme definido no arquivo de cabeçalho Shtypes. h.</span><span class="sxs-lookup"><span data-stu-id="d21a1-210">These identifiers are called item identifiers, and they have the [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) data type as defined in the Shtypes.h header file.</span></span> <span data-ttu-id="d21a1-211">Um identificador de item é um fluxo de bytes de comprimento variável que contém informações que identificam um objeto dentro de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="d21a1-211">An item identifier is a variable-length byte stream that contains information that identifies an object within a folder.</span></span> <span data-ttu-id="d21a1-212">Somente o criador de um identificador de item conhece o conteúdo e o formato do identificador.</span><span class="sxs-lookup"><span data-stu-id="d21a1-212">Only the creator of an item identifier knows the content and format of the identifier.</span></span> <span data-ttu-id="d21a1-213">A única parte de um identificador de item que o Shell usa são os dois primeiros bytes, que especificam o tamanho do identificador.</span><span class="sxs-lookup"><span data-stu-id="d21a1-213">The only part of an item identifier that the Shell uses is the first two bytes, which specify the size of the identifier.</span></span>

<span data-ttu-id="d21a1-214">Cada pasta pai tem seu próprio identificador de item que a identifica em sua própria pasta pai.</span><span class="sxs-lookup"><span data-stu-id="d21a1-214">Each parent folder has its own item identifier that identifies it within its own parent folder.</span></span> <span data-ttu-id="d21a1-215">Assim, qualquer objeto shell pode ser identificado exclusivamente por uma lista de identificadores de item.</span><span class="sxs-lookup"><span data-stu-id="d21a1-215">Thus, any Shell object can be uniquely identified by a list of item identifiers.</span></span> <span data-ttu-id="d21a1-216">Uma pasta pai mantém uma lista de identificadores para os itens que ele contém.</span><span class="sxs-lookup"><span data-stu-id="d21a1-216">A parent folder keeps a list of identifiers for the items it contains.</span></span> <span data-ttu-id="d21a1-217">A lista tem o tipo de dados [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-217">The list has the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) data type.</span></span> <span data-ttu-id="d21a1-218">As listas de identificadores de item são alocadas pelo shell e podem ser passadas entre as interfaces do Shell, como [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).</span><span class="sxs-lookup"><span data-stu-id="d21a1-218">Item identifier lists are allocated by the Shell and may be passed across Shell interfaces, such as [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).</span></span> <span data-ttu-id="d21a1-219">É importante lembrar que cada identificador em uma lista de identificadores de itens só é significativo no contexto de sua pasta pai.</span><span class="sxs-lookup"><span data-stu-id="d21a1-219">It is important to remember that each identifier in an item identifier list is only meaningful within the context of its parent folder.</span></span>

<span data-ttu-id="d21a1-220">Um aplicativo pode definir a lista de identificadores de itens de um atalho usando o método [**IShellLink:: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-220">An application can set a shortcut's item identifier list by using the [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) method.</span></span> <span data-ttu-id="d21a1-221">Esse método é útil ao definir um atalho para um objeto que não é um arquivo, como uma impressora ou unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="d21a1-221">This method is useful when setting a shortcut to an object that is not a file, such as a printer or disk drive.</span></span> <span data-ttu-id="d21a1-222">Um aplicativo pode recuperar a lista de identificadores de itens de um atalho usando o método [**IShellLink:: GetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-222">An application can retrieve a shortcut's item identifier list by using the [**IShellLink::GetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) method.</span></span>

## <a name="using-shell-links"></a><span data-ttu-id="d21a1-223">Usando links do Shell</span><span class="sxs-lookup"><span data-stu-id="d21a1-223">Using Shell Links</span></span>

<span data-ttu-id="d21a1-224">Esta seção contém exemplos que demonstram como criar e resolver atalhos de dentro de um aplicativo baseado em Win32.</span><span class="sxs-lookup"><span data-stu-id="d21a1-224">This section contains examples that demonstrate how to create and resolve shortcuts from within a Win32-based application.</span></span> <span data-ttu-id="d21a1-225">Esta seção pressupõe que você esteja familiarizado com a programação COM Win32, C++ e OLE.</span><span class="sxs-lookup"><span data-stu-id="d21a1-225">This section assumes you are familiar with Win32, C++, and OLE COM programming.</span></span>

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a><span data-ttu-id="d21a1-226">Criação de um atalho e um atalho de pasta para um arquivo</span><span class="sxs-lookup"><span data-stu-id="d21a1-226">Creating a Shortcut and a Folder Shortcut to a File</span></span>

<span data-ttu-id="d21a1-227">A função de exemplo CreateLink no exemplo a seguir cria um atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-227">The CreateLink sample function in the following example creates a shortcut.</span></span> <span data-ttu-id="d21a1-228">Os parâmetros incluem um ponteiro para o nome do arquivo a ser vinculado, um ponteiro para o nome do atalho que você está criando e um ponteiro para a descrição do link.</span><span class="sxs-lookup"><span data-stu-id="d21a1-228">The parameters include a pointer to the name of the file to link to, a pointer to the name of the shortcut that you are creating, and a pointer to the description of the link.</span></span> <span data-ttu-id="d21a1-229">A descrição consiste na cadeia de caracteres, "atalho para o **nome do arquivo**", em que **nome do arquivo** é o nome do arquivo a ser vinculado.</span><span class="sxs-lookup"><span data-stu-id="d21a1-229">The description consists of the string, "Shortcut to **file name**," where **file name** is the name of the file to link to.</span></span>

<span data-ttu-id="d21a1-230">Para criar um atalho de pasta usando a função de exemplo CreateLink, chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) usando CLSID \_ FolderShortcut, em vez de CLSID \_ ShellLink (CLSID \_ FolderShortcut dá suporte a IShellLink).</span><span class="sxs-lookup"><span data-stu-id="d21a1-230">To create a folder shortcut using the CreateLink sample function, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) using CLSID\_FolderShortcut, instead of CLSID\_ShellLink (CLSID\_FolderShortcut supports IShellLink).</span></span> <span data-ttu-id="d21a1-231">Todos os outros códigos permanecem os mesmos.</span><span class="sxs-lookup"><span data-stu-id="d21a1-231">All other code remains the same.</span></span>

<span data-ttu-id="d21a1-232">Como CreateLink chama a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , supõe-se que a função [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) já foi chamada.</span><span class="sxs-lookup"><span data-stu-id="d21a1-232">Because CreateLink calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, it is assumed that the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function has already been called.</span></span> <span data-ttu-id="d21a1-233">CreateLink usa a interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) para salvar o atalho e a interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para armazenar o nome e a descrição do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d21a1-233">CreateLink uses the [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface to save the shortcut and the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface to store the file name and description.</span></span>


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a><span data-ttu-id="d21a1-234">Resolvendo um atalho</span><span class="sxs-lookup"><span data-stu-id="d21a1-234">Resolving a Shortcut</span></span>

<span data-ttu-id="d21a1-235">Um aplicativo pode precisar acessar e manipular um atalho criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d21a1-235">An application may need to access and manipulate a shortcut that was previously created.</span></span> <span data-ttu-id="d21a1-236">Essa operação é conhecida como resolver o atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-236">This operation is referred to as resolving the shortcut.</span></span>

<span data-ttu-id="d21a1-237">A função ResolveIt definida pelo aplicativo no exemplo a seguir resolve um atalho.</span><span class="sxs-lookup"><span data-stu-id="d21a1-237">The application-defined ResolveIt function in the following example resolves a shortcut.</span></span> <span data-ttu-id="d21a1-238">Seus parâmetros incluem um identificador de janela, um ponteiro para o caminho do atalho e o endereço de um buffer que recebe o novo caminho para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-238">Its parameters include a window handle, a pointer to the path of the shortcut, and the address of a buffer that receives the new path to the object.</span></span> <span data-ttu-id="d21a1-239">O identificador de janela identifica a janela pai para qualquer caixa de mensagem que o Shell possa precisar exibir.</span><span class="sxs-lookup"><span data-stu-id="d21a1-239">The window handle identifies the parent window for any message boxes that the Shell may need to display.</span></span> <span data-ttu-id="d21a1-240">Por exemplo, o Shell pode exibir uma caixa de mensagem se o link estiver em mídia não compartilhada, se ocorrerem problemas de rede, se o usuário precisar inserir um disquete e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d21a1-240">For example, the Shell can display a message box if the link is on unshared media, if network problems occur, if the user needs to insert a floppy disk, and so on.</span></span>

<span data-ttu-id="d21a1-241">A função ResolveIt chama a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e pressupõe que a função [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) já foi chamada.</span><span class="sxs-lookup"><span data-stu-id="d21a1-241">The ResolveIt function calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and assumes that the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function has already been called.</span></span> <span data-ttu-id="d21a1-242">Observe que o ResolveIt precisa usar a interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) para armazenar as informações de link.</span><span class="sxs-lookup"><span data-stu-id="d21a1-242">Note that ResolveIt needs to use the [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface to store the link information.</span></span> <span data-ttu-id="d21a1-243">**IPersistFile** é implementado pelo objeto [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .</span><span class="sxs-lookup"><span data-stu-id="d21a1-243">**IPersistFile** is implemented by the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) object.</span></span> <span data-ttu-id="d21a1-244">As informações de link devem ser carregadas antes da recuperação das informações de caminho, que são mostradas posteriormente no exemplo.</span><span class="sxs-lookup"><span data-stu-id="d21a1-244">The link information must be loaded before the path information is retrieved, which is shown later in the example.</span></span> <span data-ttu-id="d21a1-245">A falha ao carregar as informações do link faz com que as chamadas para as funções de membro [**IShellLink:: GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) e [**IShellLink:: GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) falhem.</span><span class="sxs-lookup"><span data-stu-id="d21a1-245">Failing to load the link information causes the calls to the [**IShellLink::GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) and [**IShellLink::GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) member functions to fail.</span></span>


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a><span data-ttu-id="d21a1-246">Criando um atalho para um objeto não arquivo</span><span class="sxs-lookup"><span data-stu-id="d21a1-246">Creating a Shortcut to a Nonfile Object</span></span>

<span data-ttu-id="d21a1-247">A criação de um atalho para um objeto não arquivo, como uma impressora, é semelhante à criação de um atalho para um arquivo, exceto que, em vez de definir o caminho para o arquivo, você deve definir a lista de identificadores para a impressora.</span><span class="sxs-lookup"><span data-stu-id="d21a1-247">Creating a shortcut to a nonfile object, such as a printer, is similar to creating a shortcut to a file except that rather than setting the path to the file, you must set the identifier list to the printer.</span></span> <span data-ttu-id="d21a1-248">Para definir a lista de identificadores, chame o método [**IShellLink:: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) , especificando o endereço de uma lista de identificadores.</span><span class="sxs-lookup"><span data-stu-id="d21a1-248">To set the identifier list, call the [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) method, specifying the address of an identifier list.</span></span>

<span data-ttu-id="d21a1-249">Cada objeto dentro do namespace do Shell tem um identificador de item.</span><span class="sxs-lookup"><span data-stu-id="d21a1-249">Each object within the Shell's namespace has an item identifier.</span></span> <span data-ttu-id="d21a1-250">O Shell muitas vezes concatena identificadores de item em listas de terminação nula que consistem em qualquer número de identificadores de item.</span><span class="sxs-lookup"><span data-stu-id="d21a1-250">The Shell often concatenates item identifiers into null-terminated lists consisting of any number of item identifiers.</span></span> <span data-ttu-id="d21a1-251">Para obter mais informações sobre identificadores de item, consulte [identificadores de item e listas de identificadores](#item-identifiers-and-identifier-lists).</span><span class="sxs-lookup"><span data-stu-id="d21a1-251">For more information about item identifiers, see [Item Identifiers and Identifier Lists](#item-identifiers-and-identifier-lists).</span></span>

<span data-ttu-id="d21a1-252">Em geral, se você precisar definir um atalho para um item que não tem um nome de arquivo, como uma impressora, você já terá um ponteiro para a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) do objeto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-252">In general, if you need to set a shortcut to an item that does not have a file name, such as a printer, you will already have a pointer to the object's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="d21a1-253">**IShellFolder** é usado para criar extensões de namespace.</span><span class="sxs-lookup"><span data-stu-id="d21a1-253">**IShellFolder** is used to create namespace extensions.</span></span>

<span data-ttu-id="d21a1-254">Depois de ter o identificador de classe para [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), você pode chamar a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar o endereço da interface.</span><span class="sxs-lookup"><span data-stu-id="d21a1-254">Once you have the class identifier for [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), you can call the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve the address of the interface.</span></span> <span data-ttu-id="d21a1-255">Em seguida, você pode chamar a interface para enumerar os objetos na pasta e recuperar o endereço do identificador de item para o objeto que você está procurando.</span><span class="sxs-lookup"><span data-stu-id="d21a1-255">Then you can call the interface to enumerate the objects in the folder and retrieve the address of the item identifier for the object that you are searching for.</span></span> <span data-ttu-id="d21a1-256">Por fim, você pode usar o endereço em uma chamada para a função de membro [**IShellLink:: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) para criar um atalho para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d21a1-256">Finally, you can use the address in a call to the [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) member function to create a shortcut to the object.</span></span>

 

 

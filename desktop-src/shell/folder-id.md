---
description: Antes de usar um objeto namespace, você precisa de uma maneira de identificá-lo.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Obtendo a ID de uma pasta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2e62454bf27f2c203f59aecb325cefe6537d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988996"
---
# <a name="getting-a-folders-id"></a><span data-ttu-id="16d77-103">Obtendo a ID de uma pasta</span><span class="sxs-lookup"><span data-stu-id="16d77-103">Getting a Folder's ID</span></span>

<span data-ttu-id="16d77-104">Antes de usar um objeto namespace, você precisa de uma maneira de identificá-lo.</span><span class="sxs-lookup"><span data-stu-id="16d77-104">Before you can make use of a namespace object, you need a way to identify it.</span></span> <span data-ttu-id="16d77-105">Isso significa obter o ponteiro para uma lista de identificadores de item (PIDL) ou, no caso de objetos do sistema de arquivos, seu caminho.</span><span class="sxs-lookup"><span data-stu-id="16d77-105">This means obtaining either its pointer to an item identifier list (PIDL) or, in the case of file system objects, its path.</span></span> <span data-ttu-id="16d77-106">Esta seção aborda duas das maneiras mais simples de obter IDs de objeto.</span><span class="sxs-lookup"><span data-stu-id="16d77-106">This section discusses two of the simpler ways to obtain object IDs.</span></span>

<span data-ttu-id="16d77-107">Para obter uma abordagem mais potente que funcionará com qualquer pasta, use a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="16d77-107">For a more powerful approach that will work with any folder, use the [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="16d77-108">Consulte [obtendo informações sobre o conteúdo de uma pasta](folder-info.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="16d77-108">See [Getting Information About the Contents of a Folder](folder-info.md) for more details.</span></span>

-   [<span data-ttu-id="16d77-109">A caixa de diálogo Openfiles</span><span class="sxs-lookup"><span data-stu-id="16d77-109">The OpenFiles Dialog Box</span></span>](#the-openfiles-dialog-box)
-   [<span data-ttu-id="16d77-110">A caixa de diálogo SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="16d77-110">The SHBrowseForFolder Dialog Box</span></span>](#the-shbrowseforfolder-dialog-box)
-   [<span data-ttu-id="16d77-111">Pastas especiais e CSIDLs</span><span class="sxs-lookup"><span data-stu-id="16d77-111">Special Folders and CSIDLs</span></span>](#special-folders-and-csidls)
-   [<span data-ttu-id="16d77-112">Um exemplo simples de como usar CSIDLs e SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="16d77-112">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a><span data-ttu-id="16d77-113">A caixa de diálogo Openfiles</span><span class="sxs-lookup"><span data-stu-id="16d77-113">The OpenFiles Dialog Box</span></span>

<span data-ttu-id="16d77-114">Para permitir que o usuário navegue no namespace e selecione uma pasta, seu aplicativo pode usar a interface [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) .</span><span class="sxs-lookup"><span data-stu-id="16d77-114">To enable the user to navigate the namespace and select a folder, your application can use the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface.</span></span> <span data-ttu-id="16d77-115">Chamar essa interface com o sinalizador **FOS \_ PICKFOLDERS** inicia a caixa de diálogo [abrir arquivos](../dlgbox/open-and-save-as-dialog-boxes.md) comuns no modo "escolher pastas".</span><span class="sxs-lookup"><span data-stu-id="16d77-115">Calling this interface with the **FOS\_PICKFOLDERS** flag launches the [Open Files](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box in "pick folders" mode.</span></span>

<span data-ttu-id="16d77-116">Para o Windows Vista e posterior, essa é a maneira recomendada para escolher pastas.</span><span class="sxs-lookup"><span data-stu-id="16d77-116">For Windows Vista and later, this is the recommended way to pick folders.</span></span>

## <a name="the-shbrowseforfolder-dialog-box"></a><span data-ttu-id="16d77-117">A caixa de diálogo SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="16d77-117">The SHBrowseForFolder Dialog Box</span></span>

<span data-ttu-id="16d77-118">Para permitir que o usuário navegue pelo namespace e selecione uma pasta, seu aplicativo pode simplesmente invocar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="16d77-118">To enable the user to navigate the namespace and select a folder, your application can simply invoke [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="16d77-119">Chamar essa função inicia uma caixa de diálogo com uma interface do usuário que funciona de certa forma com as caixas de diálogo [abrir ou salvar](../dlgbox/open-and-save-as-dialog-boxes.md) em comum.</span><span class="sxs-lookup"><span data-stu-id="16d77-119">Calling this function launches a dialog box with a UI that works somewhat like the [Open or SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog boxes.</span></span>

<span data-ttu-id="16d77-120">Quando o usuário seleciona uma pasta, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) retorna o PIDL totalmente qualificado da pasta e seu nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="16d77-120">When the user selects a folder, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) returns the folder's fully qualified PIDL and its display name.</span></span> <span data-ttu-id="16d77-121">Se a pasta estiver no sistema de arquivos, o aplicativo poderá converter o PIDL em um caminho chamando [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span><span class="sxs-lookup"><span data-stu-id="16d77-121">If the folder is in the file system, the application can convert the PIDL to a path by calling [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span></span> <span data-ttu-id="16d77-122">O aplicativo também pode restringir o intervalo de pastas que o usuário pode selecionar, especificando uma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="16d77-122">The application can also restrict the range of folders that the user can select from by specifying a root folder.</span></span> <span data-ttu-id="16d77-123">Somente as pastas que estão abaixo dessa raiz no namespace serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="16d77-123">Only folders that are below that root in the namespace will appear.</span></span> <span data-ttu-id="16d77-124">A ilustração a seguir mostra a caixa de diálogo **SHBrowseForFolder** , com a pasta raiz definida como arquivos de programas.</span><span class="sxs-lookup"><span data-stu-id="16d77-124">The following illustration shows the **SHBrowseForFolder** dialog box, with the root folder set to Program Files.</span></span>

![captura de tela da caixa de diálogo Procurar pasta](images/shell1.png)

<span data-ttu-id="16d77-126">Um exemplo simples de como usar o [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) é fornecido posteriormente.</span><span class="sxs-lookup"><span data-stu-id="16d77-126">A simple example of how to use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) is provided later.</span></span>

## <a name="special-folders-and-csidls"></a><span data-ttu-id="16d77-127">Pastas especiais e CSIDLs</span><span class="sxs-lookup"><span data-stu-id="16d77-127">Special Folders and CSIDLs</span></span>

<span data-ttu-id="16d77-128">Várias pastas comumente usadas são designadas como *especiais* pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="16d77-128">A number of commonly used folders are designated as *special* by the system.</span></span> <span data-ttu-id="16d77-129">Essas pastas têm uma finalidade bem definida e a maioria delas está presente em todos os sistemas.</span><span class="sxs-lookup"><span data-stu-id="16d77-129">These folders have a well-defined purpose, and most of them are present on all systems.</span></span> <span data-ttu-id="16d77-130">Mesmo que não estejam presentes inicialmente, seus nomes e locais ainda estão definidos, para que possam ser adicionados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="16d77-130">Even if they are not present initially, their names and locations are still defined, so they can be added later.</span></span> <span data-ttu-id="16d77-131">A coleção de pastas especiais inclui todas as pastas virtuais padrão do sistema, como impressoras, meus documentos e ambiente de rede.</span><span class="sxs-lookup"><span data-stu-id="16d77-131">The collection of special folders includes all of the system's standard virtual folders, such as Printers, My Documents, and Network Neighborhood.</span></span> <span data-ttu-id="16d77-132">Ele também inclui várias pastas padrão do sistema de arquivos, como arquivos de programas e sistema.</span><span class="sxs-lookup"><span data-stu-id="16d77-132">It also includes a number of standard file system folders, such as Program Files and System.</span></span>

<span data-ttu-id="16d77-133">Embora as pastas sejam um componente padrão de todos os sistemas, seus nomes e locais no namespace podem variar.</span><span class="sxs-lookup"><span data-stu-id="16d77-133">Even though the folders are a standard component of all systems, their names and locations in the namespace can vary.</span></span> <span data-ttu-id="16d77-134">Por exemplo, o diretório do sistema é C: \\ WinNT \\ System32 em alguns sistemas e C: \\ Windows \\ System32 em outros.</span><span class="sxs-lookup"><span data-stu-id="16d77-134">For example, the System directory is C:\\Winnt\\System32 on some systems and C:\\Windows\\System32 on others.</span></span> <span data-ttu-id="16d77-135">No passado, as variáveis de ambiente forneciam uma maneira de determinar o nome e o local de uma pasta especial em qualquer sistema específico.</span><span class="sxs-lookup"><span data-stu-id="16d77-135">In the past, environment variables provided a way to determine the name and location of a special folder on any particular system.</span></span> <span data-ttu-id="16d77-136">O Shell agora fornece uma maneira mais robusta e flexível de identificar pastas especiais, [**CSIDLs**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="16d77-136">The Shell now provides a more robust and flexible way to identify special folders, [**CSIDLs**](csidl.md).</span></span> <span data-ttu-id="16d77-137">Geralmente, você deve usá-los em vez de variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="16d77-137">You should generally use them instead of environment variables.</span></span>

<span data-ttu-id="16d77-138">O CSIDLs fornece uma maneira uniforme de identificar e localizar pastas especiais, independentemente de seu nome ou local em um sistema específico.</span><span class="sxs-lookup"><span data-stu-id="16d77-138">CSIDLs provide a uniform way of identifying and locating special folders, regardless of their name or location on a particular system.</span></span> <span data-ttu-id="16d77-139">Ao contrário das variáveis de ambiente, CSIDLs pode ser usado com pastas virtuais, bem como pastas do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="16d77-139">Unlike environment variables, CSIDLs can be used with virtual folders as well as file system folders.</span></span> <span data-ttu-id="16d77-140">Cada pasta especial tem um CSID exclusivo atribuído a ela.</span><span class="sxs-lookup"><span data-stu-id="16d77-140">Each special folder has a unique CSIDL assigned to it.</span></span> <span data-ttu-id="16d77-141">Por exemplo, a pasta sistema de arquivos de arquivos de programas tem um CSIDl de **\_ \_ arquivos de programa CSIDL** e a pasta virtual de ambiente de rede tem uma CSIDL de **\_ rede CSIDL**.</span><span class="sxs-lookup"><span data-stu-id="16d77-141">For example, the Program Files file system folder has a CSIDL of **CSIDL\_PROGRAM\_FILES**, and the Network Neighborhood virtual folder has a CSIDL of **CSIDL\_NETWORK**.</span></span>

<span data-ttu-id="16d77-142">Uma CSIDl é usada em conjunto com uma das várias funções de Shell para recuperar o PIDL de uma pasta especial ou um caminho de pasta do sistema de arquivos especial.</span><span class="sxs-lookup"><span data-stu-id="16d77-142">A CSIDL is used in conjunction with one of several Shell functions to retrieve a special folder's PIDL, or a special file system folder's path.</span></span> <span data-ttu-id="16d77-143">Se a pasta não existir em um sistema, seu aplicativo poderá forçá-la a ser criada combinando seu CSIDl com o **sinalizador CSIDL \_ \_ criar**.</span><span class="sxs-lookup"><span data-stu-id="16d77-143">If the folder does not exist on a system, your application can force it to be created by combining its CSIDL with **CSIDL\_FLAG\_CREATE**.</span></span> <span data-ttu-id="16d77-144">O CSIDl pode ser passado para as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="16d77-144">The CSIDL can be passed to the following functions:</span></span>

-   <span data-ttu-id="16d77-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), que recupera o PIDL de uma pasta especial.</span><span class="sxs-lookup"><span data-stu-id="16d77-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), which retrieves the PIDL of a special folder.</span></span>
-   <span data-ttu-id="16d77-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), que recupera o caminho de uma pasta especial do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="16d77-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), which retrieves the path of a file system special folder.</span></span>

<span data-ttu-id="16d77-147">Observe que essas duas funções foram introduzidas com a versão 5,0 do Shell e substituem as funções [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) e [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) .</span><span class="sxs-lookup"><span data-stu-id="16d77-147">Note that these two functions were introduced with version 5.0 of the Shell and supersede the [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) and [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) functions.</span></span>

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a><span data-ttu-id="16d77-148">Um exemplo simples de como usar CSIDLs e SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="16d77-148">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>

<span data-ttu-id="16d77-149">A seguinte função de exemplo, PidlBrowse, ilustra como usar CSIDLs para recuperar a PIDL de uma pasta e usar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) para que o usuário selecione uma pasta.</span><span class="sxs-lookup"><span data-stu-id="16d77-149">The following sample function, PidlBrowse, illustrates how to use CSIDLs to retrieve a folder's PIDL, and use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) to have the user select a folder.</span></span> <span data-ttu-id="16d77-150">Ele retorna o PIDL e o nome de exibição da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="16d77-150">It returns the PIDL and display name of the selected folder.</span></span>


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



<span data-ttu-id="16d77-151">O aplicativo de chamada passa em um identificador de janela, que é necessário para o [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="16d77-151">The calling application passes in a window handle, which is needed by [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="16d77-152">O parâmetro *nCSIDL* é um CSIDL opcional que é usado para especificar uma pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="16d77-152">The *nCSIDL* parameter is an optional CSIDL that is used to specify a root folder.</span></span> <span data-ttu-id="16d77-153">Somente as pastas abaixo da pasta raiz na hierarquia serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="16d77-153">Only folders below the root folder in the hierarchy will be displayed.</span></span> <span data-ttu-id="16d77-154">A ilustração mostrada anteriormente foi gerada chamando essa função com *nCSIDL* definido como **arquivos de \_ programa \_ CSIDL**.</span><span class="sxs-lookup"><span data-stu-id="16d77-154">The illustration shown earlier was generated by calling this function with *nCSIDL* set to **CSIDL\_PROGRAM\_FILES**.</span></span> <span data-ttu-id="16d77-155">O aplicativo de chamada também passa um buffer de cadeia de caracteres, *pszDisplayName*, para manter o nome de exibição da pasta selecionada quando PidlBrowse retorna.</span><span class="sxs-lookup"><span data-stu-id="16d77-155">The calling application also passes in a string buffer, *pszDisplayName*, to hold the display name of the selected folder when PidlBrowse returns.</span></span> <span data-ttu-id="16d77-156">É responsabilidade do aplicativo de chamada liberar o IDList retornado pelo **SHBrowseForFolder** usando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="16d77-156">It is the responsibility of the calling application to free the IDList returned by **SHBrowseForFolder** using [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

 

 

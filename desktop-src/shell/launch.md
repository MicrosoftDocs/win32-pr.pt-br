---
description: Depois que o aplicativo tiver localizado um objeto File, a próxima etapa costuma agir de alguma forma.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Iniciando aplicativos (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827893"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="b7e07-103">Iniciando aplicativos (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span><span class="sxs-lookup"><span data-stu-id="b7e07-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="b7e07-104">Depois que o aplicativo tiver localizado um objeto File, a próxima etapa costuma agir de alguma forma.</span><span class="sxs-lookup"><span data-stu-id="b7e07-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="b7e07-105">Por exemplo, seu aplicativo pode querer iniciar outro aplicativo que permite ao usuário modificar um arquivo de dados.</span><span class="sxs-lookup"><span data-stu-id="b7e07-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="b7e07-106">Se o arquivo de interesse for um executável, seu aplicativo talvez queira simplesmente iniciá-lo.</span><span class="sxs-lookup"><span data-stu-id="b7e07-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="b7e07-107">Este documento discute como usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para executar essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="b7e07-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="b7e07-108">Usando ShellExecute e ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="b7e07-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="b7e07-109">Verbos de objeto</span><span class="sxs-lookup"><span data-stu-id="b7e07-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="b7e07-110">Usando o ShellExecuteEx para fornecer serviços de ativação de um site</span><span class="sxs-lookup"><span data-stu-id="b7e07-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="b7e07-111">Usando ShellExecute para iniciar a caixa de diálogo de pesquisa</span><span class="sxs-lookup"><span data-stu-id="b7e07-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="b7e07-112">Um exemplo simples de como usar ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="b7e07-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="b7e07-113">Usando ShellExecute e ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="b7e07-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="b7e07-114">Para usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), seu aplicativo deve especificar o objeto de arquivo ou pasta a ser acionado e um *verbo* que especifica a operação.</span><span class="sxs-lookup"><span data-stu-id="b7e07-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="b7e07-115">Para **ShellExecute**, atribua esses valores aos parâmetros apropriados.</span><span class="sxs-lookup"><span data-stu-id="b7e07-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="b7e07-116">Para **ShellExecuteEx**, preencha os membros apropriados de uma estrutura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b7e07-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="b7e07-117">Também há vários outros membros ou parâmetros que podem ser usados para ajustar o comportamento das duas funções.</span><span class="sxs-lookup"><span data-stu-id="b7e07-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="b7e07-118">Os objetos de arquivo e pasta podem fazer parte do sistema de arquivos ou de objetos virtuais, e podem ser identificados por caminhos ou ponteiros para listas de identificadores de item (PIDLs).</span><span class="sxs-lookup"><span data-stu-id="b7e07-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="b7e07-119">Verbos de objeto</span><span class="sxs-lookup"><span data-stu-id="b7e07-119">Object Verbs</span></span>

<span data-ttu-id="b7e07-120">Os verbos disponíveis para um objeto são essencialmente os itens encontrados no menu de atalho de um objeto.</span><span class="sxs-lookup"><span data-stu-id="b7e07-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="b7e07-121">Para descobrir quais verbos estão disponíveis, procure no registro em</span><span class="sxs-lookup"><span data-stu-id="b7e07-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="b7e07-122">**HKEY \_ \_** \\ Verbo de shell do CLSID raiz \\ *{Object \_ CLSID}* de \\  \\  classes</span><span class="sxs-lookup"><span data-stu-id="b7e07-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="b7e07-123">em *que \_ CLSID do objeto* é o identificador de classe (CLSID) do objeto, e *verbo* é o nome do verbo disponível.</span><span class="sxs-lookup"><span data-stu-id="b7e07-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="b7e07-124">A  \\ subchave de **comando** Verb contém os dados indicando o que acontece quando esse verbo é invocado.</span><span class="sxs-lookup"><span data-stu-id="b7e07-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="b7e07-125">Para descobrir quais verbos estão disponíveis para objetos de [shell predefinidos](handlers.md), procure no registro em</span><span class="sxs-lookup"><span data-stu-id="b7e07-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="b7e07-126">**HKEY \_ \_** \\ *\_* Verbo de \\ **shell** \\  de nome de objeto raiz de classes</span><span class="sxs-lookup"><span data-stu-id="b7e07-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="b7e07-127">em *que \_ nome do objeto* é o nome do objeto de shell predefinido.</span><span class="sxs-lookup"><span data-stu-id="b7e07-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="b7e07-128">Novamente, a  \\ subchave de **comando** Verb contém os dados indicando o que acontece quando esse verbo é invocado.</span><span class="sxs-lookup"><span data-stu-id="b7e07-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="b7e07-129">Os verbos normalmente disponíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="b7e07-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="b7e07-130">Verbo</span><span class="sxs-lookup"><span data-stu-id="b7e07-130">Verb</span></span>       | <span data-ttu-id="b7e07-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7e07-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e07-132">editar</span><span class="sxs-lookup"><span data-stu-id="b7e07-132">edit</span></span>       | <span data-ttu-id="b7e07-133">Inicia um editor e abre o documento para edição.</span><span class="sxs-lookup"><span data-stu-id="b7e07-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="b7e07-134">localizar</span><span class="sxs-lookup"><span data-stu-id="b7e07-134">find</span></span>       | <span data-ttu-id="b7e07-135">Inicia uma pesquisa a partir do diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="b7e07-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="b7e07-136">Abrir</span><span class="sxs-lookup"><span data-stu-id="b7e07-136">open</span></span>       | <span data-ttu-id="b7e07-137">Inicia um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7e07-137">Launches an application.</span></span> <span data-ttu-id="b7e07-138">Se esse arquivo não for um arquivo executável, seu aplicativo associado será iniciado.</span><span class="sxs-lookup"><span data-stu-id="b7e07-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="b7e07-139">print</span><span class="sxs-lookup"><span data-stu-id="b7e07-139">print</span></span>      | <span data-ttu-id="b7e07-140">Imprime o arquivo de documento.</span><span class="sxs-lookup"><span data-stu-id="b7e07-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="b7e07-141">properties</span><span class="sxs-lookup"><span data-stu-id="b7e07-141">properties</span></span> | <span data-ttu-id="b7e07-142">Exibe as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="b7e07-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="b7e07-143">runas</span><span class="sxs-lookup"><span data-stu-id="b7e07-143">runas</span></span>      | <span data-ttu-id="b7e07-144">Inicia um aplicativo como administrador.</span><span class="sxs-lookup"><span data-stu-id="b7e07-144">Launches an application as Administrator.</span></span> <span data-ttu-id="b7e07-145">O UAC (controle de conta de usuário) solicitará o consentimento do usuário para</span><span class="sxs-lookup"><span data-stu-id="b7e07-145">User Account Control (UAC) will prompt the user for consent to</span></span> |
|            | <span data-ttu-id="b7e07-146">Execute o aplicativo com privilégios elevados ou insira as credenciais de uma conta de administrador usada para executar o</span><span class="sxs-lookup"><span data-stu-id="b7e07-146">run the application elevated or enter the credentials of an administrator account used to run the</span></span>        |
|            | <span data-ttu-id="b7e07-147">.</span><span class="sxs-lookup"><span data-stu-id="b7e07-147">application.</span></span>                                                                                             |

 

<span data-ttu-id="b7e07-148">Cada verbo corresponde ao comando que seria usado para iniciar o aplicativo a partir de uma janela de console.</span><span class="sxs-lookup"><span data-stu-id="b7e07-148">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="b7e07-149">O verbo **Open** é um bom exemplo, pois ele é comumente suportado.</span><span class="sxs-lookup"><span data-stu-id="b7e07-149">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="b7e07-150">Para arquivos. exe, **abrir** simplesmente inicia o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7e07-150">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="b7e07-151">No entanto, ele é mais comumente usado para iniciar um aplicativo que opera em um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="b7e07-151">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="b7e07-152">Por exemplo, os arquivos. txt podem ser abertos pelo Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="b7e07-152">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="b7e07-153">O verbo **Open** para um arquivo. txt, portanto, corresponderia a algo como o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b7e07-153">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="b7e07-154">Quando você usa [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para abrir um arquivo. txt, Wordpad.exe é iniciado com o arquivo especificado como seu argumento.</span><span class="sxs-lookup"><span data-stu-id="b7e07-154">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="b7e07-155">Alguns comandos podem ter argumentos adicionais, como sinalizadores, que podem ser adicionados conforme necessário para iniciar o aplicativo corretamente.</span><span class="sxs-lookup"><span data-stu-id="b7e07-155">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="b7e07-156">Para obter mais informações sobre menus de atalho e verbos, consulte [estendendo menus de atalho](context.md).</span><span class="sxs-lookup"><span data-stu-id="b7e07-156">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="b7e07-157">Em geral, a tentativa de determinar a lista de verbos disponíveis para um arquivo específico é um pouco complicada.</span><span class="sxs-lookup"><span data-stu-id="b7e07-157">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="b7e07-158">Em muitos casos, você pode simplesmente definir o parâmetro *lpVerb* como **NULL**, que invoca o comando padrão para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b7e07-158">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="b7e07-159">Esse procedimento geralmente é equivalente a definir *lpVerb* como "Open", mas alguns tipos de arquivo podem ter um comando padrão diferente.</span><span class="sxs-lookup"><span data-stu-id="b7e07-159">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="b7e07-160">Para obter mais informações, consulte [estendendo menus de atalho](context.md) e a documentação de referência do [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="b7e07-160">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="b7e07-161">Usando o ShellExecuteEx para fornecer serviços de ativação de um site</span><span class="sxs-lookup"><span data-stu-id="b7e07-161">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="b7e07-162">Os serviços de uma cadeia de sites podem controlar vários comportamentos de ativação de itens.</span><span class="sxs-lookup"><span data-stu-id="b7e07-162">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="b7e07-163">A partir do Windows 8, você pode fornecer um ponteiro para a cadeia de site para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para habilitar esses comportamentos.</span><span class="sxs-lookup"><span data-stu-id="b7e07-163">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="b7e07-164">Para fornecer ao site **ShellExecuteEx**:</span><span class="sxs-lookup"><span data-stu-id="b7e07-164">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="b7e07-165">Especifique o sinalizador \_ de \_ máscara \_ hinst \_ is \_ site no membro **fMask** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="b7e07-165">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="b7e07-166">Forneça o [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) no membro **hInstApp** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="b7e07-166">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="b7e07-167">Usando ShellExecute para iniciar a caixa de diálogo de pesquisa</span><span class="sxs-lookup"><span data-stu-id="b7e07-167">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="b7e07-168">Quando um usuário clica com o botão direito do mouse em um ícone de pasta no Windows Explorer, um dos itens de menu é "pesquisa".</span><span class="sxs-lookup"><span data-stu-id="b7e07-168">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="b7e07-169">Se eles selecionarem esse item, o Shell iniciará seu utilitário de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b7e07-169">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="b7e07-170">Esse utilitário exibe uma caixa de diálogo que pode ser usada para pesquisar arquivos em busca de uma cadeia de texto especificada.</span><span class="sxs-lookup"><span data-stu-id="b7e07-170">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="b7e07-171">Um aplicativo pode iniciar programaticamente o utilitário de pesquisa para um diretório chamando [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), com "Find" como o parâmetro *lpVerb* e o caminho do diretório como o parâmetro *lpFile* .</span><span class="sxs-lookup"><span data-stu-id="b7e07-171">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="b7e07-172">Por exemplo, a linha de código a seguir inicia o utilitário de pesquisa para o \\ diretório c: Myprograms.</span><span class="sxs-lookup"><span data-stu-id="b7e07-172">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="b7e07-173">Um exemplo simples de como usar ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="b7e07-173">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="b7e07-174">O exemplo de aplicativo de console a seguir ilustra o uso de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="b7e07-174">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="b7e07-175">A maioria dos códigos de verificação de erros foi omitida para fins de clareza.</span><span class="sxs-lookup"><span data-stu-id="b7e07-175">Most error checking code has been omitted for clarity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



<span data-ttu-id="b7e07-176">O aplicativo primeiro recupera o PIDL do diretório do Windows e enumera seu conteúdo até encontrar o primeiro arquivo. bmp.</span><span class="sxs-lookup"><span data-stu-id="b7e07-176">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="b7e07-177">Ao contrário do exemplo anterior, [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) é usado para recuperar o nome de análise do arquivo em vez de seu nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="b7e07-177">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="b7e07-178">Como essa é uma pasta do sistema de arquivos, o nome de análise é um caminho totalmente qualificado, que é o que é necessário para o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="b7e07-178">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="b7e07-179">Depois que o primeiro arquivo. bmp tiver sido localizado, os valores apropriados serão atribuídos aos membros de uma estrutura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b7e07-179">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="b7e07-180">O membro **lpFile** é definido como o nome de análise do arquivo e o membro **lpVerb** como **NULL**, para iniciar a operação padrão.</span><span class="sxs-lookup"><span data-stu-id="b7e07-180">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="b7e07-181">Nesse caso, a operação padrão é "abrir".</span><span class="sxs-lookup"><span data-stu-id="b7e07-181">In this case, the default operation is "open".</span></span> <span data-ttu-id="b7e07-182">Em seguida, a estrutura é passada para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), que inicia o manipulador padrão para arquivos de bitmap, normalmente MSPaint.exe, para abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="b7e07-182">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="b7e07-183">Depois que a função retorna, as PIDLs são liberadas e a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) da pasta do Windows é liberada.</span><span class="sxs-lookup"><span data-stu-id="b7e07-183">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 

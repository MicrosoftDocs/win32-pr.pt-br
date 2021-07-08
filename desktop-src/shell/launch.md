---
description: Depois que o aplicativo tiver localizado um objeto de arquivo, a próxima etapa geralmente será agir sobre ele de alguma forma.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Iniciando aplicativos (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508607"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="827c2-103">Iniciando aplicativos (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span><span class="sxs-lookup"><span data-stu-id="827c2-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="827c2-104">Depois que o aplicativo tiver localizado um objeto de arquivo, a próxima etapa geralmente será agir sobre ele de alguma forma.</span><span class="sxs-lookup"><span data-stu-id="827c2-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="827c2-105">Por exemplo, seu aplicativo pode querer iniciar outro aplicativo que permita que o usuário modifique um arquivo de dados.</span><span class="sxs-lookup"><span data-stu-id="827c2-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="827c2-106">Se o arquivo de interesse for um executável, o aplicativo talvez queira simplesmente inocioná-lo.</span><span class="sxs-lookup"><span data-stu-id="827c2-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="827c2-107">Este documento discute como usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx para**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) executar essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="827c2-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="827c2-108">Usando ShellExecute e ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="827c2-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="827c2-109">Verbos de objeto</span><span class="sxs-lookup"><span data-stu-id="827c2-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="827c2-110">Usando ShellExecuteEx para fornecer serviços de ativação de um site</span><span class="sxs-lookup"><span data-stu-id="827c2-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="827c2-111">Usando ShellExecute para iniciar a caixa de diálogo de pesquisa</span><span class="sxs-lookup"><span data-stu-id="827c2-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="827c2-112">Um exemplo simples de como usar ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="827c2-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="827c2-113">Usando ShellExecute e ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="827c2-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="827c2-114">Para usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), seu aplicativo deve especificar o objeto de arquivo ou pasta que deve ser agido e um *verbo* que especifica a operação.</span><span class="sxs-lookup"><span data-stu-id="827c2-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="827c2-115">Para **ShellExecute**, atribua esses valores aos parâmetros apropriados.</span><span class="sxs-lookup"><span data-stu-id="827c2-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="827c2-116">Para **ShellExecuteEx**, preencha os membros apropriados de uma [**estrutura SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)</span><span class="sxs-lookup"><span data-stu-id="827c2-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="827c2-117">Também há vários outros membros ou parâmetros que podem ser usados para ajustar o comportamento das duas funções.</span><span class="sxs-lookup"><span data-stu-id="827c2-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="827c2-118">Objetos de arquivo e pasta podem fazer parte do sistema de arquivos ou objetos virtuais e podem ser identificados por caminhos ou ponteiros para PIDLs (listas de identificadores de item).</span><span class="sxs-lookup"><span data-stu-id="827c2-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="827c2-119">Verbos de objeto</span><span class="sxs-lookup"><span data-stu-id="827c2-119">Object Verbs</span></span>

<span data-ttu-id="827c2-120">Os verbos disponíveis para um objeto são essencialmente os itens que você encontra no menu de atalho de um objeto.</span><span class="sxs-lookup"><span data-stu-id="827c2-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="827c2-121">Para descobrir quais verbos estão disponíveis, procure no Registro em</span><span class="sxs-lookup"><span data-stu-id="827c2-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="827c2-122">**HKEY \_ CLASSES \_ ROOT** \\ **CLSID** \\ *{object \_ clsid}* \\ **Shell** \\ *verb*</span><span class="sxs-lookup"><span data-stu-id="827c2-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="827c2-123">em *que \_ object clsid* é o CLSID (identificador de classe) do objeto e *verb* é o nome do verbo disponível.</span><span class="sxs-lookup"><span data-stu-id="827c2-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="827c2-124">A  \\ **sub-chave do** comando verbo contém os dados que indicam o que acontece quando esse verbo é invocado.</span><span class="sxs-lookup"><span data-stu-id="827c2-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="827c2-125">Para descobrir quais verbos estão disponíveis para [objetos shell predefinidos,](handlers.md)procure no Registro em</span><span class="sxs-lookup"><span data-stu-id="827c2-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="827c2-126">**HKEY \_ Verbo \_ do** \\ shell *do nome do \_ objeto* CLASSES \\  \\  ROOT</span><span class="sxs-lookup"><span data-stu-id="827c2-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="827c2-127">em *que \_ nome do* objeto é o nome do objeto Shell predefinido.</span><span class="sxs-lookup"><span data-stu-id="827c2-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="827c2-128">Novamente, *a* \\ sub-chave **de comando** do verbo contém os dados que indicam o que acontece quando esse verbo é invocado.</span><span class="sxs-lookup"><span data-stu-id="827c2-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="827c2-129">Os verbos normalmente disponíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="827c2-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="827c2-130">Verbo</span><span class="sxs-lookup"><span data-stu-id="827c2-130">Verb</span></span>       | <span data-ttu-id="827c2-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="827c2-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="827c2-132">editar</span><span class="sxs-lookup"><span data-stu-id="827c2-132">edit</span></span>       | <span data-ttu-id="827c2-133">Inicia um editor e abre o documento para edição.</span><span class="sxs-lookup"><span data-stu-id="827c2-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="827c2-134">localizar</span><span class="sxs-lookup"><span data-stu-id="827c2-134">find</span></span>       | <span data-ttu-id="827c2-135">Inicia uma pesquisa começando no diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="827c2-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="827c2-136">Abrir</span><span class="sxs-lookup"><span data-stu-id="827c2-136">open</span></span>       | <span data-ttu-id="827c2-137">Inicia um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="827c2-137">Launches an application.</span></span> <span data-ttu-id="827c2-138">Se esse arquivo não for um arquivo executável, seu aplicativo associado será lançado.</span><span class="sxs-lookup"><span data-stu-id="827c2-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="827c2-139">print</span><span class="sxs-lookup"><span data-stu-id="827c2-139">print</span></span>      | <span data-ttu-id="827c2-140">Imprime o arquivo de documento.</span><span class="sxs-lookup"><span data-stu-id="827c2-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="827c2-141">properties</span><span class="sxs-lookup"><span data-stu-id="827c2-141">properties</span></span> | <span data-ttu-id="827c2-142">Exibe as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="827c2-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="827c2-143">runas</span><span class="sxs-lookup"><span data-stu-id="827c2-143">runas</span></span>      | <span data-ttu-id="827c2-144">Inicia um aplicativo como Administrador.</span><span class="sxs-lookup"><span data-stu-id="827c2-144">Launches an application as Administrator.</span></span> <span data-ttu-id="827c2-145">O UAC (Controle de Conta de Usuário) solicitará ao usuário o consentimento para executar o aplicativo com privilégios elevados ou inserirá as credenciais de uma conta de administrador usada para executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="827c2-145">User Account Control (UAC) will prompt the user for consent to run the application elevated or enter the credentials of an administrator account used to run the application.</span></span> |



<span data-ttu-id="827c2-146">Cada verbo corresponde ao comando que seria usado para iniciar o aplicativo de uma janela do console.</span><span class="sxs-lookup"><span data-stu-id="827c2-146">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="827c2-147">O **verbo** aberto é um bom exemplo, pois é comumente suportado.</span><span class="sxs-lookup"><span data-stu-id="827c2-147">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="827c2-148">Para .exe arquivos, **abrir** simplesmente inicia o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="827c2-148">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="827c2-149">No entanto, ele é mais comumente usado para iniciar um aplicativo que opera em um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="827c2-149">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="827c2-150">Por exemplo, .txt arquivos podem ser abertos pelo Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="827c2-150">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="827c2-151">O **verbo** aberto para um .txt arquivo corresponderia, portanto, a algo como o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="827c2-151">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="827c2-152">Quando você usa [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para abrir um arquivo .txt, Wordpad.exe é lançado com o arquivo especificado como seu argumento.</span><span class="sxs-lookup"><span data-stu-id="827c2-152">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="827c2-153">Alguns comandos podem ter argumentos adicionais, como sinalizadores, que podem ser adicionados conforme necessário para iniciar o aplicativo corretamente.</span><span class="sxs-lookup"><span data-stu-id="827c2-153">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="827c2-154">Para mais discussão sobre menus de atalho e verbos, consulte [Estendendo menus de atalho.](context.md)</span><span class="sxs-lookup"><span data-stu-id="827c2-154">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="827c2-155">Em geral, tentar determinar a lista de verbos disponíveis para um arquivo específico é um pouco complicado.</span><span class="sxs-lookup"><span data-stu-id="827c2-155">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="827c2-156">Em muitos casos, você pode simplesmente definir o *parâmetro lpVerb* como **NULL,** que invoca o comando padrão para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="827c2-156">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="827c2-157">Esse procedimento geralmente é equivalente à configuração *de lpVerb* como "open", mas alguns tipos de arquivo podem ter um comando padrão diferente.</span><span class="sxs-lookup"><span data-stu-id="827c2-157">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="827c2-158">Para obter mais informações, consulte [Estendendo menus de atalho e](context.md) a documentação de referência [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)</span><span class="sxs-lookup"><span data-stu-id="827c2-158">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="827c2-159">Usando ShellExecuteEx para fornecer serviços de ativação de um site</span><span class="sxs-lookup"><span data-stu-id="827c2-159">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="827c2-160">Os serviços de uma cadeia de sites podem controlar muitos comportamentos de ativação de item.</span><span class="sxs-lookup"><span data-stu-id="827c2-160">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="827c2-161">A partir Windows 8, você pode fornecer um ponteiro para a cadeia de sites para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para habilitar esses comportamentos.</span><span class="sxs-lookup"><span data-stu-id="827c2-161">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="827c2-162">Para fornecer o site ao **ShellExecuteEx:**</span><span class="sxs-lookup"><span data-stu-id="827c2-162">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="827c2-163">Especifique \_ o sinalizador SEE MASK FLAG \_ \_ \_ HINST IS SITE no membro \_ **fMask** de [**SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)</span><span class="sxs-lookup"><span data-stu-id="827c2-163">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="827c2-164">Forneça [**o IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) no membro **hInstApp** de [**SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)</span><span class="sxs-lookup"><span data-stu-id="827c2-164">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="827c2-165">Usando ShellExecute para iniciar a caixa de diálogo de pesquisa</span><span class="sxs-lookup"><span data-stu-id="827c2-165">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="827c2-166">Quando um usuário clica com o botão direito do mouse em um ícone de pasta Windows Explorer, um dos itens de menu é "Pesquisar".</span><span class="sxs-lookup"><span data-stu-id="827c2-166">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="827c2-167">Se eles selecionarem esse item, o Shell iniciará seu utilitário Search.</span><span class="sxs-lookup"><span data-stu-id="827c2-167">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="827c2-168">Esse utilitário exibe uma caixa de diálogo que pode ser usada para pesquisar arquivos para uma cadeia de caracteres de texto especificada.</span><span class="sxs-lookup"><span data-stu-id="827c2-168">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="827c2-169">Um aplicativo pode iniciar programaticamente o utilitário Search para um diretório chamando [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), com "find" como o parâmetro *lpVerb* e o caminho do diretório como o *parâmetro lpFile.*</span><span class="sxs-lookup"><span data-stu-id="827c2-169">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="827c2-170">Por exemplo, a seguinte linha de código inicia o utilitário Search para o diretório c: \\ MyPrograms.</span><span class="sxs-lookup"><span data-stu-id="827c2-170">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="827c2-171">Um exemplo simples de como usar ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="827c2-171">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="827c2-172">O aplicativo de console de exemplo a seguir ilustra o uso de [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)</span><span class="sxs-lookup"><span data-stu-id="827c2-172">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="827c2-173">A maioria dos códigos de verificação de erro foi omitida para maior clareza.</span><span class="sxs-lookup"><span data-stu-id="827c2-173">Most error checking code has been omitted for clarity.</span></span>


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



<span data-ttu-id="827c2-174">O aplicativo primeiro recupera o PIDL do diretório Windows e enumera seu conteúdo até encontrar o primeiro .bmp arquivo.</span><span class="sxs-lookup"><span data-stu-id="827c2-174">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="827c2-175">Ao contrário do exemplo anterior, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) é usado para recuperar o nome de análise do arquivo em vez de seu nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="827c2-175">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="827c2-176">Como essa é uma pasta do sistema de arquivos, o nome da análise é um caminho totalmente qualificado, que é o que é necessário para [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)</span><span class="sxs-lookup"><span data-stu-id="827c2-176">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="827c2-177">Depois que o .bmp arquivo for localizado, os valores apropriados serão atribuídos aos membros de uma [**estrutura SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)</span><span class="sxs-lookup"><span data-stu-id="827c2-177">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="827c2-178">O **membro lpFile** é definido como o nome de análise do arquivo e o membro **lpVerb** como **NULL** para iniciar a operação padrão.</span><span class="sxs-lookup"><span data-stu-id="827c2-178">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="827c2-179">Nesse caso, a operação padrão é "aberta".</span><span class="sxs-lookup"><span data-stu-id="827c2-179">In this case, the default operation is "open".</span></span> <span data-ttu-id="827c2-180">Em seguida, a estrutura é passada [**para ShellExecuteEx,**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)que inicia o manipulador padrão para arquivos bitmap, normalmente MSPaint.exe, para abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="827c2-180">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="827c2-181">Depois que a função retorna, as PIDLs são liberadas e a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) da pasta Windows é liberada.</span><span class="sxs-lookup"><span data-stu-id="827c2-181">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 

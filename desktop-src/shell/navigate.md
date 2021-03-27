---
description: Agora você tem todos os elementos essenciais necessários para navegar em qualquer lugar no namespace.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Navegando no namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24993369222fb32f9de6c79a0c998b1d7be9f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010606"
---
# <a name="navigating-the-namespace"></a><span data-ttu-id="9a082-103">Navegando no namespace</span><span class="sxs-lookup"><span data-stu-id="9a082-103">Navigating the Namespace</span></span>

<span data-ttu-id="9a082-104">Agora você tem todos os elementos essenciais necessários para navegar em qualquer lugar no namespace.</span><span class="sxs-lookup"><span data-stu-id="9a082-104">You now have all the essential elements needed to navigate anywhere in the namespace.</span></span> <span data-ttu-id="9a082-105">A maneira mais simples de começar é fazer com que seu aplicativo chame [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) para recuperar a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a082-105">The simplest way to start is to have your application call [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) to retrieve the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="9a082-106">Em seguida, para navegar para baixo pelo namespace, seu aplicativo pode seguir estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9a082-106">Then, to navigate downward through the namespace, your application can follow these steps:</span></span>

1.  <span data-ttu-id="9a082-107">Enumere o conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="9a082-107">Enumerate the folder's contents.</span></span>
2.  <span data-ttu-id="9a082-108">Determine quais objetos são subpastas e selecione um.</span><span class="sxs-lookup"><span data-stu-id="9a082-108">Determine which objects are subfolders, and select one.</span></span>
3.  <span data-ttu-id="9a082-109">Associe-se à subpasta para recuperar sua interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="9a082-109">Bind to the subfolder to retrieve its [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span>

<span data-ttu-id="9a082-110">Repita essas etapas sempre que necessário para alcançar o destino.</span><span class="sxs-lookup"><span data-stu-id="9a082-110">Repeat these steps as often as necessary to reach the target.</span></span>

## <a name="a-simple-example-of-namespace-navigation"></a><span data-ttu-id="9a082-111">Um exemplo simples de navegação de namespace</span><span class="sxs-lookup"><span data-stu-id="9a082-111">A Simple Example of Namespace Navigation</span></span>

<span data-ttu-id="9a082-112">A parte de código de exemplo a seguir é um aplicativo de console simples que ilustra vários dos procedimentos discutidos nas seções anteriores.</span><span class="sxs-lookup"><span data-stu-id="9a082-112">The following piece of sample code is a simple console application that illustrates a number of the procedures discussed in the preceding sections.</span></span> <span data-ttu-id="9a082-113">A verificação de erros foi omitida para fins de clareza.</span><span class="sxs-lookup"><span data-stu-id="9a082-113">Error checking has been omitted for clarity.</span></span> <span data-ttu-id="9a082-114">O aplicativo executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="9a082-114">The application performs the following tasks:</span></span>

1.  <span data-ttu-id="9a082-115">Recupera a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) da pasta arquivos de programas ([usando a interface IShellFolder](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="9a082-115">Retrieves the Program Files folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface ([Using the IShellFolder Interface](folder-info.md)).</span></span>
2.  <span data-ttu-id="9a082-116">Enumera o conteúdo da pasta ([enumerando o conteúdo de uma pasta](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="9a082-116">Enumerates the contents of the folder ([Enumerating the Contents of a Folder](folder-info.md)).</span></span>
3.  <span data-ttu-id="9a082-117">Determina todos os nomes de exibição e os imprime ([determinando nomes de exibição e outras propriedades](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="9a082-117">Determines all the display names and prints them ([Determining Display Names and Other Properties](folder-info.md)).</span></span>
4.  <span data-ttu-id="9a082-118">Procura uma subpasta ([obtendo um ponteiro para a interface IShellFolder de uma subpasta](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="9a082-118">Looks for a subfolder ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
5.  <span data-ttu-id="9a082-119">Associa-se à primeira subpasta encontrada ([obtendo um ponteiro para a interface IShellFolder de uma subpasta](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="9a082-119">Binds to the first subfolder it finds ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
6.  <span data-ttu-id="9a082-120">Imprime os nomes de exibição dos objetos na subpasta.</span><span class="sxs-lookup"><span data-stu-id="9a082-120">Prints the display names of the objects in the subfolder.</span></span>


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>

main()
{
    LPITEMIDLIST pidlProgFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfFirstFolder = NULL;
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfProgFiles = NULL;
    LPENUMIDLIST ppenum = NULL;
    ULONG celtFetched;
    HRESULT hr;
    STRRET strDispName;
    TCHAR pszDisplayName[MAX_PATH];
    ULONG uAttr;
   
    CoInitialize( NULL );
    
    hr = SHGetFolderLocation(NULL, CSIDL_PROGRAM_FILES, NULL, 0, &pidlProgFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlProgFiles, NULL, IID_IShellFolder, (LPVOID *) &psfProgFiles);
    psfDeskTop->Release();

    hr = psfProgFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfProgFiles->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
        cout << pszDisplayName << '\n';
        if(!psfFirstFolder)
        {
            uAttr = SFGAO_FOLDER;
            psfProgFiles->GetAttributesOf(1, (LPCITEMIDLIST *) &pidlItems, &uAttr);
            if(uAttr & SFGAO_FOLDER)
            {
                hr = psfProgFiles->BindToObject(pidlItems, NULL, IID_IShellFolder, (LPVOID *) &psfFirstFolder);
            }
        }
        CoTaskMemFree(pidlItems);
    }

    cout << "\n\n";

    ppenum->Release();

    if(psfFirstFolder)
    {
        hr = psfFirstFolder->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

        while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
        {
            psfFirstFolder->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
            StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
            cout << pszDisplayName << '\n';
            CoTaskMemFree(pidlItems);
        }
    }

    ppenum->Release();
    CoTaskMemFree(pidlProgFiles);
    psfProgFiles->Release();
    psfFirstFolder->Release();

    CoUninitialize();
    return 0;
}
```



 

 

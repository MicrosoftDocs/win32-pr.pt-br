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
# <a name="navigating-the-namespace"></a>Navegando no namespace

Agora você tem todos os elementos essenciais necessários para navegar em qualquer lugar no namespace. A maneira mais simples de começar é fazer com que seu aplicativo chame [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) para recuperar a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) da área de trabalho. Em seguida, para navegar para baixo pelo namespace, seu aplicativo pode seguir estas etapas:

1.  Enumere o conteúdo da pasta.
2.  Determine quais objetos são subpastas e selecione um.
3.  Associe-se à subpasta para recuperar sua interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

Repita essas etapas sempre que necessário para alcançar o destino.

## <a name="a-simple-example-of-namespace-navigation"></a>Um exemplo simples de navegação de namespace

A parte de código de exemplo a seguir é um aplicativo de console simples que ilustra vários dos procedimentos discutidos nas seções anteriores. A verificação de erros foi omitida para fins de clareza. O aplicativo executa as seguintes tarefas:

1.  Recupera a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) da pasta arquivos de programas ([usando a interface IShellFolder](folder-info.md)).
2.  Enumera o conteúdo da pasta ([enumerando o conteúdo de uma pasta](folder-info.md)).
3.  Determina todos os nomes de exibição e os imprime ([determinando nomes de exibição e outras propriedades](folder-info.md)).
4.  Procura uma subpasta ([obtendo um ponteiro para a interface IShellFolder de uma subpasta](folder-info.md)).
5.  Associa-se à primeira subpasta encontrada ([obtendo um ponteiro para a interface IShellFolder de uma subpasta](folder-info.md)).
6.  Imprime os nomes de exibição dos objetos na subpasta.


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



 

 

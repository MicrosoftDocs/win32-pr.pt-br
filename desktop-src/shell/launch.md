---
description: Depois que o aplicativo tiver localizado um objeto File, a próxima etapa costuma agir de alguma forma.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Iniciando aplicativos (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b871e3560ce1cb0c38e91d6ea3baa7a9364c16e500be949b734f9b4b195a24e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720214"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Iniciando aplicativos (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)

Depois que o aplicativo tiver localizado um objeto File, a próxima etapa costuma agir de alguma forma. Por exemplo, seu aplicativo pode querer iniciar outro aplicativo que permite ao usuário modificar um arquivo de dados. Se o arquivo de interesse for um executável, seu aplicativo talvez queira simplesmente iniciá-lo. Este documento discute como usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para executar essas tarefas.

-   [Usando ShellExecute e ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Verbos de objeto](#object-verbs)
    -   [Usando o ShellExecuteEx para fornecer serviços de ativação de um site](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Usando ShellExecute para iniciar a caixa de diálogo de pesquisa](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Um exemplo simples de como usar ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Usando ShellExecute e ShellExecuteEx

Para usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), seu aplicativo deve especificar o objeto de arquivo ou pasta a ser acionado e um *verbo* que especifica a operação. Para **ShellExecute**, atribua esses valores aos parâmetros apropriados. Para **ShellExecuteEx**, preencha os membros apropriados de uma estrutura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . Também há vários outros membros ou parâmetros que podem ser usados para ajustar o comportamento das duas funções.

Os objetos de arquivo e pasta podem fazer parte do sistema de arquivos ou de objetos virtuais, e podem ser identificados por caminhos ou ponteiros para listas de identificadores de item (PIDLs).

### <a name="object-verbs"></a>Verbos de objeto

Os verbos disponíveis para um objeto são essencialmente os itens encontrados no menu de atalho de um objeto. Para descobrir quais verbos estão disponíveis, procure no registro em

**HKEY \_ \_** \\ Verbo de shell do CLSID raiz \\ *{Object \_ CLSID}* de \\  \\  classes

em *que \_ CLSID do objeto* é o identificador de classe (CLSID) do objeto, e *verbo* é o nome do verbo disponível. A  \\ subchave de **comando** Verb contém os dados indicando o que acontece quando esse verbo é invocado.

Para descobrir quais verbos estão disponíveis para objetos de [shell predefinidos](handlers.md), procure no registro em

**HKEY \_ \_** \\ *\_* Verbo de \\ **shell** \\  de nome de objeto raiz de classes

em *que \_ nome do objeto* é o nome do objeto de shell predefinido. Novamente, a  \\ subchave de **comando** Verb contém os dados indicando o que acontece quando esse verbo é invocado.

Os verbos normalmente disponíveis incluem:



| Verbo       | Descrição                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| editar       | Inicia um editor e abre o documento para edição.                                                   |
| localizar       | Inicia uma pesquisa a partir do diretório especificado.                                                |
| Abrir       | Inicia um aplicativo. Se esse arquivo não for um arquivo executável, seu aplicativo associado será iniciado. |
| print      | Imprime o arquivo de documento.                                                                                |
| properties | Exibe as propriedades do objeto.                                                                        |
| runas      | Inicia um aplicativo como administrador. O UAC (controle de conta de usuário) solicitará que o usuário tenha consentimento para executar o aplicativo com privilégios elevados ou insira as credenciais de uma conta de administrador usada para executar o aplicativo. |



Cada verbo corresponde ao comando que seria usado para iniciar o aplicativo a partir de uma janela de console. O verbo **Open** é um bom exemplo, pois ele é comumente suportado. Para .exe arquivos, **abrir** simplesmente inicia o aplicativo. No entanto, ele é mais comumente usado para iniciar um aplicativo que opera em um arquivo específico. Por exemplo, .txt arquivos podem ser abertos pelo Microsoft WordPad. O verbo **Open** para um arquivo de .txt, portanto, corresponderia a algo como o seguinte comando:


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



Quando você usa [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para abrir um arquivo de .txt, Wordpad.exe é iniciado com o arquivo especificado como seu argumento. Alguns comandos podem ter argumentos adicionais, como sinalizadores, que podem ser adicionados conforme necessário para iniciar o aplicativo corretamente. Para obter mais informações sobre menus de atalho e verbos, consulte [estendendo menus de atalho](context.md).

Em geral, a tentativa de determinar a lista de verbos disponíveis para um arquivo específico é um pouco complicada. Em muitos casos, você pode simplesmente definir o parâmetro *lpVerb* como **NULL**, que invoca o comando padrão para o tipo de arquivo. Esse procedimento geralmente é equivalente a definir *lpVerb* como "Open", mas alguns tipos de arquivo podem ter um comando padrão diferente. Para obter mais informações, consulte [estendendo menus de atalho](context.md) e a documentação de referência do [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Usando o ShellExecuteEx para fornecer serviços de ativação de um site

Os serviços de uma cadeia de sites podem controlar vários comportamentos de ativação de itens. a partir de Windows 8, você pode fornecer um ponteiro para a cadeia de site para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para habilitar esses comportamentos. Para fornecer ao site **ShellExecuteEx**:

-   Especifique o sinalizador \_ de \_ máscara \_ hinst \_ is \_ site no membro **fMask** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).
-   Forneça o [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) no membro **hInstApp** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Usando ShellExecute para iniciar a caixa de diálogo de pesquisa

quando um usuário clica com o botão direito do mouse em um ícone de pasta no Windows Explorer, um dos itens de menu é "pesquisa". Se eles selecionarem esse item, o Shell iniciará seu utilitário de pesquisa. Esse utilitário exibe uma caixa de diálogo que pode ser usada para pesquisar arquivos em busca de uma cadeia de texto especificada. Um aplicativo pode iniciar programaticamente o utilitário de pesquisa para um diretório chamando [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), com "Find" como o parâmetro *lpVerb* e o caminho do diretório como o parâmetro *lpFile* . Por exemplo, a linha de código a seguir inicia o utilitário de pesquisa para o \\ diretório c: Myprograms.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Um exemplo simples de como usar ShellExecuteEx

O exemplo de aplicativo de console a seguir ilustra o uso de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa). A maioria dos códigos de verificação de erros foi omitida para fins de clareza.


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



o aplicativo primeiro recupera o PIDL do diretório Windows e enumera seu conteúdo até encontrar o primeiro arquivo de .bmp. Ao contrário do exemplo anterior, [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) é usado para recuperar o nome de análise do arquivo em vez de seu nome de exibição. Como essa é uma pasta do sistema de arquivos, o nome de análise é um caminho totalmente qualificado, que é o que é necessário para o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

Depois que o primeiro arquivo de .bmp tiver sido localizado, os valores apropriados serão atribuídos aos membros de uma estrutura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . O membro **lpFile** é definido como o nome de análise do arquivo e o membro **lpVerb** como **NULL**, para iniciar a operação padrão. Nesse caso, a operação padrão é "abrir". Em seguida, a estrutura é passada para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), que inicia o manipulador padrão para arquivos de bitmap, normalmente MSPaint.exe, para abrir o arquivo. depois que a função retorna, as PIDLs são liberadas e a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) da pasta de Windows é liberada.

 

 

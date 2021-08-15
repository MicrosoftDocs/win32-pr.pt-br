---
description: Windows O Explorer é um aplicativo de gerenciamento e navegação de recursos poderoso.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Desenvolvendo com Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d00b513b3ee73c30b100cb4236d2c9fb327e1f9557d12ba86738ee9e910ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460179"
---
# <a name="developing-with-windows-explorer"></a>Desenvolvendo com Windows Explorer

Windows O Explorer é um aplicativo de gerenciamento e navegação de recursos poderoso. Windows O Explorer pode ser acessado como um todo integrado por meio Explorer.exe ou a interface [**IExplorerBrowser.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) Windows O Explorer (Explorer.exe) pode ser gerado como um processo separado usando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ou uma função semelhante.

> [!Note]  
> As opções de linha de comando Explorer.exe estão documentadas no site de Suporte do Microsoft Windows no artigo [Windows Explorer Command-Line Opções .](https://support.microsoft.com/kb/152457)

 

As janelas do Open Explorer podem ser descobertas e programadas usando [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (SHELL CLSIDWindows) e novas instâncias do Windows Explorer podem ser criadas usando \_ [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (Shell CLSIDBrowserWindow). \_

O exemplo de código a seguir demonstra como o modelo de automação Windows Explorer pode ser usado para criar e descobrir janelas do Explorer em execução.


```
#define _WIN32_WINNT 0x0600
#define _WIN32_IE 0x0700
#define _UNICODE

#include <windows.h>
#include <shobjidl.h>
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>
#include <propvarutil.h>
 
#pragma comment(lib, "shlwapi.lib")
#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "shell32.lib")
#pragma comment(lib, "propsys.lib")
 
// Use the Shell Windows object to find all of the explorer and IExplorer 
// windows and close them.
 
void CloseExplorerWindows()
{
    IShellWindows* psw;
    
    if (SUCCEEDED(CoCreateInstance(CLSID_ShellWindows, 
                                   NULL,  
                                   CLSCTX_LOCAL_SERVER, 
                                   IID_PPV_ARGS(&psw))))
    {
        VARIANT v = { VT_I4 };
        if (SUCCEEDED(psw->get_Count(&v.lVal)))
        {
            // Walk backward to make sure that the windows that close
            // do not cause the array to be reordered.
            while (--v.lVal >= 0)
            {
                IDispatch *pdisp;
                
                if (S_OK == psw->Item(v, &pdisp))
                {
                    IWebBrowser2 *pwb;
                    if (SUCCEEDED(pdisp->QueryInterface(IID_PPV_ARGS(&pwb))))
                    {
                        pwb->Quit();
                        pwb->Release();
                    }
                    pdisp->Release();
                }
            }
        }
        psw->Release();
    }
}
 
// Convert an IShellItem or IDataObject into a VARIANT that holds an IDList
// suitable for use with IWebBrowser2::Navigate2.
 
HRESULT InitVariantFromObject(IUnknown *punk, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetIDListFromObject(punk, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}
 
HRESULT ParseItemAsVariant(PCWSTR pszItem, IBindCtx *pbc, VARIANT *pvar)
{
    VariantInit(pvar);
 
    IShellItem *psi;
    HRESULT hr = SHCreateItemFromParsingName(pszItem, NULL, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

HRESULT GetKnownFolderAsVariant(REFKNOWNFOLDERID kfid, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetKnownFolderIDList(kfid, 0, NULL, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}

HRESULT GetShellItemFromCommandLine(REFIID riid, void **ppv)
{
    *ppv = NULL;
    HRESULT hr = E_FAIL;

    int cArgs;
    PWSTR *ppszCmd = CommandLineToArgvW(GetCommandLineW(), &cArgs);
    if (ppszCmd && cArgs > 1)
    {
        WCHAR szSpec[MAX_PATH];
        StringCchCopyW(szSpec, ARRAYSIZE(szSpec), ppszCmd[1]);
        PathUnquoteSpacesW(szSpec);

        hr = szSpec[0] ? S_OK : E_FAIL;   // Protect against empty data
        if (SUCCEEDED(hr))
        {
            hr = SHCreateItemFromParsingName(szSpec, NULL, riid, ppv);
            if (FAILED(hr))
            {
                WCHAR szFolder[MAX_PATH];
                GetCurrentDirectoryW(ARRAYSIZE(szFolder), szFolder);

                hr = PathAppendW(szFolder, szSpec) ? S_OK : E_FAIL;
                if (SUCCEEDED(hr))
                {
                    hr = SHCreateItemFromParsingName(szFolder, NULL, riid, ppv);
                }
            }
        }
    }
    return hr;
}

HRESULT GetShellItemFromCommandLineAsVariant(VARIANT *pvar)
{
    VariantInit(pvar);

    IShellItem *psi;
    HRESULT hr = GetShellItemFromCommandLine(IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

void OpenWindow()
{
    IWebBrowser2 *pwb;
    HRESULT hr = CoCreateInstance(CLSID_ShellBrowserWindow, 
                                  NULL,
                                  CLSCTX_LOCAL_SERVER, 
                                  IID_PPV_ARGS(&pwb));
    if (SUCCEEDED(hr))
    {
        CoAllowSetForegroundWindow(pwb, 0);

        pwb->put_Left(100);
        pwb->put_Top(100);
        pwb->put_Height(600);
        pwb->put_Width(800);
 
        VARIANT varTarget = {0};
        hr = GetShellItemFromCommandLineAsVariant(&varTarget);
        if (FAILED(hr))
        {
            hr = GetKnownFolderAsVariant(FOLDERID_UsersFiles, &varTarget);
        }

        if (SUCCEEDED(hr))
        {
            VARIANT vEmpty = {0};
            hr = pwb->Navigate2(&varTarget, &vEmpty, &vEmpty, &vEmpty, &vEmpty);
            if (SUCCEEDED(hr))
            {
                pwb->put_Visible(VARIANT_TRUE);
            }
            VariantClear(&varTarget);
        }
        pwb->Release();
    }
}

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |  COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CloseExplorerWindows();

        OpenWindow();

        CoUninitialize();
    }
    return 0;
}
```



A Windows de cliente do Windows Explorer pode ser hospedada usando a interface [IExplorerBrowser.](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) O Windows Explorer e os controles de árvore de namespace são componentes padrão do Windows Vista e posterior. Os desenvolvedores podem reutilizar as interfaces como componentes de criação. Um uso comum desses controles é criar exploradores personalizados apropriados para o domínio do problema.

Os controles no Windows Explorer são classificados nas seguintes categorias funcionais:

-   [Controles de navegação](#navigation-controls)
-   [Controles de comando](#command-controls)
-   [Controles de propriedade e visualização](#property-and-preview-controls)
-   [Filtragem e controles de exibição](#filtering-and-view-controls)
-   [Controle Listview](#listview-control)

## <a name="navigation-controls"></a>Controles de navegação

Os controles de navegação ajudam os usuários a determinar o contexto e navegar pelo espaço de domínio lógico associado, chamado de espaço de página. Por exemplo, o espaço de página para Windows Explorer é o namespace shell. Os pagespaces são compostos por zero ou mais páginas.

A tabela a seguir lista e descreve os controles de navegação disponíveis no Windows Explorer no Windows Vista e sistemas operacionais posteriores.



| Controle de navegação               | Descrição                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra de Endereços (controle Breadcrumb) | Exibe o endereço da página atual no espaço de páginas. É possível clicar em botões de navegação para navegar até qualquer ancestral no espaço de páginas. Os usuários também podem digitar URLs e caminhos para navegar. |
| Árvore de Pastas                      | Fornece uma nova versão de um controle de árvore, otimizada para pagespaces grandes.                                                                                                                  |
| Viagem                           | Habilita a navegação relativa por meio de botões no estilo web, como **Voltar e** **Encaminhar.**                                                                                                    |
| Título                            | Exibe o nome e o contexto atuais do explorer.                                                                                                                                            |
| Espaço de página                        | Exibe o branch atual do espaço de página. As páginas podem ser ordenadas por critérios diferentes. Os usuários podem clicar em uma página para navegar até ela.                                                        |



 

## <a name="command-controls"></a>Controles de comando

Os controles de comando anunciam os recursos e a funcionalidade do Windows Explorer para os usuários. Esses controles executam ações gerais ou ações específicas para um item ou itens selecionados.



| Controle de comando | Descrição                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra de ferramentas         | Exibe botões para comandos comumente usados (uma nova versão de uma barra de ferramentas de comando). As opções de personalização incluem botões de lista listada, botões de divisão, texto descritivo opcional e uma área de estouro. |
| Hero            | Aparece como um controle personalizado único e opcional no centro da barra de ferramentas. Ele representa o comando primário para o contexto atual.                                                             |
| Barra de menu        | Apresenta comandos por meio de menus.                                                                                                                                                                   |
| Menu de contexto    | Lista um subconjunto contextuticamente relevante de comandos disponíveis que são exibidos como resultado do clique com o botão direito do mouse em um item.                                                                               |



 

## <a name="property-and-preview-controls"></a>Controles de propriedade e visualização

Controles de propriedade e visualização são usados para visualizar itens e para exibir e editar propriedades de item.



| Control    | Descrição                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão Prévia    | Exibe uma visualização do item selecionado, como uma miniatura ou um ícone ao vivo.                                                                                                                                                                       |
| Propriedades | Exibe as propriedades do item selecionado. Para várias seleções, ele exibe um resumo das propriedades para o grupo de itens selecionado. Para uma seleção nula, ele exibe um resumo das propriedades da página atual (conteúdo da listview). |



 

## <a name="filtering-and-view-controls"></a>Filtragem e controles de exibição

Os controles de filtragem e exibição são usados para manipular o conjunto de itens na exibição de listagem e para alterar a apresentação de itens no listview.



| Control   | Descrição                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filtrar    | Filtra ou organiza itens em uma listview com base nas propriedades listadas como colunas. Clicar em uma coluna classifica por essa propriedade. |
| Wordwheel | Filtra dinamicamente e incrementalmente os itens exibidos em uma listview com base em uma cadeia de caracteres de texto de entrada.                      |
| Visualizar      | Permite que o usuário altere o modo de exibição de um controle listview. Um controle deslizante pode ser usado para determinar o tamanho do ícone.                |



 

## <a name="listview-control"></a>Controle Listview

O controle listview é usado para exibir um conjunto de itens em um dos quatro modos de exibição: detalhes, blocos, ícones ou panorama. O controle listview também permite que o usuário selecione e ative um ou mais itens.

> [!Caution]  
> Embora alguns desses controles tenham nomes e/ou funcionalidades semelhantes aos controles WPF (Windows Presentation Foundation padrão) encontrados no Sistema. Windows. Controla o namespace, eles são classes distintas.

 

Esses controles separados funcionam em grande parte por meio de eventos gerados pela interação do usuário ou pelos próprios controles. A tabela a seguir mostra as três categorias de evento principais.



| Categoria de evento | Exemplo                                                       |
|----------------|---------------------------------------------------------------|
| Navegação     | Ir de uma página para outra.                               |
| Seleção      | Alterando a seleção atual na listview.               |
| Exibir alteração    | Alterando a ordem de apresentação ou o modo de exibição na exibição de lista. |



 

 

 

---
description: O Windows Explorer é um poderoso aplicativo de navegação e gerenciamento de recursos.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Desenvolvendo com o Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7b68d48f2d1becea23311847a5ce41b3776321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460976"
---
# <a name="developing-with-windows-explorer"></a>Desenvolvendo com o Windows Explorer

O Windows Explorer é um poderoso aplicativo de navegação e gerenciamento de recursos. O Windows Explorer pode ser acessado como um todo integrado por meio do Explorer.exe ou da interface [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . O Windows Explorer (Explorer.exe) pode ser gerado como um processo separado usando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ou uma função semelhante.

> [!Note]  
> As opções de linha de comando para Explorer.exe estão documentadas no site de suporte do Microsoft Windows no artigo [Opções de Command-Line do Windows Explorer](https://support.microsoft.com/kb/152457).

 

As janelas abertas do Explorer podem ser descobertas e programadas usando [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows), e novas instâncias do Windows Explorer podem ser criadas usando [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).

O exemplo de código a seguir demonstra como o modelo de automação do Windows Explorer pode ser usado para criar e descobrir janelas do Explorer que estão em execução.


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



A área de cliente do Windows Explorer pode ser hospedada usando a interface [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . O cliente do Windows Explorer e os controles de árvore de namespace são componentes padrão do Windows Vista e posterior. Os desenvolvedores podem reutilizar as interfaces como componentes de criação. Um uso comum desses controles é criar gerenciadores personalizados apropriados para o domínio problemático.

Os controles no Windows Explorer são classificados nas seguintes categorias funcionais:

-   [Controles de navegação](#navigation-controls)
-   [Controles de comando](#command-controls)
-   [Controles de propriedade e visualização](#property-and-preview-controls)
-   [Controles de filtragem e exibição](#filtering-and-view-controls)
-   [Controle ListView](#listview-control)

## <a name="navigation-controls"></a>Controles de navegação

Os controles de navegação ajudam os usuários a determinar o contexto e navegar pelo espaço de domínio lógico associado, chamado de pagespace. Por exemplo, o pagespace para Windows Explorer é o namespace do Shell. Pagespaces são compostas por zero ou mais páginas.

A tabela a seguir lista e descreve os controles de navegação disponíveis no Windows Explorer no Windows Vista e sistemas operacionais posteriores.



| Controle de navegação               | Description                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra de endereços (controle de navegação estrutural) | Exibe o endereço da página atual no pagespace. Botões de navegação estrutural podem ser clicados para navegar para qualquer ancestral no pagespace. Os usuários também podem digitar URLs e caminhos para navegar. |
| Árvore de pastas                      | Fornece uma nova versão de um controle de árvore, otimizada para grandes pagespaces.                                                                                                                  |
| Viagem                           | Habilita a navegação relativa por meio de botões de estilo da Web, como **voltar** e **Avançar**.                                                                                                    |
| Título                            | Exibe o nome e o contexto atuais do Gerenciador.                                                                                                                                            |
| Pagespace                        | Exibe a ramificação atual do pagespace. As páginas podem ser ordenadas por critérios diferentes. Os usuários podem clicar em uma página para navegar até ela.                                                        |



 

## <a name="command-controls"></a>Controles de comando

Os controles de comando anunciam os recursos e a funcionalidade do Windows Explorer para os usuários. Esses controles executam ações gerais ou ações específicas de um item ou itens selecionados.



| Controle de comando | Description                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra de ferramentas         | Exibe botões para comandos comumente usados (uma nova versão de uma barra de ferramentas de comando). As opções de personalização incluem botões suspensos, botões de divisão, texto descritivo opcional e uma área de estouro. |
| Hero            | Aparece como um único, opcional, controle personalizado no centro da barra de ferramentas. Ele representa o comando primário para o contexto atual.                                                             |
| Barra de menu        | Apresenta comandos por meio de menus.                                                                                                                                                                   |
| Menu de contexto    | Lista um subconjunto relevante contextual de comandos disponíveis que são exibidos como resultado do clique com o botão direito do mouse em um item.                                                                               |



 

## <a name="property-and-preview-controls"></a>Controles de propriedade e visualização

Controles de propriedade e visualização são usados para visualizar itens e exibir e editar propriedades de item.



| Control    | Descrição                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão Prévia    | Exibe uma visualização do item selecionado, como uma miniatura ou um ícone dinâmico.                                                                                                                                                                       |
| Propriedades | Exibe as propriedades do item selecionado. Para várias seleções, ele exibe um resumo das propriedades do grupo de itens selecionado. Para uma seleção nula, exibe um resumo das propriedades da página atual (conteúdo de ListView). |



 

## <a name="filtering-and-view-controls"></a>Controles de filtragem e exibição

Controles de filtragem e exibição são usados para manipular o conjunto de itens na ListView e para alterar a apresentação de itens em ListView.



| Control   | Descrição                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filtrar    | Filtra ou organiza os itens em uma ListView com base nas propriedades listadas como colunas. Clicar em uma coluna classifica por essa propriedade. |
| Wordwheel | Filtra dinamicamente e incrementalmente os itens exibidos em uma ListView com base em uma cadeia de caracteres de texto de entrada.                      |
| Visualizar      | Permite que o usuário altere o modo de exibição de um controle ListView. Um controle deslizante pode ser usado para determinar o tamanho do ícone.                |



 

## <a name="listview-control"></a>Controle ListView

O controle ListView é usado para exibir um conjunto de itens em um dos quatro modos de exibição: detalhes, blocos, ícones ou panorama. O controle ListView também permite que o usuário selecione e ative um ou mais itens.

> [!Caution]  
> Embora alguns desses controles tenham nomes e/ou funcionalidades semelhantes aos controles padrão do Windows Presentation Foundation (WPF) encontrados no namespace System. Windows. Controls, eles são classes distintas.

 

Esses controles separados funcionam em conjunto amplamente por meio de eventos gerados pela interação do usuário ou pelos próprios controles. A tabela a seguir mostra as três categorias de evento principal.



| Categoria de evento | Exemplo                                                       |
|----------------|---------------------------------------------------------------|
| Navegação     | Indo de uma página para outra.                               |
| Seleção      | Alterando a seleção atual no ListView.               |
| Exibir alteração    | Alterar a ordem de apresentação ou o modo de exibição no ListView. |



 

 

 

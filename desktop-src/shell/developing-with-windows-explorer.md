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
# <a name="developing-with-windows-explorer"></a><span data-ttu-id="b508a-103">Desenvolvendo com o Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="b508a-103">Developing with Windows Explorer</span></span>

<span data-ttu-id="b508a-104">O Windows Explorer é um poderoso aplicativo de navegação e gerenciamento de recursos.</span><span class="sxs-lookup"><span data-stu-id="b508a-104">Windows Explorer is a powerful resource-browsing and management application.</span></span> <span data-ttu-id="b508a-105">O Windows Explorer pode ser acessado como um todo integrado por meio do Explorer.exe ou da interface [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="b508a-105">Windows Explorer can be accessed as an integrated whole through Explorer.exe or the [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="b508a-106">O Windows Explorer (Explorer.exe) pode ser gerado como um processo separado usando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ou uma função semelhante.</span><span class="sxs-lookup"><span data-stu-id="b508a-106">Windows Explorer (Explorer.exe) can be spawned as a separate process using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) or a similar function.</span></span>

> [!Note]  
> <span data-ttu-id="b508a-107">As opções de linha de comando para Explorer.exe estão documentadas no site de suporte do Microsoft Windows no artigo [Opções de Command-Line do Windows Explorer](https://support.microsoft.com/kb/152457).</span><span class="sxs-lookup"><span data-stu-id="b508a-107">Command-line options for Explorer.exe are documented on the Microsoft Windows Support site in the article [Windows Explorer Command-Line Options](https://support.microsoft.com/kb/152457).</span></span>

 

<span data-ttu-id="b508a-108">As janelas abertas do Explorer podem ser descobertas e programadas usando [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows), e novas instâncias do Windows Explorer podem ser criadas usando [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).</span><span class="sxs-lookup"><span data-stu-id="b508a-108">Open explorer windows can be discovered and programmed by using [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID\_ShellWindows), and new instances of Windows Explorer can be created by using [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID\_ShellBrowserWindow).</span></span>

<span data-ttu-id="b508a-109">O exemplo de código a seguir demonstra como o modelo de automação do Windows Explorer pode ser usado para criar e descobrir janelas do Explorer que estão em execução.</span><span class="sxs-lookup"><span data-stu-id="b508a-109">The following code sample demonstrates how the Windows Explorer automation model can be used to create and discover explorer windows that are running.</span></span>


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



<span data-ttu-id="b508a-110">A área de cliente do Windows Explorer pode ser hospedada usando a interface [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="b508a-110">The Windows Explorer client area can be hosted by using the [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="b508a-111">O cliente do Windows Explorer e os controles de árvore de namespace são componentes padrão do Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="b508a-111">The Windows Explorer client and the namespace tree controls are standard components of Windows Vista and later.</span></span> <span data-ttu-id="b508a-112">Os desenvolvedores podem reutilizar as interfaces como componentes de criação.</span><span class="sxs-lookup"><span data-stu-id="b508a-112">Developers can reuse the interfaces as building components.</span></span> <span data-ttu-id="b508a-113">Um uso comum desses controles é criar gerenciadores personalizados apropriados para o domínio problemático.</span><span class="sxs-lookup"><span data-stu-id="b508a-113">One common use of these controls is to create customized explorers appropriate to the problem domain.</span></span>

<span data-ttu-id="b508a-114">Os controles no Windows Explorer são classificados nas seguintes categorias funcionais:</span><span class="sxs-lookup"><span data-stu-id="b508a-114">The controls in Windows Explorer are classified into the following functional categories:</span></span>

-   [<span data-ttu-id="b508a-115">Controles de navegação</span><span class="sxs-lookup"><span data-stu-id="b508a-115">Navigation Controls</span></span>](#navigation-controls)
-   [<span data-ttu-id="b508a-116">Controles de comando</span><span class="sxs-lookup"><span data-stu-id="b508a-116">Command Controls</span></span>](#command-controls)
-   [<span data-ttu-id="b508a-117">Controles de propriedade e visualização</span><span class="sxs-lookup"><span data-stu-id="b508a-117">Property and Preview Controls</span></span>](#property-and-preview-controls)
-   [<span data-ttu-id="b508a-118">Controles de filtragem e exibição</span><span class="sxs-lookup"><span data-stu-id="b508a-118">Filtering and View Controls</span></span>](#filtering-and-view-controls)
-   [<span data-ttu-id="b508a-119">Controle ListView</span><span class="sxs-lookup"><span data-stu-id="b508a-119">Listview Control</span></span>](#listview-control)

## <a name="navigation-controls"></a><span data-ttu-id="b508a-120">Controles de navegação</span><span class="sxs-lookup"><span data-stu-id="b508a-120">Navigation Controls</span></span>

<span data-ttu-id="b508a-121">Os controles de navegação ajudam os usuários a determinar o contexto e navegar pelo espaço de domínio lógico associado, chamado de pagespace.</span><span class="sxs-lookup"><span data-stu-id="b508a-121">Navigation controls assist users in determining context and navigating the associated logical domain space, called the pagespace.</span></span> <span data-ttu-id="b508a-122">Por exemplo, o pagespace para Windows Explorer é o namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="b508a-122">For example, the pagespace for Windows Explorer is the Shell namespace.</span></span> <span data-ttu-id="b508a-123">Pagespaces são compostas por zero ou mais páginas.</span><span class="sxs-lookup"><span data-stu-id="b508a-123">Pagespaces are composed of zero or more pages.</span></span>

<span data-ttu-id="b508a-124">A tabela a seguir lista e descreve os controles de navegação disponíveis no Windows Explorer no Windows Vista e sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="b508a-124">The following table lists and describes the navigation controls available in Windows Explorer in the Windows Vista and later operating systems.</span></span>



| <span data-ttu-id="b508a-125">Controle de navegação</span><span class="sxs-lookup"><span data-stu-id="b508a-125">Navigation control</span></span>               | <span data-ttu-id="b508a-126">Description</span><span class="sxs-lookup"><span data-stu-id="b508a-126">Description</span></span>                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b508a-127">Barra de endereços (controle de navegação estrutural)</span><span class="sxs-lookup"><span data-stu-id="b508a-127">Address Bar (Breadcrumb control)</span></span> | <span data-ttu-id="b508a-128">Exibe o endereço da página atual no pagespace.</span><span class="sxs-lookup"><span data-stu-id="b508a-128">Displays the address of the current page in the pagespace.</span></span> <span data-ttu-id="b508a-129">Botões de navegação estrutural podem ser clicados para navegar para qualquer ancestral no pagespace.</span><span class="sxs-lookup"><span data-stu-id="b508a-129">Breadcrumb buttons can be clicked to navigate to any ancestor in the pagespace.</span></span> <span data-ttu-id="b508a-130">Os usuários também podem digitar URLs e caminhos para navegar.</span><span class="sxs-lookup"><span data-stu-id="b508a-130">Users can also type URLs and paths to navigate.</span></span> |
| <span data-ttu-id="b508a-131">Árvore de pastas</span><span class="sxs-lookup"><span data-stu-id="b508a-131">Folder Tree</span></span>                      | <span data-ttu-id="b508a-132">Fornece uma nova versão de um controle de árvore, otimizada para grandes pagespaces.</span><span class="sxs-lookup"><span data-stu-id="b508a-132">Provides a new version of a tree control, optimized for large pagespaces.</span></span>                                                                                                                  |
| <span data-ttu-id="b508a-133">Viagem</span><span class="sxs-lookup"><span data-stu-id="b508a-133">Travel</span></span>                           | <span data-ttu-id="b508a-134">Habilita a navegação relativa por meio de botões de estilo da Web, como **voltar** e **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b508a-134">Enables relative navigation through web-style buttons such as **Back** and **Forward**.</span></span>                                                                                                    |
| <span data-ttu-id="b508a-135">Título</span><span class="sxs-lookup"><span data-stu-id="b508a-135">Title</span></span>                            | <span data-ttu-id="b508a-136">Exibe o nome e o contexto atuais do Gerenciador.</span><span class="sxs-lookup"><span data-stu-id="b508a-136">Displays the current explorer name and context.</span></span>                                                                                                                                            |
| <span data-ttu-id="b508a-137">Pagespace</span><span class="sxs-lookup"><span data-stu-id="b508a-137">Pagespace</span></span>                        | <span data-ttu-id="b508a-138">Exibe a ramificação atual do pagespace.</span><span class="sxs-lookup"><span data-stu-id="b508a-138">Displays the current branch of the pagespace.</span></span> <span data-ttu-id="b508a-139">As páginas podem ser ordenadas por critérios diferentes.</span><span class="sxs-lookup"><span data-stu-id="b508a-139">Pages can be ordered by different criteria.</span></span> <span data-ttu-id="b508a-140">Os usuários podem clicar em uma página para navegar até ela.</span><span class="sxs-lookup"><span data-stu-id="b508a-140">Users can click a page to navigate to it.</span></span>                                                        |



 

## <a name="command-controls"></a><span data-ttu-id="b508a-141">Controles de comando</span><span class="sxs-lookup"><span data-stu-id="b508a-141">Command Controls</span></span>

<span data-ttu-id="b508a-142">Os controles de comando anunciam os recursos e a funcionalidade do Windows Explorer para os usuários.</span><span class="sxs-lookup"><span data-stu-id="b508a-142">Command controls advertise the features and functionality of the Windows Explorer to users.</span></span> <span data-ttu-id="b508a-143">Esses controles executam ações gerais ou ações específicas de um item ou itens selecionados.</span><span class="sxs-lookup"><span data-stu-id="b508a-143">These controls perform either general actions or actions specific to one selected item or items.</span></span>



| <span data-ttu-id="b508a-144">Controle de comando</span><span class="sxs-lookup"><span data-stu-id="b508a-144">Command control</span></span> | <span data-ttu-id="b508a-145">Description</span><span class="sxs-lookup"><span data-stu-id="b508a-145">Description</span></span>                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b508a-146">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="b508a-146">Toolbar</span></span>         | <span data-ttu-id="b508a-147">Exibe botões para comandos comumente usados (uma nova versão de uma barra de ferramentas de comando).</span><span class="sxs-lookup"><span data-stu-id="b508a-147">Displays buttons for commonly used commands (a new version of a command toolbar).</span></span> <span data-ttu-id="b508a-148">As opções de personalização incluem botões suspensos, botões de divisão, texto descritivo opcional e uma área de estouro.</span><span class="sxs-lookup"><span data-stu-id="b508a-148">Customization options include drop-down buttons, split buttons, optional descriptive text, and an overflow area.</span></span> |
| <span data-ttu-id="b508a-149">Hero</span><span class="sxs-lookup"><span data-stu-id="b508a-149">Hero</span></span>            | <span data-ttu-id="b508a-150">Aparece como um único, opcional, controle personalizado no centro da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="b508a-150">Appears as a single, optional, custom control in the center of the toolbar.</span></span> <span data-ttu-id="b508a-151">Ele representa o comando primário para o contexto atual.</span><span class="sxs-lookup"><span data-stu-id="b508a-151">It represents the primary command for the current context.</span></span>                                                             |
| <span data-ttu-id="b508a-152">Barra de menu</span><span class="sxs-lookup"><span data-stu-id="b508a-152">Menu Bar</span></span>        | <span data-ttu-id="b508a-153">Apresenta comandos por meio de menus.</span><span class="sxs-lookup"><span data-stu-id="b508a-153">Presents commands through menus.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="b508a-154">Menu de contexto</span><span class="sxs-lookup"><span data-stu-id="b508a-154">Context Menu</span></span>    | <span data-ttu-id="b508a-155">Lista um subconjunto relevante contextual de comandos disponíveis que são exibidos como resultado do clique com o botão direito do mouse em um item.</span><span class="sxs-lookup"><span data-stu-id="b508a-155">Lists a contextually relevant subset of available commands that are displayed as a result of right-clicking an item.</span></span>                                                                               |



 

## <a name="property-and-preview-controls"></a><span data-ttu-id="b508a-156">Controles de propriedade e visualização</span><span class="sxs-lookup"><span data-stu-id="b508a-156">Property and Preview Controls</span></span>

<span data-ttu-id="b508a-157">Controles de propriedade e visualização são usados para visualizar itens e exibir e editar propriedades de item.</span><span class="sxs-lookup"><span data-stu-id="b508a-157">Property and preview controls are used to preview items, and to view and edit item properties.</span></span>



| <span data-ttu-id="b508a-158">Control</span><span class="sxs-lookup"><span data-stu-id="b508a-158">Control</span></span>    | <span data-ttu-id="b508a-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="b508a-159">Description</span></span>                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b508a-160">Versão Prévia</span><span class="sxs-lookup"><span data-stu-id="b508a-160">Preview</span></span>    | <span data-ttu-id="b508a-161">Exibe uma visualização do item selecionado, como uma miniatura ou um ícone dinâmico.</span><span class="sxs-lookup"><span data-stu-id="b508a-161">Displays a preview of the selected item, such as a thumbnail or a Live Icon.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="b508a-162">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b508a-162">Properties</span></span> | <span data-ttu-id="b508a-163">Exibe as propriedades do item selecionado.</span><span class="sxs-lookup"><span data-stu-id="b508a-163">Displays properties of the selected item.</span></span> <span data-ttu-id="b508a-164">Para várias seleções, ele exibe um resumo das propriedades do grupo de itens selecionado.</span><span class="sxs-lookup"><span data-stu-id="b508a-164">For multiple selections, it displays a summary of properties for the selected group of items.</span></span> <span data-ttu-id="b508a-165">Para uma seleção nula, exibe um resumo das propriedades da página atual (conteúdo de ListView).</span><span class="sxs-lookup"><span data-stu-id="b508a-165">For a null selection, it displays a summary of properties for the current page (contents of the listview).</span></span> |



 

## <a name="filtering-and-view-controls"></a><span data-ttu-id="b508a-166">Controles de filtragem e exibição</span><span class="sxs-lookup"><span data-stu-id="b508a-166">Filtering and View Controls</span></span>

<span data-ttu-id="b508a-167">Controles de filtragem e exibição são usados para manipular o conjunto de itens na ListView e para alterar a apresentação de itens em ListView.</span><span class="sxs-lookup"><span data-stu-id="b508a-167">Filtering and view controls are used to manipulate the set of items in the listview and to change the presentation of items in the listview.</span></span>



| <span data-ttu-id="b508a-168">Control</span><span class="sxs-lookup"><span data-stu-id="b508a-168">Control</span></span>   | <span data-ttu-id="b508a-169">Descrição</span><span class="sxs-lookup"><span data-stu-id="b508a-169">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b508a-170">Filtrar</span><span class="sxs-lookup"><span data-stu-id="b508a-170">Filter</span></span>    | <span data-ttu-id="b508a-171">Filtra ou organiza os itens em uma ListView com base nas propriedades listadas como colunas.</span><span class="sxs-lookup"><span data-stu-id="b508a-171">Filters or arranges items in a listview based on properties listed as columns.</span></span> <span data-ttu-id="b508a-172">Clicar em uma coluna classifica por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b508a-172">Clicking on a column sorts by that property.</span></span> |
| <span data-ttu-id="b508a-173">Wordwheel</span><span class="sxs-lookup"><span data-stu-id="b508a-173">Wordwheel</span></span> | <span data-ttu-id="b508a-174">Filtra dinamicamente e incrementalmente os itens exibidos em uma ListView com base em uma cadeia de caracteres de texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="b508a-174">Dynamically and incrementally filters the displayed items in a listview based on an input text string.</span></span>                      |
| <span data-ttu-id="b508a-175">Visualizar</span><span class="sxs-lookup"><span data-stu-id="b508a-175">View</span></span>      | <span data-ttu-id="b508a-176">Permite que o usuário altere o modo de exibição de um controle ListView.</span><span class="sxs-lookup"><span data-stu-id="b508a-176">Enables the user to change the view mode of a listview control.</span></span> <span data-ttu-id="b508a-177">Um controle deslizante pode ser usado para determinar o tamanho do ícone.</span><span class="sxs-lookup"><span data-stu-id="b508a-177">A slider can be used to determine icon size.</span></span>                |



 

## <a name="listview-control"></a><span data-ttu-id="b508a-178">Controle ListView</span><span class="sxs-lookup"><span data-stu-id="b508a-178">Listview Control</span></span>

<span data-ttu-id="b508a-179">O controle ListView é usado para exibir um conjunto de itens em um dos quatro modos de exibição: detalhes, blocos, ícones ou panorama.</span><span class="sxs-lookup"><span data-stu-id="b508a-179">The listview control is used to view a set of items in one of four view modes: details, tiles, icons, or panorama.</span></span> <span data-ttu-id="b508a-180">O controle ListView também permite que o usuário selecione e ative um ou mais itens.</span><span class="sxs-lookup"><span data-stu-id="b508a-180">The listview control also enables the user to select and activate one or more items.</span></span>

> [!Caution]  
> <span data-ttu-id="b508a-181">Embora alguns desses controles tenham nomes e/ou funcionalidades semelhantes aos controles padrão do Windows Presentation Foundation (WPF) encontrados no namespace System. Windows. Controls, eles são classes distintas.</span><span class="sxs-lookup"><span data-stu-id="b508a-181">Although some of these controls have names and/or functionality that is similar to standard Windows Presentation Foundation (WPF) controls found in the System.Windows.Controls namespace, they are distinct classes.</span></span>

 

<span data-ttu-id="b508a-182">Esses controles separados funcionam em conjunto amplamente por meio de eventos gerados pela interação do usuário ou pelos próprios controles.</span><span class="sxs-lookup"><span data-stu-id="b508a-182">These separate controls work together largely through events generated either by user interaction or by the controls themselves.</span></span> <span data-ttu-id="b508a-183">A tabela a seguir mostra as três categorias de evento principal.</span><span class="sxs-lookup"><span data-stu-id="b508a-183">The following table shows the three primary event categories.</span></span>



| <span data-ttu-id="b508a-184">Categoria de evento</span><span class="sxs-lookup"><span data-stu-id="b508a-184">Event category</span></span> | <span data-ttu-id="b508a-185">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b508a-185">Example</span></span>                                                       |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="b508a-186">Navegação</span><span class="sxs-lookup"><span data-stu-id="b508a-186">Navigation</span></span>     | <span data-ttu-id="b508a-187">Indo de uma página para outra.</span><span class="sxs-lookup"><span data-stu-id="b508a-187">Going from one page to another.</span></span>                               |
| <span data-ttu-id="b508a-188">Seleção</span><span class="sxs-lookup"><span data-stu-id="b508a-188">Selection</span></span>      | <span data-ttu-id="b508a-189">Alterando a seleção atual no ListView.</span><span class="sxs-lookup"><span data-stu-id="b508a-189">Changing the current selection in the listview.</span></span>               |
| <span data-ttu-id="b508a-190">Exibir alteração</span><span class="sxs-lookup"><span data-stu-id="b508a-190">View Change</span></span>    | <span data-ttu-id="b508a-191">Alterar a ordem de apresentação ou o modo de exibição no ListView.</span><span class="sxs-lookup"><span data-stu-id="b508a-191">Changing the presentation order or view mode in the listview.</span></span> |



 

 

 

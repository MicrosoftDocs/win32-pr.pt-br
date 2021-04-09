---
title: Navegador de contêineres
description: Um aplicativo pode usar a função DsBrowseForContainer para exibir uma caixa de diálogo que pode ser usada para navegar pelos contêineres em um serviço de Domínio do Active Directory.
ms.assetid: aa88d565-ff25-4082-964a-9a230d2607f2
ms.tgt_platform: multiple
keywords:
- Navegador de contêiner AD
- contêineres AD, navegador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964c67873cc7936a75e2b9c1cdf331d0fa1fdae1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007348"
---
# <a name="container-browser"></a><span data-ttu-id="c63b1-105">Navegador de contêineres</span><span class="sxs-lookup"><span data-stu-id="c63b1-105">Container Browser</span></span>

<span data-ttu-id="c63b1-106">Um aplicativo pode usar a função [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) para exibir uma caixa de diálogo que pode ser usada para navegar pelos contêineres em um serviço de domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c63b1-106">An application can use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to display a dialog box that can be used to browse through the containers in an Active Directory Domain Service.</span></span> <span data-ttu-id="c63b1-107">A caixa de diálogo exibe os contêineres em um formato de árvore e permite que o usuário navegue pela árvore usando o teclado e o mouse.</span><span class="sxs-lookup"><span data-stu-id="c63b1-107">The dialog box displays the containers in a tree format and enables the user to navigate through the tree using the keyboard and mouse.</span></span> <span data-ttu-id="c63b1-108">Quando o usuário seleciona um item na caixa de diálogo, o ADsPath do contêiner selecionado pelo usuário é fornecido.</span><span class="sxs-lookup"><span data-stu-id="c63b1-108">When the user selects an item in the dialog box, the ADsPath of the container selected by the user is provided.</span></span>

<span data-ttu-id="c63b1-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) usa um ponteiro para uma estrutura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) que contém dados sobre a caixa de diálogo e retorna o ADsPath do item selecionado.</span><span class="sxs-lookup"><span data-stu-id="c63b1-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) takes a pointer to a [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure that contains data about the dialog box and returns the ADsPath of the selected item.</span></span>

<span data-ttu-id="c63b1-110">O membro **pszRoot** é um ponteiro para uma cadeia de caracteres Unicode que contém o contêiner raiz da árvore.</span><span class="sxs-lookup"><span data-stu-id="c63b1-110">The **pszRoot** member is a pointer to a Unicode string that contains the root container of the tree.</span></span> <span data-ttu-id="c63b1-111">Se **pszRoot** for **NULL**, a árvore conterá a árvore inteira.</span><span class="sxs-lookup"><span data-stu-id="c63b1-111">If **pszRoot** is **NULL**, the tree will contain the entire tree.</span></span>

<span data-ttu-id="c63b1-112">O membro **pszPath** recebe o ADsPath do objeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="c63b1-112">The **pszPath** member receives the ADsPath of the selected object.</span></span> <span data-ttu-id="c63b1-113">É possível especificar um contêiner específico para ser visível e selecionado quando a caixa de diálogo for exibida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="c63b1-113">It is possible to specify a particular container to be visible and selected when the dialog box is first displayed.</span></span> <span data-ttu-id="c63b1-114">Isso é feito definindo **pszPath** para o ADsPath do item a ser selecionado e definindo o sinalizador **DSBI \_ EXPANDONOPEN** no **dwFlags**.</span><span class="sxs-lookup"><span data-stu-id="c63b1-114">This is accomplished by setting **pszPath** to the ADsPath of the item to be selected and setting the **DSBI\_EXPANDONOPEN** flag in **dwFlags**.</span></span>

<span data-ttu-id="c63b1-115">O conteúdo e o comportamento da caixa de diálogo também podem ser controlados em tempo de execução implementando uma função [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="c63b1-115">The contents and behavior of the dialog box can also be controlled at runtime by implementing a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="c63b1-116">A função **BFFCallBack** é implementada pelo aplicativo e é chamada quando determinados eventos ocorrem.</span><span class="sxs-lookup"><span data-stu-id="c63b1-116">The **BFFCallBack** function is implemented by the application and is called when certain events occur.</span></span> <span data-ttu-id="c63b1-117">Um aplicativo pode usar esses eventos para controlar como os itens na caixa de diálogo são exibidos, bem como o conteúdo real da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c63b1-117">An application can use these events to control how the items in the dialog box are displayed as well as the actual contents of the dialog box.</span></span> <span data-ttu-id="c63b1-118">Por exemplo, um aplicativo pode filtrar os itens exibidos na caixa de diálogo implementando uma função **BFFCallBack** que pode manipular a **notificação \_ QUERYINSERT DSBM** .</span><span class="sxs-lookup"><span data-stu-id="c63b1-118">For example, an application can filter the items displayed in the dialog box by implementing a **BFFCallBack** function that can handle the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="c63b1-119">Quando uma notificação **DSBM \_ QUERYINSERT** for recebida, use o membro **pszADsPath** da estrutura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) para determinar qual item está prestes a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="c63b1-119">When a **DSBM\_QUERYINSERT** notification is received, use the **pszADsPath** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure to determine which item is about to be inserted.</span></span> <span data-ttu-id="c63b1-120">Se o aplicativo determinar que o item não deve ser exibido, ele poderá ocultar o item executando as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c63b1-120">If the application determines that the item should not be displayed, it can hide the item by performing the following steps.</span></span>

1.  <span data-ttu-id="c63b1-121">Adicione o sinalizador de **\_ estado DSBF** ao membro **dwMask** da estrutura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="c63b1-121">Add the **DSBF\_STATE** flag to the **dwMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
2.  <span data-ttu-id="c63b1-122">Adicione o **sinalizador \_ Hidden DSBS** ao membro **dwStateMask** da estrutura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="c63b1-122">Add the **DSBS\_HIDDEN** flag to the **dwStateMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
3.  <span data-ttu-id="c63b1-123">Adicione o **sinalizador \_ Hidden DSBS** ao membro **dwState** da estrutura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="c63b1-123">Add the **DSBS\_HIDDEN** flag to the **dwState** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
4.  <span data-ttu-id="c63b1-124">Retornar um valor diferente de zero da função [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="c63b1-124">Return a nonzero value from the [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span>

<span data-ttu-id="c63b1-125">Além de ocultar determinados itens, um aplicativo pode modificar o texto e o ícone exibidos para o item manipulando a notificação **DSBM \_ QUERYINSERT** .</span><span class="sxs-lookup"><span data-stu-id="c63b1-125">In addition to hiding certain items, an application can modify the text and icon displayed for the item by handling the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="c63b1-126">Para obter mais informações, consulte [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span><span class="sxs-lookup"><span data-stu-id="c63b1-126">For more information, see [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span></span>

<span data-ttu-id="c63b1-127">A função [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) pode usar a **notificação \_ inicializada BFFM** para obter o identificador da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c63b1-127">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function can use the **BFFM\_INITIALIZED** notification to obtain the handle of the dialog box.</span></span> <span data-ttu-id="c63b1-128">O aplicativo pode usar esse identificador para enviar mensagens, como **BFFM \_ ENABLEOK**, para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c63b1-128">The application can use this handle to send messages, such as **BFFM\_ENABLEOK**, to the dialog box.</span></span> <span data-ttu-id="c63b1-129">Para obter mais informações sobre as mensagens que podem ser enviadas para a caixa de diálogo, consulte [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span><span class="sxs-lookup"><span data-stu-id="c63b1-129">For more information about the messages that can be sent to the dialog box, see [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span></span>

<span data-ttu-id="c63b1-130">O identificador da caixa de diálogo também pode ser usado para obter acesso direto aos controles na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c63b1-130">The dialog box handle can also be used to gain direct access to the controls in the dialog box.</span></span> <span data-ttu-id="c63b1-131">**DSBID \_ BANNER** é o identificador do controle de texto estático no qual o membro **pszTitle** da estrutura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) é exibido.</span><span class="sxs-lookup"><span data-stu-id="c63b1-131">**DSBID\_BANNER** is the identifier for the static text control that the **pszTitle** member of the [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure is displayed in.</span></span> <span data-ttu-id="c63b1-132">**DSBID \_ CONTAINERlist** é o identificador do controle de exibição de árvore usado para exibir o conteúdo da árvore.</span><span class="sxs-lookup"><span data-stu-id="c63b1-132">**DSBID\_CONTAINERLIST** is the identifier of the tree view control used to display the tree contents.</span></span> <span data-ttu-id="c63b1-133">O uso desses itens deve ser evitado, se possível, para evitar problemas futuros de compatibilidade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c63b1-133">Use of these items should be avoided, if possible, to prevent future application compatibility problems.</span></span>

<span data-ttu-id="c63b1-134">O exemplo de código C++ a seguir mostra como usar a função [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) para criar a caixa de diálogo de navegador de contêiner e implementar uma função [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="c63b1-134">The following C++ code example shows how to use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to create the container browser dialog box and implement a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="c63b1-135">O [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) usa a notificação **DSBM \_ QUERYINSERT** para alterar o nome de exibição de cada item para o nome distinto do item.</span><span class="sxs-lookup"><span data-stu-id="c63b1-135">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) uses the **DSBM\_QUERYINSERT** notification to change the display name for each item to the distinguished name of the item.</span></span>


```C++
#include <shlobj.h>
#include <dsclient.h>
#include <atlbase.h>

/**********

    WideCharToLocal()
   
***********/

int WideCharToLocal(LPTSTR pLocal, LPWSTR pWide, DWORD dwChars)
{
    *pLocal = NULL;
    size_t nWideLength = 0;
    wchar_t *pwszSubstring;

    nWideLength = wcslen(pWide);

#ifdef UNICODE
    if(nWideLength < dwChars)
    {
        wcsncpy_s(pLocal, pWide, dwChars);
    }
    else
    {
        wcsncpy_s(pLocal, pWide, dwChars-1);
        pLocal[dwChars-1] = NULL;
    }
#else
    if(nWideLength < dwChars)
    {
        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pWide, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);
    }
    else
    {
        pwszSubstring = new WCHAR[dwChars];
        wcsncpy_s(pwszSubstring,pWide,dwChars-1);
        pwszSubstring[dwChars-1] = NULL;

        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pwszSubstring, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);

    delete [] pwszSubstring;
    }
#endif

    return lstrlen(pLocal);
}

/**********

    BrowseCallback()

***********/

int CALLBACK BrowseCallback(HWND hWnd, 
                            UINT uMsg, 
                            LPARAM lParam, 
                            LPARAM lpData)
{
    switch(uMsg)
    {
    case DSBM_QUERYINSERT:
        {
            BOOL fReturn = FALSE;
            DSBITEM *pItem = (DSBITEM*)lParam;

            /*
            If this is to the root item, get the distinguished name 
            for the object and set the display name to the 
            distinguished name.
            */
            if(!(pItem->dwState & DSBS_ROOT))
            {
                HRESULT hr;
                IADs    *pads;

                hr = ADsGetObject(pItem->pszADsPath , 
                    IID_IADs, (LPVOID*)&pads);
                if(SUCCEEDED(hr))
                {
                    VARIANT var;

                    VariantInit(&var);
                    hr = pads->Get(CComBSTR("distinguishedName"), 
                        &var);
                    if(SUCCEEDED(hr))
                    {
                        if(VT_BSTR == var.vt)
                        {
                            WideCharToLocal(pItem->szDisplayName, 
                                var.bstrVal, 
                                DSB_MAX_DISPLAYNAME_CHARS);
                            pItem->dwMask |= DSBF_DISPLAYNAME;
                            fReturn = TRUE;
                        }
                        
                        VariantClear(&var);
                    }
                    
                    pads->Release();
                }
            }

            return fReturn;
        }

        break;
    }
    
    return FALSE;
}

/***********

    BrowseForContainer()

************/

HRESULT BrowseForContainer(HWND hwndParent, 
    LPOLESTR *ppContainerADsPath)
{
    HRESULT hr = E_FAIL;
    DSBROWSEINFO dsbi;
    OLECHAR wszPath[MAX_PATH * 2];
    DWORD result;
 
    if(!ppContainerADsPath)
    {
        return E_INVALIDARG;
    }
 
    ZeroMemory(&dsbi, sizeof(dsbi));
    dsbi.hwndOwner = hwndParent;
    dsbi.cbStruct = sizeof (DSBROWSEINFO);
    dsbi.pszCaption = TEXT("Browse for a Container");
    dsbi.pszTitle = TEXT("Select an Active Directory container.");
    dsbi.pszRoot = NULL;
    dsbi.pszPath = wszPath;
    dsbi.cchPath = sizeof(wszPath)/sizeof(OLECHAR);
    dsbi.dwFlags = DSBI_INCLUDEHIDDEN |
                    DSBI_IGNORETREATASLEAF|
                    DSBI_RETURN_FORMAT;
    dsbi.pfnCallback = BrowseCallback;
    dsbi.lParam = 0;
    dsbi.dwReturnFormat = ADS_FORMAT_X500;
 
    // Display the browse dialog box.
    // Returns -1, 0, IDOK, or IDCANCEL.
    result = DsBrowseForContainer(&dsbi); 
    if(IDOK == result)
    {
        // Allocate memory for the string.
        *ppContainerADsPath = (OLECHAR*)CoTaskMemAlloc(
            sizeof(OLECHAR)*(wcslen(wszPath) + 1));
        if(*ppContainerADsPath)
        {
            wcscpy_s(*ppContainerADsPath, wszPath);
            // Caller must free using CoTaskMemFree. 
            hr = S_OK;
        }
        else
        {
            hr = E_FAIL;
        }
    }
    else
    {
        hr = E_FAIL;
    }
 
    return hr;
}
```



 

 
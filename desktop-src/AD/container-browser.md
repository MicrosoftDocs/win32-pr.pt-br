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
# <a name="container-browser"></a>Navegador de contêineres

Um aplicativo pode usar a função [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) para exibir uma caixa de diálogo que pode ser usada para navegar pelos contêineres em um serviço de domínio do Active Directory. A caixa de diálogo exibe os contêineres em um formato de árvore e permite que o usuário navegue pela árvore usando o teclado e o mouse. Quando o usuário seleciona um item na caixa de diálogo, o ADsPath do contêiner selecionado pelo usuário é fornecido.

[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) usa um ponteiro para uma estrutura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) que contém dados sobre a caixa de diálogo e retorna o ADsPath do item selecionado.

O membro **pszRoot** é um ponteiro para uma cadeia de caracteres Unicode que contém o contêiner raiz da árvore. Se **pszRoot** for **NULL**, a árvore conterá a árvore inteira.

O membro **pszPath** recebe o ADsPath do objeto selecionado. É possível especificar um contêiner específico para ser visível e selecionado quando a caixa de diálogo for exibida pela primeira vez. Isso é feito definindo **pszPath** para o ADsPath do item a ser selecionado e definindo o sinalizador **DSBI \_ EXPANDONOPEN** no **dwFlags**.

O conteúdo e o comportamento da caixa de diálogo também podem ser controlados em tempo de execução implementando uma função [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . A função **BFFCallBack** é implementada pelo aplicativo e é chamada quando determinados eventos ocorrem. Um aplicativo pode usar esses eventos para controlar como os itens na caixa de diálogo são exibidos, bem como o conteúdo real da caixa de diálogo. Por exemplo, um aplicativo pode filtrar os itens exibidos na caixa de diálogo implementando uma função **BFFCallBack** que pode manipular a **notificação \_ QUERYINSERT DSBM** . Quando uma notificação **DSBM \_ QUERYINSERT** for recebida, use o membro **pszADsPath** da estrutura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) para determinar qual item está prestes a ser inserido. Se o aplicativo determinar que o item não deve ser exibido, ele poderá ocultar o item executando as etapas a seguir.

1.  Adicione o sinalizador de **\_ estado DSBF** ao membro **dwMask** da estrutura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
2.  Adicione o **sinalizador \_ Hidden DSBS** ao membro **dwStateMask** da estrutura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
3.  Adicione o **sinalizador \_ Hidden DSBS** ao membro **dwState** da estrutura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
4.  Retornar um valor diferente de zero da função [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .

Além de ocultar determinados itens, um aplicativo pode modificar o texto e o ícone exibidos para o item manipulando a notificação **DSBM \_ QUERYINSERT** . Para obter mais informações, consulte [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).

A função [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) pode usar a **notificação \_ inicializada BFFM** para obter o identificador da caixa de diálogo. O aplicativo pode usar esse identificador para enviar mensagens, como **BFFM \_ ENABLEOK**, para a caixa de diálogo. Para obter mais informações sobre as mensagens que podem ser enviadas para a caixa de diálogo, consulte [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).

O identificador da caixa de diálogo também pode ser usado para obter acesso direto aos controles na caixa de diálogo. **DSBID \_ BANNER** é o identificador do controle de texto estático no qual o membro **pszTitle** da estrutura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) é exibido. **DSBID \_ CONTAINERlist** é o identificador do controle de exibição de árvore usado para exibir o conteúdo da árvore. O uso desses itens deve ser evitado, se possível, para evitar problemas futuros de compatibilidade de aplicativos.

O exemplo de código C++ a seguir mostra como usar a função [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) para criar a caixa de diálogo de navegador de contêiner e implementar uma função [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . O [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) usa a notificação **DSBM \_ QUERYINSERT** para alterar o nome de exibição de cada item para o nome distinto do item.


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



 

 
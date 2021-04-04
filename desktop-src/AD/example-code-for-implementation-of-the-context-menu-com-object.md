---
title: Código de exemplo para implementação do objeto COM do menu de contexto
description: O exemplo de código a seguir pode ser usado para implementar uma extensão de menu de contexto Active Directory. O item de menu de contexto único exibirá uma caixa de mensagem que contém o ADsPath de cada item selecionado.
ms.assetid: dc8f2c31-6031-4c7d-a173-5cedcedbfb26
ms.tgt_platform: multiple
keywords:
- Active Directory AD, código de exemplo C/C++, implementação do objeto COM do menu de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99402606b21f3b91e0511a4baf4ca18e8a2e8c23
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007311"
---
# <a name="example-code-for-implementation-of-the-context-menu-com-object"></a>Código de exemplo para implementação do objeto COM do menu de contexto

O exemplo de código a seguir pode ser usado para implementar uma extensão de menu de contexto Active Directory. O item de menu de contexto único exibirá uma caixa de mensagem que contém o ADsPath de cada item selecionado.

## <a name="ishellextinit-implementation"></a>Implementação de IShellExtInit

O exemplo de código a seguir pode ser usado para implementar os métodos [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) .


```C++
///////////////////////////////////////////////////////////////////////////
//
// IShellExtInit Implementation
//

/**************************************************************************

   CContMenuExt::Initialize()

**************************************************************************/

STDMETHODIMP CContMenuExt::Initialize(  LPCITEMIDLIST pidlFolder,
                                        LPDATAOBJECT pDataObj,
                                        HKEY  hKeyProgId)
{
    STGMEDIUM   stm;
    FORMATETC   fe;
    HRESULT     hr;

    if(NULL == pDataObj)
    {
        return E_INVALIDARG;
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DSOBJECTNAMES);
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObj->GetData(&fe, &stm);
    if(SUCCEEDED(hr))
    {
        LPDSOBJECTNAMES pdson = (LPDSOBJECTNAMES)GlobalLock(stm.hGlobal);

        if(pdson)
        {
            DWORD   dwBytes = GlobalSize(stm.hGlobal);

            m_pObjectNames = (DSOBJECTNAMES*)GlobalAlloc(GPTR, dwBytes);
            if(m_pObjectNames)
            {
                CopyMemory(m_pObjectNames, pdson, dwBytes);
            }
            
            GlobalUnlock(stm.hGlobal);
        }
        
        ReleaseStgMedium(&stm);
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DS_DISPLAY_SPEC_OPTIONS);
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObj->GetData(&fe, &stm);
    if(SUCCEEDED(hr))
    {
        PDSDISPLAYSPECOPTIONS   pdso;
        
        pdso = (PDSDISPLAYSPECOPTIONS)GlobalLock(stm.hGlobal);
        if(pdso)
        {
            DWORD   dwBytes = GlobalSize(stm.hGlobal);

            m_pDispSpecOpts = (PDSDISPLAYSPECOPTIONS)GlobalAlloc(GPTR, dwBytes);
            if(m_pDispSpecOpts)
            {
                CopyMemory(m_pDispSpecOpts, pdso, dwBytes);
            }
            
            GlobalUnlock(stm.hGlobal);
        }

        ReleaseStgMedium(&stm);
    }

    return hr;
}

```



## <a name="icontextmenu-implementation"></a>Implementação de IContextMenu

O exemplo de código a seguir pode ser usado para implementar os métodos [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .


```C++
///////////////////////////////////////////////////////////////////////////
//
// IContextMenu Implementation
//

/**************************************************************************

   CContMenuExt::QueryContextMenu()

**************************************************************************/

STDMETHODIMP CContMenuExt::QueryContextMenu(    HMENU hMenu,
                                                UINT indexMenu,
                                                UINT idCmdFirst,
                                                UINT idCmdLast,
                                                UINT uFlags)
{
    if(m_pObjectNames && !(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu( hMenu, 
                    indexMenu, 
                    MF_STRING | MF_BYPOSITION, 
                    idCmdFirst + IDM_CONTMENU, 
                    TEXT("AD Sample Context Menu"));

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_CONTMENU + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}

/**************************************************************************

   CContMenuExt::InvokeCommand()

**************************************************************************/

STDMETHODIMP CContMenuExt::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    if(LOWORD(lpcmi->lpVerb) > IDM_CONTMENU)
    {
        return E_INVALIDARG;
    }

    switch (LOWORD(lpcmi->lpVerb))
    {
    case IDM_CONTMENU:
        {
            LPWSTR  pwszName;
            DWORD   dwBytes;
            UINT    i;

            for(i = 0, dwBytes = 0; i < m_pObjectNames->cItems; i++)
            {
                pwszName = (LPWSTR)((LPBYTE)m_pObjectNames + m_pObjectNames->aObjects[i].offsetName);
                dwBytes += (lstrlenW(pwszName) + 2) * sizeof(WCHAR);
            }

            LPWSTR  pwszText = (LPWSTR)GlobalAlloc(GPTR, dwBytes);

            if(pwszText)
            {
                pwszText[0] = 0;
                for(i = 0; i < m_pObjectNames->cItems; i++)
                {
                    pwszName = (LPWSTR)((LPBYTE)m_pObjectNames + m_pObjectNames->aObjects[i].offsetName);
                    wcscat_s(pwszText, pwszName);
                    wcscat_s(pwszText, L"\n");
                }
                
                MessageBoxW(lpcmi->hwnd, 
                            pwszText, 
                            L"Sample Command", 
                            MB_OK | MB_ICONINFORMATION);

                GlobalFree(pwszText);
            }
        }
        break;
    }

    return NOERROR;
}

/**************************************************************************

   CContMenuExt::GetCommandString()

**************************************************************************/

STDMETHODIMP CContMenuExt::GetCommandString(    UINT idCommand,
                                                UINT uFlags,
                                                LPUINT lpReserved,
                                                LPSTR lpszName,
                                                UINT uMaxNameLen)
{
    HRESULT hr = E_INVALIDARG;
    TCHAR   szHelp[] = TEXT("Sample Context Menu Command");
    TCHAR   szVerb[] = TEXT("adcontmenu");

    switch(uFlags)
    {
    case GCS_HELPTEXTA:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToAnsi((LPSTR)lpszName, szHelp, uMaxNameLen);
            hr = S_OK;
            break;
         }
        break;
   
    case GCS_HELPTEXTW:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToWideChar((LPWSTR)lpszName, szHelp, uMaxNameLen);
            hr = S_OK;
            break;
         }
        break;
   
    case GCS_VERBA:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToAnsi((LPSTR)lpszName, szVerb, uMaxNameLen);
            hr = S_OK;
            break;
        }
        break;
   
    case GCS_VERBW:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToWideChar((LPWSTR)lpszName, szVerb, uMaxNameLen);
            hr = S_OK;
            break;
        }
        break;
   
    case GCS_VALIDATE:
        hr = S_OK;
        break;
    }

    return hr;
}

```



 

 
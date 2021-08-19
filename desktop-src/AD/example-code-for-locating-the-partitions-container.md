---
title: Código de exemplo para localizar o contêiner de partições
description: Este tópico inclui exemplos de código que localizam o contêiner de partição.
ms.assetid: 7aa6ad5a-7baf-484a-9296-eafb61da5f4e
ms.tgt_platform: multiple
keywords:
- Código de exemplo para localizar o AD do contêiner de partições
- Application Directory Partitions AD , código de exemplo para localizar o contêiner de partições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5757e638e046089d828ee1c681d04ec210986181cb74ec3b1253c05515eda2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962297"
---
# <a name="example-code-for-locating-the-partitions-container"></a>Código de exemplo para localizar o contêiner de partições

Este tópico inclui exemplos de código que localizam o contêiner de partição.

O exemplo de código C/C++ a seguir obtém o nome diferenciado do contêiner Partições pesquisando o contêiner de configuração para o [**objeto crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer)


```C++
/***************************************************************************

    GetPartitionsDNSearch()

    Description: Gets the distinguished name of the Partitions container in 
    the current enterprise forest.

    Parameters:

    ppwszPartitionsDN - Pointer to an LPWSTR that receives the distinguished 
    name string. The caller must free this memory with 
    FreeADsMem when it is no longer required.

***************************************************************************/

HRESULT GetPartitionsDNSearch(LPWSTR *ppwszPartitionsDN)
{
 
    *ppwszPartitionsDN = NULL;
    
    HRESULT hr;

    IADs *padsRootDSE;

    // Bind to the RootDSE to get the configurationNamingContext property.
    hr = ADsOpenObject( L"LDAP://RootDSE",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&padsRootDSE);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;

        // Get the configurationNamingContext property.
        hr = padsRootDSE->Get(CComBSTR("configurationNamingContext"), &svar);
        if(SUCCEEDED(hr))
        {
            IDirectorySearch *pConfigSearch;

            // Bind to the Configuration container.
            CComBSTR sbstrPath = "LDAP://";
            sbstrPath += svar.bstrVal;

            hr = ADsOpenObject( sbstrPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IDirectorySearch, 
                                (LPVOID*)&pConfigSearch);

            if(SUCCEEDED(hr))
            {
                // Search for an object that is of type crossRefContainer.
                ADS_SEARCHPREF_INFO SearchPref[1];

                // Set the search scope.
                SearchPref[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
                SearchPref[0].vValue.dwType = ADSTYPE_INTEGER;
                SearchPref[0].vValue.Integer = ADS_SCOPE_ONELEVEL;
                
                hr = pConfigSearch->SetSearchPreference(SearchPref, sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO));
                if(SUCCEEDED(hr))
                {
                    ADS_SEARCH_HANDLE hSearch = NULL;
                    LPWSTR pwszAttributes[1] = {L"distinguishedName"};
                    LPWSTR pwszSearchFilter = L"(&(objectClass=crossRefContainer))";
                    
                    // Execute the search.
                    hr = pConfigSearch->ExecuteSearch(pwszSearchFilter, 
                        pwszAttributes, 
                        sizeof(pwszAttributes)/sizeof(LPWSTR), 
                        &hSearch);
                    if(SUCCEEDED(hr))
                    {
                        // Get the first result row. There should never be more than one match.
                        hr = pConfigSearch->GetFirstRow(hSearch);
                        if(S_OK == hr)
                        {
                            ADS_SEARCH_COLUMN col;

                            // Get the search result. The distinguishedName attribute will be a string.
                            hr = pConfigSearch->GetColumn(hSearch, pwszAttributes[0], &col);
                            if(SUCCEEDED(hr))
                            {
                                // col.pADsValues[0].DNString;
                                DWORD dwChars = lstrlenW(col.pADsValues[0].DNString) + 1;
                                
                                *ppwszPartitionsDN = (LPWSTR)AllocADsMem(dwChars * sizeof(WCHAR));
                                
                                if(*ppwszPartitionsDN)
                                {
                                    wcsncpy_s(*ppwszPartitionsDN, col.pADsValues[0].DNString, dwChars);
                                }
                                else
                                {
                                    hr = E_OUTOFMEMORY;
                                }

                                pConfigSearch->FreeColumn(&col);
                            }
                        }
                        else
                        {
                            hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
                        }
                        
                        // Close the search handle to cleanup.
                        pConfigSearch->CloseSearchHandle(hSearch);
                    }
                }

                pConfigSearch->Release();
            }
        }
        
        padsRootDSE->Release();
    }

    return hr;
}
```



O exemplo Visual Basic código do Scripting Edition a seguir obtém o nome diferenciado do contêiner Partições pesquisando o contêiner de configuração para o [**objeto crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer)


```VB
Const ADS_SECURE_AUTHENTICATION = 1

'
'   GetPartitionsDNSearch
'
'   Description: Gets the distinguished name of the Partitions container in
'   the current enterprise forest.
'
Function GetPartitionsDNSearch()
    ' Bind to RootDSE.
    Set oRootDSE = GetObject("LDAP://RootDSE")
    
    Set oConn = CreateObject("ADODB.Connection")
    Set oComm = CreateObject("ADODB.Command")
     
    oConn.Provider = "ADsDSOObject"

    ' Set the binding options for the search.
    oConn.Properties("ADSI Flag") = ADS_SECURE_AUTHENTICATION
    
    oConn.Open
    oComm.ActiveConnection = oConn
    
    oComm.CommandText = "<LDAP://" + oRootDSE.Get("configurationNamingContext") + ">;(&(objectClass=crossRefContainer));distinguishedName;onelevel"
    
    ' WScript.Echo oComm.CommandText
    
    ' Execute the query.
    Set oResults = oComm.Execute
    
    ' Get the first result. This should be the only result.
    Set oField = oResults(0)
    
    GetPartitionsDNSearch = oField.Value
End Function
```



O exemplo de código C/C++ a seguir obtém o nome diferenciado do contêiner Partições criando manualmente o nome diferenciado.


```C++
/***************************************************************************

    GetPartitionsDNManual()

    Description: Gets the distinguished name of the Partitions container in 
    the current enterprise forest.

    Parameters:

    ppwszPartitionsDN - Pointer to an LPWSTR that receives the distinguished 
    name string. The caller must free this memory with 
    FreeADsMem when it is no longer required.

***************************************************************************/

HRESULT GetPartitionsDNManual(LPWSTR *ppwszPartitionsDN)
{

    *ppwszPartitionsDN = NULL;

    HRESULT hr;

    IADs *padsRootDSE;

    // Bind to the RootDSE to get the configurationNamingContext property.
    hr = ADsOpenObject( L"LDAP://RootDSE",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&padsRootDSE);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;

        // Get the configurationNamingContext property.
        hr = padsRootDSE->Get(CComBSTR("configurationNamingContext"), &svar);
        if(SUCCEEDED(hr))
        {
            CComBSTR sbstrDN = "CN=Partitions,";
            sbstrDN += svar.bstrVal;
            DWORD dwChars = sbstrDN.Length() + 1;

            *ppwszPartitionsDN = (LPWSTR)AllocADsMem(dwChars * sizeof(WCHAR));
            
            if(*ppwszPartitionsDN)
            {
                wcsncpy_s(*ppwszPartitionsDN, sbstrDN.m_str, dwChars);
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
        
        padsRootDSE->Release();
    }

    return hr;
}
```



O exemplo Visual Basic código a seguir obtém o nome diferenciado do contêiner Partições criando manualmente o nome diferenciado.


```VB
'
'   GetPartitionsDNManual
'
'   Description: Gets the distinguished name of the Partitions container in
'   the current enterprise forest.
'
Function GetPartitionsDNManual()
    ' Bind to RootDSE.
    Set oRootDSE = GetObject("LDAP://RootDSE")
    
    ' Get the configurationNamingContext property.
    GetPartitionsDNManual = "CN=Partitions," + oRootDSE.Get("configurationNamingContext")
End Function
```



O exemplo de código C# a seguir obtém o nome diferenciado do contêiner Partitions pesquisando o contêiner de configuração para o [**objeto crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer) Este exemplo usa C# com System.DirectoryServices.


```CSharp
/***************************************************************************

    GetPartitionsDN()

    Description: Gets the distinguished name of the Partition container in 
    the current enterprise forest.

***************************************************************************/

static string GetPartitionsDN()
{
    // Bind to the RootDSE to get the configurationNamingContext property.
    DirectoryEntry RootDSE = new DirectoryEntry("LDAP://RootDSE");
    DirectoryEntry ConfigContainer = new DirectoryEntry("LDAP://" + 
        RootDSE.Properties["configurationNamingContext"].Value);

    // Search for an object that is of type crossRefContainer.
    DirectorySearcher ConfigSearcher = new DirectorySearcher(ConfigContainer);
    ConfigSearcher.Filter = "(&(objectClass=crossRefContainer))";
    ConfigSearcher.PropertiesToLoad.Add("distinguishedName");
    ConfigSearcher.SearchScope = SearchScope.OneLevel;

    SearchResult result = ConfigSearcher.FindOne();

    return result.Properties["distinguishedName"][0].ToString();
}
```



O exemplo Visual Basic código .NET a seguir obtém o nome diferenciado do contêiner De partição pesquisando o contêiner de configuração para o [**objeto crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer) Este exemplo usa Visual Basic .NET com System.DirectoryServices.


```VB
'**************************************************************************
'
'   GetPartitionsDN()
'
'
'   Description: Gets the distinguished name of the Partitions container in 
'   the current enterprise forest.
'
'**************************************************************************

Function GetPartitionsDN() As String
    ' Bind to the RootDSE to get the configurationNamingContext property.
    Dim RootDSE As New DirectoryEntry("LDAP://RootDSE")

    ' Bind to the Configuraiton container.
    Dim Path As String = "LDAP://" + RootDSE.Properties("configurationNamingContext").Value
    Dim ConfigContainer As New DirectoryEntry(Path)

    ' Search for an object that is of type crossRefContainer.
    Dim ConfigSearcher As New DirectorySearcher(ConfigContainer)
    ConfigSearcher.Filter = "(&(objectClass=crossRefContainer))"
    ConfigSearcher.SearchScope = SearchScope.OneLevel

    Dim result As SearchResult = ConfigSearcher.FindOne()

    Return result.Properties("distinguishedName")(0).ToString()
End Function
```



 

 
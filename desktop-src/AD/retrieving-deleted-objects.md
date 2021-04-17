---
title: Recuperando objetos excluídos
description: Os objetos excluídos são armazenados no contêiner objetos excluídos.
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- Recuperando o AD de objetos excluídos
- ANÚNCIO de objeto, recuperando objetos excluídos
- Active Directory, usando, recuperando objetos excluídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b2062c747e38bc0b3a9b1b793a102006c11512
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453909"
---
# <a name="retrieving-deleted-objects"></a>Recuperando objetos excluídos

Os objetos excluídos são armazenados no contêiner objetos excluídos. O contêiner objetos excluídos não é normalmente visível, mas o contêiner objetos excluídos pode ser associado por um membro do grupo Administradores. O conteúdo do contêiner de objetos excluídos pode ser enumerado e os atributos de objeto excluídos individuais podem ser obtidos usando a interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) com a preferência de pesquisa de **marcas de \_ \_ exclusão do ADS SEARCHPREF** .

O contêiner objetos excluídos pode ser obtido pela associação ao **\_ \_ \_ contêiner de objetos excluídos GUID** GUID bem conhecido definido em NTDSAPI. h. Para obter mais informações sobre a associação a GUIDs conhecidos, consulte [associação a objetos de Well-Known usando o WKGUID](binding-to-well-known-objects-using-wkguid.md).

Especifique a opção de **\_ \_ ligação rápida do ADS** ao associar ao contêiner de objetos excluídos. Isso significa que as interfaces ADSI usadas para trabalhar com um objeto em Active Directory Domain Services, como [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), não podem ser usadas no contêiner objetos excluídos. Para obter mais informações e um exemplo de código que mostra como associar ao contêiner de objetos excluídos, consulte a função de exemplo GetDeletedObjectsContainer abaixo.

-   [Enumerando objetos excluídos](#enumerating-deleted-objects)
-   [Localizando um objeto excluído específico](#finding-a-specific-deleted-object)
    -   [GetDeletedObjectsContainer](#getdeletedobjectscontainer)
    -   [EnumDeletedObjects](#enumdeletedobjects)
    -   [FindDeletedObjectByGUID](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a>Enumerando objetos excluídos

A interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) é usada para procurar objetos excluídos.

**Para enumerar objetos excluídos**

1.  Obtenha a interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para o contêiner objetos excluídos. Isso é feito ligando-se ao contêiner de objetos excluídos e solicitando a interface **IDirectorySearch** . Para obter mais informações e um exemplo de código que mostra como associar ao contêiner de objetos excluídos, consulte o exemplo de função **GetDeletedObjectsContainer** a seguir.
2.  Defina a preferência de pesquisa **\_ escopo de \_ pesquisa \_ do ADS SEARCHPREF** para o **\_ escopo ADS \_ onelevet** usando o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) . A preferência de **\_ \_ subárvore de escopo ADS** também pode ser usada, mas o contêiner de objetos excluídos é apenas um nível, portanto, usar a **\_ \_ subárvore de escopo ADS** é redundante.
3.  Defina a preferência de pesquisa de **\_ marcas de \_ exclusão do ADS SEARCHPREF** como **true**. Isso faz com que a pesquisa inclua objetos excluídos.
4.  Defina a preferência de pesquisa do **\_ SEARCHPREF \_ PageSize do ADS** com um valor menor que, ou igual a, 1000. Isso é opcional, mas se isso não for feito, mais de 1000 objetos excluídos poderão ser recuperados.
5.  Defina o filtro de pesquisa na chamada [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) para "(IsDeleted =**true**)". Isso faz com que a pesquisa recupere somente objetos com o atributo **IsDeleted** definido como **true**.

Para um código de exemplo de código que mostra como enumerar objetos excluídos, consulte o exemplo de função **EnumDeletedObjects** a seguir.

A pesquisa pode ser refinada ainda mais adicionando ao filtro de pesquisa, conforme mostrado no [dialeto LDAP](/windows/desktop/ADSI/ldap-dialect). Por exemplo, para pesquisar todos os objetos excluídos com um nome que comece com "Jeff", o filtro de pesquisa seria definido como "(& (IsDeleted =**true**) (CN = Jeff \* ))".

Como os objetos excluídos têm a maioria de seus atributos removidos quando são excluídos, não é possível associar diretamente a um objeto excluído. A opção de **\_ \_ ligação rápida do ADS** deve ser especificada durante a associação a um objeto excluído. Isso significa que as interfaces ADSI usadas para trabalhar com um objeto Active Directory Domain Services, como [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), não podem ser usadas em um contêiner de objeto excluído.

## <a name="finding-a-specific-deleted-object"></a>Localizando um objeto excluído específico

Também é possível localizar um objeto excluído específico. Se o **objectGUID** do objeto for conhecido, ele poderá ser usado para pesquisar o objeto com esse **objectGUID** específico. Para obter mais informações e um exemplo de código que mostra como localizar um objeto excluído específico, consulte **FindDeletedObjectByGUID** abaixo.

### <a name="getdeletedobjectscontainer"></a>GetDeletedObjectsContainer

O exemplo de código C++ a seguir mostra como associar ao contêiner objetos excluídos.


```C++
//***************************************************************************
//
//  GetDeletedObjectsContainer()
//
//  Binds to the Deleted Object container.
//
//***************************************************************************

HRESULT GetDeletedObjectsContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + wcslen(GUID_DELETED_OBJECTS_CONTAINER_W) + wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, GUID_DELETED_OBJECTS_CONTAINER_W, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_FAST_BIND | ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}

```



### <a name="enumdeletedobjects"></a>EnumDeletedObjects

O exemplo de código C++ a seguir mostra como enumerar os objetos no contêiner objetos excluídos.


```C++
//***************************************************************************
//
//  EnumDeletedObjects()
//
//  Enumerates all of the objects in the Deleted Objects container.
//
//***************************************************************************

HRESULT EnumDeletedObjects()
{
    HRESULT hr;
    IADsContainer *pDeletedObjectsCont = NULL;
    IDirectorySearch *pSearch = NULL;

    hr = GetDeletedObjectsContainer(&pDeletedObjectsCont);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    hr = pDeletedObjectsCont->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Only search for direct child objects of the container.
    ADS_SEARCHPREF_INFO rgSearchPrefs[3];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the page size.
    rgSearchPrefs[2].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
    rgSearchPrefs[2].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[2].vValue.Integer = 1000;

    // Set the search preference
    hr = pSearch->SetSearchPreference(rgSearchPrefs, ARRAYSIZE(rgSearchPrefs));
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    LPWSTR pszSearch = L"(cn=*)";

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search
    hr = pSearch->ExecuteSearch(    pszSearch,
                                    rgAttributes,
                                    ARRAYSIZE(rgAttributes),
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;
                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pDeletedObjectsCont)
    {
        pDeletedObjectsCont->Release();
    }

    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}

```



### <a name="finddeletedobjectbyguid"></a>FindDeletedObjectByGUID

O exemplo de código C++ a seguir mostra como localizar um objeto excluído específico da propriedade **objectGUID** do objeto.


```C++
HRESULT FindDeletedObjectByGUID(IADs *padsDomain, GUID *pguid)
{
    HRESULT hr;
    IDirectorySearch *pSearch = NULL;
    LPWSTR pwszGuid = NULL;

    hr = padsDomain->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Search the entire tree.
    ADS_SEARCHPREF_INFO rgSearchPrefs[2];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the search preference.
    hr = pSearch->SetSearchPreference(rgSearchPrefs, 2);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    LPWSTR pwszFormat = L"(objectGUID=%s)";

    LPWSTR pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
    if(NULL == pwszSearch)
    {
        goto cleanup;
    }
    
    swprintf_s(pwszSearch, pwszFormat, pwszGuid);
    
    FreeADsMem(pwszGuid);

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search.
    hr = pSearch->ExecuteSearch(    pwszSearch,
                                    rgAttributes,
                                    3,
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data.
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                GUID guid;
                                LPBYTE pb = col.pADsValues[x].OctetString.lpValue;
                                WCHAR wszGUID[MAX_PATH];

                                // Convert the octet string into a GUID.
                                guid.Data1 = *((long*)pb);
                                pb += sizeof(guid.Data1);
                                guid.Data2 = *((short*)pb);
                                pb += sizeof(guid.Data2);
                                guid.Data3 = *((short*)pb);
                                pb += sizeof(guid.Data3);
                                CopyMemory(&guid.Data4, pb, sizeof(guid.Data4));

                                // Convert the GUID into a string.
                                StringFromGUID2(guid, wszGUID, MAX_PATH);
                                wprintf(wszGUID);

                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                                OutputDebugStringW(wszGUID);
                                OutputDebugStringW(L"\n");

                                {
                                    DWORD a;

                                    for(a = 0, *wszGUID = 0; a < col.pADsValues[x].OctetString.dwLength; a++)
                                    {
                                        swprintf_s(wszGUID + lstrlenW(wszGUID), L"%02X", *(LPBYTE)(col.pADsValues[x].OctetString.lpValue + a));
                                    }

                                    OutputDebugStringW(wszGUID);
                                    OutputDebugStringW(L"\n");
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pwszSearch)
    {
        delete pwszSearch;
    }
    
    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}
```



 

 
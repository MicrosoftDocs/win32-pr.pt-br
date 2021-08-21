---
title: Código de exemplo para detecção de colisões de nomenclatura de esquema
description: Este tópico inclui um exemplo de código que detecta colisões de nomenclatura de esquema.
ms.assetid: e56cefcf-ea34-4217-9aa7-2f0d4a4d06a4
ms.tgt_platform: multiple
keywords:
- Código de exemplo para detectar o anúncio de colisões de nomenclatura de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7203cb9c1d03b02c77a57dde6ebfdda004f21792b7fab94bc37ccfe07e6b0eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694002"
---
# <a name="example-code-for-detecting-schema-naming-collisions"></a>Código de exemplo para detecção de colisões de nomenclatura de esquema

Este tópico inclui um exemplo de código que detecta colisões de nomenclatura de esquema.

O exemplo de código C/C++ a seguir consulta o esquema para os atributos de nomeação de chave em um objeto **classSchema** ou **attributeSchema** .

Retornará **true** se forem encontrados atributos ou classes conflitantes. Ele retornará **false** se o atributo ou classe com o **CN**, **lDAPDisplayName**, **OID**, **schemaIDGUID** ou **LinkId** especificado não entrar em conflito com o esquema e, portanto, for seguro para adicionar ao esquema.


```C++
/********************************************************************

    FindCollidingAttributesOrClasses()

********************************************************************/

HRESULT FindCollidingAttributesOrClasses(
    IDirectorySearch *pSchemaNC, // IDirectorySearch pointer to 
                                 // schema naming context.
    LPWSTR szName,
    LPWSTR szLDAPDisplayName,
    LPWSTR szOID,
    const GUID * pSchemaIDGUID,
    DWORD dwLinkID, // Value is zero (0) if the attribute is not linked,
                    // or if checking for class.
    BOOL *pfIsColliding)
{
    if (!pSchemaNC || 
        !szName ||
        !szLDAPDisplayName || 
        !szOID || 
        !pSchemaIDGUID)
    {
        return E_POINTER;
    }
 
    HRESULT hr = E_FAIL;
        
    LPWSTR szBuffer = NULL;
        
    hr = ADsEncodeBinaryData((LPBYTE)pSchemaIDGUID, 
                             sizeof(GUID), 
                             &szBuffer);
    if (SUCCEEDED(hr))
    {
        LPWSTR pwszFormatLinkID = L"(|(cn=%s)(lDAPDisplayName=%s)(attributeID=%s)(governsID=%s)(schemaIDGUID=%s)(linkID=%d))";
        LPWSTR pwszFormatNoLinkID = L"(|(cn=%s)(lDAPDisplayName=%s)(attributeID=%s)(governsID=%s)(schemaIDGUID=%s))";
        LPWSTR szFilter = new WCHAR[lstrlenW(pwszFormatLinkID) + 
                                    lstrlenW(szName) + 
                                    lstrlenW(szLDAPDisplayName) + 
                                    lstrlenW(szOID) + 
                                    lstrlenW(szOID) +
                                    lstrlenW(szBuffer) +
                                    20 +
                                    1];

        if(szFilter)
        {
            if (dwLinkID > 0L)
            {
                swprintf_s(szFilter,
                    pwszFormatLinkID,
                    szName,
                    szLDAPDisplayName,
                    szOID,
                    szOID,
                    szBuffer,
                    dwLinkID);
            }
            else
            {
                swprintf_s(szFilter,
                    pwszFormatNoLinkID,
                    szName,
                    szLDAPDisplayName,
                    szOID,
                    szOID,
                    szBuffer);
            }
            
            // Attributes are one-level deep in the Schema 
            // container so only search one level.
            ADS_SEARCHPREF_INFO SearchPrefs[2];
            SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
            SearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
            SearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

            SearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
            SearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER;
            SearchPrefs[1].vValue.Integer = 1000;
            
            int iCount = 0;
            
            // Set the search preference
            hr = pSchemaNC->SetSearchPreference(
                   SearchPrefs, 
                   sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO)
                 );
            if (SUCCEEDED(hr))
            {
                LPWSTR pszAttribs[] = {
                    L"lDAPDisplayName", 
                    L"cn", 
                    L"attributeID", 
                    L"governsID", 
                    L"schemaIDGUID", 
                    L"linkID", 
                    L"objectCategory"
                };

                // Handle used for searching
                ADS_SEARCH_HANDLE hSearch = NULL;
                DWORD x = 0L;
                
                hr = pSchemaNC->ExecuteSearch(szFilter,
                                pszAttribs,
                                sizeof(pszAttribs)/sizeof(LPWSTR),
                                &hSearch);
                if (SUCCEEDED(hr))
                {
                    // Call IDirectorySearch::GetNextRow() 
                    // to retrieve the next row  of data.
                    hr = pSchemaNC->GetFirstRow(hSearch);
                    while (hr != S_ADS_NOMORE_ROWS)
                    {
                        // Keep track of count.
                        iCount++;

                        // Get the next row
                        hr = pSchemaNC->GetNextRow(hSearch);
                    }
            
                    // Close the search handle to cleanup
                    pSchemaNC->CloseSearchHandle(hSearch);

                    if(SUCCEEDED(hr))
                    {
                        if (0 == iCount)
                        {
                            *pfIsColliding = FALSE;
                        }
                        else
                        {
                            *pfIsColliding = TRUE;
                        }

                        hr = S_OK;
                    }
                }
            }

            delete szFilter;
        }
            
        FreeADsMem(szBuffer);
    }
    
    return hr;
}
```



 

 





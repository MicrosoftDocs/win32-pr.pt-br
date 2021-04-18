---
title: Executando uma consulta de escopo de atributo
description: A consulta de escopo de atributo é uma preferência de pesquisa que permite a execução de uma pesquisa de atributos com valor de nome distinto de um objeto.
ms.assetid: 026fbe17-5df7-4007-9d74-5c0abbe793b1
ms.tgt_platform: multiple
keywords:
- Executando uma consulta de escopo de atributo ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, consulta de escopo de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10f5b666028c5fd46e7394b52a1328370e317bc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105752985"
---
# <a name="performing-an-attribute-scope-query"></a><span data-ttu-id="ef402-105">Executando uma consulta de escopo de atributo</span><span class="sxs-lookup"><span data-stu-id="ef402-105">Performing an Attribute Scope Query</span></span>

<span data-ttu-id="ef402-106">A consulta de escopo de atributo é uma preferência de pesquisa que permite a execução de uma pesquisa de atributos com valor de nome distinto de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ef402-106">The attribute scope query is a search preference that enables a search of an object's distinguished name valued attributes to be performed.</span></span> <span data-ttu-id="ef402-107">O atributo a ser pesquisado pode ser único ou com vários valores, mas deve ser do tipo de **\_ cadeia de \_ caracteres DN do ADS** .</span><span class="sxs-lookup"><span data-stu-id="ef402-107">The attribute to search can be either single or multi-valued, but must be of the **ADS\_DN\_STRING** type.</span></span> <span data-ttu-id="ef402-108">Quando a pesquisa for executada, a ADSI enumerará os valores de nome distinto do atributo e executará a pesquisa nos objetos representados pelos nomes distintos.</span><span class="sxs-lookup"><span data-stu-id="ef402-108">When the search is performed, ADSI will enumerate the distinguished name values of the attribute and perform the search on the objects represented by the distinguished names.</span></span> <span data-ttu-id="ef402-109">Por exemplo, se um atributo de pesquisa com escopo for executado do atributo [**Member**](/windows/desktop/ADSchema/a-member) de um objeto Group, a ADSI enumerará os nomes distintos no atributo **Member** e pesquisará cada um dos membros do grupo para os critérios de pesquisa especificados.</span><span class="sxs-lookup"><span data-stu-id="ef402-109">For example, if an attribute scoped search is performed of the [**member**](/windows/desktop/ADSchema/a-member) attribute of a group object, ADSI will enumerate the distinguished names in the **member** attribute and search each of the members of the group for the specified search criteria.</span></span>

<span data-ttu-id="ef402-110">Se uma consulta com escopo de atributo for executada em um atributo que não seja do **tipo \_ \_ cadeia de caracteres DN do ADS**, a pesquisa falhará.</span><span class="sxs-lookup"><span data-stu-id="ef402-110">If an attribute scoped query is performed on an attribute that is not of type **ADS\_DN\_STRING**, the search will fail.</span></span> <span data-ttu-id="ef402-111">A consulta com escopo de atributo também requer que a preferência de **\_ escopo de \_ pesquisa \_ do ADS SEARCHPREF** seja definida como **\_ \_ base de escopo ADS**.</span><span class="sxs-lookup"><span data-stu-id="ef402-111">The attribute scoped query also requires that the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference be set to **ADS\_SCOPE\_BASE**.</span></span> <span data-ttu-id="ef402-112">A preferência de **\_ escopo de \_ pesquisa \_ do ADS SEARCHPREF** será definida automaticamente como **\_ \_ base de escopo ADS**, mas se a preferência de **escopo de pesquisa do ADS \_ SEARCHPREF \_ \_** for definida como qualquer outro valor, [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) falhará com o **E ADS um \_ \_ \_ parâmetro insatisfatório**.</span><span class="sxs-lookup"><span data-stu-id="ef402-112">The **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference will automatically be set to **ADS\_SCOPE\_BASE**, but if the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference is set to any other value, [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) will fail with **E\_ADS\_BAD\_PARAMETER**.</span></span>

<span data-ttu-id="ef402-113">Os resultados de uma consulta de escopo de atributo podem abranger vários servidores e um servidor pode não retornar todos os dados solicitados para todas as linhas retornadas.</span><span class="sxs-lookup"><span data-stu-id="ef402-113">The results of an attribute-scope query may span multiple servers and a server may not return all the data requested for the all the rows returned.</span></span> <span data-ttu-id="ef402-114">Se isso ocorrer, quando a última linha for recuperada chamando [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ou [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), a ADSI retornará **s \_ anúncios \_ ERRORSOCCURRED** em vez de **s \_ anúncios e \_ mais \_ linhas**.</span><span class="sxs-lookup"><span data-stu-id="ef402-114">If this occurs, when the last row is retrieved by calling [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) or [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI will return **S\_ADS\_ERRORSOCCURRED** instead of **S\_ADS\_NOMORE\_ROWS**.</span></span>

<span data-ttu-id="ef402-115">Para especificar uma consulta de escopo de atributo, defina uma opção de pesquisa de **\_ consulta de \_ atributo \_ ADS SEARCHPREF** com um valor de **cadeia de \_ \_ \_ caracteres de ignorar caso de ADSTYPE** definido como o lDAPDisplayName do atributo para pesquisar na matriz de [**\_ \_ informações de SEARCHPREF de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="ef402-115">To specify an attribute scope query, set an **ADS\_SEARCHPREF\_ATTRIBUTE\_QUERY** search option with an **ADSTYPE\_CASE\_IGNORE\_STRING** value set to the lDAPDisplayName of the attribute to search in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="ef402-116">Essa operação é mostrada no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ef402-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
SearchPref.vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
SearchPref.vValue.Boolean = L"member";
```



<span data-ttu-id="ef402-117">O exemplo de código a seguir mostra como usar a opção de pesquisa de **\_ consulta de \_ atributo \_ ADS SEARCHPREF** .</span><span class="sxs-lookup"><span data-stu-id="ef402-117">The following code example shows how to use the **ADS\_SEARCHPREF\_ATTRIBUTE\_QUERY** search option.</span></span>


```C++
/***************************************************************************

    SearchGroupMembers()

    Searches the members of a group that are of type user and prints each 
    user's cn and distinguishedName values to the console.

    Parameters:

    pwszGroupDN - Contains the distinguished name of the group whose 
    members will be searched.

***************************************************************************/

HRESULT SearchGroupMembers(LPCWSTR pwszGroupDN)
{
    HRESULT hr;
    CComPtr<IDirectorySearch> spSearch;
    CComBSTR sbstrADsPath;
 
    // Bind to the group and get the IDirectorySearch interface.
    sbstrADsPath = "LDAP://";
    sbstrADsPath += pwszGroupDN;
    hr = ADsOpenObject(sbstrADsPath,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IDirectorySearch,
        (void**)&spSearch);
    if(FAILED(hr))
    {
        return hr;
    }
 
    ADS_SEARCHPREF_INFO SearchPrefs[1];

    // Set the ADS_SEARCHPREF_ATTRIBUTE_QUERY search preference.
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
    SearchPrefs[0].vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
    SearchPrefs[0].vValue.CaseIgnoreString = L"member";

    // Set the search preferences.
    hr = spSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO));
    if(FAILED(hr))
    {
        return hr;
    }

    ADS_SEARCH_HANDLE hSearch;
    
    // Create the search filter.
    LPWSTR pwszSearchFilter = L"(&(objectClass=user))";
 
    // Set attributes to return.
    LPWSTR rgpwszAttributes[] = {L"cn", L"distinguishedName"};
    DWORD dwNumAttributes = sizeof(rgpwszAttributes)/sizeof(LPWSTR);
 
    // Execute the search.
    hr = spSearch->ExecuteSearch(pwszSearchFilter,
        rgpwszAttributes,
        dwNumAttributes,
        &hSearch);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the first result row.
    hr = spSearch->GetFirstRow(hSearch);
    while(S_OK == hr)
    {
        ADS_SEARCH_COLUMN col;

        // Enumerate the retrieved attributes.
        for(DWORD i = 0; i < dwNumAttributes; i++)
        {
            hr = spSearch->GetColumn(hSearch, rgpwszAttributes[i], &col);
            if(SUCCEEDED(hr))
            {
                switch(col.dwADsType)
                {
                case ADSTYPE_DN_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].DNString);
                    break;

                case ADSTYPE_CASE_IGNORE_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].CaseExactString);
                    break;

                default:
                    break;
                }
                
                // Free the column.
                spSearch->FreeColumn(&col);
            }
        }
        
        // Get the next row.
        hr = spSearch->GetNextRow(hSearch);
    }

    // Close the search handle to cleanup.
    hr = spSearch->CloseSearchHandle(hSearch);

    return hr;
}
```



<span data-ttu-id="ef402-118">Quando essa pesquisa é executada e os resultados são enumerados, ele retorna o **nome**, o **número de telefone** e o **número de escritório** de todos os objetos de usuário contidos na lista de atributo de **membro** do grupo.</span><span class="sxs-lookup"><span data-stu-id="ef402-118">When this search is executed and the results are enumerated, it would return the **name**, **telephone number**, and **office number** of all of the user objects contained in the group's **member** attribute list.</span></span>

<span data-ttu-id="ef402-119">Tratamento de erro: os resultados de uma consulta de escopo de atributo podem abranger vários servidores e um servidor pode não retornar todos os dados solicitados para todas as linhas retornadas.</span><span class="sxs-lookup"><span data-stu-id="ef402-119">Error handling: The results of an attribute-scope query may span multiple servers and a server may not return all the data requested for the all the rows returned.</span></span> <span data-ttu-id="ef402-120">Se isso ocorrer, quando a última linha for recuperada chamando [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ou [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), a ADSI retornará **s \_ anúncios \_ ERRORSOCCURRED**, em vez de **s \_ anúncios, \_ mais \_ linhas**.</span><span class="sxs-lookup"><span data-stu-id="ef402-120">If this occurs, when the last row is retrieved by calling [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) or [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI will return **S\_ADS\_ERRORSOCCURRED**, instead of **S\_ADS\_NOMORE\_ROWS**.</span></span>

 

 
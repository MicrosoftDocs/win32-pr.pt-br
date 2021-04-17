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
# <a name="retrieving-deleted-objects"></a><span data-ttu-id="40f26-106">Recuperando objetos excluídos</span><span class="sxs-lookup"><span data-stu-id="40f26-106">Retrieving Deleted Objects</span></span>

<span data-ttu-id="40f26-107">Os objetos excluídos são armazenados no contêiner objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="40f26-107">Deleted objects are stored in the Deleted Objects container.</span></span> <span data-ttu-id="40f26-108">O contêiner objetos excluídos não é normalmente visível, mas o contêiner objetos excluídos pode ser associado por um membro do grupo Administradores.</span><span class="sxs-lookup"><span data-stu-id="40f26-108">The Deleted Objects container is not normally visible, but the Deleted Objects container can be bound to by a member of the administrators group.</span></span> <span data-ttu-id="40f26-109">O conteúdo do contêiner de objetos excluídos pode ser enumerado e os atributos de objeto excluídos individuais podem ser obtidos usando a interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) com a preferência de pesquisa de **marcas de \_ \_ exclusão do ADS SEARCHPREF** .</span><span class="sxs-lookup"><span data-stu-id="40f26-109">The contents of the Deleted Objects container can be enumerated and individual deleted object attributes can be obtained using the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface with the **ADS\_SEARCHPREF\_TOMBSTONE** search preference.</span></span>

<span data-ttu-id="40f26-110">O contêiner objetos excluídos pode ser obtido pela associação ao **\_ \_ \_ contêiner de objetos excluídos GUID** GUID bem conhecido definido em NTDSAPI. h.</span><span class="sxs-lookup"><span data-stu-id="40f26-110">The Deleted Objects container can be obtained by binding to the well-known GUID **GUID\_DELETED\_OBJECTS\_CONTAINER** defined in Ntdsapi.h.</span></span> <span data-ttu-id="40f26-111">Para obter mais informações sobre a associação a GUIDs conhecidos, consulte [associação a objetos de Well-Known usando o WKGUID](binding-to-well-known-objects-using-wkguid.md).</span><span class="sxs-lookup"><span data-stu-id="40f26-111">For more information about binding to well-known GUIDs, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span></span>

<span data-ttu-id="40f26-112">Especifique a opção de **\_ \_ ligação rápida do ADS** ao associar ao contêiner de objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="40f26-112">Specify the **ADS\_FAST\_BIND** option when binding to the Deleted Objects container.</span></span> <span data-ttu-id="40f26-113">Isso significa que as interfaces ADSI usadas para trabalhar com um objeto em Active Directory Domain Services, como [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), não podem ser usadas no contêiner objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="40f26-113">This means that the ADSI interfaces used to work with an object in Active Directory Domain Services, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on the Deleted Objects container.</span></span> <span data-ttu-id="40f26-114">Para obter mais informações e um exemplo de código que mostra como associar ao contêiner de objetos excluídos, consulte a função de exemplo GetDeletedObjectsContainer abaixo.</span><span class="sxs-lookup"><span data-stu-id="40f26-114">For more information and a code example that shows how to bind to the Deleted Objects container, see the GetDeletedObjectsContainer example function below.</span></span>

-   [<span data-ttu-id="40f26-115">Enumerando objetos excluídos</span><span class="sxs-lookup"><span data-stu-id="40f26-115">Enumerating Deleted Objects</span></span>](#enumerating-deleted-objects)
-   [<span data-ttu-id="40f26-116">Localizando um objeto excluído específico</span><span class="sxs-lookup"><span data-stu-id="40f26-116">Finding a Specific Deleted Object</span></span>](#finding-a-specific-deleted-object)
    -   [<span data-ttu-id="40f26-117">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="40f26-117">GetDeletedObjectsContainer</span></span>](#getdeletedobjectscontainer)
    -   [<span data-ttu-id="40f26-118">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="40f26-118">EnumDeletedObjects</span></span>](#enumdeletedobjects)
    -   [<span data-ttu-id="40f26-119">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="40f26-119">FindDeletedObjectByGUID</span></span>](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a><span data-ttu-id="40f26-120">Enumerando objetos excluídos</span><span class="sxs-lookup"><span data-stu-id="40f26-120">Enumerating Deleted Objects</span></span>

<span data-ttu-id="40f26-121">A interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) é usada para procurar objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="40f26-121">The [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface is used to search for deleted objects.</span></span>

<span data-ttu-id="40f26-122">**Para enumerar objetos excluídos**</span><span class="sxs-lookup"><span data-stu-id="40f26-122">**To enumerate deleted objects**</span></span>

1.  <span data-ttu-id="40f26-123">Obtenha a interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para o contêiner objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="40f26-123">Obtain the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface for the Deleted Objects container.</span></span> <span data-ttu-id="40f26-124">Isso é feito ligando-se ao contêiner de objetos excluídos e solicitando a interface **IDirectorySearch** .</span><span class="sxs-lookup"><span data-stu-id="40f26-124">This is accomplished by binding to the Deleted Objects container and requesting the **IDirectorySearch** interface.</span></span> <span data-ttu-id="40f26-125">Para obter mais informações e um exemplo de código que mostra como associar ao contêiner de objetos excluídos, consulte o exemplo de função **GetDeletedObjectsContainer** a seguir.</span><span class="sxs-lookup"><span data-stu-id="40f26-125">For more information and a code example that shows how to bind to the Deleted Objects container, see the following **GetDeletedObjectsContainer** function example.</span></span>
2.  <span data-ttu-id="40f26-126">Defina a preferência de pesquisa **\_ escopo de \_ pesquisa \_ do ADS SEARCHPREF** para o **\_ escopo ADS \_ onelevet** usando o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="40f26-126">Set the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** search preference to **ADS\_SCOPE\_ONELEVEL** using the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="40f26-127">A preferência de **\_ \_ subárvore de escopo ADS** também pode ser usada, mas o contêiner de objetos excluídos é apenas um nível, portanto, usar a **\_ \_ subárvore de escopo ADS** é redundante.</span><span class="sxs-lookup"><span data-stu-id="40f26-127">The **ADS\_SCOPE\_SUBTREE** preference can also be used, but the Deleted Objects container is only one level, so using **ADS\_SCOPE\_SUBTREE** is redundant.</span></span>
3.  <span data-ttu-id="40f26-128">Defina a preferência de pesquisa de **\_ marcas de \_ exclusão do ADS SEARCHPREF** como **true**.</span><span class="sxs-lookup"><span data-stu-id="40f26-128">Set the **ADS\_SEARCHPREF\_TOMBSTONE** search preference to **TRUE**.</span></span> <span data-ttu-id="40f26-129">Isso faz com que a pesquisa inclua objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="40f26-129">This causes the search to include deleted objects.</span></span>
4.  <span data-ttu-id="40f26-130">Defina a preferência de pesquisa do **\_ SEARCHPREF \_ PageSize do ADS** com um valor menor que, ou igual a, 1000.</span><span class="sxs-lookup"><span data-stu-id="40f26-130">Set the **ADS\_SEARCHPREF\_PAGESIZE** search preference to a value less than, or equal to, 1000.</span></span> <span data-ttu-id="40f26-131">Isso é opcional, mas se isso não for feito, mais de 1000 objetos excluídos poderão ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="40f26-131">This is optional, but if this is not done, no more than 1000 deleted objects can be retrieved.</span></span>
5.  <span data-ttu-id="40f26-132">Defina o filtro de pesquisa na chamada [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) para "(IsDeleted =**true**)".</span><span class="sxs-lookup"><span data-stu-id="40f26-132">Set the search filter in the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) call to "(isDeleted=**TRUE**)".</span></span> <span data-ttu-id="40f26-133">Isso faz com que a pesquisa recupere somente objetos com o atributo **IsDeleted** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="40f26-133">This causes the search to only retrieve objects with the **isDeleted** attribute set to **TRUE**.</span></span>

<span data-ttu-id="40f26-134">Para um código de exemplo de código que mostra como enumerar objetos excluídos, consulte o exemplo de função **EnumDeletedObjects** a seguir.</span><span class="sxs-lookup"><span data-stu-id="40f26-134">For a code example code that shows how to enumerate deleted objects, see the following **EnumDeletedObjects** function example.</span></span>

<span data-ttu-id="40f26-135">A pesquisa pode ser refinada ainda mais adicionando ao filtro de pesquisa, conforme mostrado no [dialeto LDAP](/windows/desktop/ADSI/ldap-dialect).</span><span class="sxs-lookup"><span data-stu-id="40f26-135">The search can be refined further by adding to the search filter as shown in [LDAP Dialect](/windows/desktop/ADSI/ldap-dialect).</span></span> <span data-ttu-id="40f26-136">Por exemplo, para pesquisar todos os objetos excluídos com um nome que comece com "Jeff", o filtro de pesquisa seria definido como "(& (IsDeleted =**true**) (CN = Jeff \* ))".</span><span class="sxs-lookup"><span data-stu-id="40f26-136">For example, to search for all of the deleted objects with a name that begins with "Jeff", the search filter would be set to "(&(isDeleted=**TRUE**)(cn=Jeff\*))".</span></span>

<span data-ttu-id="40f26-137">Como os objetos excluídos têm a maioria de seus atributos removidos quando são excluídos, não é possível associar diretamente a um objeto excluído.</span><span class="sxs-lookup"><span data-stu-id="40f26-137">Because deleted objects have most of their attributes removed when they are deleted, it is not possible to bind directly to a deleted object.</span></span> <span data-ttu-id="40f26-138">A opção de **\_ \_ ligação rápida do ADS** deve ser especificada durante a associação a um objeto excluído.</span><span class="sxs-lookup"><span data-stu-id="40f26-138">The **ADS\_FAST\_BIND** option must be specified when binding to a deleted object.</span></span> <span data-ttu-id="40f26-139">Isso significa que as interfaces ADSI usadas para trabalhar com um objeto Active Directory Domain Services, como [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), não podem ser usadas em um contêiner de objeto excluído.</span><span class="sxs-lookup"><span data-stu-id="40f26-139">This means that the ADSI interfaces used to work with an Active Directory Domain Services object, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on a deleted object container.</span></span>

## <a name="finding-a-specific-deleted-object"></a><span data-ttu-id="40f26-140">Localizando um objeto excluído específico</span><span class="sxs-lookup"><span data-stu-id="40f26-140">Finding a Specific Deleted Object</span></span>

<span data-ttu-id="40f26-141">Também é possível localizar um objeto excluído específico.</span><span class="sxs-lookup"><span data-stu-id="40f26-141">It is also possible to find a specific deleted object.</span></span> <span data-ttu-id="40f26-142">Se o **objectGUID** do objeto for conhecido, ele poderá ser usado para pesquisar o objeto com esse **objectGUID** específico.</span><span class="sxs-lookup"><span data-stu-id="40f26-142">If the **objectGUID** of the object is known, it can be used to search for the object with that specific **objectGUID**.</span></span> <span data-ttu-id="40f26-143">Para obter mais informações e um exemplo de código que mostra como localizar um objeto excluído específico, consulte **FindDeletedObjectByGUID** abaixo.</span><span class="sxs-lookup"><span data-stu-id="40f26-143">For more information and a code example that shows how to find a specific deleted object, see **FindDeletedObjectByGUID** below.</span></span>

### <a name="getdeletedobjectscontainer"></a><span data-ttu-id="40f26-144">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="40f26-144">GetDeletedObjectsContainer</span></span>

<span data-ttu-id="40f26-145">O exemplo de código C++ a seguir mostra como associar ao contêiner objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="40f26-145">The following C++ code example shows how to bind to the Deleted Objects container.</span></span>


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



### <a name="enumdeletedobjects"></a><span data-ttu-id="40f26-146">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="40f26-146">EnumDeletedObjects</span></span>

<span data-ttu-id="40f26-147">O exemplo de código C++ a seguir mostra como enumerar os objetos no contêiner objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="40f26-147">The following C++ code example shows how to enumerate the objects in the Deleted Objects container.</span></span>


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



### <a name="finddeletedobjectbyguid"></a><span data-ttu-id="40f26-148">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="40f26-148">FindDeletedObjectByGUID</span></span>

<span data-ttu-id="40f26-149">O exemplo de código C++ a seguir mostra como localizar um objeto excluído específico da propriedade **objectGUID** do objeto.</span><span class="sxs-lookup"><span data-stu-id="40f26-149">The following C++ code example shows how to find a specific deleted object from the object's **objectGUID** property.</span></span>


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



 

 
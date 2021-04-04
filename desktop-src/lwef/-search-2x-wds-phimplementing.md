---
title: Implementando um manipulador de protocolo para o WDS
description: A criação de um manipulador de protocolo envolve a implementação de ISearchProtocol para gerenciar objetos UrlAccessor, IUrlAccessor para gerar metadados sobre e identificar os filtros apropriados para os itens no armazenamento de dados, IProtocolHandlerSite para instanciar um objeto SearchProtocol e identificar os filtros apropriados e IFilterto filtrar arquivos proprietários ou enumerar e filtrar arquivos armazenados hierarquicamente.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084492"
---
# <a name="implementing-a-protocol-handler-for-wds"></a><span data-ttu-id="c84bd-103">Implementando um manipulador de protocolo para o WDS</span><span class="sxs-lookup"><span data-stu-id="c84bd-103">Implementing a Protocol Handler for WDS</span></span>

> [!NOTE]
> <span data-ttu-id="c84bd-104">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c84bd-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c84bd-105">Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c84bd-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="c84bd-106">A criação de um manipulador de protocolo envolve a implementação de [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) para gerenciar objetos UrlAccessor, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) para gerar metadados sobre e identificar os filtros apropriados para os itens no armazenamento de dados, IProtocolHandlerSite para instanciar um objeto SearchProtocol e identificar os filtros apropriados e o [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para filtrar arquivos proprietários ou para enumerar e filtrar arquivos armazenados hierarquicamente.</span><span class="sxs-lookup"><span data-stu-id="c84bd-106">Creating a protocol handler involves implementing [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) to generate metadata about and to identify appropriate filters for items in the data store, IProtocolHandlerSite to instantiate a SearchProtocol object and identify appropriate filters, and [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span> <span data-ttu-id="c84bd-107">O manipulador de protocolo deve ser multithread.</span><span class="sxs-lookup"><span data-stu-id="c84bd-107">The protocol handler must be multithreaded.</span></span>

<span data-ttu-id="c84bd-108">Estas seções contêm os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="c84bd-108">This sections contains the following topics:</span></span>

-   [<span data-ttu-id="c84bd-109">Observação sobre URLs</span><span class="sxs-lookup"><span data-stu-id="c84bd-109">Note on URLs</span></span>](#note-on-urls)
-   [<span data-ttu-id="c84bd-110">Interfaces de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c84bd-110">Protocol Handler Interfaces</span></span>](#protocol-handler-interfaces)
-   [<span data-ttu-id="c84bd-111">IFilters para contêineres</span><span class="sxs-lookup"><span data-stu-id="c84bd-111">IFilters for Containers</span></span>](#ifilters-for-containers)
-   [<span data-ttu-id="c84bd-112">Adicionando funcionalidade de opções de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c84bd-112">Adding Protocol Handler Options Functionality</span></span>](#adding-protocol-handler-options-functionality)
    -   [<span data-ttu-id="c84bd-113">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="c84bd-113">ISearchProtocolOptions</span></span>](#isearchprotocoloptions)
-   [<span data-ttu-id="c84bd-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c84bd-114">Related topics</span></span>](#related-topics)

## <a name="note-on-urls"></a><span data-ttu-id="c84bd-115">Observação sobre URLs</span><span class="sxs-lookup"><span data-stu-id="c84bd-115">Note on URLs</span></span>

<span data-ttu-id="c84bd-116">O Microsoft Windows Desktop Search (WDS) usa URLs para identificar exclusivamente os itens em um sistema de arquivos, dentro de uma loja do tipo banco de dados ou na Web.</span><span class="sxs-lookup"><span data-stu-id="c84bd-116">Microsoft Windows Desktop Search (WDS) uses URLs to uniquely identify items in a file system, inside a database-like store, or on the Web.</span></span> <span data-ttu-id="c84bd-117">Uma URL que define um nó de entrada é chamada de página inicial; O WDS começa nessa página inicial e rastreia recursivamente o armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="c84bd-117">A URL that defines an entry node is called a start page; WDS begins at that start page and recursively crawls the data store.</span></span> <span data-ttu-id="c84bd-118">A estrutura de URL típica é:</span><span class="sxs-lookup"><span data-stu-id="c84bd-118">The typical URL structure is:</span></span>

`protocol://host/path/name.extension`

> [!Note]
>
> <span data-ttu-id="c84bd-119">Quando desejar adicionar um novo armazenamento de dados, você precisará selecionar um nome para identificá-lo que não entre em conflito com os atuais.</span><span class="sxs-lookup"><span data-stu-id="c84bd-119">When you want to add a new data store, you'll need to select a name to identify it that does not conflict with current ones.</span></span> <span data-ttu-id="c84bd-120">Recomendamos esta Convenção de nomenclatura: companyName. Scheme.</span><span class="sxs-lookup"><span data-stu-id="c84bd-120">We recommend this naming convention: companyName.scheme.</span></span>

 

## <a name="protocol-handler-interfaces"></a><span data-ttu-id="c84bd-121">Interfaces de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c84bd-121">Protocol Handler Interfaces</span></span>

<span data-ttu-id="c84bd-122">**ISearchProtocol**</span><span class="sxs-lookup"><span data-stu-id="c84bd-122">**ISearchProtocol**</span></span>

<span data-ttu-id="c84bd-123">A interface [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) invoca, inicializa e gerencia objetos UrlAccessor.</span><span class="sxs-lookup"><span data-stu-id="c84bd-123">The [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) interface invokes, initializes, and manages UrlAccessor objects.</span></span> <span data-ttu-id="c84bd-124">Para obter mais informações sobre como implementar a interface ISearchProtocol, consulte **referência de interface ISearchProtocol**.</span><span class="sxs-lookup"><span data-stu-id="c84bd-124">For more information on implementing the ISearchProtocol interface, see **ISearchProtocol Interface reference**.</span></span>

<span data-ttu-id="c84bd-125">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="c84bd-125">**IUrlAccessor**</span></span>

<span data-ttu-id="c84bd-126">Para uma URL especificada, a interface [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) gera metadados sobre a estrutura de local, bem como itens contidos, e vincula esses itens a um filtro.</span><span class="sxs-lookup"><span data-stu-id="c84bd-126">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface generates metadata about the location structure as well as contained items, and it binds those items to an filter.</span></span> <span data-ttu-id="c84bd-127">O objeto **IUrlAccessor** é instanciado e inicializado por um objeto SearchProtocol; no entanto, você também pode implementar um método de inicialização interno para que o objeto **IUrlAccessor** possa executar tarefas de inicialização específicas para seu manipulador de protocolo, como validar a URL de um item que está sendo acessado ou verificar a hora da última modificação para determinar se um arquivo deve ser processado no rastreamento atual.</span><span class="sxs-lookup"><span data-stu-id="c84bd-127">The **IUrlAccessor** object is instantiated and initialized by an SearchProtocol object; however, you can also implement an internal initialization method so your **IUrlAccessor** object can perform initialization tasks specific to your protocol handler, such as validating the URL for an item being accessed or checking the last modified time to determine if a file must be processed in the current crawl.</span></span>

> [!Note]
>
> <span data-ttu-id="c84bd-128">Os horários modificados para diretórios são ignorados.</span><span class="sxs-lookup"><span data-stu-id="c84bd-128">Modified times for directories are ignored.</span></span> <span data-ttu-id="c84bd-129">O objeto [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) deve enumerar os objetos filho para determinar se houve modificações ou exclusões.</span><span class="sxs-lookup"><span data-stu-id="c84bd-129">The [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) object must enumerate the child objects to determine whether there have been any modifications or deletions.</span></span>

 

<span data-ttu-id="c84bd-130">Grande parte do design do objeto **UrlAccessor** depende se a estrutura é hierárquica ou baseada em link.</span><span class="sxs-lookup"><span data-stu-id="c84bd-130">Much of the design of the **UrlAccessor** object is dependent on whether the structure is hierarchical or link-based.</span></span> <span data-ttu-id="c84bd-131">Para armazenamentos de dados hierárquicos, o objeto **UrlAccessor** deve encontrar um filtro que possa enumerar seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c84bd-131">For hierarchical data stores, the **UrlAccessor** object must find an filter that can enumerate their contents.</span></span> <span data-ttu-id="c84bd-132">Outra distinção entre os manipuladores de protocolo hierárquico e baseado em link é o uso do método IsDirectory.</span><span class="sxs-lookup"><span data-stu-id="c84bd-132">Another distinction between hierarchical and link-based protocol handlers is the use of the IsDirectory method.</span></span> <span data-ttu-id="c84bd-133">Em manipuladores de protocolo baseado em link, esse método deve retornar S \_ false.</span><span class="sxs-lookup"><span data-stu-id="c84bd-133">In link-based protocol handlers, this method should return S\_FALSE.</span></span> <span data-ttu-id="c84bd-134">Os manipuladores de protocolo hierárquicos devem retornar S \_ OK para contêineres.</span><span class="sxs-lookup"><span data-stu-id="c84bd-134">Hierarchical protocol handlers must return S\_OK for containers.</span></span>

<span data-ttu-id="c84bd-135">Para obter mais instruções sobre como implementar uma interface [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) , consulte a referência da [**Interface IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) .</span><span class="sxs-lookup"><span data-stu-id="c84bd-135">For further instructions on implementing an [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface, see the [**IUrlAccessor Interface**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) reference.</span></span>

<span data-ttu-id="c84bd-136">**IProtocolHandlerSite**</span><span class="sxs-lookup"><span data-stu-id="c84bd-136">**IProtocolHandlerSite**</span></span>

<span data-ttu-id="c84bd-137">Essa interface é usada para criar uma instância de um objeto **SearchProtocol** e também fornece o objeto **UrlAccessor** com um filtro apropriado para uma ID de classe especificada (CLSID).</span><span class="sxs-lookup"><span data-stu-id="c84bd-137">This interface is used to instantiate a **SearchProtocol** object and also provides the **UrlAccessor** object with an appropriate filter for a specified class ID (CLSID).</span></span>

## <a name="ifilters-for-containers"></a><span data-ttu-id="c84bd-138">IFilters para contêineres</span><span class="sxs-lookup"><span data-stu-id="c84bd-138">IFilters for Containers</span></span>

<span data-ttu-id="c84bd-139">Se você estiver implementando um manipulador de protocolo hierárquico, deverá implementar um componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)de contêiner que enumere URLs que representam contêineres ou pastas.</span><span class="sxs-lookup"><span data-stu-id="c84bd-139">If you are implementing a hierarchical protocol handler, you must implement a container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component that enumerates URLs representing containers or folders.</span></span> <span data-ttu-id="c84bd-140">O processo de enumeração é um loop pelos métodos **GetChunk** e **GetValue** da interface IFilter que retornam uma lista de URLs que representam cada item no contêiner.</span><span class="sxs-lookup"><span data-stu-id="c84bd-140">The enumeration process is a loop through the **GetChunk** and **GetValue** methods of the IFilter interface that return a list of URLs that represent each item in the container.</span></span>

<span data-ttu-id="c84bd-141">Primeiro, **GetChunk** retorna um FULLPROSPEC com o conjunto de propriedades coletar \_ propset e:</span><span class="sxs-lookup"><span data-stu-id="c84bd-141">First, **GetChunk** returns a FULLPROSPEC with the property set GATHER\_PROPSET and either:</span></span>

-   <span data-ttu-id="c84bd-142">PID \_ GTHR \_ DIRLINK, a URL para o item sem a hora da última modificação ou</span><span class="sxs-lookup"><span data-stu-id="c84bd-142">PID\_GTHR\_DIRLINK, the URL to the item without the last modified time, or</span></span>
-   <span data-ttu-id="c84bd-143">PID \_ GTHR \_ DIRLINK \_ com \_ tempo, a URL junto com a hora da última modificação</span><span class="sxs-lookup"><span data-stu-id="c84bd-143">PID\_GTHR\_DIRLINK\_WITH\_TIME, the URL along with the last modified time</span></span>

<span data-ttu-id="c84bd-144">O GUID do conjunto de propriedades para coletar \_ propset é 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span><span class="sxs-lookup"><span data-stu-id="c84bd-144">The property set GUID for GATHER\_PROPSET is 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span></span> <span data-ttu-id="c84bd-145">A propriedade PROPSPEC é PID \_ GTHR \_ DIRLINK = 2 ou PID \_ GTHR \_ DIRLINK \_ com \_ time = 12 decimal.</span><span class="sxs-lookup"><span data-stu-id="c84bd-145">The PROPSPEC Property is either PID\_GTHR\_DIRLINK=2 or PID\_GTHR\_DIRLINK\_WITH\_TIME = 12 decimal.</span></span>

<span data-ttu-id="c84bd-146">Retornar o PID \_ GTHR \_ DIRLINK \_ com \_ tempo é mais eficiente, pois o indexador pode determinar imediatamente se o item precisa ser indexado sem chamar os métodos ISearchProtocol->CreateUrlAccessor () e IUrlAccessor->GetLastModified ().</span><span class="sxs-lookup"><span data-stu-id="c84bd-146">Returning PID\_GTHR\_DIRLINK\_WITH\_TIME is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the ISearchProtocol->CreateUrlAccessor() and IUrlAccessor->GetLastModified() methods.</span></span>

<span data-ttu-id="c84bd-147">Em seguida, **GetValue** retorna um PROPVARIANT para a URL (e a hora da última modificação, se usado), como:</span><span class="sxs-lookup"><span data-stu-id="c84bd-147">Then **GetValue** returns a PROPVARIANT for the URL (and last modified time if used), as either:</span></span>

-   <span data-ttu-id="c84bd-148">VT \_ LPWStr, a URL do item filho ou</span><span class="sxs-lookup"><span data-stu-id="c84bd-148">VT\_LPWSTR, the URL of the child item, or</span></span>
-   <span data-ttu-id="c84bd-149">Vetor da URL seguido por um FILETIME</span><span class="sxs-lookup"><span data-stu-id="c84bd-149">Vector of the URL followed by a FILETIME</span></span>

<span data-ttu-id="c84bd-150">O código de exemplo a seguir demonstra como criar o PID \_ GTHR \_ DIRLINK adequado \_ com \_ tempo.</span><span class="sxs-lookup"><span data-stu-id="c84bd-150">The following sample code demonstrates how to build the proper PID\_GTHR\_DIRLINK\_WITH\_TIME.</span></span>

> [!Note]
>
> <span data-ttu-id="c84bd-151">**ESSE CÓDIGO E AS INFORMAÇÕES SÃO FORNECIDOS "NO ESTADO EM QUE SE ENCONTRAM", SEM GARANTIAS DE QUALQUER TIPO, EXPRESSAS OU IMPLÍCITAS, INCLUINDO, MAS NÃO SE LIMITANDO ÀS GARANTIAS IMPLÍCITAS DE COMERCIALIZAÇÃO E/OU ADEQUAÇÃO A UMA FINALIDADE ESPECÍFICA.**</span><span class="sxs-lookup"><span data-stu-id="c84bd-151">**THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.**</span></span>
>
> <span data-ttu-id="c84bd-152">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c84bd-152">Copyright (C) Microsoft.</span></span> <span data-ttu-id="c84bd-153">Todos os direitos reservados.</span><span class="sxs-lookup"><span data-stu-id="c84bd-153">All rights reserved.</span></span>

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]
>
> <span data-ttu-id="c84bd-154">Um componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)do contêiner sempre deve enumerar todas as URLs filho, mesmo que as URLs filho não tenham sido alteradas, pois o indexador detecta as exclusões por meio do processo de enumeração.</span><span class="sxs-lookup"><span data-stu-id="c84bd-154">A container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component should always enumerate all child URLs even if the child URLs have not changed, because the Indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="c84bd-155">Se a saída de data em um DIR \_ links \_ com o \_ tempo indicar que os dados não foram alterados, o indexador não atualizará os dados para essa URL.</span><span class="sxs-lookup"><span data-stu-id="c84bd-155">If the date output in a DIR\_LINKS\_WITH\_TIME indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

<span data-ttu-id="c84bd-156">A URL física é a URL que o objeto **UrlAccessor** processa.</span><span class="sxs-lookup"><span data-stu-id="c84bd-156">The physical URL is the URL that the **UrlAccessor** object processes.</span></span> <span data-ttu-id="c84bd-157">Se o filtro não emitir um DisplayUrl amigável para o usuário, o WDS exibirá a URL física para o usuário como parte dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c84bd-157">If the filter does not emit a user-friendly DisplayUrl, WDS displays the physical URL to the user as part of the search results.</span></span> <span data-ttu-id="c84bd-158">O esquema do WDS contém duas propriedades para controlar o que é exibido para o usuário final, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c84bd-158">The WDS schema contains two properties to control what is displayed to the end user, as shown in the table below.</span></span>



| <span data-ttu-id="c84bd-159">GUID</span><span class="sxs-lookup"><span data-stu-id="c84bd-159">GUID</span></span>                                 | <span data-ttu-id="c84bd-160">PROPSPEC</span><span class="sxs-lookup"><span data-stu-id="c84bd-160">PROPSPEC</span></span>      | <span data-ttu-id="c84bd-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="c84bd-161">Description</span></span>                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| <span data-ttu-id="c84bd-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="c84bd-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="c84bd-163">DisplayFolder</span><span class="sxs-lookup"><span data-stu-id="c84bd-163">DisplayFolder</span></span> | <span data-ttu-id="c84bd-164">Caminho da pasta exibido para o usuário nos resultados da pesquisa</span><span class="sxs-lookup"><span data-stu-id="c84bd-164">Folder Path displayed to the user in search results</span></span> |
| <span data-ttu-id="c84bd-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="c84bd-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="c84bd-166">FolderName</span><span class="sxs-lookup"><span data-stu-id="c84bd-166">FolderName</span></span>    | <span data-ttu-id="c84bd-167">Nome de exibição da pasta pai</span><span class="sxs-lookup"><span data-stu-id="c84bd-167">Display name of the parent folder</span></span>                   |



 

<span data-ttu-id="c84bd-168">Se o seu código não emitir um DisplayFolder ou nome_da_pasta, esses valores serão computados a partir do DisplayUrl.</span><span class="sxs-lookup"><span data-stu-id="c84bd-168">If your code does not emit a DisplayFolder or FolderName, these values are computed from the DisplayUrl.</span></span> <span data-ttu-id="c84bd-169">As barras invertidas na URL denotam contêineres na loja ou no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c84bd-169">Forward slashes in the URL denote containers within the store or file system.</span></span>

## <a name="adding-protocol-handler-options-functionality"></a><span data-ttu-id="c84bd-170">Adicionando funcionalidade de opções de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c84bd-170">Adding Protocol Handler Options Functionality</span></span>

<span data-ttu-id="c84bd-171">Para que o manipulador de protocolo tenha uma página inicial padrão (e a URL do nó de entrada), você deve implementar a interface **ISearchProtocolOptions** .</span><span class="sxs-lookup"><span data-stu-id="c84bd-171">For your protocol handler to have a default start page (and entry node URL), you must implement the **ISearchProtocolOptions** interface.</span></span> <span data-ttu-id="c84bd-172">Em versões futuras do WDS, essa interface fornecerá ganchos para a caixa de diálogo de opções para uma experiência de usuário aprimorada.</span><span class="sxs-lookup"><span data-stu-id="c84bd-172">In future versions of WDS, this interface will provide hooks to the Options dialog for an enhanced user experience.</span></span> <span data-ttu-id="c84bd-173">Essa interface fornece a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="c84bd-173">This interface provides the following functionality:</span></span>

-   <span data-ttu-id="c84bd-174">Determina se os requisitos para seu manipulador de protocolo são atendidos.</span><span class="sxs-lookup"><span data-stu-id="c84bd-174">Determines whether the requirements for your protocol handler are met.</span></span> <span data-ttu-id="c84bd-175">Por exemplo, o armazenamento do manipulador de protocolo pode exigir acesso a um determinado aplicativo para indexar corretamente os dados do aplicativo, mas esse aplicativo não está disponível.</span><span class="sxs-lookup"><span data-stu-id="c84bd-175">For example, your protocol handler's store may require access to a given application to properly index the application's data but that application is unavailable.</span></span>
-   <span data-ttu-id="c84bd-176">Identifica os requisitos mínimos que seu manipulador de protocolo precisa para processar um item.</span><span class="sxs-lookup"><span data-stu-id="c84bd-176">Identifies the minimum requirements your protocol handler needs to process an item.</span></span> <span data-ttu-id="c84bd-177">Os requisitos podem ser expressos em uma descrição independente do usuário, localizada, como "Microsoft Outlook 2000 ou superior".</span><span class="sxs-lookup"><span data-stu-id="c84bd-177">Requirements can be expressed in a user-friendly, localized description, such as "Microsoft Outlook 2000 or greater."</span></span>
-   <span data-ttu-id="c84bd-178">Define as URLs que seu manipulador de protocolo deve processar por padrão.</span><span class="sxs-lookup"><span data-stu-id="c84bd-178">Defines the URLs your protocol handler should process by default.</span></span>

### <a name="isearchprotocoloptions"></a><span data-ttu-id="c84bd-179">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="c84bd-179">ISearchProtocolOptions</span></span>

<span data-ttu-id="c84bd-180">A tabela a seguir descreve os métodos que você precisa implementar para a interface **ISearchProtocolOptions** .</span><span class="sxs-lookup"><span data-stu-id="c84bd-180">The following table describes the methods you need to implement for the **ISearchProtocolOptions** interface.</span></span>



| <span data-ttu-id="c84bd-181">Método</span><span class="sxs-lookup"><span data-stu-id="c84bd-181">Method</span></span>               | <span data-ttu-id="c84bd-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="c84bd-182">Description</span></span>                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84bd-183">CheckRequirements</span><span class="sxs-lookup"><span data-stu-id="c84bd-183">CheckRequirements</span></span>    | <span data-ttu-id="c84bd-184">Determina se os requisitos mínimos de um manipulador de protocolo personalizado são atendidos</span><span class="sxs-lookup"><span data-stu-id="c84bd-184">Determines whether a custom protocol handler's minimum requirements are met</span></span>                             |
| <span data-ttu-id="c84bd-185">GetDefaultCrawlScope</span><span class="sxs-lookup"><span data-stu-id="c84bd-185">GetDefaultCrawlScope</span></span> | <span data-ttu-id="c84bd-186">Retorna uma lista de URLs padrão em um repositório especificado para um manipulador de protocolo personalizado</span><span class="sxs-lookup"><span data-stu-id="c84bd-186">Returns a list of default URLs within a specified store for a custom protocol handler</span></span>                   |
| <span data-ttu-id="c84bd-187">Getrequirements</span><span class="sxs-lookup"><span data-stu-id="c84bd-187">GetRequirements</span></span>      | <span data-ttu-id="c84bd-188">Identifica uma descrição independente do usuário e localizada de requisitos mínimos para um manipulador de protocolo personalizado</span><span class="sxs-lookup"><span data-stu-id="c84bd-188">Identifies a user-friendly, localized description of minimum requirements for a custom protocol handler</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c84bd-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c84bd-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c84bd-190">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c84bd-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c84bd-191">Notificando o índice das alterações</span><span class="sxs-lookup"><span data-stu-id="c84bd-191">Notifying the Index of Changes</span></span>](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="c84bd-192">Adicionando ícones, visualizações e menus de contexto com extensões de Shell</span><span class="sxs-lookup"><span data-stu-id="c84bd-192">Adding Icons, Previews, and Context Menus with Shell Extensions</span></span>](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="c84bd-193">Instalando e Registrando manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="c84bd-193">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 
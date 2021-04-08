---
description: Este tópico descreve como usar as interfaces que fornecem acesso a referências de página em um OM XPS.
ms.assetid: bb227536-3b29-4221-b2d5-bab5e9d91448
title: Trabalhando com interfaces IXpsOMPageReference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4526e6c561a962b77fa3f2fc62d56431359aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828762"
---
# <a name="working-with-ixpsompagereference-interfaces"></a><span data-ttu-id="0373a-103">Trabalhando com interfaces IXpsOMPageReference</span><span class="sxs-lookup"><span data-stu-id="0373a-103">Working with IXpsOMPageReference Interfaces</span></span>

<span data-ttu-id="0373a-104">Este tópico descreve como usar as interfaces que fornecem acesso a referências de página em um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="0373a-104">This topic describes how to use the interfaces that provide access to page references in an XPS OM.</span></span>



| <span data-ttu-id="0373a-105">Nome da interface</span><span class="sxs-lookup"><span data-stu-id="0373a-105">Interface name</span></span>                                                  | <span data-ttu-id="0373a-106">Interfaces filho lógicas</span><span class="sxs-lookup"><span data-stu-id="0373a-106">Logical child interfaces</span></span>                    | <span data-ttu-id="0373a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0373a-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0373a-108">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="0373a-108">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [<span data-ttu-id="0373a-109">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="0373a-109">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | <span data-ttu-id="0373a-110">Virtualiza o conteúdo de uma página de documento.</span><span class="sxs-lookup"><span data-stu-id="0373a-110">Virtualizes the content of a document page.</span></span> <br/> <span data-ttu-id="0373a-111">Uma referência de página contém informações básicas sobre a página, algumas propriedades de página e um link para o conteúdo da página.</span><span class="sxs-lookup"><span data-stu-id="0373a-111">A page reference contains basic information about the page, some page properties, and a link to the page contents.</span></span> <span data-ttu-id="0373a-112">A interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que compreende o conteúdo da página é retornada pelo método [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) .</span><span class="sxs-lookup"><span data-stu-id="0373a-112">The [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises page contents is returned by the [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) method.</span></span><br/> |
| [<span data-ttu-id="0373a-113">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="0373a-113">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | <span data-ttu-id="0373a-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0373a-114">None</span></span><br/>                             | <span data-ttu-id="0373a-115">Contém uma lista de itens de página que são destinos de hiperlink.</span><span class="sxs-lookup"><span data-stu-id="0373a-115">Contains a list of page items that are hyperlink targets.</span></span> <span data-ttu-id="0373a-116">A lista é retornada pelo método [**IXpsOMPageReference:: CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) .</span><span class="sxs-lookup"><span data-stu-id="0373a-116">The list is returned by the [**IXpsOMPageReference::CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) method.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="0373a-117">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="0373a-117">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | <span data-ttu-id="0373a-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0373a-118">None</span></span><br/>                             | <span data-ttu-id="0373a-119">Contém uma lista dos recursos baseados em parte associados à página.</span><span class="sxs-lookup"><span data-stu-id="0373a-119">Contains a list of the part-based resources that are associated with the page.</span></span> <span data-ttu-id="0373a-120">Essa lista é retornada pelo método [**IXpsOMPageReference:: CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) .</span><span class="sxs-lookup"><span data-stu-id="0373a-120">This list is returned by the [**IXpsOMPageReference::CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) method.</span></span><br/>                                                                                                                                     |



 

## <a name="code-examples"></a><span data-ttu-id="0373a-121">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="0373a-121">Code Examples</span></span>

<span data-ttu-id="0373a-122">Os exemplos de código a seguir ilustram como trabalhar com as interfaces de referência de página em um programa.</span><span class="sxs-lookup"><span data-stu-id="0373a-122">The following code examples illustrate how to work with the page reference interfaces in a program.</span></span>

-   [<span data-ttu-id="0373a-123">Obter o conteúdo da página</span><span class="sxs-lookup"><span data-stu-id="0373a-123">Get the page contents</span></span>](#get-the-page-contents)
-   [<span data-ttu-id="0373a-124">Obter a lista de destinos de hiperlink nesta página</span><span class="sxs-lookup"><span data-stu-id="0373a-124">Get the list of hyperlink targets on this page</span></span>](#get-the-list-of-hyperlink-targets-on-this-page)
-   [<span data-ttu-id="0373a-125">Obter os recursos da parte associados a esta página</span><span class="sxs-lookup"><span data-stu-id="0373a-125">Get the part resources that are associated with this page</span></span>](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a><span data-ttu-id="0373a-126">Obter o conteúdo da página</span><span class="sxs-lookup"><span data-stu-id="0373a-126">Get the page contents</span></span>

<span data-ttu-id="0373a-127">O exemplo de código a seguir obtém um ponteiro para a interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que inclui o conteúdo da página.</span><span class="sxs-lookup"><span data-stu-id="0373a-127">The following code example gets a pointer to the [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises the page contents.</span></span> <span data-ttu-id="0373a-128">Se a página não tiver sido carregada no OM XPS, como acontece quando o OM XPS é inicializado chamando [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), chamando [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) carregará a página no Om XPS.</span><span class="sxs-lookup"><span data-stu-id="0373a-128">If the page has not been loaded into the XPS OM, as happens when the XPS OM is initialized by calling [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), calling [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) will load the page into the XPS OM.</span></span>


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a><span data-ttu-id="0373a-129">Obter a lista de destinos de hiperlink nesta página</span><span class="sxs-lookup"><span data-stu-id="0373a-129">Get the list of hyperlink targets on this page</span></span>

<span data-ttu-id="0373a-130">O exemplo de código a seguir obtém um ponteiro para a interface [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) que contém a lista de itens de página que são destinos de hiperlink.</span><span class="sxs-lookup"><span data-stu-id="0373a-130">The following code example gets a pointer to the [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) interface that contains the list of page items that are hyperlink targets.</span></span> <span data-ttu-id="0373a-131">Se a página não tiver sido carregada no OM XPS, a lista de destinos de hiperlink será lida na marcação **PageContent. LinkTargets** .</span><span class="sxs-lookup"><span data-stu-id="0373a-131">If the page has not been loaded into the XPS OM, the list of hyperlink targets is read from the **PageContent.LinkTargets** markup.</span></span> <span data-ttu-id="0373a-132">Se a página tiver sido carregada, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) verificará cada elemento na página e retornará uma lista de elementos cujo atributo **IsHyperlinkTarget** é **true**.</span><span class="sxs-lookup"><span data-stu-id="0373a-132">If the page has been loaded, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) checks each element in the page and returns a list of elements whose **IsHyperlinkTarget** attribute is **TRUE**.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMPage                      *page = NULL;
    IXpsOMNameCollection            *linkTargets = NULL;

    UINT32 numTargets = 0;
    UINT32 thisTarget = 0;
    LPWSTR thisTargetName = NULL;

    // pageRef contains the current page reference 

    // if the page hasn't been loaded yet, for example, if the XPS OM 
    //  was loaded from an XPS document, CollectLinkTargets obtains the
    //  list of link targets from the <PageContent.LinkTargets> markup
    hr = pageRef->CollectLinkTargets(&linkTargets);

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);

    // after the page object has been loaded and calling GetPage or 
    //  by creating a page in the XPS OM, CollectLinkTargets will now check
    //  each of the page elements to return the list so this call to
    //  CollectLinkTargets might take longer to return than the previous
    //  call above if the XPS OM was created from a file
    linkTargets->Release(); // release previous collection
    hr = pageRef->CollectLinkTargets(&linkTargets);
    
    // walk the list of link targets returned
    hr = linkTargets->GetCount( &numTargets );
    thisTarget = 0;
    while (thisTarget < numTargets) {
        hr = linkTargets->GetAt (thisTarget, &thisTargetName);
        printf ("%s\n", thisTargetName);
        // release the target string returned to prevent memory leaks
        CoTaskMemFree (thisTargetName);
        // get next target in list
        thisTarget++;
    }
    // release page and the link target collection
    page->Release();
    linkTargets->Release();
```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="0373a-133">Obter os recursos da parte associados a esta página</span><span class="sxs-lookup"><span data-stu-id="0373a-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="0373a-134">O exemplo de código a seguir obtém as listas dos diferentes recursos que são usados por essa página.</span><span class="sxs-lookup"><span data-stu-id="0373a-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );
```



## <a name="related-topics"></a><span data-ttu-id="0373a-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0373a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0373a-136">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="0373a-136">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[<span data-ttu-id="0373a-137">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="0373a-137">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="0373a-138">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="0373a-138">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="0373a-139">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="0373a-139">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[<span data-ttu-id="0373a-140">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="0373a-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 





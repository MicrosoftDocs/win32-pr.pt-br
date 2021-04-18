---
description: Este tópico descreve como criar um OM XPS em branco.
ms.assetid: 5b6f12ba-9a41-4252-96c4-391bb8d75cd4
title: Criar um OM XPS em branco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0588fc11deb4b3d980e978dfe8a5370bc170d506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786223"
---
# <a name="create-a-blank-xps-om"></a><span data-ttu-id="7a0e1-103">Criar um OM XPS em branco</span><span class="sxs-lookup"><span data-stu-id="7a0e1-103">Create a Blank XPS OM</span></span>

<span data-ttu-id="7a0e1-104">Este tópico descreve como criar um OM XPS em branco.</span><span class="sxs-lookup"><span data-stu-id="7a0e1-104">This topic describes how to create a blank XPS OM.</span></span> <span data-ttu-id="7a0e1-105">Ele apresenta os exemplos de código que ilustram como usar um OM XPS para criar a estrutura do documento de um documento XPS que tem uma página em branco.</span><span class="sxs-lookup"><span data-stu-id="7a0e1-105">It presents the code examples that illustrate how to use an XPS OM to build the document structure of an XPS document that has one blank page.</span></span>

<span data-ttu-id="7a0e1-106">Para ser salvo como um documento XPS, o OM XPS requer pelo menos os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="7a0e1-106">To be saved as an XPS document, the XPS OM requires at least the following components:</span></span>

-   <span data-ttu-id="7a0e1-107">Um [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) que descreve o pacote de documento XPS</span><span class="sxs-lookup"><span data-stu-id="7a0e1-107">An [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) that describes the XPS document package</span></span>
-   <span data-ttu-id="7a0e1-108">Um [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) que contém a estrutura do conteúdo do pacote</span><span class="sxs-lookup"><span data-stu-id="7a0e1-108">An [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) that contains the framework of the package contents</span></span>
-   <span data-ttu-id="7a0e1-109">Um [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) que contém a estrutura de um documento dentro do pacote</span><span class="sxs-lookup"><span data-stu-id="7a0e1-109">An [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) that contains the framework of a document within the package</span></span>
-   <span data-ttu-id="7a0e1-110">Um [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) que contém a coleção de páginas no documento</span><span class="sxs-lookup"><span data-stu-id="7a0e1-110">An [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) that contains the collection of pages in the document</span></span>
-   <span data-ttu-id="7a0e1-111">Um [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que contém uma página em branco</span><span class="sxs-lookup"><span data-stu-id="7a0e1-111">An [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) that contains a blank page</span></span>

<span data-ttu-id="7a0e1-112">Quando essas interfaces são usadas, o OM XPS conterá um documento que tem uma página em branco.</span><span class="sxs-lookup"><span data-stu-id="7a0e1-112">When these interfaces are used, the XPS OM will contain a document that has one blank page.</span></span> <span data-ttu-id="7a0e1-113">Para criar esse documento em um OM XPS, o programa deve primeiro criar os componentes individuais e vinculá-los juntos.</span><span class="sxs-lookup"><span data-stu-id="7a0e1-113">To create this document in an XPS OM, the program must first create the individual components and then link them together.</span></span>

<span data-ttu-id="7a0e1-114">Antes de usar os exemplos de código a seguir, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="7a0e1-114">Before using the following code examples, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-examples"></a><span data-ttu-id="7a0e1-115">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="7a0e1-115">Code Examples</span></span>

<span data-ttu-id="7a0e1-116">O exemplo de código a seguir pressupõe que a inicialização, descrita em [inicializar um om XPS](xps-object-model-initialization.md), tenha sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7a0e1-116">The following code example assumes that the initialization, described in [Initialize an XPS OM](xps-object-model-initialization.md), has succeeded.</span></span>


```C++
    // Declare the variables used in this section.
    HRESULT                       hr = S_OK;
    IOpcPartUri                   *opcPartUri = NULL;
    IXpsOMPackage                 *xpsPackage = NULL;
    IXpsOMDocumentSequence        *xpsFDS = NULL;
    IXpsOMDocumentCollection      *fixedDocuments = NULL;
    IXpsOMDocument                *xpsFD = NULL;
    IXpsOMPage                    *xpsPage = NULL;
    IXpsOMPageReferenceCollection *pageRefs = NULL;
    IXpsOMPageReference           *xpsPageRef = NULL;
    // These values are set outside of this code example.
    XPS_SIZE pageSize = {width, height}; 
    
    // Create the package.
    hr = xpsFactory->CreatePackage( &xpsPackage );

    // Create the URI for the fixed document sequence part and then  
    //  create the fixed document sequence
    hr = xpsFactory->CreatePartUri( 
        L"/FixedDocumentSequence.fdseq", &opcPartUri );
    hr = xpsFactory->CreateDocumentSequence( opcPartUri, &xpsFDS );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create the URI for the document part and then create the document.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/FixedDocument.fdoc", &opcPartUri );
    hr = xpsFactory->CreateDocument( opcPartUri, &xpsFD );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a blank page.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/Pages/1.fpage", &opcPartUri );
    hr = xpsFactory->CreatePage(
        &pageSize,                  // Page size
        L"en-US",                   // Page language
        opcPartUri,                 // Page part name
        &xpsPage);                
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a page reference for the page.
    hr = xpsFactory->CreatePageReference( &pageSize, &xpsPageRef );

    // Add the fixed document sequence to the package.
    hr = xpsPackage->SetDocumentSequence( xpsFDS );

    // Get the document collection of the fixed document sequence
    //  and then add the document to the collection.
    hr = xpsFDS->GetDocuments( &fixedDocuments );
    hr = fixedDocuments->Append( xpsFD );

    // Get the page reference collection from the document
    //  and add the page reference and blank page.
    hr = xpsFD->GetPageReferences( &pageRefs );
    hr = pageRefs->Append( xpsPageRef );
    hr = xpsPageRef->SetPage( xpsPage );

    // Release interface pointer
    if (NULL != xpsPage) xpsPage->Release();
    if (NULL != pageRefs) pageRefs->Release();
    if (NULL != fixedDocuments) fixedDocuments->Release();
    if (NULL != xpsPageRef) xpsPageRef->Release();
    if (NULL != xpsFD) xpsFD->Release();
    if (NULL != xpsFDS) xpsFDS->Release();
    if (NULL != xpsPackage) xpsPackage->Release();

```



## <a name="best-practices"></a><span data-ttu-id="7a0e1-117">Práticas Recomendadas</span><span class="sxs-lookup"><span data-stu-id="7a0e1-117">Best Practices</span></span>

<span data-ttu-id="7a0e1-118">Depois de ter usado uma interface [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) para criar um componente (como depois de chamar o método **CreateDocument** no exemplo de código), libere o ponteiro para essa interface — a menos que você precise dele para outra chamada.</span><span class="sxs-lookup"><span data-stu-id="7a0e1-118">After you have used an [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) interface to create a component (such as after calling the **CreateDocument** method in the code example), release the pointer to that interface—unless you need it for another call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a0e1-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a0e1-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7a0e1-120">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="7a0e1-121">Navegar no OM XPS</span><span class="sxs-lookup"><span data-stu-id="7a0e1-121">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="7a0e1-122">Gravar texto em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="7a0e1-122">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="7a0e1-123">Desenhar gráficos em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="7a0e1-123">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="7a0e1-124">Coloque as imagens em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="7a0e1-124">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="7a0e1-125">**Usado nesta página**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-125">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="7a0e1-126">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-126">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="7a0e1-127">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-127">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="7a0e1-128">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-128">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="7a0e1-129">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-129">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="7a0e1-130">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-130">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="7a0e1-131">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-131">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="7a0e1-132">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-132">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="7a0e1-133">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-133">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="7a0e1-134">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-134">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="7a0e1-135">**tamanho do XPS \_**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-135">**XPS\_SIZE**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

<span data-ttu-id="7a0e1-136">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="7a0e1-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="7a0e1-137">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="7a0e1-137">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="7a0e1-138">API de empacotamento</span><span class="sxs-lookup"><span data-stu-id="7a0e1-138">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="7a0e1-139">Referência da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="7a0e1-139">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="7a0e1-140">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="7a0e1-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

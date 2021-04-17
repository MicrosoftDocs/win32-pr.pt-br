---
description: Este tópico descreve as interfaces que fornecem acesso aos componentes de nível de documento de um OM XPS.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Trabalhando com interfaces IXpsOMDocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299452195dc8f14ebd08508c3fd9a6e198781a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770619"
---
# <a name="working-with-ixpsomdocument-interfaces"></a><span data-ttu-id="2f78a-103">Trabalhando com interfaces IXpsOMDocument</span><span class="sxs-lookup"><span data-stu-id="2f78a-103">Working with IXpsOMDocument Interfaces</span></span>

<span data-ttu-id="2f78a-104">Este tópico descreve as interfaces que fornecem acesso aos componentes de nível de documento de um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="2f78a-104">This topic describes the interfaces that provide access to the document-level components of an XPS OM.</span></span>



| <span data-ttu-id="2f78a-105">Nome da interface</span><span class="sxs-lookup"><span data-stu-id="2f78a-105">Interface name</span></span>                                                                        | <span data-ttu-id="2f78a-106">Interfaces filho lógicas</span><span class="sxs-lookup"><span data-stu-id="2f78a-106">Logical child interfaces</span></span>                                      | <span data-ttu-id="2f78a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f78a-107">Description</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f78a-108">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="2f78a-108">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [<span data-ttu-id="2f78a-109">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="2f78a-109">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | <span data-ttu-id="2f78a-110">Representa uma única parte de FixedDocument e associa uma coleção de referências de página.</span><span class="sxs-lookup"><span data-stu-id="2f78a-110">Represents a single FixedDocument part and binds a collection of page references.</span></span><br/> <span data-ttu-id="2f78a-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) é a interface de coleção usada para iterar pelas interfaces [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) em um documento.</span><span class="sxs-lookup"><span data-stu-id="2f78a-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) is the collection interface that is used to iterate through the [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces in a document.</span></span><br/> |
| [<span data-ttu-id="2f78a-112">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="2f78a-112">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | <span data-ttu-id="2f78a-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2f78a-113">None</span></span><br/>                                               | <span data-ttu-id="2f78a-114">Representa a parte DocumentStructure.</span><span class="sxs-lookup"><span data-stu-id="2f78a-114">Represents the DocumentStructure part.</span></span><br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a><span data-ttu-id="2f78a-115">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="2f78a-115">Code Examples</span></span>

<span data-ttu-id="2f78a-116">Os exemplos de código nesta seção ilustram como algumas das interfaces de documento são usadas em um programa.</span><span class="sxs-lookup"><span data-stu-id="2f78a-116">The code examples in this section illustrate how some of the document interfaces are used in a program.</span></span>

### <a name="get-the-page-references-of-a-document"></a><span data-ttu-id="2f78a-117">Obter as referências de página de um documento</span><span class="sxs-lookup"><span data-stu-id="2f78a-117">Get the page references of a document</span></span>

<span data-ttu-id="2f78a-118">O exemplo de código a seguir obtém um ponteiro para o [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) que contém a lista de interfaces [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) para o documento que é referenciado pelo parâmetro *Doc* .</span><span class="sxs-lookup"><span data-stu-id="2f78a-118">The following code example gets a pointer to the [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) that contains the list of [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces for the document that is referenced by *doc* parameter.</span></span>


```C++
    HRESULT                               hr = S_OK;


    IXpsOMPageReferenceCollection         *pages;
    IXpsOMPageReference                   *pageRef;
    IXpsOMPage                            *page;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // get the doc contents
    hr = doc->GetPageReferences(&pages);
        
    // walk the collection of page references
    hr = pages->GetCount(&numPageRefs);
    thisPageRef = 0;
    while (thisPageRef < numPageRefs) {
        // get this page reference
        hr = pages->GetAt(thisPageRef, &pageRef);

        // get the page content of this page reference
        hr = pageRef->GetPage (&page);

        // use the page

        // free this page & page reference and go to next
        page->Release();
        pageRef->Release();
        thisPageRef++;
    }

    pages->Release();
```



### <a name="get-the-document-structure-of-a-document"></a><span data-ttu-id="2f78a-119">Obter a estrutura do documento de um documento</span><span class="sxs-lookup"><span data-stu-id="2f78a-119">Get the document structure of a document</span></span>

<span data-ttu-id="2f78a-120">O exemplo de código a seguir obtém o recurso que contém a estrutura do documento.</span><span class="sxs-lookup"><span data-stu-id="2f78a-120">The following code example gets the resource that contains the document structure.</span></span>


```C++
    HRESULT                             hr = S_OK;
    
    IXpsOMDocumentStructureResource     *docStruct;
    IStream                             *docStructResStream;

    // doc is passed in as an argument
    // get the doc contents
    hr = doc->GetDocumentStructureResource(&docStruct);
   
    hr = docStruct->GetStream ( &docStructResStream );

    // access the document structure resource 
    //  contents by reading from the stream

    docStructResStream->Release();
    docStruct->Release();

```



 

 





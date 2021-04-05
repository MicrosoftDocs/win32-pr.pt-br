---
description: As interfaces de pacote representam o nível superior do OM XPS, que corresponde a um arquivo de documento XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Interfaces de pacote do XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827788"
---
# <a name="xps-om-package-interfaces"></a><span data-ttu-id="68f2b-103">Interfaces de pacote do XPS OM</span><span class="sxs-lookup"><span data-stu-id="68f2b-103">XPS OM Package Interfaces</span></span>

<span data-ttu-id="68f2b-104">As interfaces de pacote representam o nível superior do OM XPS, que corresponde a um arquivo de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="68f2b-104">The package interfaces represent the top level of the XPS OM, which corresponds to an XPS document file.</span></span> <span data-ttu-id="68f2b-105">Essas interfaces contêm métodos que serializam um OM XPS para um documento ou fluxo XPS e desserializam um pacote XPS para criar um OM XPS que permite que um programa acesse o conteúdo de um documento.</span><span class="sxs-lookup"><span data-stu-id="68f2b-105">These interfaces contain methods that serialize an XPS OM to an XPS document or stream, and deserialize an XPS package to create an XPS OM that enables a program to access the contents of a document.</span></span>



| <span data-ttu-id="68f2b-106">Nome da interface</span><span class="sxs-lookup"><span data-stu-id="68f2b-106">Interface name</span></span>                                                  | <span data-ttu-id="68f2b-107">Interfaces filho lógicas</span><span class="sxs-lookup"><span data-stu-id="68f2b-107">Logical child interfaces</span></span>                                                                                                            | <span data-ttu-id="68f2b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="68f2b-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68f2b-109">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="68f2b-109">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [<span data-ttu-id="68f2b-110">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="68f2b-110">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="68f2b-111">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="68f2b-111">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="68f2b-112">O OM XPS completo que corresponde ao pacote que contém o documento XPS.</span><span class="sxs-lookup"><span data-stu-id="68f2b-112">The complete XPS OM that corresponds to the package that contains the XPS document.</span></span><br/> |
| [<span data-ttu-id="68f2b-113">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="68f2b-113">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | <span data-ttu-id="68f2b-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="68f2b-114">None</span></span><br/>                                                                                                                     | <span data-ttu-id="68f2b-115">Habilita a serialização incremental de páginas de documento para um pacote.</span><span class="sxs-lookup"><span data-stu-id="68f2b-115">Enables incremental serialization of document pages to a package.</span></span><br/>                   |
| [<span data-ttu-id="68f2b-116">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="68f2b-116">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="68f2b-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="68f2b-117">None</span></span><br/>                                                                                                                     | <span data-ttu-id="68f2b-118">Acessa os metadados do documento.</span><span class="sxs-lookup"><span data-stu-id="68f2b-118">Accesses the document metadata.</span></span> <br/>                                                    |



 

## <a name="code-examples"></a><span data-ttu-id="68f2b-119">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="68f2b-119">Code Examples</span></span>

<span data-ttu-id="68f2b-120">Os exemplos de código a seguir ilustram como algumas das interfaces de pacote são usadas por um programa.</span><span class="sxs-lookup"><span data-stu-id="68f2b-120">The code examples that follow illustrate how some of the package interfaces are used by a program.</span></span> <span data-ttu-id="68f2b-121">A menos que indicado de outra forma, todos os itens em itálico são nomes de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="68f2b-121">Unless noted otherwise, all italicized items are parameter names.</span></span>

-   [<span data-ttu-id="68f2b-122">Ler um documento XPS em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="68f2b-122">Read an XPS document into an XPS OM</span></span>](#read-an-xps-document-into-an-xps-om)
-   [<span data-ttu-id="68f2b-123">Gravar um OM XPS em um arquivo de documento XPS</span><span class="sxs-lookup"><span data-stu-id="68f2b-123">Write an XPS OM to an XPS document file</span></span>](#write-an-xps-om-to-an-xps-document-file)
-   [<span data-ttu-id="68f2b-124">Acessar a sequência de documentos do OM XPS</span><span class="sxs-lookup"><span data-stu-id="68f2b-124">Access the document sequence of the XPS OM</span></span>](#access-the-document-sequence-of-the-xps-om)
-   [<span data-ttu-id="68f2b-125">Acessar as coreProperties do documento</span><span class="sxs-lookup"><span data-stu-id="68f2b-125">Access the document's CoreProperties</span></span>](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="68f2b-126">Ler um documento XPS em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="68f2b-126">Read an XPS document into an XPS OM</span></span>

<span data-ttu-id="68f2b-127">A partir de um documento XPS existente cujo nome de arquivo é armazenado em *xpsDocumentFilename*, este exemplo de código cria um om XPS que é referenciado por *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="68f2b-127">From an existing XPS document whose file name is stored in *xpsDocumentFilename*, this code example creates an XPS OM that is referenced by *xpsPackage*.</span></span>


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a><span data-ttu-id="68f2b-128">Gravar um OM XPS em um arquivo de documento XPS</span><span class="sxs-lookup"><span data-stu-id="68f2b-128">Write an XPS OM to an XPS document file</span></span>

<span data-ttu-id="68f2b-129">O exemplo de código a seguir grava o OM XPS que é referenciado por *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="68f2b-129">The following code example writes the XPS OM that is referenced by *xpsPackage*.</span></span> <span data-ttu-id="68f2b-130">O exemplo cria um documento XPS no arquivo cujo nome é armazenado em *filename*.</span><span class="sxs-lookup"><span data-stu-id="68f2b-130">The example creates an XPS document in the file whose name is stored in *fileName*.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a><span data-ttu-id="68f2b-131">Acessar a sequência de documentos do OM XPS</span><span class="sxs-lookup"><span data-stu-id="68f2b-131">Access the document sequence of the XPS OM</span></span>

<span data-ttu-id="68f2b-132">O exemplo de código a seguir obtém um ponteiro para a interface [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , que contém a sequência de documento do OM XPS representado por *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="68f2b-132">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface, which contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a><span data-ttu-id="68f2b-133">Acessar as coreProperties do documento</span><span class="sxs-lookup"><span data-stu-id="68f2b-133">Access the document's CoreProperties</span></span>

<span data-ttu-id="68f2b-134">O exemplo de código a seguir obtém um ponteiro para a interface [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , permitindo que o programa acesse o conteúdo da parte coreProperties.</span><span class="sxs-lookup"><span data-stu-id="68f2b-134">The following is code example obtains a pointer to the [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) interface, allowing the program to access the contents of the CoreProperties part.</span></span> <span data-ttu-id="68f2b-135">No exemplo, presume-se que o documento tenha sido lido em um OM XPS representado por *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="68f2b-135">In the example, the document is assumed to have been read into an XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a><span data-ttu-id="68f2b-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68f2b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68f2b-137">Usando a interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="68f2b-137">Using the IXpsOMPackageWriter Interface</span></span>](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[<span data-ttu-id="68f2b-138">Navegar no OM XPS</span><span class="sxs-lookup"><span data-stu-id="68f2b-138">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="68f2b-139">**Interface IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="68f2b-139">**IXpsOMDocumentSequence Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="68f2b-140">**Interface IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="68f2b-140">**IXpsOMPackage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="68f2b-141">**Interface IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="68f2b-141">**IXpsOMPackageWriter Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="68f2b-142">**Interface IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="68f2b-142">**IXpsOMCoreProperties Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 





---
description: Este tópico descreve como usar as interfaces que fornecem acesso ao FixedDocumentSequence, que é o nível superior da hierarquia de documentos em um OM XPS.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Trabalhando com interfaces IXpsOMDocumentSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f108cbadf735b334f758102915abbda239a4e974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811471"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a><span data-ttu-id="915bb-103">Trabalhando com interfaces IXpsOMDocumentSequence</span><span class="sxs-lookup"><span data-stu-id="915bb-103">Working with IXpsOMDocumentSequence Interfaces</span></span>

<span data-ttu-id="915bb-104">Este tópico descreve como usar as interfaces que fornecem acesso ao FixedDocumentSequence, que é o nível superior da hierarquia de documentos em um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="915bb-104">This topic describes how to use the interfaces that provide access to the FixedDocumentSequence, which is the top level of the document hierarchy in an XPS OM.</span></span>



| <span data-ttu-id="915bb-105">Nome da interface</span><span class="sxs-lookup"><span data-stu-id="915bb-105">Interface name</span></span>                                                          | <span data-ttu-id="915bb-106">Interfaces filho lógicas</span><span class="sxs-lookup"><span data-stu-id="915bb-106">Logical child interfaces</span></span>                            | <span data-ttu-id="915bb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="915bb-107">Description</span></span>                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="915bb-108">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="915bb-108">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [<span data-ttu-id="915bb-109">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="915bb-109">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | <span data-ttu-id="915bb-110">Agrupa um conjunto de FixedDocuments em uma lista ordenada.</span><span class="sxs-lookup"><span data-stu-id="915bb-110">Groups a set of FixedDocuments into an ordered list.</span></span><br/>          |
| [<span data-ttu-id="915bb-111">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="915bb-111">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | <span data-ttu-id="915bb-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="915bb-112">None</span></span><br/>                                     | <span data-ttu-id="915bb-113">A coleção de FixedDocuments em uma sequência de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="915bb-113">The collection of FixedDocuments in an XPS document sequence.</span></span><br/> |



 

## <a name="code-example"></a><span data-ttu-id="915bb-114">Exemplo de código</span><span class="sxs-lookup"><span data-stu-id="915bb-114">Code Example</span></span>

<span data-ttu-id="915bb-115">O exemplo de código a seguir obtém um ponteiro para a interface [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) que contém a sequência de documento do OM XPS representado por *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="915bb-115">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface that contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span> <span data-ttu-id="915bb-116">Em seguida, o exemplo enumera os documentos na coleção.</span><span class="sxs-lookup"><span data-stu-id="915bb-116">The example then enumerates the documents in the collection.</span></span>


```C++
    HRESULT                         hr = S_OK;

    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
 
        // use this doc for something

        // release this doc and then go to the next one
        doc->Release();
        thisDoc++;
    }
    // release the document collection and
    // the document sequence
    docs->Release();
    docSeq->Release();
```



 

 





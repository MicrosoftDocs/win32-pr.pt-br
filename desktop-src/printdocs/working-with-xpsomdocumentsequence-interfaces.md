---
description: Este tópico descreve como usar as interfaces que fornecem acesso ao FixedDocumentSequence, que é o nível superior da hierarquia de documentos em um OM XPS.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Trabalhando com interfaces IXpsOMDocumentSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edac74809de63c1ae4e688bb99214d11b091ee4e877c921e9280abc9c6868121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098658"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a>Trabalhando com interfaces IXpsOMDocumentSequence

Este tópico descreve como usar as interfaces que fornecem acesso ao FixedDocumentSequence, que é o nível superior da hierarquia de documentos em um OM XPS.



| Nome da interface                                                          | Interfaces filho lógicas                            | Descrição                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | Grupos de um conjunto de FixedDocuments em uma lista ordenada.<br/>          |
| [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | Nenhum<br/>                                     | A coleção de FixedDocuments em uma sequência de documentos XPS.<br/> |



 

## <a name="code-example"></a>Exemplo de código

O exemplo de código a seguir obtém um ponteiro para a interface [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) que contém a sequência de documentos do OM XPS representada por *xpsPackage*. Em seguida, o exemplo enumera os documentos na coleção.


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



 

 





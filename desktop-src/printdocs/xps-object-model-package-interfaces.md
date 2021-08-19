---
description: As interfaces de pacote representam o nível superior do OM XPS, que corresponde a um arquivo de documento XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Interfaces de pacote do XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6732531e3874046bbd174c363db24e304da95b9596b810014abb52a795e720c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886136"
---
# <a name="xps-om-package-interfaces"></a>Interfaces de pacote do XPS OM

As interfaces de pacote representam o nível superior do OM XPS, que corresponde a um arquivo de documento XPS. Essas interfaces contêm métodos que serializam um OM XPS para um documento ou fluxo XPS e desserializam um pacote XPS para criar um OM XPS que permite que um programa acesse o conteúdo de um documento.



| Nome da interface                                                  | Interfaces filho lógicas                                                                                                            | Descrição                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | O OM XPS completo que corresponde ao pacote que contém o documento XPS.<br/> |
| [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | Nenhum<br/>                                                                                                                     | Habilita a serialização incremental de páginas de documento para um pacote.<br/>                   |
| [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | Nenhum<br/>                                                                                                                     | Acessa os metadados do documento. <br/>                                                    |



 

## <a name="code-examples"></a>Exemplos de código

Os exemplos de código a seguir ilustram como algumas das interfaces de pacote são usadas por um programa. A menos que indicado de outra forma, todos os itens em itálico são nomes de parâmetro.

-   [Ler um documento XPS em um OM XPS](#read-an-xps-document-into-an-xps-om)
-   [Gravar um OM XPS em um arquivo de documento XPS](#write-an-xps-om-to-an-xps-document-file)
-   [Acessar a sequência de documentos do OM XPS](#access-the-document-sequence-of-the-xps-om)
-   [Acessar as coreProperties do documento](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>Ler um documento XPS em um OM XPS

A partir de um documento XPS existente cujo nome de arquivo é armazenado em *xpsDocumentFilename*, este exemplo de código cria um om XPS que é referenciado por *xpsPackage*.


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



### <a name="write-an-xps-om-to-an-xps-document-file"></a>Gravar um OM XPS em um arquivo de documento XPS

O exemplo de código a seguir grava o OM XPS que é referenciado por *xpsPackage*. O exemplo cria um documento XPS no arquivo cujo nome é armazenado em *filename*.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>Acessar a sequência de documentos do OM XPS

O exemplo de código a seguir obtém um ponteiro para a interface [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , que contém a sequência de documento do OM XPS representado por *xpsPackage*.


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



### <a name="access-the-documents-coreproperties"></a>Acessar as coreProperties do documento

O exemplo de código a seguir obtém um ponteiro para a interface [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , permitindo que o programa acesse o conteúdo da parte coreProperties. No exemplo, presume-se que o documento tenha sido lido em um OM XPS representado por *xpsPackage*.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a interface IXpsOMPackageWriter](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[Navegar no OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[**Interface IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**Interface IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Interface IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**Interface IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 





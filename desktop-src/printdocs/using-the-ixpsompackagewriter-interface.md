---
description: A interface IXpsOMPackageWriter cria um arquivo de documento XPS no qual os aplicativos podem gravar o conteúdo das interfaces IXpsOMPage de um OM XPS.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Usando a interface IXpsOMPackageWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8a34a0538ff09cc050ac287d5314be93f0da8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784645"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Usando a interface IXpsOMPackageWriter

A interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) cria um arquivo de documento XPS no qual os aplicativos podem gravar o conteúdo das interfaces [**IXPSOMPAGE**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) de um om XPS. A interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) é mais útil quando o conteúdo do documento está sendo processado ou criado sequencialmente. Ao contrário dos métodos [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) e [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) da interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) , a interface **IXpsOMPackageWriter** deve ser usada nem o FixedDocument inteiro, nem o FixedDocumentSequence precisa ser concluído.

## <a name="overview"></a>Visão geral

A interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) grava uma página por vez, na primeira página de um documento XPS até o último. A interface pode ser usada para criar arquivos de documento XPS simples e também arquivos de documento XPS complexos que contêm mais de um FixedDocument no FixedDocumentSequence. Em arquivos de documento XPS complexos, os FixedDocuments também são criados em sequência, começando com o primeiro FixedDocument no FixedDocumentSequence. A interface **IXpsOMPackageWriter** não oferece suporte à criação de conteúdo do documento em ordem aleatória. Use-o, por exemplo, para criar um relatório sequencial ou para executar o processamento em um filtro de driver de dispositivo em que o conteúdo do documento é alimentado para o driver em sequência.

## <a name="terminology-review"></a>Revisão da terminologia

Um *arquivo de documento XPS* é um pacote OPC (Open Packaging Conventions) que está em conformidade com a especificação de papel XML. Portanto, tecnicamente, a interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) cria um *pacote OPC*, mas é um pacote OPC que está em conformidade com a especificação de papel XML. Por esse motivo, em discussões sobre documentos XPS, os termos *documento XPS* e *pacote* são frequentemente usados de maneira intercambiável.

O *pacote* criado pela interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) conterá os componentes de documento XPS necessários: um FixedDocumentSequence, pelo menos um FixedDocument e pelo menos um FixedPage. O FixedDocumentSequence é criado quando a interface **IXpsOMPackageWriter** é instanciada. Um FixedDocument é criado toda vez que [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) é chamado e um FixedPage é criado toda vez que [**IXpsOMPackageWriter:: AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) é chamado. Como a interface grava o conteúdo do documento em sequência, o método **AddPage** adiciona a página ao FixedDocument criado mais recentemente.

## <a name="using-the-ixpsompackagewriter-interface"></a>Usando a interface IXpsOMPackageWriter

O procedimento a seguir descreve como criar um arquivo de documento XPS usando a interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) . O procedimento não descreve como criar uma instância de uma interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) e seu conteúdo. Para obter mais informações sobre **IXpsOMPage** e adicionar conteúdo a uma página, consulte [interfaces de página do XPS OM](xps-object-model-page-interfaces.md) e os tópicos listados na seção Consulte também.

 **Criando um documento**

1.  Crie uma instância de uma interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) .

    Isso cria um FixedDocumentSequence vazio no pacote.

    -   Para criar um documento XPS em um arquivo, chame [**IXpsOMObjectFactory:: CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile).
    -   Para criar um documento XPS em um fluxo, chame [**IXpsOMObjectFactory:: CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream).

2.  Inicie um novo documento no pacote chamando [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).

    Antes de adicionar uma página, chame [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) para adicionar um FixedDocument ao FixedDocumentSequence que foi criado na etapa 1.

3.  Adicionar conteúdo.
    -   Para adicionar um novo FixedPage ao documento, chame [**IXpsOMPackageWriter:: AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage), passando um ponteiro para a interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que tem o conteúdo do FixedPage que você deseja adicionar.
    -   Para criar um novo FixedDocument no FixedDocumentSequence, chame [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).
4.  Feche o pacote e seu conteúdo chamando [**IXpsOMPackageWriter:: Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close).

## <a name="advanced-features"></a>Recursos avançados

Os métodos da interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) também oferecem suporte à adição de recursos, miniaturas e Tíquetes de impressão. Esses componentes de documento podem ser adicionados nos níveis pacote, FixedDocumentSequence, FixedDocument e FixedPage. Para obter mais informações sobre como usar essa interface para impressão, consulte [imprimir um om XPS](print-an-xps-om.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Uso da API de assinatura digital do XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Interfaces de página do XPS OM](xps-object-model-page-interfaces.md)
</dt> <dt>

[Navegar no OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[Trabalhando com interfaces visuais e telas do XPS OM](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Trabalhando com interfaces de caminho de OM XPS](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Trabalhando com interfaces de texto, gráficos e imagens de OM XPS](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[Interfaces de tíquete de impressão XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[Referência da API do documento XPS](xps-programming-reference.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




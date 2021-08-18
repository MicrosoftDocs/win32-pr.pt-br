---
description: A interface IXpsOMPackageWriter cria um arquivo de documento XPS no qual os aplicativos podem gravar o conteúdo das interfaces IXpsOMPage de um OM XPS.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Usando a interface IXpsOMPackageWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a4437f939821b826fa0d5c30407777b7d44c5d03c236f4ef850d52145b4f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098698"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Usando a interface IXpsOMPackageWriter

A interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) cria um arquivo de documento XPS no qual os aplicativos podem gravar o conteúdo das interfaces [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) de um OM XPS. A interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) é mais útil quando o conteúdo do documento está sendo processado ou criado sequencialmente. Ao contrário dos métodos [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) e [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) da interface [**IXpsOMPackage,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) para que a interface **IXpsOMPackageWriter** seja usada nem todo o FixedDocument nem o FixedDocumentSequence precisa ser concluído.

## <a name="overview"></a>Visão geral

A interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) grava uma página por vez, da primeira página de um documento XPS até a última. A interface pode ser usada para criar arquivos de documento XPS simples e também arquivos de documento XPS complexos que contêm mais de um FixedDocument no FixedDocumentSequence. Em arquivos de documento XPS complexos, os FixedDocuments também são criados em sequência, começando com o primeiro FixedDocument no FixedDocumentSequence. A interface **IXpsOMPackageWriter** não dá suporte à criação de conteúdo do documento em ordem aleatória. Use-o, por exemplo, para criar um relatório sequencial ou para executar o processamento em um filtro de driver de dispositivo em que o conteúdo do documento é alimentado para o driver em sequência.

## <a name="terminology-review"></a>Análise de terminologia

Um *arquivo de documento XPS* é um Open Packaging Conventions (OPC) que está em conformidade com o XML Paper Specification. Portanto, tecnicamente, a interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) cria um pacote *OPC,* mas é um pacote OPC que está em conformidade com o XML Paper Specification. Por esse motivo, em discussões sobre documentos XPS, os termos documento e pacote *XPS* *geralmente* são usados de forma intercambiável.

O  pacote criado pela interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) conterá os componentes de documento XPS necessários: um FixedDocumentSequence, pelo menos um FixedDocument e pelo menos um FixedPage. O FixedDocumentSequence é criado quando a interface **IXpsOMPackageWriter** é instanciada. Um FixedDocument é criado sempre que [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) é chamado e uma FixedPage é criada sempre que [**IXpsOMPackageWriter::AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) é chamado. Como a interface grava o conteúdo do documento sequencialmente, o **método AddPage** adiciona a página ao FixedDocument criado mais recentemente.

## <a name="using-the-ixpsompackagewriter-interface"></a>Usando a interface IXpsOMPackageWriter

O procedimento a seguir descreve como criar um arquivo de documento XPS usando a interface [**IXpsOMPackageWriter.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) O procedimento não descreve como insinuar uma interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) e seu conteúdo. Para obter mais informações sobre **IXpsOMPage** e adicionar conteúdo a uma página, consulte Interfaces de página [OM XPS](xps-object-model-page-interfaces.md) e os tópicos listados na seção Consulte Também.

 **Criando um documento**

1.  Insinue uma interface [**IXpsOMPackageWriter.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)

    Isso cria um FixedDocumentSequence vazio no pacote.

    -   Para criar um documento XPS em um arquivo, chame [**IXpsOMObjectFactory::CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile).
    -   Para criar um documento XPS em um fluxo, chame [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream).

2.  Inicie um novo documento no pacote chamando [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).

    Antes de adicionar uma página, chame [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) para adicionar um FixedDocument ao FixedDocumentSequence criado na etapa 1.

3.  Adicionar conteúdo.
    -   Para adicionar uma nova FixedPage ao documento, chame [**IXpsOMPackageWriter::AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage), passando um ponteiro para a interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) que tem o conteúdo da FixedPage que você deseja adicionar.
    -   Para criar um novo FixedDocument no FixedDocumentSequence, chame [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).
4.  Feche o pacote e seu conteúdo chamando [**IXpsOMPackageWriter::Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close).

## <a name="advanced-features"></a>Recursos avançados

Os métodos da interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) também suportam a adição de recursos, miniaturas e tíquetes de impressão. Esses componentes de documento podem ser adicionados aos níveis FixedDocumentSequence, FixedDocument e FixedPage. Para obter mais informações sobre como usar essa interface para impressão, consulte [Imprimir um OM XPS](print-an-xps-om.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Uso da API de assinatura digital do XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Interfaces de página do XPS OM](xps-object-model-page-interfaces.md)
</dt> <dt>

[Navegar pelo OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[Trabalhando com interfaces visuais e tela do OM XPS](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Trabalhando com interfaces de caminho do OM XPS](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Trabalhando com interfaces de texto, gráficos e imagens do XPS OM](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[Interfaces de tíquete de impressão do OM XPS](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[Referência da API de Documento XPS](xps-programming-reference.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




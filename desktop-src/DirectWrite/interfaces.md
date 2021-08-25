---
title: Interfaces DirectWrite
description: Lista as interfaces definidas por DirectWrite.
ms.assetid: 7075e771-ce34-4426-8c07-13e85ff4d453
keywords:
- DirectWrite,interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1abd75d83fedf29da1bb5f67073dd74ca10816fdeb6ca43a61f40ad8ae26c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048606"
---
# <a name="directwrite-interfaces"></a>Interfaces DirectWrite

DirectWrite define as interfaces a seguir.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) | Representa o resultado de uma operação assíncrona. Um cliente pode usar a interface para aguardar a conclusão da operação e obter o resultado.  |
| [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) | Encapsula um bitmap independente de dispositivo de 32 bits e o contexto do dispositivo, que pode ser usado para renderizar glifos. |
| [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1) | Encapsula um bitmap independente de dispositivo de 32 bits e o contexto do dispositivo, que você pode usar para renderizar glifos. |
| [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2) | Encapsula um bitmap independente de dispositivo de 32 bits e o contexto do dispositivo, que pode ser usado para renderizar glifos. |
| [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) | Essa interface permite que o aplicativo enumere por meio das executações de glifo de cor. |
| [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) | Enumerador para uma coleção ordenada de glifo de cor é executado. |
| [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) | Usado para criar todos os objetos DirectWrite subsequentes. Essa interface é a interface de fábrica raiz para todos os DirectWrite objetos. |
| [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) | A interface de fábrica raiz para todos [DirectWrite](direct-write-portal.md) objetos. |
| [**IDWriteFactory2**](idwritefactory2.md) | A interface de fábrica raiz para todos [DirectWrite](direct-write-portal.md) objetos. |
| [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) | A interface de fábrica raiz para todos [DirectWrite](direct-write-portal.md) objetos. |
| [**IDWriteFactory4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4) | A interface de fábrica raiz para todos DirectWrite objetos. |
| [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) | A interface de fábrica raiz para todos DirectWrite objetos. |
| [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) | Isso representa um objeto de fábrica do qual todos DirectWrite objetos são criados. **IDWriteFactory6** adiciona novos recursos para trabalhar com fontes e recursos de fonte. |
| [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) | Essa interface representa um objeto de fábrica do qual todos DirectWrite objetos são criados. **IDWriteFactory7** adiciona novos recursos para trabalhar com fontes do sistema. |
| [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | Representa uma fonte física em uma coleção de fontes. Essa interface é usada para criar faces de fonte de fontes físicas ou para recuperar informações como métricas de face de fonte ou nomes de rosto de rostos de fontes existentes. |
| [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) | Representa uma fonte física em uma coleção de fontes. |
| [**IDWriteFont2**](idwritefont2.md) | Representa uma fonte física em uma coleção de fontes. |
| [**IDWriteFont3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3) | Representa uma fonte em uma coleção de fontes. |
| [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) | Um objeto que encapsula um conjunto de fontes, como o conjunto de fontes instaladas no sistema ou o conjunto de fontes em um diretório específico. A API de coleção de fontes pode ser usada para descobrir quais fontes e famílias de fontes estão disponíveis e para obter alguns metadados sobre as fontes. |
| [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) | Um objeto que encapsula um conjunto de fontes, como o conjunto de fontes instaladas no sistema ou o conjunto de fontes em um diretório específico. A API de coleção de fontes pode ser usada para descobrir quais fontes e famílias de fontes estão disponíveis e para obter alguns metadados sobre as fontes. |
| [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) | Essa interface encapsula um conjunto de fontes, como o conjunto de fontes instaladas no sistema ou o conjunto de fontes em um diretório específico. |
| [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) | Essa interface encapsula um conjunto de fontes, como o conjunto de fontes instaladas no sistema ou o conjunto de fontes em um diretório específico. |
| [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) | Usado para construir uma coleção de fontes considerando um tipo específico de chave.  |
| [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) | Interface de retorno de chamada definida pelo aplicativo que recebe notificações da fila de download de fonte (interface [**IDWriteFontDownloadQueue).**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) Os retornos de chamada ocorrerão no thread de download e os objetos devem estar preparados para lidar com chamadas em seus métodos de outros threads a qualquer momento. |
| [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) | Interface que enquera solicitações de download para fontes remotas, caracteres, glifos e fragmentos de fonte.  |
| [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) | Essa interface expõe vários dados de fonte, como métricas, nomes e contornos de glifo. Ele contém o tipo de face da fonte, as referências de arquivo apropriadas e os dados de identificação facial. |
| [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) | Contém o tipo de face da fonte, as referências de arquivo apropriadas e os dados de identificação facial.  |
| [**IDWriteFontFace2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2) | Essa interface contém o tipo de face da fonte, as referências de arquivo apropriadas e os dados de identificação facial. Ele adiciona a capacidade de verificar se um caminho de renderização de cor é potencialmente necessário.  |
| [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) | Contém o tipo de face da fonte, as referências de arquivo apropriadas e os dados de identificação facial. |
| [**IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4) | Contém o tipo de face da fonte, as referências de arquivo apropriadas e os dados de identificação facial. |
| [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) | Essa interface contém o tipo de face da fonte, as referências de arquivo apropriadas e os dados de identificação facial. Ele adiciona novos recursos, como comparar duas faces de fonte, recuperar valores de eixo de fonte e recuperar o recurso de fonte subjacente. |
| [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) | Representa uma referência a um rosto de fonte. Uma referência de identificação exclusiva para uma fonte, na qual você pode criar um rosto de fonte para consultar métricas de fonte e usar para renderização. Uma referência facial de fonte consiste em um arquivo de fonte, índice facial de fonte e simulação de face de fonte. Os dados do arquivo podem ou não estar fisicamente presentes no computador local ainda.  |
| [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) | Representa uma referência a um rosto de fonte. Uma referência de identificação exclusiva para uma fonte, na qual você pode criar um rosto de fonte para consultar métricas de fonte e usar para renderização. |
| [**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback) | Permite que você acesse fontes de fallback na lista de fontes. |
| [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) | Permite que você crie mapeamentos de fallback de fonte Unicode e crie um objeto de fallback de fonte com base nesses mapeamentos. |
| [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) | Representa uma família de fontes relacionadas. |
| [**IDWriteFontFamily1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1) | Representa uma família de fontes relacionadas. |
| [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) | Representa uma família de fontes relacionadas. **IDWriteFontFamily2** adiciona novos recursos, incluindo a recuperação de fontes por valores de eixo de fonte. |
| [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) | Representa um arquivo de fonte. Aplicativos como gerenciadores de fontes ou visualizadores de fontes podem chamar [**IDWriteFontFile::Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) para descobrir se um arquivo específico é um arquivo de fonte e se é um tipo de fonte com suporte pelo sistema de fontes. |
| [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) | Encapsula uma coleção de arquivos de fonte. O sistema de fontes usa essa interface para enumerar arquivos de fonte ao criar uma coleção de fontes. |
| [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) | Lida com o carregamento de recursos de arquivo de fonte de um tipo específico de uma chave de referência de arquivo de fonte em um objeto de fluxo de arquivo de fonte.  |
| [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) | Carrega dados de arquivo de fonte de um carregador de arquivo de fonte personalizado.  |
| [**IDWriteFontList**](/windows/win32/api/dwrite/nn-dwrite-idwritefontlist) | Representa uma lista de fontes. |
| [**IDWriteFontList1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1) | Representa uma lista de fontes. |
| [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) | Representa uma lista de fontes. **IDWriteFontList2** adiciona novos recursos, incluindo a recuperação do conjunto de fontes subjacente usado pela lista. |
| [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) | nn-dwrite_3-idwritefontresource |
| [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) | Representa um conjunto de fontes. |
| [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) | Representa um conjunto de fontes. |
| [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) | Representa um conjunto de fontes. |
| [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) | Representa um conjunto de fontes. |
| [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) | Contém métodos para criar um conjunto de fontes. |
| [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) | Contém métodos para criar um conjunto de fontes. |
| [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) | Contém métodos para criar um conjunto de fontes. |
| [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) | Fornece interoperabilidade com GDI, como métodos para converter uma face de fonte em uma estrutura LOGFONT ou para converter uma descrição de fonte GDI em um rosto de fonte. Ele também é usado para criar objetos de destino de renderização de bitmap. |
| [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1) | Fornece interoperabilidade com GDI, como métodos para converter uma face de fonte em uma estrutura LOGFONT ou para converter uma descrição de fonte GDI em um rosto de fonte. Ele também é usado para criar objetos de destino de renderização de bitmap. |
| [**IDWriteGeometrySink**](idwritegeometrysink.md) | [**IDWriteGeometrySink**](idwritegeometrysink.md) é um **typedef** da interface [**ID2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) Consulte a página [**de referência ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) para obter mais informações. |
| [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) | Contém informações de baixo nível usadas para renderizar uma run de glifo. |
| [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) | Envolve um gráfico em linha definido pelo aplicativo, permitindo que DWrite consulte métricas como se o gráfico fosse um glifo em linha com o texto. |
| [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) | Representa um carregador de arquivo de fonte que pode acessar fontes na memória. |
| [**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md) | Uma implementação integrado da interface [**IDWriteFontFileLoader,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) que opera em arquivos de fonte locais e expõe informações de arquivo de fonte local da chave de referência do arquivo de fonte. As referências de arquivo de fonte criadas [**usando CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usam esse carregador de arquivo de fonte. |
| [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) | Representa uma coleção de cadeias de caracteres indexadas pelo nome da localidade. |
| [**IDWriteNumberSubstitution**](./idwritenumbersubstitution.md) | Contém os dígitos apropriados e a pontuação numérica para uma localidade especificada. |
| [**IDWritePixelSnapping**](/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping) | Define as propriedades de ajuste de pixel, como pixels por DIP (pixel independente do dispositivo) e a matriz de transformação atual de um renderador de texto. |
| [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) | Representa um carregador de arquivo de fonte que pode acessar fontes remotas (ou seja, baixáveis).  |
| [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) | Representa um fluxo de arquivos de fonte, partes das quais podem ser não locais.  |
| [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) | Representa configurações de renderização de texto, como nível ClearType, contraste aprimorado e correção gama para rasterização e filtragem de glifo. Um aplicativo normalmente obtém um objeto de parâmetros de renderização chamando o [**método IDWriteFactory::CreateMonitorRenderingParams.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) |
| [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1) | Representa as configurações de renderização de texto para rasterização e filtragem de glifos. |
| [**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2) | Representa as configurações de renderização de texto para rasterização e filtragem de glifos. |
| [**IDWriteRenderingParams3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriterenderingparams3) | Representa as configurações de renderização de texto para rasterização e filtragem de glifos. |
| [**IDWriteStringList**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist) | Representa uma coleção de cadeias de caracteres indexadas por número. |
| [**IDWriteTextAnalysisSink**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink) | Essa interface é implementada pelo cliente do analisador de texto para receber a saída de uma determinada análise de texto.  |
| [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) | A interface que você implementa para receber a saída dos analisadores de texto. |
| [**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) | Implementado pelo cliente do analisador de texto para fornecer texto ao analisador. Ele permite a separação entre a exibição lógica do texto como um fluxo contínuo de caracteres identificáveis por posições de texto exclusivas e o layout de memória real de blocos de texto potencialmente discretos no armazenamento de backing do cliente.  |
| [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) | A interface que você implementa para fornecer as informações necessárias para o analisador de texto, como o texto e as propriedades de texto associadas. |
| [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) | Analisa várias propriedades de texto para processamento de script complexo, como suporte bidirecional (bidi) para idiomas como árabe, determinação de oportunidades de quebra de linha, posicionamento de glifo e substituição de número. |
| [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) | Analisa várias propriedades de texto para processamento de script complexo. |
| [**IDWriteTextAnalyzer2**](idwritetextanalyzer2.md) | Analisa várias propriedades de texto para processamento de script complexo. |
| [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) | A interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) descreve as propriedades de fonte e parágrafo usadas para formatar texto e descreve informações de localidade.  |
| [**IDWriteTextFormat1**](idwritetextformat1.md) | Descreve as propriedades de fonte e parágrafo usadas para formatar texto e descreve informações de localidade.  |
| [**IDWriteTextFormat2**](idwritetextformat2.md) | Descreve as propriedades de fonte e parágrafo usadas para formatar texto e descreve informações de localidade.  |
| [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) | Descreve as propriedades de fonte e parágrafo usadas para formatar texto e descreve informações de localidade. |
| [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) | A interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) representa um bloco de texto depois que ele é totalmente analisado e formatado. |
| [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) | Representa um bloco de texto depois que ele foi totalmente analisado e formatado. |
| [**IDWriteTextLayout2**](idwritetextlayout2.md) | Representa um bloco de texto depois que ele foi totalmente analisado e formatado. |
| [**IDWriteTextLayout3**](idwritetextlayout3.md) | Representa um bloco de texto depois que ele foi totalmente analisado e formatado.  |
| [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) | Representa um conjunto de retornos de chamada definidos pelo aplicativo que executam a renderização de texto, objetos em linha e decorações, como sublinhados. |
| [**IDWriteTextRenderer1**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1) | Representa um conjunto de retornos de chamada definidos pelo aplicativo que executam a renderização de texto, objetos em linha e decorações, como sublinhados.  |
| [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) | Representa uma configuração de tipografia de fonte. |
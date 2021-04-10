---
description: Exemplo de filtro assíncrono
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Exemplo de filtro assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010052"
---
# <a name="async-filter-sample"></a>Exemplo de filtro assíncrono

## <a name="description"></a>Descrição

O exemplo de filtro assíncrono é um filtro de leitor de arquivo que dá suporte ao download progressivo. Este filtro de exemplo implementa as interfaces [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) . Ele dá suporte a arquivos MPEG, mas não a arquivos AVI.

## <a name="usage"></a>Uso

Este exemplo inclui um pequeno aplicativo de linha de comando, Memfile.exe, que demonstra o filtro. Os argumentos de linha de comando especificam um arquivo de mídia e uma taxa de bits, em quilobytes por segundo. O aplicativo lê o arquivo na memória na taxa especificada e executa o arquivo. Para fazer isso, ele cria uma instância do filtro, adiciona o filtro ao gráfico de filtro e renderiza o pino de saída do filtro.

Na linha de comando, digite:

**Taxa de bits de memfile filename**  

O filtro de exemplo assíncrono não oferece suporte a arquivos AVI, pois ele não pode se conectar ao filtro de [Splitter AVI](avi-splitter-filter.md) . O pino de saída do filtro assíncrono propõe \_ o fluxo de MediaType e MEDIASUBTYPE \_ nulo para o tipo de mídia. O pino de entrada no filtro de Splitter AVI não aceita MEDIASUBTYPE \_ NULL e não propõe nenhum tipo próprio. Portanto, a conexão do PIN falha. O filtro assíncrono pode ser aprimorado para oferecer MEDIASUBTYPE \_ AVI quando apropriado. Por exemplo, ele pode examinar o formato de arquivo ou usar a extensão de arquivo.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: exemplos de \[ *raiz do SDK* \] \\ filtros de \\ multimídia do \\ DirectShow \\ \\ assíncronos.

## <a name="related-topics"></a>Tópicos relacionados



[Amostras do DirectShow](directshow-samples.md)


 

 




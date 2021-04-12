---
title: Suporte ao código de tempo SMPTE
description: Suporte ao código de tempo SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- SDK do Windows Media Format, códigos de tempo SMPTE
- Formato de sistema avançado (ASF), códigos de tempo SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- SDK do Windows Media Format, interface IWMReaderTimecode
- Formato de sistema avançado (ASF), interface IWMReaderTimecode
- ASF (formato de sistemas avançados), interface IWMReaderTimecode
- Códigos de tempo SMPTE, sobre
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104498984"
---
# <a name="smpte-time-code-support"></a>Suporte ao código de tempo SMPTE

O Windows Media Format SDK fornece suporte limitado para o código de tempo SMPTE, que é um formato de código de hora padrão para filmes e televisão. Você pode incluir dados de código de tempo SMPTE com exemplos como extensões de unidade de dados. A parte de dados da extensão é uma estrutura de [**\_ dados de \_ extensão \_ do código**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) de tempo WMT que contém as informações do carimbo de data/hora SMPTE original.

Manter o código de tempo SMPTE em seus arquivos ASF vem com limites de desempenho. Cada exemplo com um carimbo de data/hora SMPTE associado requer o transporte dos 14 bytes na estrutura de carimbo de data/hora. Em um cenário de streaming, esse maior requisito de largura de banda pode ser catastrófico. Como resultado, é recomendável que os códigos de tempo SMPTE só sejam mantidos em arquivos ASF durante o processo de edição de vídeo, que normalmente é feito com arquivos locais. Quando o arquivo final for criado, você deverá remover as extensões de unidade de dados.

Você pode ler carimbos de data/hora SMPTE da mesma forma que você lê qualquer outra extensão de unidade de dados, mas os objetos de leitura fornecem suporte integrado para pesquisa por código de tempo SMPTE. Para poder Pesquisar carimbos de data/hora SMPTE, você deve primeiro indexar o arquivo pelo código de tempo SMPTE. Você pode configurar o indexador para indexar os códigos de tempo usando o método [**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .

Usando o leitor assíncrono, você pode navegar por um arquivo em carimbos de data/hora do SMPTE usando os métodos da interface [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) e o método [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) . Com o leitor síncrono, use [**IWMSyncReader2:: SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Configurar extensões de unidade de dados**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 





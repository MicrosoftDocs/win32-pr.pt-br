---
title: Suporte a código de hora SMPTE
description: Suporte a código de hora SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows SDK de Formato de Mídia, códigos de tempo SMPTE
- AsF (Advanced Systems Format), códigos de hora SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- Windows SDK de Formato de Mídia, interface IWMReaderTimecode
- AsF (Advanced Systems Format), interface IWMReaderTimecode
- ASF (Formato de Sistemas Avançados), interface IWMReaderTimecode
- Códigos de hora SMPTE, sobre
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19e3d7a85c797a3b0247bedb2359b4b40b60e8d4f243f14e2c94175bb1e2740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929606"
---
# <a name="smpte-time-code-support"></a>Suporte a código de hora SMPTE

O SDK Windows Formato de Mídia oferece suporte limitado para o código de tempo SMPTE, que é um formato de código de hora padrão para filmes e tv. Você pode incluir dados de código de tempo SMPTE com exemplos como extensões de unidade de dados. A parte de dados da extensão é uma estrutura DE DADOS DE EXTENSÃO [**DO WMT \_ TIMECODE \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) que contém as informações do carimbo de data/hora SMPTE original.

Manter o código de tempo SMPTE em seus arquivos ASF vem com limites de desempenho. Cada exemplo com um carimbo de data/hora SMPTE associado requer o transporte dos 14 bytes na estrutura de carimbo de data/hora. Em um cenário de streaming, esse requisito de largura de banda maior pode ser catastrófico. Como resultado, é sugerido que os códigos de tempo SMPTE sejam persistentes apenas em arquivos ASF durante o processo de edição de vídeo, o que normalmente é feito com arquivos locais. Quando o arquivo final for criado, você deverá remover as extensões da unidade de dados.

Você pode ler carimbos de data/hora SMPTE da mesma forma que leria qualquer outra extensão de unidade de dados, mas os objetos de leitura fornecem suporte integrado para pesquisa por código de hora SMPTE. Para poder pesquisar carimbos de data/hora SMPTE, primeiro você deve indexar o arquivo por código de hora SMPTE. Você pode configurar o indexador para indexar códigos de tempo usando o [**método IWMIndexer2::Configure.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)

Usando o leitor assíncrono, você pode navegar por um arquivo por carimbos de data/hora SMPTE usando os métodos da interface [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) e o método [**IWMReaderAdvanced3::StartAtPosition.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) Com o leitor síncrono, use [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Configurar extensões de unidade de dados**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 





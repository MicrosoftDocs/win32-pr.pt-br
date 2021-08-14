---
title: Trabalhando com saídas
description: Trabalhando com saídas
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows SDK de Formato de Mídia, trabalhando com saídas
- ASF (Advanced Systems Format), trabalhando com saídas
- ASF (Formato de Sistemas Avançados), trabalhando com saídas
- FORMATO AVANÇADO de Sistemas (ASF), números de saída e formatos
- ASF (Formato de Sistemas Avançados), números de saída e formatos
- números de saída e formatos, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e5b4980ef14126006d3f19fe0717aa9eb6fd5c1a8f7baaf91e35084faeacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697720"
---
# <a name="working-with-outputs"></a>Trabalhando com saídas

Por padrão, cada amostra que você recebe de qualquer objeto de leitor é associada a um número de saída. Cada número de saída corresponde a um fluxo no arquivo ASF. O leitor atribui números de saída aos fluxos no arquivo quando o arquivo é aberto. Normalmente, há uma saída para cada fluxo em um arquivo. Se o arquivo usar a exclusão mútua, no entanto, cada grupo de fluxos mutuamente exclusivos será atribuído a um único número de saída. O fluxo que corresponde ao número de saída dos fluxos mutuamente exclusivos é determinado pelo leitor, no caso de arquivos MBR (taxa de bits múltipla) ou por seu aplicativo, se você estiver usando a seleção manual de fluxo.

Como o nome da conexão definido no perfil não é persistido no arquivo, o leitor cria um nome de conexão padrão para cada saída que é simplesmente uma representação de cadeia de caracteres do número de saída, por exemplo "1", "2", "3" e assim por diante. Os nomes de conexão permitem que os aplicativos e o próprio leitor correlacionem saídas a fluxos. Em um arquivo de taxa de vários bits, vários fluxos compartilham um nome de conexão. Isso não importa para o leitor, porque as propriedades de saída para cada fluxo MBR são idênticas.

Cada saída tem um ou mais formatos de saída com suporte. Um formato de saída é o formato que as amostras descompactadas entregues pelo leitor usam. Quando o leitor abre um arquivo, ele define o formato de cada saída como o padrão para o subtipo de mídia. O número e o tipo de formatos de saída com suporte são determinados pelo codec que descompacta os dados de mídia.

Os tópicos a seguir explicam como trabalhar com saídas:

-   [Para identificar números de saída](to-identify-output-numbers.md)
-   [Atribuindo formatos de saída](assigning-output-formats.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMSyncReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 





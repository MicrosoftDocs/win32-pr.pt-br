---
title: Trabalhando com saídas
description: Trabalhando com saídas
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows SDK do formato de mídia, trabalhando com saídas
- ASF (Advanced Systems Format), trabalhando com saídas
- ASF (formato de sistemas avançados), trabalhando com saídas
- ASF (Advanced Systems Format), formatos e números de saída
- ASF (formato de sistemas avançados), números e formatos de saída
- formatos e números de saída, sobre
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

Como padrão, cada exemplo que você recebe de um objeto leitor é associado a um número de saída. Cada número de saída corresponde a um fluxo no arquivo ASF. O leitor atribui números de saída aos fluxos no arquivo quando o arquivo é aberto. Normalmente, há uma saída para cada fluxo em um arquivo. No entanto, se o arquivo usar a exclusão mútua, cada grupo de fluxos mutuamente exclusivos será atribuído a um único número de saída. O fluxo que corresponde ao número de saída dos fluxos mutuamente exclusivos é determinado pelo leitor, no caso de arquivos de taxa de bits múltipla (MBR) ou por seu aplicativo, se você estiver usando a seleção de fluxo manual.

Como o nome de conexão definido no perfil não é persistido no arquivo, o leitor cria um nome de conexão padrão para cada saída que é simplesmente uma representação de cadeia de caracteres do número de saída, por exemplo "1", "2", "3" e assim por diante. Os nomes de conexão habilitam aplicativos e o próprio leitor, para correlacionar saídas a fluxos. Em um arquivo de taxa de vários bits, vários fluxos compartilham um nome de conexão. Isso não importa com o leitor, porque as propriedades de saída para cada fluxo de MBR são idênticas.

Cada saída tem um ou mais formatos de saída com suporte. Um formato de saída é o formato que os exemplos não compactados fornecidos pelo leitor usam. Quando o leitor abre um arquivo, ele define o formato de cada saída para o padrão para o subtipo de mídia. O número e o tipo de formatos de saída com suporte são determinados pelo codec que descompacta os dados de mídia.

Os tópicos a seguir explicam como trabalhar com saídas:

-   [Para identificar os números de saída](to-identify-output-numbers.md)
-   [Atribuindo formatos de saída](assigning-output-formats.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 





---
title: Trabalhando com saídas
description: Trabalhando com saídas
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- SDK do Windows Media Format, trabalhando com saídas
- ASF (Advanced Systems Format), trabalhando com saídas
- ASF (formato de sistemas avançados), trabalhando com saídas
- ASF (Advanced Systems Format), formatos e números de saída
- ASF (formato de sistemas avançados), números e formatos de saída
- formatos e números de saída, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640135"
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

 

 





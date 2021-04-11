---
description: Multiplexador ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexador ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010331"
---
# <a name="asf-multiplexer"></a>Multiplexador ASF

O *multiplexador* de ASF é um objeto de camada WMContainer que funciona com o [objeto de dados ASF](asf-file-structure.md) e dá a um aplicativo a capacidade de gerar pacotes de dados para um contêiner ASF. O multiplexador aceita dados de mídia na forma de [amostras de mídia](media-samples.md) e gera amostras de mídia com base nos parâmetros de streaming e de pacote ASF definidos no [objeto de cabeçalho ASF](asf-file-structure.md). Os exemplos de mídia de saída armazenam referências a um ou mais buffers de mídia que contêm dados de mídia digital em pacotes. Você pode usar esse objeto em um cenário de codificação de arquivo em que ele recebe amostras de fluxo codificadas do codificador ou para transcodificação ASF-ASF (remuxing).

O diagrama a seguir ilustra a geração de pacotes de dados ASF para um arquivo ASF usando o multiplexador.

![diagrama mostrando a geração de pacotes de dados ASF](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).

Esta seção contém os seguintes tópicos:



| Tópico                                                                  | Descrição                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Criando o objeto Multiplexador](creating-the-multiplexer-object.md) | Como criar e inicializar o multiplexador.                     |
| [Gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md) | Como gerar pacotes de dados para constituir um novo objeto de dados ASF. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: copiando fluxos ASF de um arquivo para outro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: gravando um arquivo WMA usando a codificação de CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 




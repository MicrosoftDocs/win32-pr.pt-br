---
description: Multiplexador ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexador ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e1577f005004dbbe6bbb27e1ce7af346e56e134aff2b3201f5670175b015c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035554"
---
# <a name="asf-multiplexer"></a>Multiplexador ASF

O *multiplexador* ASF é um objeto de camada WMContainer que funciona com o objeto de dados [ASF](asf-file-structure.md) e fornece a um aplicativo a capacidade de gerar pacotes de dados para um contêiner ASF. O multiplexador aceita dados de mídia na forma de [Exemplos](media-samples.md) de Mídia e saídas de amostras de mídia com base em parâmetros de pacote ASF e streaming definidos no Objeto de [Header asF](asf-file-structure.md). Os exemplos de mídia de saída contêm referências a um ou mais buffers de mídia que contêm dados de mídia digital em pacotes. Você pode usar esse objeto em um cenário de codificação de arquivo em que ele recebe exemplos de fluxo codificado do codificador ou para transcodificação asF-ASF (remuxing).

O diagrama a seguir ilustra a geração de pacotes de dados ASF para um arquivo ASF usando o multiplexador.

![diagrama mostrando a geração de pacotes de dados asf](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

Para obter informações sobre a estrutura de um arquivo ASF, consulte [Estrutura de arquivos ASF](asf-file-structure.md).

Esta seção contém os seguintes tópicos:



| Tópico                                                                  | Descrição                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Criando o objeto multiplexador](creating-the-multiplexer-object.md) | Como criar e inicializar o multiplexador.                     |
| [Gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md) | Como gerar pacotes de dados para constituir um novo objeto de dados ASF. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes DOF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: Copiando as Fluxos ASF de um arquivo para outro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: Escrevendo um arquivo WMA usando a codificação CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 




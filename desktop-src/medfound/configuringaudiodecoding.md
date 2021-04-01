---
description: Configurando a decodificação de áudio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configurando a decodificação de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646607"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>Configurando a decodificação de áudio (Microsoft Media Foundation)

A decodificação do conteúdo de áudio do Windows Media é muito mais fácil do que codificá-lo. Depois de criar um objeto de decodificador de áudio, defina o tipo de entrada usando o método **IMediaObject:: SetInputType** ou **IMFTransform:: SetInputType** . O tipo de mídia que você usa para a entrada do decodificador deve corresponder ao tipo de saída que foi usado quando o conteúdo foi codificado. Isso inclui os dados de formato estendidos anexados à estrutura **WAVEFORMATEX** . Você deve garantir que esses dados estejam corretos, pois o decodificador não pode processar amostras sem ele.

Depois de definir o tipo de entrada, você pode configurar os recursos de decodificador que deseja usar. Os recursos do decodificador, como os usados para codificação, são definidos usando os métodos de **IPropertyBag** ou **IPropertyStore**.

Depois que o tipo de entrada é definido e todos os recursos do decodificador são configurados, você pode enumerar os tipos de saída com suporte pelo decodificador fazendo chamadas para **IMediaObject:: GetOutputType** ou **IMFTransform:: GetOutputType**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> </dl>

 

 




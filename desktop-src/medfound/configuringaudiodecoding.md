---
description: Configurando a decodificação de áudio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configurando a decodificação de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee274fd714065a1c89c9d634dd80de4d59c9eb567d67ed8045d2b89bece87d74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664637"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>Configurando a decodificação de áudio (Microsoft Media Foundation)

A decodificação Windows de áudio de mídia é muito mais fácil do que a codificação. Depois de criar um objeto de decodificador de áudio, de definir o tipo de entrada usando o método **IMediaObject::SetInputType** ou **IMFTransform::SetInputType.** O tipo de mídia que você usa para a entrada do decodificador deve corresponder ao tipo de saída que foi usado quando o conteúdo foi codificado. Isso inclui os dados de formato estendido anexados à estrutura **WAVEFORMATEX.** Você deve garantir que esses dados estão corretos, pois o decodificador não pode processar exemplos sem eles.

Depois de definir o tipo de entrada, você pode configurar os recursos do decodificador que deseja usar. Os recursos do decodificador, como aqueles usados para codificação, são definidos usando os métodos de **IPropertyBag** ou **IPropertyStore**.

Depois que o tipo de entrada é definido e todos os recursos do decodificador são configurados, você pode enumerar os tipos de saída com suporte pelo decodificador fazendo chamadas para **IMediaObject::GetOutputType** ou **IMFTransform::GetOutputType**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> </dl>

 

 




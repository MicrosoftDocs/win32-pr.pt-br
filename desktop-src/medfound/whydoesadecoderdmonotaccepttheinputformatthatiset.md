---
description: Por que um decodificador não aceita o formato de entrada que eu defini?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Por que um decodificador não aceita o formato de entrada que eu defini?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7299045e41c7ec6e4c4796ed77e22c4b59af1f2c63dfc8817de8a551021f29b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887036"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a>Por que um decodificador não aceita o formato de entrada que eu defini?

Há muitas razões pelas quais um decodificador pode rejeitar um formato. O mais comum são dados de formato estendidos ausentes ou incorretos. Os dados de formato estendido são informações específicas do codec que são acrescentadas à estrutura que descreve o tipo de mídia.

quando você enumera um tipo de saída usando um objeto de codificador, o membro **pbFormat** da estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) apontará para uma estrutura **WAVEFORMATEX** . Essa estrutura tem dados de formato estendidos anexados a ele, e o tamanho desses dados é armazenado no membro **WAVEFORMATEX. cbSize** . Independentemente do contêiner usado para armazenar os dados compactados, você deve persistir a estrutura **WAVEFORMATEX** e usá-la no tipo de entrada para o decodificador. Sem os dados de formato estendidos, o decodificador não pode descompactar o conteúdo.

Para formatos de vídeo, você deve recuperar manualmente os dados de formato estendido e acrescentá-los à estrutura **VIDEOINFOHEADER** . Para obter mais informações, consulte [usando dados privados do codec de vídeo](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perguntas frequentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 

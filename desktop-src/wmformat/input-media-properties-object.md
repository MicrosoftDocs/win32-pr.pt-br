---
title: Objeto de propriedades de mídia de entrada
description: Objeto de propriedades de mídia de entrada
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows SDK do formato de mídia, objetos de propriedades de mídia de entrada
- ASF (Advanced Systems Format), objetos de propriedades de mídia de entrada
- ASF (formato de sistemas avançados), objetos de propriedades de mídia de entrada
- objetos, objetos de propriedades de mídia de entrada
- objetos de propriedades de mídia de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf5fac14de1c0fdc6619ab0dfe61feb9fcf577acb5c22dc2243a96d943921c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809026"
---
# <a name="input-media-properties-object"></a>Objeto de propriedades de mídia de entrada

Um objeto de propriedades de mídia de entrada criado pelo objeto gravador dá suporte às seguintes interfaces. Essas interfaces são acessadas por uma chamada para **QueryInterface** em uma das interfaces do objeto Writer.



| Interface                                        | Descrição                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | Recupera as propriedades de um fluxo de entrada.                                                               |
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Usado como interface base para as outras interfaces de propriedade de mídia (entrada, saída e vídeo).             |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Gerencia as propriedades de um fluxo de vídeo. Essa é uma interface opcional, disponível apenas para fluxos de vídeo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto**](objects.md)
</dt> <dt>

[**Objeto do gravador**](writer-object.md)
</dt> </dl>

 

 





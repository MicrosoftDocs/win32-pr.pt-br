---
title: Objeto de propriedades de mídia de entrada
description: Objeto de propriedades de mídia de entrada
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- SDK do Windows Media Format, objetos de propriedades de mídia de entrada
- ASF (Advanced Systems Format), objetos de propriedades de mídia de entrada
- ASF (formato de sistemas avançados), objetos de propriedades de mídia de entrada
- objetos, objetos de propriedades de mídia de entrada
- objetos de propriedades de mídia de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823558"
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

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto do gravador**](writer-object.md)
</dt> </dl>

 

 





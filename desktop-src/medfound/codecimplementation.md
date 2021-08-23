---
description: Implementação de codec.
ms.assetid: 5ec23f95-cc7d-4c16-979a-f1d2cc485bb0
title: Implementação de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1bb9c51788526d68b370dec782b433e6f8d7114ece2b4f5a735ef7662f869d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974855"
---
# <a name="codec-implementation"></a>Implementação de codec

Os codecs Windows Áudio de Mídia e Vídeo são implementados como objetos COM. Normalmente, um codec é implementado como um par de objetos COM: um para o codificador e outro para o decodificador. O codificador tem um CLSID (identificador de classe) e o decodificador tem um CLSID diferente. Por exemplo, a parte do codificador do codec do Windows Media Audio 9 tem um CLSID representado pela constante **CLSID \_ CWMAEncMediaObject** e a parte do decodificador desse mesmo codec tem um CLSID representado pela constante **CLSID \_ CWMADecMediaObject**.

Em alguns casos, mais de um codificador é incluído em um único objeto COM. Por exemplo, o codificador Windows Media Video 9 e o codificador Windows Media Video 9.1 fazem parte do mesmo objeto COM. Consequentemente, ambos têm a mesma CLSID, que é representada pela constante **CLSID \_ CWMV9EncMediaObject**. Da mesma forma, alguns objetos COM incluem mais de um decodificador.

Cada objeto codificador ou decodificador expõe a interface [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) para que o objeto possa ser usado como um Objeto de Mídia DirectX (DMO) e a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma MFT (Transformação Media Foundation).

Para a maioria dos codificadores, independentemente de você usar o codificador como um DMO ou um MFT, use o mesmo CLSID para criar uma instância do codificador. Por exemplo, para criar uma instância do codificador Windows Media Video 9, use **CLSID \_ CWMV9EncMediaObject**, independentemente de você pretender usar o codificador como um DMO ou um MFT. Da mesma forma, para a maioria dos decodificadores, cada decodificador tem um único CLSID, independentemente de você usar o decodificador como um DMO ou um MFT.

> [!Note]  
> Há algumas exceções à instrução anterior sobre como usar um único CLSID para o DMO e o MFT. Por exemplo, o decodificador MPEG-4 Parte 2 tem um CLSID quando está atuando como um DMO e um CLSID diferente quando está atuando como um MFT.

 

Além das interfaces principais, cada objeto codificador ou decodificador implementa duas interfaces semelhantes para trabalhar com propriedades de codec, **IPropertyBag** e **IPropertyStore.** Versões mais antigas dos objetos codificador e decodificador usavam **IPropertyBag,** que identifica cada propriedade por um valor de cadeia de caracteres que contém um nome de propriedade. **IPropertyStore** é uma interface mais nova que identifica propriedades com um valor de chave de propriedade exclusivo. O suporte **para IPropertyStore** foi adicionado para fornecer suporte para MFTs. A maioria das cadeias de caracteres de nome da propriedade **IPropertyBag** tem um GUID de chave de propriedade **IPropertyStore** correspondente e a maioria dos GUIDs tem uma cadeia de caracteres de nome **IPropertyBag** correspondente, com algumas exceções.

Esta documentação lista as propriedades por constante de chave de propriedade, mas cada entrada inclui a constante de cadeia de caracteres de nome de propriedade para uso com **IPropertyBag** quando apropriado.

## <a name="related-topics"></a>Tópicos relacionados

[Codificações de mídia do Windows](windows-media-codecs.md)

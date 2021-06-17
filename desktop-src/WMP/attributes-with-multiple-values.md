---
title: Atributos com vários valores (SDK do Windows Media Player)
description: Saiba mais sobre atributos com vários valores no SDK do Windows Media Player. Alguns atributos de item de mídia podem ter vários valores.
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player, atributos para itens de mídia
- Modelo de objeto do Windows Media Player, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Mobile, atributos para itens de mídia
- Controle ActiveX do Windows Media Player, atributos para itens de mídia
- Controle ActiveX móvel do Windows Media Player, atributos para itens de mídia
- Controle ActiveX, atributos para itens de mídia
- Biblioteca do Windows Media Player, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, vários valores
- vários valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16baf4bab47dc972ec7b043980dccb0f2aadd57
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262598"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>Atributos com vários valores (SDK do Windows Media Player)

Alguns atributos de item de mídia podem ter vários valores. Por exemplo, os atributos **autor**, **WM/Composer** e **WM/gênero** podem ter mais de um valor. O tipo de dados desses atributos é uma **cadeia de caracteres com valores múltiplos**.

No Windows Media Player, a biblioteca exibe vários valores em um único campo, separando os valores com ponto e vírgula. No entanto, cada valor é, na verdade, um atributo separado no item Windows Media.

Você pode escrever um código que determinará se um determinado atributo tem vários valores e, em seguida, recuperar todos esses valores. Você deve usar a *mídia*. **getItemInfoByType**. Se você usar a *mídia*. método **getItemInfo** para recuperar um atributo com valores múltiplos, você recuperará apenas o primeiro valor.

O exemplo final no tópico [valores de atributo de leitura](reading-attribute-values.md) demonstra o uso da *mídia*. **getAttributeCountByType** e *mídia*. métodos **getItemInfoByType** para recuperar vários valores para um determinado atributo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos de item de mídia**](media-item-attributes.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Lendo valores de atributo de um CD ou DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 





---
title: Atributos com vários valores (SDK do Windows Media Player)
description: Atributos com vários valores
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
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369146"
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

 

 





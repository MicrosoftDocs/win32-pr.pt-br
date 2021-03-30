---
title: Eventos internos
description: Eventos internos
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Capas do Windows Media Player, eventos internos
- capas, eventos internos
- eventos, internos
- escrevendo código para capas, eventos internos
- eventos internos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916056"
---
# <a name="internal-events"></a>Eventos internos

Você pode detectar alterações que ocorrem no Windows Media Player ou alterações em sua própria aparência. Elas podem ser alterações em métodos ou propriedades de objeto do Windows Media Player, alterações em atributos de capa e assim por diante.

## <a name="windows-media-player-property-changes"></a>Alterações de Propriedade do Windows Media Player

Você pode processar alterações no Windows Media Player usando o ouvinte wmpprop. Você deve configurar o ouvinte como um valor de um atributo. Coloque o valor entre aspas duplas e comece com a palavra "wmpprop" seguida por dois-pontos. Em seguida, você inclui a propriedade que deseja escutar. Quando a propriedade for alterada, o valor do atributo também será alterado. Por exemplo, para que um valor do elemento Slider seja alterado sempre que o valor do atributo **CurrentPosition** for alterado, digite o seguinte:


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Importante** Não use wmpprop nos métodos do Windows Media Player. Podem ocorrer resultados inesperados.

## <a name="windows-media-player-method-changes"></a>Alterações de método do Windows Media Player

Você pode fazer com que sua capa responda à disponibilidade de métodos no Windows Media Player usando wmpenabled e wmpdisabled. Eles são usados de forma semelhante ao ouvinte wmpprop, exceto que você só pode usá-los em métodos do objeto de **controle** que são suportados pelo método **IsAvailable** .

Por exemplo, você pode habilitar um botão somente quando o método **Play** está habilitado, usando um código como este:


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Importante** Não use wmpenabled ou wmpdisabled nas propriedades do Windows Media Player. Podem ocorrer resultados inesperados.

## <a name="skin-attribute-changes"></a>Alterações de atributo de aparência

Você pode responder às alterações nos atributos de capa de uma das duas maneiras, usando wmpprop ou o evento **\_ onChange** .

Você pode usar o wmpprop para escutar alterações em sua própria aparência. Por exemplo, para mostrar o valor do controle deslizante em uma caixa de texto, você pode digitar o seguinte:


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



Você pode usar o evento **\_ onChange** para processar eventos dentro de um elemento. Você deve anexar o nome do atributo que deseja rastrear para **\_ onChange**. Por exemplo, se você quiser acompanhar o valor de uma caixa de texto, digite:


```C++
value_onchange

```



Em seguida, você atribuiria uma cadeia de caracteres JScript que você deseja executar quando o valor for alterado. Por exemplo, para responder a uma alteração no valor de uma caixa de texto que pode ser usada para ajustar o volume do Windows Media Player, digite o seguinte dentro de seu elemento de **texto** como um atributo:


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Manipulando eventos**](handling-events.md)
</dt> </dl>

 

 





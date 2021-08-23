---
title: Eventos internos
description: Eventos internos
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Windows Media Player capas, eventos internos
- capas, eventos internos
- eventos, internos
- escrevendo código para capas, eventos internos
- eventos internos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8859ed86cb4951509d452b24c108e73d4129e474abf1c0bc2f51487e2d42bd9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572516"
---
# <a name="internal-events"></a>Eventos internos

você pode detectar alterações que ocorrem em Windows Media Player ou alterações em sua própria aparência. elas podem ser alterações em Windows Media Player propriedades de objeto ou métodos, alterações em atributos de capa e assim por diante.

## <a name="windows-media-player-property-changes"></a>Windows Media Player Alterações de propriedade

você pode processar alterações em Windows Media Player usando o ouvinte wmpprop. Você deve configurar o ouvinte como um valor de um atributo. Coloque o valor entre aspas duplas e comece com a palavra "wmpprop" seguida por dois-pontos. Em seguida, você inclui a propriedade que deseja escutar. Quando a propriedade for alterada, o valor do atributo também será alterado. Por exemplo, para que um valor do elemento Slider seja alterado sempre que o valor do atributo **CurrentPosition** for alterado, digite o seguinte:


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Importante** não use wmpprop em métodos Windows Media Player. Podem ocorrer resultados inesperados.

## <a name="windows-media-player-method-changes"></a>Windows Media Player Alterações de método

você pode fazer com que sua capa responda à disponibilidade de métodos em Windows Media Player usando wmpenabled e wmpdisabled. Eles são usados de forma semelhante ao ouvinte wmpprop, exceto que você só pode usá-los em métodos do objeto de **controle** que são suportados pelo método **IsAvailable** .

Por exemplo, você pode habilitar um botão somente quando o método **Play** está habilitado, usando um código como este:


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Importante** não use wmpenabled ou wmpdisabled em propriedades Windows Media Player. Podem ocorrer resultados inesperados.

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



em seguida, você atribuiria uma cadeia de caracteres de JScript que deseja executar quando o valor for alterado. por exemplo, para responder a uma alteração no valor de uma caixa de texto que pode ser usada para ajustar o volume de Windows Media Player, digite o seguinte dentro de seu elemento de **texto** como um atributo:


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Manipulando eventos**](handling-events.md)
</dt> </dl>

 

 





---
title: CUSTOMSLIDER.positionImage
description: O atributo positionImage especifica ou recupera o mapa de imagem usado para determinar qual imagem de posição do arquivo de imagem a ser exibida.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- CUSTOMSLIDER. positionImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727601ceb7ed078e40a284ab291f2e182a4270682b5f1db104515e31d3dbe2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749983"
---
# <a name="customsliderpositionimage"></a>CUSTOMSLIDER.positionImage

O atributo **positionImage** especifica ou recupera o mapa de imagem usado para determinar qual imagem de posição do arquivo de imagem a ser exibida.

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

Esse atributo é necessário e deve ser especificado.

O **positionImage** não é exibido. Em vez disso, ele serve como um mapa que define as regiões clicáveis da imagem exibida. A imagem exibida é uma das subimagems do arquivo de imagem e representa o estado real do controle deslizante. O **positionImage** inclui várias regiões de escala cinza iguais ao número dessas subimagems. As subimagems devem ter as mesmas dimensões que o **positionImage** ou o controle deslizante personalizado não funcionará corretamente.

Qualquer região que não esteja em escala cinza não será clicável. As regiões clicáveis devem ser definidas para valores de cor que variam uniformemente no espectro de escala cinza de preto para branco, com a primeira região puro preto e a última região em branco puro. Os valores de cor de cada região sucessiva devem ser incrementados por um valor igual a 255 dividido pelo número total de regiões menos um, arredondando para o número inteiro mais próximo.

Por exemplo, se houver seis regiões, o incremento seria 51 (255 dividido por 5) e os seis valores de escala de cinza seriam 0, 51, 102, 153, 204 e 255. Os valores de cor hexadecimais para as seis regiões seriam \# 000000, \# 333333, \# 666666, \# 999999, \# CCCCCC e \# FFFFFF.

Dessa forma, as regiões terão uma sequência determinada por seus valores de cor de escala cinza e essa sequência corresponderá à sequência de subimagem no arquivo de imagem. Quando uma das regiões é clicada, a subimagem correspondente é mostrada e o **valor** do controle deslizante personalizado é atualizado de acordo.

Os tipos de arquivo de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).

## <a name="examples"></a>Exemplos

Veja a seguir um exemplo de um controle deslizante personalizado **positionImage**. A imagem correspondente é mostrada na seção de exemplo da propriedade **Image** .

![gráfico positionimage de exemplo](images/dialmap.png)

O código a seguir ilustra o uso de atributos **CUSTOMSLIDER** .


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

    <SLIDER
      id = "myslider"
      min = "0"
      max = "wmpprop:player.currentMedia.duration"
      onmouseup = "player.controls.currentPosition = myslider.value; "
      tooltip = "current position"
      height = "10"
      width = "180"
      top = "150"
      left = "88"
      backgroundColor = "red"
      foregroundColor = "blue"
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. Image**](customslider-image.md)
</dt> </dl>

 

 






---
title: Controls.currentMarker
description: A propriedade currentMarker especifica ou recupera o número do marcador atual.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Controls.currentMarker Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc11f79460661b6622da529b0de025672794af660aeb27bf56c7910a6d5a50b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580302"
---
# <a name="controlscurrentmarker"></a>Controls.currentMarker

A **propriedade currentMarker** especifica ou recupera o número do marcador atual.

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um  número de leitura/gravação (**long**) com um valor padrão de zero.

## <a name="remarks"></a>Comentários

Definir **currentMarker** faz com que a reprodução inicie no marcador especificado. Antes de tentar definir **currentMarker**, determine se um arquivo tem marcadores e quantos ele tem usando **markerCount**. Se um arquivo não tiver marcadores, definir **currentMarker** como qualquer coisa, menos zero, resulta em um erro. Definir **currentMarker** como um número maior que **markerCount** também resulta em um erro.

A **propriedade currentMarker** sempre retorna o marcador atual ou o último, o que significa que a posição real do arquivo pode estar no marcador atual ou antes do próximo marcador. Os marcadores são numerados a partir de 1, portanto, se um arquivo tiver marcadores, você poderá definir **currentMarker** como zero para alterar a posição do arquivo como zero.

Até que o item de mídia atual seja definido (usando *Player*.**URL ou** *Player.* **currentMedia**), **currentMarker** retorna zero.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa **currentMarker** para iniciar a reprodução de vídeo do marcador que corresponde à propriedade **selectedIndex** de um elemento HTML SELECT. O **objeto** Player foi criado com ID = "Player".


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Media.markerCount**](media-markercount.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 






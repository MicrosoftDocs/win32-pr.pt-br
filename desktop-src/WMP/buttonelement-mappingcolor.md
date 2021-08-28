---
title: BUTTONelement. mappingColor
description: O atributo mappingColor especifica ou recupera a chave de cor que identifica esse BUTTONelement no botão.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- Windows Media Playercollection. mappingColor
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29badef71eda70782203effb7098c7ee5bc7a62b67d28ccbc9428c74e9473012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764336"
---
# <a name="buttonelementmappingcolor"></a>BUTTONelement. mappingColor

O atributo **mappingColor** especifica ou recupera a chave de cor que identifica esse **buttonelement** no **botão**.

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer. Não tem nenhum valor padrão.

## <a name="remarks"></a>Comentários

Esse atributo especifica a cor da região no grupo de botões **mappingImage** que corresponde a esse elemento Button. Todos os cliques nessa região são tratados por este elemento Button.

Se uma cor inválida for especificada, o **botãoelement** não será ativado.

## <a name="examples"></a>Exemplos

O exemplo a seguir é um arquivo de definição de capa completa que ilustra como alguns dos atributos **buttonelement** são usados. Ele pode ser encontrado no diretório de exemplos que foi instalado com o SDK.


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
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

[**Referência de cor**](color-reference.md)
</dt> <dt>

[**Elemento BUTTONelement**](buttonelement-element.md)
</dt> <dt>

[**BUTTON. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 






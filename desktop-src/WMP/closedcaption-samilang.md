---
title: ClosedCaption.SAMILang
description: A propriedade SAMILang especifica ou recupera o idioma exibido para legendas ocultas.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption. SAMILang Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781267"
---
# <a name="closedcaptionsamilang"></a>ClosedCaption.SAMILang

A propriedade **SAMILang** especifica ou recupera o idioma exibido para legendas ocultas.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Um arquivo SAMI pode conter texto para uma ou várias linguagens. Os idiomas disponíveis para legendas codificadas são definidos entre as marcas <STYLE> e </STYLE> no arquivo Sami. Um identificador de idioma é especificado com uma cadeia de caracteres alfanumérica exclusiva que é precedida por um ponto (.). O nome especificado para um idioma pode ser qualquer cadeia de caracteres. Por exemplo, o seguinte pode ser usado para definir o inglês dos EUA:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Se nenhum idioma SAMI for especificado, o primeiro idioma definido no arquivo SAMI será usado por padrão.

O valor que você passa usando *ClosedCaption*. **SAMILang** deve corresponder ao atributo **Name** no especificador de idioma.

**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *ClosedCaption*. **SAMILang** em um elemento HTML SELECT para especificar a linguagem de legenda oculta. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 






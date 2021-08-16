---
title: ClosedCaption.SAMILang
description: A propriedade SAMILang especifica ou recupera o idioma exibido para legendas fechadas.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption.SAMILang Windows Media Player
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
ms.openlocfilehash: 4c423b041601a38e81b1c4e83c34c010edb3365a4eb7e05596038fa887818ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342281"
---
# <a name="closedcaptionsamilang"></a>ClosedCaption.SAMILang

A **propriedade SAMILang** especifica ou recupera o idioma exibido para legendas fechadas.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Um arquivo SAMI pode conter texto para um ou vários idiomas. Os idiomas disponíveis para legendas fechadas são definidos entre as marcas <STYLE> e </STYLE> no arquivo SAMI. Um identificador de idioma é especificado com uma cadeia de caracteres alfanumérico exclusiva precedida por um ponto (.). O nome especificado para um idioma pode ser qualquer cadeia de caracteres. Por exemplo, o seguinte pode ser usado para definir o inglês dos EUA:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Se nenhuma linguagem SAMI for especificada, o primeiro idioma definido no arquivo SAMI será usado por padrão.

O valor que você passa usando *ClosedCaption.* **SAMILang** deve corresponder ao **atributo Name** no especificador de idioma.

**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *ClosedCaption*. **SAMILang em** um elemento HTML SELECT para especificar a linguagem de legenda fechada. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 






---
title: Elemento REPEAT
description: o elemento REPEAT define o número de vezes que Windows Media Player repete um ou mais elementos de entrada ou ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- Windows Media Player de elemento REPEAT
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 330eda0757acb29b48ed10636d8f479b6ebb1395d088020876c717a78f41ae6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002536"
---
# <a name="repeat-element"></a>Elemento REPEAT

o elemento **REPEAT** define o número de vezes que Windows Media Player repete um ou mais elementos de **entrada** ou **ENTRYREF** .

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Atributos

**COUNT**

o inteiro que representa o número de vezes que Windows Media Player repete os elementos **ENTRY** e **ENTRYREF** dentro desse escopo do elemento.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                |
|-----------------|-------------------------|
| Elementos pai | **ASX**                 |
| Elementos filho  | **entrada**, **ENTRYREF** |



 

## <a name="remarks"></a>Comentários

esse elemento define o número de vezes que Windows Media Player repetições ou loops por meio de, os clipes definidos pelos elementos **ENTRY** e **ENTRYREF** dentro desse escopo do elemento. Somente o primeiro elemento **REPEAT** em um metarquivo é válido; os elementos **repetidos** subsequentes são ignorados.

Se nenhum atributo **Count** for definido, o conteúdo na **entrada** associada e nos elementos **ENTRYREF** repetirá um número infinito de vezes. um valor de zero faz com que Windows Media Player ignore o elemento **REPEAT** e reproduza o conteúdo uma vez.

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metarquivo de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 






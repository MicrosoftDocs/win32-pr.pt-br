---
title: Elemento REPEAT
description: O elemento REPEAT define o número de vezes que o Windows Media Player repete um ou mais elementos de entrada ou ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- REPETIR elemento Windows Media Player
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752595"
---
# <a name="repeat-element"></a>Elemento REPEAT

O elemento **REPEAT** define o número de vezes que o Windows Media Player repete um ou mais elementos de **entrada** ou **ENTRYREF** .

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Atributos

**COUNT**

Inteiro que representa o número de vezes que o Windows Media Player repete a **entrada** e os elementos **ENTRYREF** dentro desse escopo do elemento.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                |
|-----------------|-------------------------|
| Elementos pai | **ASX**                 |
| Elementos filho  | **entrada**, **ENTRYREF** |



 

## <a name="remarks"></a>Comentários

Esse elemento define o número de vezes que o Windows Media Player se repete ou faz um loop pelos clipes definidos pelos elementos **entry** e **ENTRYREF** dentro desse escopo do elemento. Somente o primeiro elemento **REPEAT** em um metarquivo é válido; os elementos **repetidos** subsequentes são ignorados.

Se nenhum atributo **Count** for definido, o conteúdo na **entrada** associada e nos elementos **ENTRYREF** repetirá um número infinito de vezes. Um valor de zero faz com que o Windows Media Player ignore o elemento **REPEAT** e reproduza o conteúdo uma vez.

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

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





